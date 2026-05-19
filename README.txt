ZTH & LYH 爱心备忘录 · PWA 手机 App
=====================================

【文件夹内容】
  memo.html       主页面（含 PWA 配置）
  manifest.json   App 清单
  sw.js           离线缓存 Service Worker
  icon-192.png    应用图标 192×192
  icon-512.png    应用图标 512×512

【安装到手机 - 方法一：局域网临时访问（最快）】
1. 在本机打开 PowerShell，进入本文件夹：
   cd "d:\桌面\love-memo"
2. 启动本地服务器（需已安装 Python 或 Node）：
   npx --yes serve -p 8080
   或：python -m http.server 8080
3. 查看电脑 IP（ipconfig），手机连同一 WiFi，浏览器访问：
   http://你的电脑IP:8080/memo.html
4. 安装：
   · iPhone Safari：分享 → 添加到主屏幕
   · Android Chrome：菜单 → 安装应用 / 添加到主屏幕

【安装到手机 - 方法二：正式部署（推荐长期使用）】
将本文件夹上传到支持 HTTPS 的空间，例如：
  · GitHub Pages  · Vercel  · Netlify  · 自己的服务器
PWA 必须通过 HTTPS（或 localhost）才能注册 Service Worker。

【注意】
· 备忘录数据保存在手机浏览器 localStorage，卸载或清数据会丢失
· 自定义背景图较大时可能占较多存储空间
· 离线时只能使用已缓存的页面；新建备忘录仍可用（数据在本地）
