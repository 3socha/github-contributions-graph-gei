# Contributions Graph 芸

## 第33回シェル芸勉強会 大阪サテライトLT
## 2018/1/27
## so

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

## Contributions Graph みたいなのをシェル芸で

- [ANSI カラー](https://en.wikipedia.org/wiki/ANSI_escape_code)で `■` に色を付けて出力

| Commit | CSS Color Code | RGB (6段階) | ANSI Color Code |
| --- | --- | --- | --- |
| 0 | <p style="color:#eeeeee">#eeeeee</p> |  -  | <p style="color:#e4e4e4">254</p> |
| 1 | <p style="color:#c6e48b">#c6e48b</p> | 342 | <p style="color:#afd787">150</p> |
| 2 | <p style="color:#7bc96f">#7bc96f</p> | 241 | <p style="color:#87d75f">113</p> |
| 3 | <p style="color:#239a3b">#239a3b</p> | 121 | <p style="color:#5f875f">65</p> |
| 4 | <p style="color:#196127">#196127</p> | 010 | <p style="color:#005f00">22</p> |

- `ANSI Color Code = 36 * R + 6 * G + B + 16`

>>>

## で、こんな感じ

```
$ cat /dev/urandom | xxd -p | head -10 | grep -o . | awk '{switch($0){case 1:v=150;break;case 2:v=113;break;case 3:v=65;break;case 4:v=22;break;default: v=254}printf "\033[38;5;"v"m■ "}' | grep -oP '(?:\e[^\e]*){7}' | head -52 | rs -T | sed -E 's/ +/ /g'
```
