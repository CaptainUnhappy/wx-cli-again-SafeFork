# wx-cli-again-SafeFork

这是 [jackwener/wx-cli-again](https://github.com/jackwener/wx-cli-again) 的 SafeFork。

## 分支用途

- [main](../../tree/main)：保留上游源码与 Git 历史，沿用上游的 Apache-2.0 许可证。
- sync-control：默认分支，仅保存自动同步工作流，不属于上游源码。

## 同步规则

- 每小时检查一次，也可在 Actions 中手动执行；GitHub 可能延迟或跳过定时运行。
- 只创建缺失分支、快进已有分支、复制缺失 Tag。
- 遇到分叉历史或同名异 SHA 的 Tag 会停止，不会强制覆盖。
- 不删除 Fork 独有分支或 Tag，不创建自动备份分支。

查看源码请切换到 [main](../../tree/main)。本控制分支的 SafeFork 工作流采用 [MPL-2.0](https://github.com/CaptainUnhappy/SafeFork/blob/main/LICENSE)。