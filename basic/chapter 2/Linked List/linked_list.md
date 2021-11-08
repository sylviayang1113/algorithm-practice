## 👉👉 单链表

#### 👉 链表初始化

​      链表的头节点指向-1,代表空节点
​      head存的是链表第一个点的下标
​      head不是节点，只是指向某个节点的指针

```
int head, e[N], ne[N], idx;
void init()
{
    idx = 0;
    
    head = -1;
}
```

#### 👉在链表头插入一个数x

```
void insert(int x)
{
    e[idx] = x, ne[idx] = head, head = idx ++ ;
}
```

#### 👉在表中k位置插入x

```
void add(int k,int x){
    n[idx]=x;
    ne[idx]=ne[k];
    ne[k]=idx++;
}
```
#### 👉将k删除（头节点存在）

```
void remove(int k)
{
    ne[k]=ne[ne[k]];

}
```

