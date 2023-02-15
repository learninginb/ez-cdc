# ez-cdc
一个带可视化界面的数据变更捕获工具/A data change capture tool with visual interface;

基于内嵌的debezium，支持捕获数据库的数据变更，并且可以配置数据处理/过滤等操作。

支持的关系型数据库有postgresql，mysql
支持消费到kafka，rocketmq，elasticsearch

整体由，一个控制台前端服务，一个控制台后端服务和一个worker集群组成

ez-cdc-console-web 

    控制台web端：登录，报表，用户管理，crud，看日志

ez-cdc-console-server：

    控制台server端：注册中心，报表+监控，任务调度，crud，邮件报警，登录

ez-cdc-worker：

    配置接收，状态上报，异常告警，ip上报，日志上传，任务执行

控制台统一调度，worker执行具体的任务，元数据由redis保存

中心化的架构
