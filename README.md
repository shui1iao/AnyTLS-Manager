# AnyTLS-Manager

[![Release](https://img.shields.io/github/v/release/shui1iao/AnyTLS-Manager?style=flat-square&color=2563eb)](https://github.com/shui1iao/AnyTLS-Manager/releases/latest)
[![Shell](https://img.shields.io/badge/Shell-Bash-4EAA25?style=flat-square&logo=gnu-bash&logoColor=white)](anytls.sh)
[![Platform](https://img.shields.io/badge/Platform-Linux%20amd64%20%7C%20arm64-1e293b?style=flat-square&logo=linux&logoColor=white)](https://github.com/shui1iao/AnyTLS-Manager/releases)

**中文** | [English](README.en.md)

**轻量级 AnyTLS-Go 服务端一键安装与管理脚本**——快速部署、配置与升级 AnyTLS 代理节点。

## 核心特性

- **一键安装与升级**：支持 `amd64` / `arm64` 架构，自动安装与更新 AnyTLS-Go 核心并在升级后自动重启服务。
- **安全凭据隔离**：密码与运行参数存于 `0600` 权限的独立 `EnvironmentFile`，避免密码暴露于进程命令行，并内置密码合法性校验。
- **简洁运维管理**：支持交互式修改端口与密码、systemd 服务启停状态查看及脚本自更新检查。

## 快速开始

### 方式一：短链一键运行（推荐）

```bash
bash <(curl -Ls https://anytls.siaoz.si)
```

### 方式二：运行最新正式发布版

```bash
curl -fsSLO https://github.com/shui1iao/AnyTLS-Manager/releases/latest/download/anytls.sh
bash anytls.sh
```

## 注意事项

- 面向 Linux root + systemd 环境，请在可信 VPS 上执行。
- 涉及端口与防火墙变更前，建议保留现有 SSH 会话不断开。
