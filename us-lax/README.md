# 美国洛杉矶住宅节点（US-LAX）

独立 Clash 配置，规则与韩国仓库 `my-proxy-config` 对齐，节点换成美国洛杉矶住宅 IP。

给 Codex / ChatGPT 用这份，不要和韩国机房节点混在同一个配置里来回切。

## 导入

Clash Verge / Clash Meta / Mihomo 导入 `clash.yaml` 即可。

## 节点

| 项 | 值 |
| --- | --- |
| 名称 | US-LAX |
| 协议 | VLESS + Reality + Vision |
| 地址 | `64.81.25.96` |
| 端口 | `443`（备用 `25152`） |
| UUID | `1cbeb21f-cdcf-4d91-a97a-e8f7419d7105` |
| SNI | `www.cloudflare.com` |
| short-id | `b8fe67ee219a5897` |
| 指纹 | chrome |

出口实测为洛杉矶 `64.81.25.96`。

## 和韩国节点的差异

- 协议栈相同：VLESS / TCP / Reality / `xtls-rprx-vision` / chrome 指纹
- 美国节点走住宅 IP，AI 流量出口在洛杉矶
- 伪装站用 `www.cloudflare.com`（美国机房实测 `www.microsoft.com` 无法完成 Reality 握手）
- 监听 `443` 和 `25152`，客户端默认 `443`

## 说明

当前 GitHub 授权只能写入本仓库 `my-proxy-config`，无法自动新建第二个远程仓库。美国配置先放在 `us-lax/`。若你在 GitHub 建好空仓库 `my-proxy-config-us` 并授权，可以把该目录拆过去。
