# 为 [FastGit](https://github.com/FastGitORG/nginx-conf) 项目域名配置 DNS 记录的脚本

## 特点

- [x] 支持 [Cloudflare DNS](https://www.cloudflare.com/)
- [x] 支持 [DNSPod](https://www.dnspod.cn/)
- [x] 支持 [DigitalOcean DNS](https://www.digitalocean.com/)
- [x] 支持 [Vultr DNS](https://vultr.com/)
- [x] 支持 [Linode DNS](https://www.linode.com/)
- [x] 支持 [GoDaddy DNS](https://godaddy.com/)
- [x] 支持非交互模式，可用于自动化部署

*欢迎 PR 新的 DNS 服务商支持*

## 准备工作

- Python 3.6+
- `pip install dnspython` 或者 `sudo apt install python3-dnspython`
- 一个域名（仅支持顶级域名，不支持二级域名)，需要使用支持 DNS API 的 DNS 服务商（见上）
- DNS 服务商的 API Token

## 用法

```bash
$ ./dns-setup.py # 交互式模式
$ ./dns-setup.py -t <token> -d <域名> -n # 非交互模式
$ ./dns-setup.py -4 <ipv4> -6 <ipv6> -t <token> -d <域名> -n # 指定 IPv4 和 IPv6 地址
```

*为 @KevinZonda 的 [FastGit](https://github.com/FastGitORG/nginx-conf) 项目而生*
