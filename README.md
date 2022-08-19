# leetcode-278-binary-2


            #The isBadVersion API is already defined for you.
            #@param version, an integer
            #@return a bool
            #def isBadVersion(version):

二分法取临界值：

            class Solution(object):
                def firstBadVersion(self, n):
                    """
                    :type n: int
                    :rtype: int
                    """
                    l = 1
                    r = n
                    while l <= r:
                        mid = (l+r)//2
                          # 以上都是一样的套路，注意while/ <=/ 取整数//2
                        if isBadVersion(mid) == False:
                            l = mid+1
                        else:
                            r = mid -1
                              # 这里只有两个可能：T/F。
                              # 因为要的是最大的false，所以跟着false走，取了left
                    return l 
