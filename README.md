# Udacity 灾难管道课程    
## 项目概述：
    通过项目给的数据，建立数据ETL管道和机器学习管道，对事件进行分类。
## 数据来源：
    messages,categories数据集
## 文档结构：
- | Readme.md自述文档
- |   
- +-App
- | | run.py //运行Web应用程序的Flask文件
- | |   
- |  --- templates //包含Web应用程序的html文件
- | go.html
- | master.html
- |           
- +-Data
- | DisasterResponse.db // ETL管道的输出
- | crash_categories.csv //所有类别的数据文件
- | crash_messages.csv //所有消息的数据文件
- | process_data.py // ETL管道脚本
- |       
- +-models
- | train_classifier.py//用于训练和导出分类器的机器学习管道脚本
## 项目结构：
### 1.ETL 管道
    在 Python 脚本 process_data.py 中，编写一个数据清洗管道，实现：加载 messages 和 categories数据集将两个数据集进行合并(merge)，清洗数据，将其存储到 SQLite 数据库中
### 2.机器学习管道
    在 Python 脚本 train_classifier.py 中编写机器学习管道，实现：
    从 SQLite 数据库中加载数据
    将数据集分成训练和测试集
    搭建文本处理和机器学习管道
    使用 GridSearchCV 对模型进行训练和微调
    输出测试集的结果    
    将最终的模型输出为 pickle 文件
### 3.项目演示
    1. 在项目的根目录中运行以下命令来设置数据库和模型。
    - 运行ETL管道来清理数据并存储在数据库中:
        `python data/process_data.py data/disaster_messages.csv data/disaster_categories.csv data/DisasterResponse.db`
    - 运行训练分类器并保存: 
        `python models/train_classifier.py data/DisasterResponse.db models/classifier.pkl`

    2. 在应用程序的目录中运行以下命令以运行web应用程序.
        `python run.py`
    3. 运行 http://127.0.0.1:3001/

