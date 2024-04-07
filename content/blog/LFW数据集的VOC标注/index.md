---
title: LFW数据集的VOC标注
date: 2022-07-19T16:34:00Z
summary: 并没有什么卵用~🤣
---

LFW 数据集标注后的 VOC 格式。一张图片只标注了一张人脸，人脸的范围中包含额头、耳朵等裸露的头部皮肤。

## img_list.py

按照`/lfw/peopleDevTrain.txt`或`/lfw/peopleDevTest.txt`的顺序，将图片路径导出到`/lfw/img_list.txt`。

```python
img_dir_2_txt(is_train = True/False)
```

## jpg_2_dir.py

按照`/lfw/peopleDevTrain.txt`或`/lfw/peopleDevTest.txt`的分类，将图片分别放到`/lfw/train`根目录或`/lfw/test`根目录，不再放置到人名子目录。

```python
# __main__
if __name__ == '__main__':
    img_dir_2_txt(is_train=True)
    copy_img_2_dir(is_train=True)
    img_dir_2_txt(is_train=False)
    copy_img_2_dir(is_train=False)
```

## 相关

使用[chaiwenda/ImgLabel](https://github.com/chaiwenda/ImgLabel)手动标注。

## License

[MIT license](https://github.com/dunxuan/LFW-VOC-Label/blob/main/LICENSE)
