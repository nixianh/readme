leetcode 经典堆相关题目
https://labuladong.github.io/algo/4/29


# 滑窗算法
```c
/* 滑动窗口算法框架 */
void slidingWindow(string s, string t) {
    unordered_map<char, int> need, window;
    for (char c : t) need[c]++;
    
    int left = 0, right = 0;
    int valid = 0; 
    while (right < s.size()) {
        char c = s[right];
        // 右移（增大）窗口
        right++;
        // 进行窗口内数据的一系列更新

        while (window needs shrink) {
            char d = s[left];
            // 左移（缩小）窗口
            left++;
            // 进行窗口内数据的一系列更新
        }
    }
}

```

# 回溯算法
代码方面，回溯算法的框架：
```c
result = []
def backtrack(路径, 选择列表):
    if 满足结束条件:
        result.add(路径)
        return
    
    for 选择 in 选择列表:
        做选择
        backtrack(路径, 选择列表)
        撤销选择
```
```python
def backtrace(self, nums, start): 
        # 判断visited not 0:
        #   return
        # 加入track，visited set 1
        # 判断是否满足条件
        #     加入结果
        # for 相邻节点遍历：
        #     backtrace递归
        # 移除track列表, visited set 0
```
# DFS
```
        # 判断visited not 0:
        #   return

           work
        # visited set 1
        # 判断是否满足条件
        #     加入结果
        # for 相邻节点遍历：
        #     backtrace递归
        #  visited set 2

def dfs(self):
        for aVertex in self:
            aVertex.setColor('white')
            aVertex.setPred(-1)
        for aVertex in self:
            if aVertex.getColor() == 'white':
                self.dfsvisit(aVertex)

    def dfsvisit(self,startVertex):
        startVertex.setColor('gray')
        self.time += 1
        startVertex.setDiscovery(self.time)
        for nextVertex in startVertex.getConnections():
            if nextVertex.getColor() == 'white':
                nextVertex.setPred(startVertex)
                self.dfsvisit(nextVertex)
        startVertex.setColor('black')
        self.time += 1
        startVertex.setFinish(self.time)
```
