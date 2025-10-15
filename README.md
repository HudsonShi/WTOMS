# WTOMS - 智能全渠道供应链管理系统
https://img.shields.io/badge/Go-1.21+-00ADD8?style=flat&logo=go
https://img.shields.io/badge/Vue-3.3+-4FC08D?style=flat&logo=vue.js
https://img.shields.io/badge/PostgreSQL-16+-4169E1?style=flat&logo=postgresql

🚀 技术选型
领域	技术选型	说明
后端	Go (Gin) + GORM	构建高性能、高并发的核心业务API
数据库	PostgreSQL	支持JSONB、全文搜索与空间数据的关系型数据库
前端	Vue 3 + TypeScript + Vite + Element Plus	构建现代化、类型安全的单页面应用
数据分析	Python (Pandas + Scikit-learn)	用于需求预测、库存优化等异步分析任务
部署	Docker & Docker Compose	提供一键式环境配置与部署
📡 核心接口功能列表
订单管理 (OMS)
POST /api/v1/orders - 接收订单：从电商平台推送订单，是业务流程的起点。

POST /api/v1/inventory/hold - 查询与占用库存：锁定库存，防止超卖。

GET /api/v1/orders - 订单查询与筛选：支持多条件查询订单列表。

PUT /api/v1/orders/{id}/status - 订单状态更新：手动调整订单状态（如审核通过、取消）。

仓储管理 (WMS)
POST /api/v1/fulfillment/ship-orders - 创建发货任务：向仓库下发发货指令。

POST /api/v1/warehouse/receipts - 创建入库单：登记货物到达，生成收货单。

POST /api/v1/warehouse/putaway-tasks - 执行上架操作：确认货物存放至具体货位。

POST /api/v1/warehouse/picking-tasks - 创建拣货任务：根据订单生成拣货单。

GET /api/v1/inventory - 库存查询：查询指定SKU和仓库的实时库存水平。

运输管理 (TMS)
POST /api/v1/shipments - 创建运单：根据发货任务生成运输订单。

POST /api/v1/shipments/routing - 路由与计费：获取最优运输路径与预估成本。

GET /api/v1/shipments/{id}/tracking - 物流轨迹查询：获取运单的实时物流状态。

主数据管理
CRUD /api/v1/products - 商品信息管理：对商品SKU进行增删改查。

CRUD /api/v1/warehouses - 仓库信息管理：维护仓库和库位信息
