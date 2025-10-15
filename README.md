# 🚀 WTOMS - 智能全渠道供应链管理系统

**W**arehouse **T**ransportation **O**rder **M**anagement **S**ystem

## 🛠️ 技术选型

### 后端技术栈
- **Go** + **Gin** - 高性能HTTP框架
- **GORM** - 优雅的ORM库
- **PostgreSQL** - 企业级关系型数据库

### 前端技术栈  
- **Vue 3** + **TypeScript** - 现代化前端框架
- **Vite** - 下一代构建工具
- **Element Plus** - 企业级UI组件库

### 数据分析与部署
- **Python** - 数据科学与机器学习
- **Docker** & **Docker Compose** - 容器化部署

## 📡 核心接口功能列表

### 📦 订单管理 (OMS)
- `POST /api/v1/orders` - 接收多渠道订单
- `POST /api/v1/inventory/hold` - 库存查询与占用
- `GET /api/v1/orders` - 订单查询与筛选
- `PUT /api/v1/orders/{id}/status` - 订单状态更新

### 🏭 仓储管理 (WMS)  
- `POST /api/v1/fulfillment/ship-orders` - 创建发货任务
- `POST /api/v1/warehouse/receipts` - 创建入库单
- `POST /api/v1/warehouse/putaway-tasks` - 执行上架操作
- `POST /api/v1/warehouse/picking-tasks` - 创建拣货任务
- `GET /api/v1/inventory` - 实时库存查询

### 🚚 运输管理 (TMS)
- `POST /api/v1/shipments` - 创建运输订单
- `POST /api/v1/shipments/routing` - 智能路由规划
- `GET /api/v1/shipments/{id}/tracking` - 物流轨迹追踪

### 📊 主数据管理
- `CRUD /api/v1/products` - 商品SKU管理
- `CRUD /api/v1/warehouses` - 仓库信息管理
- `CRUD /api/v1/carriers` - 承运商管理

## 🚀 快速开始

## 🚀 快速开始
# 克隆项目
```bash
git clone https://github.com/your-username/wtoms.git
···
# 启动服务
```bash
cd wtoms && docker-compose up -d
```

访问地址：http://localhost:3000
