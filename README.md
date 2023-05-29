# Chinese-ChatBot/中文聊天機器人
* 作者已經全面轉到GNN圖神經網絡方向，不再跟進NLP方面，項目代碼停止維護。遙想項目完成時，網上資源甚少，作者一時興起初次接觸NLP與Deep Learning，克服重重困難，終於寫出這個Toy Model。因此，作者深知小白不易，所以即使項目不再維護，但issue或郵件(jayeew@qq.com)一定會及時答覆，以幫助Deep Learning新人。<br>
* GNN方面暫時只改編整理了一套基準對比模型：[GNNs-Baseline](https://github.com/jayeew/GNNs-Baseline) ，以方便快速驗證idea，歡迎同好補充、交流、學習。
## 環境配置
| 程序         | 版本      |
| ---------- | ------- |
| python     | 3.68    |
| tensorflow | 1.13.1  |
| Keras      | 2.2.4   |
| windows10  |         |
| jupyter    |         |

## 主要參考資料
* 論文[《NEURAL MACHINE TRANSLATION BY JOINTLY LEARNING TO ALIGN AND TRANSLATE(**點擊標題下載**)》](https://arxiv.org/pdf/1409.0473.pdf)
* Attention結構圖<br>![](https://github.com/jiayiwang5/Chinese-ChatBot/blob/master/image/image3.png)

## 關鍵點
* LSTM
* seq2seq
* attention 實驗表明加入attention機制後訓練速度快，收斂快，效果更好。
## 語料及訓練環境
  青雲語料庫10萬組對話，在google colaboratory訓練。
## 運行
### 方式一：完整過程
- **數據預處理**<br>
  `get_data`<br>
- **模型訓練**<br>
  `chatbot_train`(此為掛載到google colab版本，本地跑對路徑等需略加修改)<br>
- **模型預測**<br>
  `chatbot_inference_Attention`<br>
### 方式二：加載現有模型
- 運行`chatbot_inference_Attention`<br>
- 加載`models/W--184-0.5949-.h5` 
## 界面(Tkinter)
![](https://github.com/jiayiwang5/Chinese-ChatBot/blob/master/image/image.png)

## Attention權重可視化
![](https://github.com/jiayiwang5/Chinese-ChatBot/blob/master/image/image2.png)

## 其他
* 訓練文件chat_bot中，最後三塊代碼前兩個是掛載谷歌雲盤用的，最後一個是獲取那些loss方便畫圖，不知道為什麽回調函數裏的tensorbord不好使，故出此下策；<br>
* 預測文件裏倒數第二塊代碼只有文字輸入沒界面，最後一塊代碼是界面，根據需求兩塊跑其一即刻；<br>
* 代碼中有很多中間輸出，希望對你理解代碼提供了些許幫助;<br>
* models裏面有一個我訓練好的模型，正常運行應該是沒有問題的，你也可以自己訓練<br>
* 作者能力有限，並未找到量化對話效果的指標，因此loss只能大致反映訓練進度。<br>

"# Chinese_ChatBot" 
"# Chinese_ChatBot" 
"# Chinese_ChatBot" 
