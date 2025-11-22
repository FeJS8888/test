# 3500 常用汉字

本仓库包含一个 JSON 文件，收录了 3500 个常用汉字。

## 文件结构

### chinese_characters_3500.json

JSON 文件包含一个由 3500 个对象组成的数组，每个对象代表一个汉字，结构如下：

```json
[
  {
    "name": "的",
    "phrases": ["目的", "有的放矢"],
    "meaning": "助词，用在定语后；真正，确实"
  },
  ...
]
```

每个对象包含：
- **name**: 汉字本身
- **phrases**: 包含 2 个使用该汉字的词语示例
- **meaning**: 汉字的中文释义和定义

## 字符选择

这些汉字基于《通用规范汉字表》，按使用频率组织：
- 一级字表：最常用的 1000 个汉字（使用频率最高）
- 二级字表：常用的 1500 个汉字（使用频率中等）
- 三级字表：较少使用但仍重要的 1000 个汉字

最常用的 192 个汉字有详细准确的词语和释义。其他汉字有生成的示例数据。

## 生成脚本

`generate_chinese_characters.py` 脚本用于创建此 JSON 文件。可以运行它来重新生成文件：

```bash
python3 generate_chinese_characters.py
```

## 文件信息

- 总字符数：3500
- 文件大小：约 207KB
- 格式：JSON（UTF-8 编码）
- 结构：对象数组

## 使用方法

您可以在各种应用程序中加载和使用这些数据：

```python
import json

with open('chinese_characters_3500.json', 'r', encoding='utf-8') as f:
    characters = json.load(f)
    
# 访问字符数据
for char in characters[:5]:
    print(f"{char['name']}: {char['meaning']}")
    print(f"词语: {', '.join(char['phrases'])}")
```

```javascript
// 在 Node.js 或浏览器中
const characters = require('./chinese_characters_3500.json');

characters.forEach(char => {
    console.log(`${char.name}: ${char.meaning}`);
    console.log(`词语: ${char.phrases.join(', ')}`);
});
```
