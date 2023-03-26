# LaTeX_project_template

LaTeX プロジェクトでは, ビルドの過程で補助ファイルを出力, 参照します. 
このテンプレートは, ソースファイルと補助ファイルの住み分けをする目的で作成したものです. 
ビルドには, `make` コマンドを使用します.

## 数学関連の LaTeX プロジェクト

### ディレクトリ構造

```
math/
├── src/
│   ├── intro.tex
│   ├── main.tex
│   ├── math.bib
│   └── preamble.tex
├── temp/
│   ├── intro/
│   │   ├── intro.aux
│   │   └── intro.out
│   └── main/
│       ├── main.aux
│       ├── main.bbl
│       ├── main.out
│       └── main.toc
├── intro.pdf
├── main.pdf
└── makefile
```

### ビルドコマンド

* `make main` で `main.pdf` をビルド.
* `make mainbib` で参考文献を追加.
* `make intro` で `intro.pdf` をビルド.

## 注意
* `makefile` 内に記述するコマンドのパスは適宜変更してください.
* subfile の追加に応じて, `makefile` にコマンドを追加してください.
