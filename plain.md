- **迭代器**

  ```c++
  vector<int> v;
  const vector<int> cv;
  auto it1 = v.begin();  // it1 has type vector<int>::iterator
  auto it2 = cv.begin(); // it2 has type vector<int>::const_iterator
  ```

  可以使用`cbegin`和`cend`指定获取只读的迭代器

  ```C++
  auto it3 = v.cbegin(); // it3 has type vector<int>::const_iterator
  ```

  dereference：

  ```C++
  (*it).empty() // dereferences it and calls the member empty on the resulting object
  *it.empty()   // error: attempts to fetch the member named empty from it
                //     but it is an iterator and has no member named empty
  it -> empty() //简化了上面的()操作
  ```

  迭代器算术：
  ![image-20241117232633796](C:\Users\MoooYuuu\AppData\Roaming\Typora\typora-user-images\image-20241117232633796.png)

  值得注意的是，迭代器之间**没有加法**，迭代器之间的**减法返回值类型是deference_type**

