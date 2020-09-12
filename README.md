# Udacity 灾难管道课程    
##项目概述：
通过项目给的数据，建立数据ETL管道和机器学习管道，对事件进行分类。
##数据来源：
messages,categories数据集
##项目结构：
###1.ETL 管道
在 Python 脚本 process_data.py 中，编写一个数据清洗管道，实现：
加载 messages 和 categories 数据集
将两个数据集进行合并 (merge)
清洗数据
将其存储到 SQLite 数据库中
###2.机器学习管道
在 Python 脚本 train_classifier.py 中编写机器学习管道，实现：
从 SQLite 数据库中加载数据
将数据集分成训练和测试集
搭建文本处理和机器学习管道
使用 GridSearchCV 对模型进行训练和微调
输出测试集的结果
将最终的模型输出为 pickle 文件
###3.项目演示
1. Run the following commands in the project's root directory to set up your database and model.

    - To run ETL pipeline that cleans data and stores in database
        `python data/process_data.py data/disaster_messages.csv data/disaster_categories.csv data/DisasterResponse.db`
    - To run ML pipeline that trains classifier and saves
        `python models/train_classifier.py data/DisasterResponse.db models/classifier.pkl`

2. Run the following command in the app's directory to run your web app.
    `python run.py`

3. Go to http://0.0.0.0:3001/

