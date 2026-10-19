# 来源与第三方依赖

此仓库从已公开去敏的分类工程当前版本建立独立维护入口。导出基线为 `8f143f67598f88fbb8a16d599a7f3d17c623d281` 中的 `projects/job-text-classification`；此提交标识用于迁移追溯，不表示导入其历史。

分类逻辑基于已有研究脚本重组；公共单元测试与合成样例用于验证代码行为。此仓库没有声明独立实现 scikit-learn、PyTorch、Transformers，也没有将原论文 RAG 协议的效果归给此基线。

| 依赖 | 使用范围 |
| --- | --- |
| [scikit-learn](https://github.com/scikit-learn/scikit-learn) | TF-IDF 特征、随机森林、数据划分与指标 |
| [NumPy](https://github.com/numpy/numpy) | 数值数组与辅助计算 |
| [joblib](https://github.com/joblib/joblib) | 本地可信模型序列化 |
| [PyTorch](https://github.com/pytorch/pytorch) / [Transformers](https://github.com/huggingface/transformers) | 可选 BERT 训练与加载路径；此次未实际训练或下载模型 |

上述依赖通过包管理器安装，未复制源码、模型权重或服务数据。现有整理版没有独立许可证文件，本次未替作者添加许可或推断权利归属；使用上游能力应遵守对应许可证及模型条款。

`tools/check_publication.py` 复用已公开审查的文件允许列表与秘密扫描实现；对应测试只对齐独立仓库路径，实际 Git index 扫描逻辑保持不变。
