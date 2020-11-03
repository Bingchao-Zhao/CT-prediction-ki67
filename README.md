# 基于CT的影像组学术前预测胃癌Ki-67表达水平的研究

这里是 《基于CT的影像组学术前预测胃癌Ki-67表达水平的研究》 论文验证集R语言的SVM模型和数据的R语言文件。
其中`SVM.RData`是已经训练好的SVM模型，`validation.Rdata`是经过特征工程后的验证集的特征。

## 使用方法：
`svm = load("SVM.RData") #读取SVM.RData模型文件` <br/> 
`fit.svm = get(svm) ` <br/> 
`data = load("validation.RData") #读取验证集数据文件` <br/> 
`valid_all = get(data) ` <br/> 
`r_score_pre_val <- predict(fit.svm,newdata = valid_all)#计算模型Rad-score` <br/> 
