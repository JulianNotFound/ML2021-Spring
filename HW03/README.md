simple baseline仍是直接运行即可通过(public:0.44862, private:0.47220)，个人运行结果public：0.48984，private：0.47878。

medium baseline(public:0.52807, private:0.54393)经过适当的调整架构以及输入数据后可以通过。个人的主要做法是将有标签的数据左右对称后作为也输入，增加数据集规模，最终结果public:0.58721, private:0.55648。