# 木犀电商平台

[![Python](https://img.shields.io/badge/Python-3.10+-blue.svg)](https://www.python.org/)

[![Django](https://img.shields.io/badge/Django-4.2-green.svg)](https://www.djangoproject.com/)

[![FastAPI](https://img.shields.io/badge/FastAPI-0.104-orange.svg)](https://fastapi.tiangolo.com/)

[![Redis](https://img.shields.io/badge/Redis-7.0-red.svg)](https://redis.io)

[![RabbitMQ](https://img.shields.io/badge/RabbitMQ-3.12-purple.svg?logo=rabbitmq)](https://www.rabbitmq.com/)

[![Elasticsearch](https://img.shields.io/badge/Elasticsearch-8.10-yellow.svg)](https://www.elastic.co/)



## 📋 核心定位

独立开发的高并发分布式电商系统，聚焦【高并发秒杀】、【分布式一致性】、【性能优化】三大技术难点，已部署至阿里云稳定运行。



## 📋 项目概述

- **线上地址**：https://nwq1309.shop

  ​                   https://admin.nwq1309.shop

测试账号：4@qq.com        测试密码：123456

沙箱账号：ixvbxq4794@sandbox.com   密码(包括支付):111111

- **视频演示**：

  - **木犀电商平台核心演示：**（核心！！！）
  
  [Project1.mp4](https://github.com/s19m3nug-boop/Project_Description/raw/main/videos/Project1.mp4)
  
  <details>
      <summary>📺 核心功能演示（点击展开）</summary>
      <video src="https://raw.githubusercontent.com/s19m3nug-boop/Project_Description/main/videos/Project1.mp4" width="800" controls="controls"></video>
  </details>
  
  
  
  
  - **校园二手交易站**（它这里跟木犀电商平台完全无关，只是为了占个广告位~~~）
  
  [Project2.mp4](https://github.com/s19m3nug-boop/Project_Description/raw/main/videos/Project2.mp4)
  
  <details>
      <summary>📺 核心功能演示（点击展开）</summary>
      <video src="https://raw.githubusercontent.com/s19m3nug-boop/Project_Description/main/videos/Project2.mp4" width="800" controls="controls"></video>
  </details>
  
  
  
  
  - **个人博客**（这里也是占个广告位！！！）
  
  [Project3.mp4](https://github.com/s19m3nug-boop/Project_Description/raw/main/videos/Project3.mp4)
  
  <details>
      <summary>📺 核心功能演示（点击展开）</summary>
      <video src="https://raw.githubusercontent.com/s19m3nug-boop/Project_Description/main/videos/Project3.mp4" width="800" controls="controls"></video>
  </details>

​          



## 🚀 技术栈

- **后端框架**：Django 4.2 + DRF + FastAPI
- **数据存储**：MySQL + Redis + Elasticsearch
- **异步队列**：RabbitMQ + Celery
- **部署运维**：Nginx + UWSGI + Systemd
- **监控告警**：Prometheus + Grafana
- **性能测试**：Locust
- **一致性保障**：Saga事件驱动模式



## 🎯 核心功能

### 高并发秒杀

- **双模式设计**：Redis原子扣减/ RabbitMQ+Celery队列
- **实时推送**：Tornado WebSocket推送秒杀结果，用户体验无感知
- **防超卖**：Redis分布式锁 + 库存预扣减，Locust压测200并发零超卖



### 分布式一致性保障

- 基于Saga模式拆分订单链路为3个子事务：创建订单-->扣减库存-->支付回调
- 每个子事务提供补偿逻辑（如支付失败-->恢复库存），保证最终一致性



### 性能优化成果

- 商品搜索，Elasticsearch分词优化，响应时间从2s-->200ms
- 接口QPS，多级Redis缓存，商品详情页QPS从100-->1500+
- 并发支持，系统峰值支持5000+并发，核心API平均响应<300ms



### 工程化保障

- **日志系统**：自定义按行数轮转日志，快速定位线上问题
- **监控体系**：Prometheus+Grafana监控QPS、响应时间、Redis缓存命中率
- **服务管理**：Systemd托管UWSGI/Celery，保证进程常驻



## 📚 核心导航

- [📖 核心接口设计](docs/api-highlight.md) - 接口规范+状态码+核心接口示例
- [🏗️ 架构设计](docs/arch-design.md) - 系统架构+Saga模式+缓存策略
- [📊 性能优化](docs/performance.md) - 压测数据/SSL证书/监控体系
- [🗄️ 数据库设计](docs/database.md) - 表结构/ER图/索引设计



### 系统拓扑图

> 注：拓扑图源文件为 drawio 格式，可下载编辑；PNG 为可视化版本，方便快速查看。

! [木犀电商平台系统拓扑图](https://raw.githubusercontent.com/s19m3nug-boop/Project_Description/main/assets/系统拓扑图.png)

拓扑图源文件：[系统拓扑图.drawio](https://raw.githubusercontent.com/s19m3nug-boop/Project_Description/main/assets/系统拓扑图.drawio)



