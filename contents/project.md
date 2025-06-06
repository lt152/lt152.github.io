
#### 流媒体协议实现与应用案例开发-课设项目
- **项目时间**：2022.11 - 2022.12
- **成果及贡献**：
  - 设计研究**RTSP，RTP/RTCP**协议,使用**Java**简单实现视频文件推流和播放控制
  - 技术栈：**Java Swing、ByteBuffer**类
  - 根据参考资料，手动定义服务端RTP协议的封装格式，包括HEADER_SIZE、VERSION等字段；使用UDP封装RTCP包；完成建立RTSP的TCP连接、建立用于RTP/RTCP传输的UDP连接、接收客户端的RTSP请求并作出回应、控制视频流的发送，暂停与停止、调整发送质量等功能
  - 客户端实现的功能包括：流媒体视频接收、视频显示、发送视频播放控制请求等，基于Swing实现
  - 自定义MJPEG视频编码、压缩，使用OpenCV完成
  
#### 图像文本识别APP开发-毕设项目
- **项目时间**：2023.01 - 2023.05
- **成果及贡献**：
  - 开发了一个基于Android的OCR软件，包含文本识别、切换引擎、历史记录、分享导出功能
  - 技术栈：**Java**作为开发语言，基于开源**Tesseract OCR**与**百度Paddle OCR**进行二次开发，使用**FastDeploy**部署，灵活运用了实体类、碎片、适配器等开发知识
  - 无需联网，实现**本地**图文识别，应用的**精确率、召回率均达到90%以上，同类软件领先**（相比Text Fairy等开源软件）

#### 跨模态图文检索模型-国网基金论文项目
- **项目时间**：2024.05 - 2024.10
- **成果及贡献**：
  - 针对跨模态检索领域模态内特征信息表征问题，提出基于交叉注意力与特征聚合的图文检索模型，设计池化聚合模块，通过神经网络学习动态权重参数，实现对图像区域特征和文本序列特征的高效聚合
  -	技术栈：**Faster RCNN+BERT-base+Bi-GRU+Attention**
  -	在MS COCO 和 Flickr 30K 数据集上的结果表明，**模型检索性能指标rSum分别达到499.8与527.1**，优于同类方法，相关成果已申请专利
  - 链接：https://doi.org/10.19678/j.issn.1000-3428.0070119

#### 仿大众点评项目-自学项目
- **项目时间**：2025.03 - 2025.04
- **成果及贡献**：
  - 实现商户信息查询、优惠券秒杀、附近的商户、UV统计、用户签到、好友关注等功能；
  -	技术栈：SpringBoot+MySQL+Redis+MyBatis-Plus+Hutool+Lombok+Redisson+RabbitMQ
  -	为解决集群模式下Session共享问题，配合Redis与ThreadLocal使用双层拦截器进行用户的登录校验，或使用Jwt进行登录验证；基于Cache Aside更新数据，并解决缓存与数据库之间的缓存穿透、热点key问题，并保证一致性；通过加锁的方式解决超卖和实现一人一单，使用Redisson实现分布式锁等。
  - 在模拟高并发高负载实验中，通过合理分配新生代与老年代空间，解决频繁Full GC问题导致的STW缓慢