# ez-cdc
一个带可视化界面的数据变更捕获工具/A data change capture tool with visual interface;

基于内嵌的debezium，支持捕获数据库的数据变更，并且可以配置数据处理/过滤等操作。

支持的关系型数据库有postgresql，mysql
支持消费到kafka，rocketmq，elasticsearch

整体由，一个控制台前端服务，一个控制台后端服务和一个worker集群组成

ez-cdc-console-web 
ez-cdc-console-server
ez-cdc-worker

控制台统一调度，worker执行具体的任务，元数据由redis保存
