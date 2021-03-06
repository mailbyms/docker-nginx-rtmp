
>**更推荐使用 [SRS](https://github.com/ossrs/srs)，有官方镜像，有集群、http-flv、h5、webrtc 等**

# nginx-rtmp
RTMP服务器：nginx with nginx-rtmp-module

## 构建概况
- 基础镜像: `Centos7.9`
- `nginx`版本：1.20.2
- `nginx-rtmp-module`版本：1.2.2

集成 `ffmpeg-4.2.1`，在视频录制结束后，自动转码为 mp4 并生成一张截图

## 部署
镜像使用配置见 [docker-compose.yml](https://github.com/mailbyms/nginx-rtmp) 文件

## 资源访问
- 直播推流地址：rtmp://host:1935/live/{CHANNEL_ID}
- **用 FFMPEG 推流时，服务器使用 IP 而不是域名**
- 直播列表：http://host:9090

## API 接口
- 开始录制：`POST` http://host:9090/control/record/start?rec=eduitv&app=live&name={CHANNEL_ID}
- 结束录制：`POST` http://host:9090/control/record/stop?rec=eduitv&app=live&name={CHANNEL_ID}
