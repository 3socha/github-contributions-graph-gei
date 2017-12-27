# Contributions Graph 芸

## 第33回シェル芸勉強会 大阪サテライトLT
## 2018/1/27
## so

>>>

- [スライド](https://horo17.github.io/github-contributions-graph-gei/)

>>>

## `$ whoami`

![so](img/so.png)

* so ([@3socha](https://twitter.com/3socha))
* インフラエンジニア (AWS/Azure)

---

## GitHub Contributions Graph

これ

![ContributiosGraph](img/GitHubContributionsGraph.png)

進捗ダメ

>>>

## ハックする

[ github contributions graph hack ] [🔍検索](https://www.google.co.jp/search?q=github+contributions+graph+hack&tbm=isch)

---

## Contributions Graph もどきをシェル芸で

```
$ cat /dev/urandom | xxd -p | head -20 | grep -o . | awk '{switch($0){case 1:v=150;break;case 2:v=113;break;case 3:v=65;break;case 4:v=22;break;default: v=254}printf "\033[38;5;"v"m■ "}' | grep -oP '(?:\e[^\e]*){7}' | head -52 | rs -T | sed -E 's/ +/ /g'
```


