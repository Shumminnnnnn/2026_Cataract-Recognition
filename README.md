# 2026_Cataract-Recognition
2026 DL bonas project. 


## Cataract Classification with ResNet-50
使用遷移學習 (ResNet-50) 對眼底/眼部影像進行白內障分類,區分immature(未成熟白內障)與mature(成熟白內障)兩類。本專案在Google Colab上以PyTorch實作,並針對小型且經過增強的資料集做了避免資料洩漏的嚴謹處理。

## 專案特色
- 使用ResNet-50遷移學習
- 依原始圖片分組切割，避免增強版影像洩漏到測試集
- 可繪製訓練、驗證的Loss與Accuracy曲線
- 建立Confusion Matrix與Precision/Recall/F1 
- (可選用)GroupKFold交叉驗證
- 可上傳自己的圖片進行預測
- 將訓練好的模型存成 .pth

## 專案結構

├── README.md
├── LICENSE 
├── cataract_resnet50.ipynb    
└── data/
    └── train/
        ├── immature/               
        └── mature/                 
        
## 執行方法
1. 將cataract_resnet50.ipynb上傳到Colab。
2. 選擇GPU(T4)。
3. 依序執行每個cell。第2個cell需上傳自己的kaggle.json，用來下載資料集。
   (若不想用Kaggle下載,也可以直接使用本repo data/資料夾中的影像，將notebook的TRAIN_DIR指向該資料夾即可。)


