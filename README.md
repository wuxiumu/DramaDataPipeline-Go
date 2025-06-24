# DramaDataPipeline-Go
一个模拟海外短剧数据采集、处理、建模、监测分析的 Golang 全栈数据中台项目。


## 🧐 项目简介

海外短剧火成这样，咱们工程师能干瞪眼？  
DramaDataPipeline-Go 是一个模拟真实短剧业务场景的**全链路数据监测系统**，从数据采集、消息队列处理、指标计算、缓存加速、可视化展示一应俱全，支持一键部署 & 压测闭环，拿它去面试，谁用谁自信 💼。

---

## ✨ 特性 Highlights

- 🔧 **Golang 高性能后端**：Gin + GORM + Kafka + Redis，满满的工业风
- 🔄 **ETL 模拟链路**：自定义数据管道，支持实时/离线两种模式
- 💾 **MySQL+Redis 多级存储**：冷热分离，助你秒出热榜数据
- 📊 **Vue3 + Arco 管理后台**：颜值高，还能跑，能带图表的那种
- 📦 **Kafka 模拟业务投放**：剧情数据走消息队列，够架构味儿
- 📈 **Prometheus 监控**：不是纸老虎，服务有指标才有话语权
- 🚀 **Docker 一键部署**：支持本地起飞，面试现场演示，帅爆了

---

## 🏗️ 技术架构
```

[Vue3 Dashboard] ← RESTful API → [Gin/GORM Service] ←→ [Kafka ETL]

↓

[MySQL | Redis]

↓

[Prometheus + Grafana]

```
<img src="https://archive.biliimg.com/bfs/archive/433fd5cecc2541e99fcd536027a3abc2f0318886.png"   referrerpolicy="no-referrer">


---

## 📦 快速开始

1. 克隆项目

```bash
git https://github.com/wuxiumu/DramaDataPipeline-Go.git
cd DramaDataPipeline-Go
```



2. 启动服务

```
cp .env.example .env
docker-compose up --build
```



3. 打开浏览器：



- 后台面板：http://localhost:5173
- API 接口：http://localhost:8080/api/dramas
- Kafka 管理：http://localhost:9000（如启用）





------





## **📚 目录结构（节选）**



```
dramaradar/
├── api/                # Golang 后端服务
├── frontend/           # Vue3 + Arco 前端
├── kafka/              # Kafka 消息处理逻辑
├── jobs/               # ETL 定时任务
├── deploy/             # Dockerfile、nginx、init.sql
├── data/               # 模拟数据 CSV/JSON
├── test/               # API 测试 & 压测脚本
├── docs/               # 架构图、数据流文档
└── docker-compose.yml  # 一键启动
```



------





## **🧪 测试用例**



| **场景**     | **入口路径**             | **说明**               |
| ------------ | ------------------------ | ---------------------- |
| 获取热剧榜单 | /api/dramas/hot          | 支持分页 + 缓存        |
| 模拟投放     | Kafka topic drama_events | 支持 CLI 模拟发送事件  |
| ETL 执行     | jobs/etl.go              | 每分钟聚合播放数据     |
| 前端展示     | /dashboard               | 图表自动刷新，实时感人 |



------





## **💡 灵感与用途**





这个项目灵感源于短剧业务爆发背后对**数据中台**和**系统稳定性**的极致要求。

无论你是：



- 想练习 Golang 架构师路线 🧱
- 想参与大数据链路处理的同学 🧮
- 想找一份靠谱工作的开发者 💼





它都能给你带来收获。



------





## **📬 联系我 / Star 一下不迷路**





作者：Aric

擅长 PHP/Golang/Vue 全栈项目开发，正在寻找全栈/架构岗位，欢迎内推 🤝



如果你觉得这个项目不错，点个 ⭐ Star 支持一下吧，这将是我继续更新的动力！



------

