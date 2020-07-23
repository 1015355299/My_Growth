# 二分法查找

## 二分法(折半查找)

- 时间复杂度O(logn)级别的查找，在有序队列中使用
- 每次查找范围缩小一半，所以也叫折半查找

代码实现

```js js 二分法
const array = [0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11]
// 基于递归的二分法查找
function search(arr, target, l = 0, r = arr.length - 1) {
  // 超限表示不存在
  if (l > r) return -1;
  // 取中
  let mid = (r + l) >>> 1
  if (arr[mid] == target) { // 相等
    return mid
  }
  if (arr[mid] < target) { // 右边
    return search(arr, target, mid + 1, r) // 右限[mid+1,r]
  }
  if (arr[mid] > target) { // 左边
    return search(arr, target, l, mid - 1) // 左限[l,mid-1]
  }
}
console.log(search(array, 6)) // -1
----------------------------------------------
// 非递归二分法
function search(arr, target, l = 0, r = arr.length - 1) {
  let mid
  // 超限跳出
  while (l <= r) {
    mid = (r + l) >>> 1
    // 找到
    if (arr[mid] == target) {
      return mid
    }
    // 在右边
    if (arr[mid] < target) {
      // 改左限
      l = mid + 1 // [mid+1,r]
    }
    // 在左边
    if (arr[mid] > target) {
      // 改右限
      r = mid - 1 // [l,mid-1]
    }
  }
  // 未找到
  return -1
}
console.log(search(array, 6)) // -1
```

## 二分法查找重复值的索引

代码实现

```js js 二分法查找重复值的索引
function search(arr, target, l = 0, r = arr.length - 1) {
  let mid, res = []
  // 超限跳出
  while (l <= r) {
    mid = (r + l) >>> 1
    // 找到
    if (arr[mid] == target) {
      l = mid // 记录目标关键位置
      break
    }
    // 在右边
    if (arr[mid] < target) {
      // 改左限
      l = mid + 1 // [mid+1,r]
    }
    // 在左边
    if (arr[mid] > target) {
      // 改右限
      r = mid - 1 // [l,mid-1]
    }
  }
  while (arr[--l] == target && l >= 0); // 左界
  while (arr[++l] == target && l < arr.length) { // 右界
    res.push(l)
  }
  return res.length ? res : -1
}
console.log(search(array, 7)) // [3,4,5,6,7]
```

<Vssue title="算法 issue" />