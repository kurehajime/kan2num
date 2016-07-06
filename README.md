# cjk2num

[![CircleCI](https://circleci.com/gh/kurehajime/cjk2num.svg?style=svg)](https://circleci.com/gh/kurehajime/cjk2num) / [GoDoc](https://godoc.org/github.com/kurehajime/cjk2num)

Convert /漢数字|中文数字|한자 숫자/  to number.

ようするに漢数字を数字に変換するやつ



## コマンドとしての使い方

漢数字を引数として渡すと数字に変換してくれる


```
$ cjk2num 二百五十一

>251
```

## ライブラリとしての使い方

漢数字をstring型で渡すとfloat64の数字として返ってくる。

```
import (
	"github.com/kurehajime/cjk2num"
)
func main(){
  var num float64
  var 漢数字="千二百六十万"
  num, err := cjk2num.Convert(漢数字)
  if err != nil {
    Println(err.Error())
  }
  Println(num)//12600000.0000
}
```

## インストール方法

[ここから](https://github.com/kurehajime/cjk2num/releases)ダウンロード。

ライブラリとして利用する場合はgo getで。

```
$ go get -u github.com/kurehajime/cjk2num/...
```
