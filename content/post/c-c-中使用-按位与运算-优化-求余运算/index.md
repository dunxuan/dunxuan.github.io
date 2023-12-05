---
title: C/C++中使用 按位与运算 优化 求余运算
date: 2022-11-01T10:48:00.000Z
draft: false
featured: false
image:
  filename: c-c-中使用-按位与运算-优化-求余运算.png
  focal_point: Smart
  preview_only: false
---
C/C++中使用 按位与运算 优化 求余运算，**仅限除数为 2^n 时**。
核心算法：

```cpp
(dividend % divisor) == (dividend & (divisor - 1));
```

```cpp
#include <iostream>
#include <cmath>

int main(void)
{
  int dividend = 100;
  int divisor = 16;
  int result1 = dividend % divisor;
  int result2 = dividend & (divisor - 1);

  printf("result1 = %d\nresult2 = %d", result1, result2);

  return 0;
}
```

运行结果：

```cpp
result1 = 4
result2 = 4
```