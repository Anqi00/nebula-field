# Nebula Field

一个使用摄像头与 WebGL 实现的手势驱动科幻粒子场艺术效果。

手掌移动会扰动星尘；拇指与食指捏合时，粒子会逐步聚拢，松开后产生柔和的加速度向外散开。摄像头只用于 MediaPipe Hands 手部追踪，不会显示在艺术画面中。

## 运行

需要支持 WebGL2 的现代浏览器，以及摄像头权限。

```bash
python3 -m http.server 8001
```

打开 <http://localhost:8001/> 即可。摄像头 API 需要 `localhost` 或 HTTPS。

## 技术

- Three.js WebGL2 ShaderMaterial
- MediaPipe Hands 0.4
- getUserMedia 摄像头输入
- 单文件 HTML，无构建工具

所有主要参数都集中在 `index.html` 顶部的 `CONFIG` 对象和右上角参数面板中。

页面操作界面在鼠标、触摸或键盘 5 秒无活动后会自动淡出，重新移动或触摸即可恢复。
