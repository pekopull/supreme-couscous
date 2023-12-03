# README

初賽與複賽的程式碼大致相同，唯一不同的地方是複賽將初賽訓練好的模型使用新資料繼續訓練，並且微調一部分 Catboost 參數
```
catboost_params = {
    'iterations': 5000,
    'eval_metric': 'F1', #MCC, precision, recall f1
    'early_stopping_rounds': 300,
    'verbose': 20,
    'learning_rate': 0.054,
    'has_time':True,
    'depth':16,
    'grow_policy':"Lossguide",
    'border_count':254,
    'class_weights':{0: 2.0, 1: 1.0},
    'boosting_type': "Plain",
    'score_function':"L2",
    'subsample': 0.8,
    'min_child_samples': 10,
}
```

複賽模型下載連結: https://drive.google.com/file/d/1K4Ni4cyhhuRS6zyETZckNfALSfCytUlB/view?usp=sharing

如果需要.py格式的檔案可以參考初賽繳交的檔案

初賽 Github
https://github.com/pekopull/reimagined-couscous

建議在閱讀時可以打開側邊攔，這樣可以看到各區塊的大標題

![image](https://github.com/pekopull/supreme-couscous/assets/28997752/92e8c860-c688-4286-8918-2603e994db96)
