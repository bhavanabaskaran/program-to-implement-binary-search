# program-to-implement-binary-search
def binarySearch(numbers, low, high, x):
if (high &gt;= low):
mid = low + (high - low)//2
if (numbers[mid] == x):
return mid
elif (numbers[mid] &gt; x):
return binarySearch(numbers, low, mid-1, x)
else:

return binarySearch(numbers, mid+1, high, x)
else:
return -1
numbers = [ 9,4,6,7,2,1,5 ]
x = 7
result = binarySearch(numbers, 0, len(numbers)-1, x)
if (result != -1):
print(&quot;Search successful, element found at position &quot;, result)
else:
print(&quot;The given element is not present in the array&quot;)
