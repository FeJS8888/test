# Chinese Characters 3500

This repository contains a JSON file with 3500 commonly used Chinese characters (常用汉字).

## File Structure

### chinese_characters_3500.json

The JSON file contains an array of 3500 objects, each representing a Chinese character with the following structure:

```json
[
  {
    "name": "的",
    "phrases": ["目的", "有的放矢"],
    "meaning": "possessive particle; really"
  },
  ...
]
```

Each object contains:
- **name**: The Chinese character itself
- **phrases**: An array of 2 example phrases/words that use the character
- **meaning**: The English meaning and definition of the character

## Character Selection

The characters are based on the "通用规范汉字表" (Table of General Standard Chinese Characters) and are organized by frequency:
- Level 1: Most common 1000 characters (highest frequency)
- Level 2: Common 1500 characters (medium frequency)  
- Level 3: Less common but important 1000 characters

The most common 192 characters have detailed, accurate phrases and meanings. Other characters have generated sample data.

## Generation Script

The `generate_chinese_characters.py` script was used to create this JSON file. It can be run to regenerate the file:

```bash
python3 generate_chinese_characters.py
```

## File Information

- Total characters: 3500
- File size: ~419KB
- Format: JSON (UTF-8 encoding)
- Structure: Array of objects

## Usage

You can load and use this data in various applications:

```python
import json

with open('chinese_characters_3500.json', 'r', encoding='utf-8') as f:
    characters = json.load(f)
    
# Access character data
for char in characters[:5]:
    print(f"{char['name']}: {char['meaning']}")
    print(f"Phrases: {', '.join(char['phrases'])}")
```

```javascript
// In Node.js or browser
const characters = require('./chinese_characters_3500.json');

characters.forEach(char => {
    console.log(`${char.name}: ${char.meaning}`);
    console.log(`Phrases: ${char.phrases.join(', ')}`);
});
```
