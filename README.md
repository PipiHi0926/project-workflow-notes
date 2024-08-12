<div align="center">
  <h1> 📖 專案經驗筆記 Project-workflow-notes 🖊️</h1>
</div>

### 說明:
- 簡單紀錄我的一些專案經驗作為未來檢視、參考用

- 幫助不成熟的我去反思過去更不成熟的我作法、鼓勵自己持續學習

- 用於整理、補充與過往經驗相關最新技術，利於未來revise

### 摘要:

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

### 工具:
R code(資料分析與核心撰寫), shiny package(介面實現)
https://github.com/user-attachments/assets/7af06eb5-bfa0-40b1-8e24-4b78463181c2



