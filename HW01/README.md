直接运行提供的示例文件即可通过simple baseline(public 2.03004, private 2.04826)，个人运行示例代码的结果：public: 1.59826, private: 1.68437。

对示例文件的模型微调架构并适当调参即可通过 medium baseline(public 1.28359, private 1.36937)，主要的调整内容为将模型架构中间添加两个全连接的中间层、微调学习率，以及利用L2正则化在损失函数上添加权重衰减项（SGD添加参数weight_decay）。个人代码的运行结果：public: 1.23190, private: 1.26457。

针对strong baseline(public 0.88017, private 0.89266)多次调参最终尝试失败，个人最终结果public大约在0.89，private大约在0.91。主要的调整内容是对输入进行了特征工程分析，筛选出相关性强的参数进行输入；然后对数据标准化（normalization）进行微调，使所有计算都以训练集为标准进行；另外保存结果部分将训练集的结果也一同考虑进去；损失函数使用了RMSE替代MSE以方便结果分析；后来又发现模型过学习现象严重，所以将模型重新简化为1层。

最终的代码参考了以下仓库：

<https://github.com/PolarisRisingWar/lihongyi-2021-colab>

<https://github.com/1am9trash/Hung_Yi_Lee_ML_2021>

<https://github.com/wolfparticle/machineLearningDeepLearning>

