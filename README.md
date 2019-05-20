# ICIP_Dengue_fever

## tmp.csv
訓練資料的csv file
## xml2csv.ipynb
將原訓練資料之xml檔集中轉為csv檔
## DataAnalysis.ipynb
訓練資料之初步分析
## 其他
xml2csv.ipynb中
```python=
all_file = glob.glob("train_annotations/*.xml")
```
為獲取所有訓練資料之xml檔，
其中train_annotations資料夾要自行由網站所下載之壓縮檔解壓縮
