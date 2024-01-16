# Double moving average trading strategy
設計雙均線交易策略並與買進持有比較績效
## 雙均線策略
- 今日收盤出現黃金交叉，下一個交易日開盤立即買進
- 今日收盤出現死亡交叉，下一個交易日開盤立即賣出
## code重點說明
1.  **均線計算**
- 使用rolling(window).mean()計算滾動式窗口平均
2.  **黃金交叉和死亡交叉
- 使用np.where計算data中哪一天出現黃金或死亡交叉
3.  **累計報酬**
- 使用cumsum().apply(np.exp)計算累計報酬
