# CatBoost Build

使用 GitHub Actions 在线编译 CatBoost 全平台产物，通过 Actions 页面手动触发构建，下载 artifacts。

## 支持平台

| 平台 | 架构 | CUDA |
|------|------|------|
| Linux | x86_64 | ✅ |
| Linux | aarch64 | ❌ (交叉编译) |
| macOS | universal2 (x86_64 + arm64) | ❌ |
| Windows | x86_64 | ✅ |

## 产物列表

- **catboost CLI** — 命令行训练/推理工具
- **Python wheels** — 支持 Python 3.8-3.13
- **catboostmodel 动态库** — C API 推理库 (`.so` / `.dylib` / `.dll`)
- **R 包** — `.tgz` 格式
- **JVM 包** — catboost4j-prediction / catboost4j-spark
- **测试工具**

## 使用方式

1. 进入 GitHub 仓库的 **Actions** 页面
2. 选择 **Build CatBoost All Platforms** workflow
3. 点击 **Run workflow**
4. 输入 CatBoost 版本号（例如 `1.2.8`）
5. 等待构建完成后，在 workflow run 页面下载 artifacts

## 构建时间

- Linux x86_64: ~2-3 小时
- Linux aarch64: ~2-3 小时
- macOS universal2: ~1-2 小时
- Windows x86_64: ~2-3 小时
