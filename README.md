# 服务器代理服务 Server Proxy Service

如果你觉得本项目对你有用,而且你也恰巧有这方面的需求,你也可以选择通过我的购买链接赞助我  
- [搬瓦工GIA服务器](https://bandwagonhost.com/aff.php?aff=41846)  - - - 仅推荐购买GIA套餐 - - -   

如果你希望购买一些现成的代理服务,可选择下述代理服务
- [搬瓦工官方机场](https://justmysocks.net/members/aff.php?aff=16884)  
# Uptime Kuma

Uptime Kuma is an easy-to-use self-hosted monitoring tool.

<a target="_blank" href="https://github.com/louislam/uptime-kuma"><img src="https://img.shields.io/github/stars/louislam/uptime-kuma?style=flat" /></a> <a target="_blank" href="https://hub.docker.com/r/louislam/uptime-kuma"><img src="https://img.shields.io/docker/pulls/louislam/uptime-kuma" /></a> <a target="_blank" href="https://hub.docker.com/r/louislam/uptime-kuma"><img src="https://img.shields.io/docker/v/louislam/uptime-kuma/latest?label=docker%20image%20ver." /></a> <a target="_blank" href="https://github.com/louislam/uptime-kuma"><img src="https://img.shields.io/github/last-commit/louislam/uptime-kuma" /></a>  <a target="_blank" href="https://opencollective.com/uptime-kuma"><img src="https://opencollective.com/uptime-kuma/total/badge.svg?label=Open%20Collective%20Backers&color=brightgreen" /></a>
[![GitHub Sponsors](https://img.shields.io/github/sponsors/louislam?label=GitHub%20Sponsors)](https://github.com/sponsors/louislam) <a href="https://weblate.kuma.pet/projects/uptime-kuma/uptime-kuma/">
<img src="https://weblate.kuma.pet/widgets/uptime-kuma/-/svg-badge.svg" alt="Translation status" />
</a>

<img src="https://user-images.githubusercontent.com/1336778/212262296-e6205815-ad62-488c-83ec-a5b0d0689f7c.jpg" width="700" alt="" />

## 🥔 Live Demo

Try it!

Demo Server (Location: Frankfurt - Germany): https://demo.kuma.pet/start-demo

It is a temporary live demo, all data will be deleted after 10 minutes. Sponsored by [Uptime Kuma Sponsors](https://github.com/louislam/uptime-kuma#%EF%B8%8F-sponsors).

## ⭐ Features

- Monitoring uptime for HTTP(s) / TCP / HTTP(s) Keyword / HTTP(s) Json Query / Ping / DNS Record / Push / Steam Game Server / Docker Containers
- Fancy, Reactive, Fast UI/UX
- Notifications via Telegram, Discord, Gotify, Slack, Pushover, Email (SMTP), and [90+ notification services, click here for the full list](https://github.com/louislam/uptime-kuma/tree/master/src/components/notifications)
- 20-second intervals
- [Multi Languages](https://github.com/louislam/uptime-kuma/tree/master/src/lang)
- Multiple status pages
- Map status pages to specific domains
- Ping chart
- Certificate info
- Proxy support
- 2FA support

## 🔧 How to Install

### 🐳 Docker

```bash
docker run -d --restart=always -p 3001:3001 -v uptime-kuma:/app/data --name uptime-kuma louislam/uptime-kuma:1
```

Uptime Kuma is now running on <http://0.0.0.0:3001>.

> [!WARNING]
> File Systems like **NFS** (Network File System) are **NOT** supported. Please map to a local directory or volume.

> [!NOTE]
> If you want to limit exposure to localhost (without exposing port for other users or to use a [reverse proxy](https://github.com/louislam/uptime-kuma/wiki/Reverse-Proxy)), you can expose the port like this:
> 
> ```bash
> docker run -d --restart=always -p 127.0.0.1:3001:3001 -v uptime-kuma:/app/data --name uptime-kuma louislam/uptime-kuma:1
> ```

### 💪🏻 Non-Docker

Requirements:

- Platform
  - ✅ Major Linux distros such as Debian, Ubuntu, CentOS, Fedora and ArchLinux etc.
  - ✅ Windows 10 (x64), Windows Server 2012 R2 (x64) or higher
  - ❌ Replit / Heroku
- [Node.js](https://nodejs.org/en/download/) 18 / 20.4
- [npm](https://docs.npmjs.com/cli/) 9
- [Git](https://git-scm.com/downloads)
- [pm2](https://pm2.keymetrics.io/) - For running Uptime Kuma in the background

```bash
git clone https://github.com/louislam/uptime-kuma.git
cd uptime-kuma
npm run setup

# Option 1. Try it
node server/server.js

# (Recommended) Option 2. Run in the background using PM2
# Install PM2 if you don't have it:
npm install pm2 -g && pm2 install pm2-logrotate

# Start Server
pm2 start server/server.js --name uptime-kuma
```

Uptime Kuma is now running on http://localhost:3001

More useful PM2 Commands

```bash
# If you want to see the current console output
pm2 monit

# If you want to add it to startup
pm2 save && pm2 startup
```

### Advanced Installation

If you need more options or need to browse via a reverse proxy, please read:

https://github.com/louislam/uptime-kuma/wiki/%F0%9F%94%A7-How-to-Install

## 🆙 How to Update

Please read:

https://github.com/louislam/uptime-kuma/wiki/%F0%9F%86%99-How-to-Update

## 🆕 What's Next?

I will assign requests/issues to the next milestone.

https://github.com/louislam/uptime-kuma/milestones

