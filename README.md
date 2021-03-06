
## 语义理解/口语理解
>>> 采用了深度学习等技术

主要功能：
* 中文分词
* 词性标注
* 命名实体识别
* 领域分类
* 槽填充
* 意图识别

spoken举例：
```
上海的天气
厦门明天会不会下雨
姚明真正的身高是多少
```

### 使用方式
```shell
python3 test.py
```

解析结果
```shell
{
    "input": "厦门明天会不会下雨", 
    "semantics": [
        {
            "score": "0.8", 
            "domain": "天气", 
            "intent": "雨", 
            "slot": [
                [
                    "城市", 
                    "厦门"
                ], 
                [
                    "日期", 
                    "明天"
                ]
            ]
        }
    ], 
    "词法分析": {
        "词性标注": [
            "地名", 
            "时间词", 
            "动词", 
            "动词", 
            "动词"
        ], 
        "实体识别": [
            "B-地名", 
            "O", 
            "O", 
            "O", 
            "O"
        ], 
        "中文分词": [
            "厦门", 
            "明天", 
            "会", 
            "不会", 
            "下雨"
        ]
    }
}
```