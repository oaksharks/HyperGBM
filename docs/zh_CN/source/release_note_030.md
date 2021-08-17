Version 0.3.0
=====================

本次发布优化及新增的特性：

* 数据清洗
  - 支持从数据类型为数值型的特征中自动识别类别列
  - 可指定在数据清洗时对某些列不做处理

* 特征衍生
  - 增加对时间、文本、经纬度类型的支持
  - 增加对分布式的支持

* 建模算法
  - XGBoost：分布式建模从 `dask_xgboost` 迁移到 `xgboost.dask` ，与XGBoost官网保值一致
  - LightGBM：增加对多机分布式的支持

* 模型训练
  - 搜索过程可复现
  - 支持低保真搜索
  - 基于统计信息预测学习曲线
  - 支持非侵入式超参数优化
  -  EarlyStopping时间限制的范围调整为对整个实验的训练周期
  - 训练时支持自定义pos_label
  - 分布式场景下，eval-set支持Dask数据集
  - 优化模型训练中间结果的缓存策略

* 搜索算法
  - 增加GridSearch算法
  - 增加Playback算法

* 高级特性
  - 增加一阶段特征筛选并支持多种策略
  - 二阶段特征筛选支持多种策略
  - 伪标签支持多种数据筛选策略，并增加对多分类的支持
  - 优化概念漂移处理的执行性能
  - 增加对高级特性执行中间结果的缓存机制

* 可视化
  - 实验信息可视化
  - 训练过程可视化
  
* 命令行工具
  - 模型训练时可通过命令行参数支持实验的大部分特性
  - 支持模型评价
  - 支持模型预测
