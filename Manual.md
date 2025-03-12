# マニュアル

## Features

### 💅 Lint text

[textlint](https://github.com/textlint/textlint) での自動校正が可能です。

```
$ yarn lint --fix
```

[husky](https://github.com/typicode/husky) によって commit 前にも自動で実行されます。  
校正のルールは`.textlintrc`に記載しています。

### 📝 Convert Markdown to PDF

[md-to-pdf](https://www.npmjs.com/package/md-to-pdf) での PDF 生成が可能です。

```
$ yarn build:pdf
```

出力される PDF は CSS で任意のスタイルを設定可能です。`pdf-configs/style.css`を編集してください。

### 🛠 Create release

`v**` tag をつけて push すると GitHub Actions でビルドが走り、PDF の生成、Release の作成、Assets へ PDF の登録が実行されます。

```
$ git commit -m "add job"
$ git tag v1.0
$ git push origin --tags
```

### 📆 Remind update

GitHub Actions の schedule trigger で 3 ヶ月に 1 回、職務経歴書の内容更新を促す issue が自動生成されます。

期間の変更、Job の停止は[.github/workflows/create-issue.yml](https://github.com/Yuki2Kisaragi/resume/blob/master/.github/workflows/create-issue.yml) を編集してください。
