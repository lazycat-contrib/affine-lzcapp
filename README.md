# AFFiNE for LazyCat

将 [AFFiNE](https://github.com/toeverything/AFFiNE) 打包为懒猫微服 LPK v2 应用。

## 镜像与发布策略

- AFFiNE 使用 `ghcr.1ms.run` 镜像加速，初始版本为 `0.27.3`。
- Redis 和 pgvector/PostgreSQL 使用现有懒猫官方 Registry 镜像。
- GitHub Actions 定期检查 AFFiNE 的稳定 SemVer 镜像版本，构建版本化 Release Asset，并且只发布到喵喵商店。
- 不发布到懒猫官方应用商店。

## 本地构建

```bash
lzc-cli project release -o dist/affine.lpk
```

## GitHub Secrets

发布工作流使用 `APPSTORE_URL`、`APPSTORE_TOKEN`，并可选使用 `APP_ID` 和 `PRIVATE_STORE_GROUP_CODES`。
