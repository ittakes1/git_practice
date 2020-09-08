training set:

 * train
 * validation
 
testing set:

* test

### MLP
1. model
	* 基本元件 layer，用來萃取表徵
	* .add
	* [,]

2. compile:
	* loss function: cross entropy
	* optimizer: gsd, adam...
	* metrics: accuracy

3. fit 前的資料預處理
	* np array
	* .reshape()
	* .astype('float32')
	* one hot encoding
	* ...

4. fit:
	* x_train
	* y_train
	* epochs
	* batch_size
	
5. performance?
	* .evaluate
	
### Tensor
	* axis
	* shape
	* dtype
1. numpy tensor slicing
2. batch
3. tensor operations

 Y=act(W . X + b)
 
 Y|act|W|X|b
 ---|---|---|---|---
輸出|啟動|kernel, 權重|輸入|bias


## 第3章

### loss fn, optimizer

loss function f(W)

* binary crossentropy 2分類
* categorical crossentropy 多類別
* MSE mean squared error 數值回歸
* CTC connectionist temporal classification 序列學習

### Keras 的開發步驟

1. 定義訓練資料 dataset->tensors
2. 定義模型 layers
3. 選擇 loss fn, optimizer, metrics
4. fit 訓練

### 處理標籤

* one-hot, loss fn選categorical_crossentropy
* 整數 y_train = np.array(train_labels) fn選sparse_categorical_crossentropy

loss fn | categorical_crossentropy|sparse_categorical_crossentropy
---|---|---
輸出|100,010,001 | 0/ 1/ 2

### normalization 正規化

()輸入資料 -mean)/std
 

### weight regularization

簡單模型
參數值的分配有較小的熵

減少過擬合->小的權重
weight regularization
損失函數的權重

* L1 regularization
* L2 regularization


 