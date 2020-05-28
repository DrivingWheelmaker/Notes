Hanoi Tower:

Classic Solution:

```
def HanoiTower(n, fr, by, to):
	if n<0: print('Parameter should >= 1')
	if n==0: return
	HanoiTower(n-1, fr, to, by)
	print(fr, '-->', to)
	HanoiTower(n-1, by, fr, to)
```

Non-recursive

```
def HanoiTower(n):
    if n<0: print('Parameter should >= 1')
    stack = []
    fr, by, to = 'A', 'B', 'C'
    while not(n==0 and len(stack)==0):
        while n>0:
            stack.append((n,fr,by,to))
            n -= 1
            by, to = to, by
        n, fr, by, to = stack[-1]
        del stack[-1]
        print(fr,'-->',to)
        n -= 1
        fr, by = by, fr
```

