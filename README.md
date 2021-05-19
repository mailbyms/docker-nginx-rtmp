# nginx-rtmp
RTMP服务器：nginx with nginx-rtmp-module

- 基础镜像: `Centos7.9`
- `nginx`版本：1.8.1
- `nginx-rtmp-module`版本：1.2.1

集成 `ffmpeg-4.2.1`，在视频录制结束后，自动转码为 mp4 并生成一张截图

镜像使用配置见 [docker-compose.yml](https://github.com/mailbyms/nginx-rtmp) 文件
