# ICIP_Dengue_fever

## tmp.csv
由xml2csv.ipynb產生的csv file
## train.csv
tmp.csv中drop掉含0之rows之後，所產生之訓練資料的csv file
## DataAnalysis.ipynb
訓練資料之初步分析
## Get Image Size.ipynb
為了分析圖片大小以決定anchor box size
## Get_all_imgname.ipynb
為了製作yolo檔案，取得所有圖片檔案路徑用
## json2csv.ipynb
把結果所得到的所有json檔案合併成csv file
## csv2tfrecord.py
將csv檔集中轉為TFrecord檔，作為tensorflow之輸入
```python=
python csv2tfrecord.py --csv_input=train.csv  --output_path=train.record
```
csv_input和output_path是路徑，我都放在同一個資料夾所以直接打檔名
csv2tfrecord.py內部有一些設定，參考[這裡](http://www.icode9.com/content-1-15050.html)   
## xml2csv.ipynb
將原訓練資料之xml檔集中轉為csv檔
## xml2yolo.ipynb
將annotation之xml檔案轉為yolo檔案
![](https://i.imgur.com/JI8v9AZ.png)
## 其他
xml2csv.ipynb中
```python=
all_file = glob.glob("train_annotations/*.xml")
```
為獲取所有訓練資料之xml檔，
其中train_annotations資料夾要自行由網站所下載之壓縮檔解壓縮
