训练：
首先，使用本文档中的train.txt或者类似文本作为训练文本
输入以下命令行进行训练：
java -cp BerkeleyParser-1.7.jar edu.berkeley.nlp.PCFGLA.GrammarTrainer -path train.txt -out model -treebank SINGLEFILE
如果从包含单个文件的树中学习一个语法，就需要使用-treebank选项
训练这个模型需要进行6次迭代，它会输出model_1_merging.gr,model_1_smoothing.gr,model_1_splitting（1-6次迭代生成的模型）和一个model。model为我们生成的模型。

测试：
java -jar BerkeleyParser-1.7.jar -gr model -inputFile test.txt -outputFile output.txt
output.txt为我们生成的结果




