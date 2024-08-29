<div align="center">
  <h1> 📖 專案經驗筆記 Project-workflow-notes 🖊️</h1>
</div>

### 說明:
- 簡單紀錄我的一些專案經驗作為未來檢視、參考用

- 幫助不成熟的我去反思過去更不成熟的我作法、鼓勵自己持續學習

- 用於整理、補充與過往經驗相關最新技術，利於未來revise

### 摘要:
[關鍵製程參數優化](#關鍵製程參數優化): 運用機器學習去實踐製程異常預測，並整合PSO演算法找尋最佳參數與最佳解


------------
## 📝 關鍵製程參數優化 

### 簡介:
- Key Process Parameter Optimization and forcast
  
- Optimization of Second Bond Process Parameters
  - Shorten wire bonding time
    
  - Reduce downtime frequency
    
  - Improve production capacity
    
- Assist in production line decision-making and parameter setting, replacing previous experience-based rules.

### 效益:
#### As-is 😐 
  - Average time for second welding point: 35.33 ms/line.
  - Welding product DOE time is long and trial-and-error costs are high.
  - Ineffective prediction of parameter adjustments’ impact on operations; improper adjustments decrease average fault elimination cycle and reduce capacity.

#### To-be 😄
  - Average time for second welding point: 27.04 ms/line (23% improvement).
  - Establish a decision support interface to provide timely and systematic parameter recommendations based on different product conditions.
  - Model predicts the impact of different parameter combinations on downtime with 89% accuracy and an F1 score of 91%.

### 流程:

1. 資料健檢:
   
   - 確認該製程所有相關資訊資料來源，如當下製程參數、測試參數、停機紀錄、產品別、製程輔助資源資訊(鋼嘴)...
  
   - 與domain確認各參數意義
     
   - 確認欄位有無空缺、異常、極端值，並與domain確認
  
2. 資料檢定
   
   - 利用無母數檢定(如KW-test中位數檢定)，確認有無顯著機差、lot間差距
     
3. 資料平衡
   - 欲建立分類器模型，需要解決資料不平衡問題
  
   - 最後採用SMOTE
     
4. 條件分群
   - 部分產品類型可能會有不同合適製程建議
   
   - 此目的為未來若有新的產品，可以透過分群結果快速得到他建議的生產參數，最為初步測試
  
   - 利用K-means分群，當中分群效果好壞是透過與最終模型的grid search結果得到
  
5. 多分類模型器
   
   - 本專案是採用多種分類模型


   
7. 
   

### 主要工具:
- R code(資料分析與核心撰寫)
- shiny package(介面實現)
https://github.com/user-attachments/assets/7af06eb5-bfa0-40b1-8e24-4b78463181c2



