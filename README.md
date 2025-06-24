```markdown
数据放在 `Dataset/{name}/input` 下。

依次运行以下命令：

```bash
# 1. 数据转换
python convert.py -s /path/to/your/dataset

# 2. 训练
# -s 指向处理好的数据路径
# --eval 标志至关重要，它会保留测试集用于评估
python train.py -s /path/to/processed/data --eval

# 3. 渲染
# -m 指向训练输出的模型目录
# --skip_train 表示只渲染测试集，跳过训练集
python render.py -m /path/to/output/model --skip_train

# 4. 评估指标
python metrics.py -m /path/to/output/model
```

请根据实际脚本参数和路径进行调整。
```