def profit(arr, k):
    n = (min(arr) + max(arr)) // 2
    new = []
    for i in arr:
        if max(arr) - min(arr) < k:
            return max(arr) - min(arr)
        elif i >= n:
            new.append(i - k)
        else:
            new.append(i + k)
    return max(new) - min(new)


array = [2, 9, 16]
K = 6
print("Maximum difference is :", profit(array, K))
