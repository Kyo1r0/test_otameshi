# JOI1次予選レベルの問題　解答例

## A

1時間は60分なので、Hを60倍してMを足した結果を出力すればよいです。

```python
H=int(input())
M=int(input())

print(60*H+M)
```

## B

まずはAとBの和をとって変数waに代入します。そして、strを用いてwaを文字列に変換し、lenを用いてその長さを出力します。

整数型データを文字列型にして、その長さを求めることで桁数を求めるというのは、よくあるテクニックです。

```python
A=int(input())
B=int(input())

wa=A+B
print(len(str(wa)))
```

## C

ここではflagを用いる解法を紹介します。flagはTrueかFalseを入れておく変数で、ある条件が成り立つかどうかを判断するときに使います。

Sがすべて同じ文字かを判断すればいいので、愚直にfor文を回して、隣り合う文字が同じかどうかを判断すればいいです。forのループ変数$i$の最大値が$N-1$であることに注意しましょう。

具体的には、最初にflagをTrueにして、for文を回して、隣り合う文字が異なる場合にflagをFalseにして、最後にflagがTrueであればYes、FalseであればNoを出力すればいいです。

flagが良く分からない人は、何か変数に1とか0とかを代入し、違う文字が出てきたらそれを変更し、for文のあとでその変数を見て最初と同じかどうかを判断し、YesかNoを出力するという方法でもいいです。

```python
N=int(input())
S=input()

flag=True
for i in range(N-1):
    if S[i]!=S[i+1]:
        flag=False
if flag:
    print("Yes")
else:
    print("No")
```

## D

問題の条件をよく読んで、愚直に$A_i+K=B_[j]$となるような$i,j$の組み合わせの数をカウントすれば大丈夫です。

二重ループは上位の問題では計算量が多く間に合わない手法ですが、今回は$1 \leqq N,M \leqq 100$なので、二重ループとしても計算量は高々$10^4$程度なので、十分間に合います。

```python
K=int(input())
N=int(input())
A=list(map(int,input().split()))
M=int(input())
B=list(map(int,input().split()))

ans=0
for i in range(N):
    for j in range(M):
        if A[i]+K==B[j]:
            ans+=1
print(ans)
```