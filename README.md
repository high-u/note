# Note

## このリポジトリについて

過去の失敗は忘れて、ブログじゃなくて自身のノートを公開するスタンスで書いていくつもり。

## このリポジトリ構築の履歴

```bash
gh auth login
gh repo create note --public
```

```bash
npm create astro@latest -- --template satnaing/astro-paper
```

```text
? Where would you like to create your new project? › note
? Would you like to install npm dependencies? (recommended) › Y
? Would you like to initialize a new git repository? (optional) › Y
? How would you like to setup TypeScript? › - Use arrow-keys. Return to submit.
❯   Strict - (recommended)
    Strictest
    Relaxed
    Help me choose
```

```bash
cd note
git add .
git commit -m "first commit"
git branch -M main
git remote add origin https://high-u@github.com/high-u/note.git
git push -u origin main
```

```bash
rm -rf public/googlebbcd930f1ecacd3a.html
mv README.md astro-paper.README.md
touch README.md
```

```bash
vim src/config.ts
vim src/pages/index.astro
vim src/components/Header.astro
vim src/components/Footer.astro
```
