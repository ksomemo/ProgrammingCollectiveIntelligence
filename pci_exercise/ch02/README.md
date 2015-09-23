# 2章

## 正誤
### p.10

```diff
関数が違う

->> psqrt(pow(4.5-4,2)+pow(4-1,2))
-3.1622776601683795
+>> sqrt(pow(4.5-4,2)+pow(1-2,2))
+1.1180339887498949
```

### p.11
値が異なる

```diff
->> 1/(1+sqrt(pow(5-4,2)+pow(4-1,2)))
-0.2402530733520421
+>> 1/(1+sqrt(pow(4.5-4,2)+pow(1-2,2)))
+0.47213595499957939
```

上記と式が異なり、これが違うので、実行結果も異なる

```diff
 sim_distance
-return 1/(1 + sum_of_squares)
+return 1/(1 + sqrt(sum_of_squares))
```

## 2.3.3 類似性尺度
- Jaccard係数
- マンハッタン距離
- (距離関数)[https://ja.wikipedia.org/wiki/%E8%B7%9D%E9%9B%A2%E5%87%BD%E6%95%B0]

## 2.4 アイテムを推薦する
- 類似度が高い人が評価しているものは高い評価となる
- 類似度を重みとして評価と掛けあわせて推薦の材料にする
- 評価をしていない人は、判断材料から除外する

## 2.6 del.ico.us

### pydelicous
- https://delicious.com/rss
- python2系なので3系のための書き換えが必要
- 本のSampleは0.5なので0.6から書き換えた
- https://code.google.com/p/pydelicious/downloads/list
- google から消えたらPyPIからDonwloadすればよい
 
### 書き換え
- expectの書き方
- printの書き方・out=stderr
- obj.has_key(key): key in obj  
- import library
 - md5: hashlib.md5
 - httplib: http.client
 - StringIO: io
 - urllib: urllib.resuqest, urllib.parse, urllib.error
 - urllib2: 上記からparse除き
 - urllib
  - request
   - Request
   - urlopen
   - HTTPDefaultErrorHandler
   - HTTPPasswordMgrWithDefaultRealm
   - HTTPBasicAuthHandler
   - HTTPPasswordMgr
   - HTTPHandler
   - ProxyHandler
   - build_opener
   - install_opener
  - parse
   - urlencode
   - quote_plus
  - error
   - HTTPError
   - URLError
- unichr: chr
- basestring, unicode: str
- feedparserはpython3対応しているので、pipからinstall
- % lastcall: % self.lastcall
- change default param empty list to None

