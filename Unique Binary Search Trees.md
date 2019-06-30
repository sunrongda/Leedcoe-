class Solution(object):
dic={0:1,1:1}
def numTrees(self, n  ) :
"""
:type n: int
:rtype: int
"""
dp=[1]
for i in range(1,n+1):
dp.append(0)
for j in range(1,i+1):
dp[i]+=dp[j-1]*dp[i-j]
return dp[n]
