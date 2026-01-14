---
layout: post
title: "二分查找：左边界模板"
date: 2026-01-14
categories: [算法, 二分]
tags: [binary-search, template]
---

## 模板（左边界）

```cpp
int lower_bound(vector<int>& a, int x){
  int l = 0, r = (int)a.size(); // [l, r)
  while(l < r){
    int m = l + (r - l) / 2;
    if(a[m] >= x) r = m;
    else l = m + 1;
  }
  return l;
}
