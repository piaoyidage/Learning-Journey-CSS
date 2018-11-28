# word-break/word-wrap

## word-break

规定了文本长度超过内容盒子的时候，如何换行

**属性值**

normal | break-all | keep-all | break-word

### normal

默认的换行规则

### break-all

为防止溢出，可以在任意两个字符之间换行

### keep-all

连续字符不换行，非 CJK 文字表现和 normal 一致

### break-word

为了防止溢出，如果行中没有其他可接受的断点，通常不可破坏的单词可能会在任意点被破坏。 

简单来说，如果这个单词很长，另起一行仍然不能放全，则会被截断

**目前 break-word 在 Firefox 、IE 等浏览器不支持**

## word-wrap

**word-wrap 已经改名为 overflow-wrap**

**属性值**

normal | break-word

### break-word

**表现与 word-break 中的 break-word 一致，目前浏览器均支持**

从实际使用来看，有些情况下 word-wrap: break-word 会失效，[word-wrap not working](https://codepen.io/piaoyidage/pen/dQgbEN)

**建议 word-break 和 word-wrap 一起使用**

```
word-break: break-word;
word-wrap: break-word;
```




