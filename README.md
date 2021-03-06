# emo メモリー

<img width="795" alt="スクリーンショット 2022-02-27 21 40 37" src="https://user-images.githubusercontent.com/66903388/155882734-f398892a-1633-445c-a148-a01092d0bbd6.png">

## 製作期間

v1→2021/08~09

v2→2022/02/16~02/27（今回）

## 概要

感情ベースで思ったことを呟けるメモアプリ。

`喜怒哀楽`の感情をイメージした色とキャラクターを使って感情ベースで投稿ができ、それを見返すことで自分が普段どんな感情を持って生活しているのかを分析できる。

## 作ったきっかけ

これまで Backend(Ruby on Rails)、Frontend(React＆JavaScript)を使った SPA アプリ開発を主に行ってきました。

そんな中で 2021 年（大学３年）の夏休みに作成したのが、この emo メモリーの前のバージョンになります。

そして、今回 TypeScript を練習したいという思いもあって、過去の emo メモリーを持ち出して、拙かったデザインをリニューアル、React を TypeScript で書いて一から作り直しました。

## 今回頑張ったこと

- チーム開発の経験が浅く、Github を使いこなせていないと感じていたため、今回はチーム開発の簡単な流れを反復しながら擬似チーム開発的に開発しました。
- また、Github の Projects も積極的に使用しました。

## 今回の反省

- 個人的に作ってきた分、その都度リファクタリングをせずにまとめてやろうとしてしまったため、コンポーネントがかなり膨れてしまい、後から共通するコンポーネントに分割するのがかなり難しくなってしまいました。

- コンポーネントや関数の命名にもっと明確なルールを決めてから始めるべきでしたが、その場の思いつきで命名してしまう面もあったためひと目でわかりにくい名前をつけてしまうことがありました。

## 主な使用技術

### Backend

- ruby
- rails
- devise
- devise-token-auth
- rack-cors

### Frontend

- react
- typescript
- dayjs
- @chakra-ui/react
- @chakra-ui/icons
- react-router-dom
- js-cookie
- axios
- axios-case-converter
- @fullcalendar/react
- eslint
- prettier

## URL

### Frontend リポジトリ

https://github.com/Matsushoooo12/EmoMemory-Frontend-v1

### Backend リポジトリ

https://github.com/Matsushoooo12/EmoMemory-API-v1

## 利用方法

- 新規投稿ページで感情にあったカードを選び投稿。
- 投稿一覧で自分のもの以外の投稿も見られる。
- プロフィールページでプロフィール編集や自分の投稿一覧を見ることができる。

## 目指した課題解決

コロナ化で人と会う機会も少ない中で、思ったことや本音を吐き出したいけどそれを吐き出す相手がいなくて内に溜まっていることが多くなったと個人的に感じています。

しかし、SNS で知り合いなどがいる中で発信するほどでもないなと思って吐き出せないストレスがある人も多いと思います。

それを吐き出す時に自分だけが見られるメモに書くのも良いですが、より外に思っていることを吐き出してスッキリするためには世界に発信する感覚が必要だと思いました。

そこで、喜怒哀楽それぞれごとに分けて投稿できる SNS のような作りにして、外に発信しつつ、自分のマイページで自分の投稿一覧を見ることができ、過去に投稿したものが喜怒哀楽のどれに当てはまることが多いのか、またどのようなことを書き留めているのかを振り返られるようにしました。

## ページ説明

### 新規登録ページ

<img width="1292" alt="スクリーンショット 2022-02-27 16 35 35" src="https://user-images.githubusercontent.com/66903388/155889456-12e22265-a7dd-4cf4-9660-f1650ef4c727.png">

- 名前、メールアドレス、パスワード、パスワード確認を入力して登録できる。

### ログインページ

<img width="1292" alt="スクリーンショット 2022-02-27 16 35 44" src="https://user-images.githubusercontent.com/66903388/155889482-c34b4058-8033-49d9-9404-297321a3faa7.png">

- 新規登録したユーザーのメールアドレス、パスワードを入力してログインできる。

### 新規投稿作成

<img width="1292" alt="スクリーンショット 2022-02-27 16 32 33" src="https://user-images.githubusercontent.com/66903388/155884659-4693639e-fbdd-482f-a50b-7703f38e7b7f.png">

- フォームの上の４つの顔ボタンを押したらそれぞれのフォームに切り替えられて、そのフォームで投稿したらそのメモが作成される。

### 投稿一覧

<img width="1292" alt="スクリーンショット 2022-02-27 16 32 27" src="https://user-images.githubusercontent.com/66903388/155884681-4e3f843f-871e-48cb-b812-1b8fc5f3bc17.png">

- 作成した感情のメモがこの投稿一覧ページに挿入される。ユーザー名などはなく、それぞれのユーザー詳細もないため完全匿名で投稿ができる。
- このページの投稿は全てのアカウントの投稿が表示される。
- All ボタンをクリックすると全ての感情カード一覧が、それぞれの感情の顔をクリックするとそれぞれの感情のカード一覧が表示される。
- それなボタンをクリックすることで`いいね`ができる。自分の投稿にいいねがあることで、匿名性を持ちながら承認欲求を満たすことができる。

### ログインユーザー投稿詳細

<img width="1292" alt="スクリーンショット 2022-02-27 16 32 49" src="https://user-images.githubusercontent.com/66903388/155884696-f39b19b1-e005-4bc5-84db-f8925b7fd359.png">

- 枠の付いている投稿一覧のそれぞれの投稿をクリックするとログインユーザーの投稿詳細のモーダルが出る。
- ログインユーザーの投稿であれば、投稿編集と投稿削除ができる。

### その他のユーザー投稿詳細

<img width="1292" alt="スクリーンショット 2022-02-27 16 32 54" src="https://user-images.githubusercontent.com/66903388/155885494-b5a84f00-ac03-495a-8551-55e379ad6657.png">

- 枠の付いていない投稿一覧のそれぞれの投稿をクリックするとログインユーザー以外の投稿詳細のモーダルが出る。

### プロフィール

<img width="1292" alt="スクリーンショット 2022-02-27 16 33 00" src="https://user-images.githubusercontent.com/66903388/155885543-0c0bed9a-5de4-489e-a4b4-60b7c484afa5.png">

- ログインユーザーの名前とメールアドレスが表示され、背景には現在の感情の色を指定している。
- 月表示カレンダーをつけて、1 日で多い投稿の感情の色をその日の背景に設定する（未実装）

### ログインユーザーのプロフィール編集

<img width="1292" alt="スクリーンショット 2022-02-27 16 33 11" src="https://user-images.githubusercontent.com/66903388/155885569-2cdc7ce5-6f27-474a-acf5-2e5897c86789.png">

- `Edit Profile`ボタンをクリックするとユーザー編集モーダルが出てくる。
- ここで設定した感情に一致した色がプロフィール背景に設定される。
- また、Header の名前の横の顔にも設定される。
- デフォルトでは`喜`の黄色いキャラクターが設定されている。

### ログインユーザーの投稿一覧

<img width="1292" alt="スクリーンショット 2022-02-27 16 33 25" src="https://user-images.githubusercontent.com/66903388/155885645-8f1becb3-d41e-4468-9722-e361bbf772cc.png">

- ログインユーザーの投稿一覧が表示されている。
- All ボタンをクリックすると全ての感情カード一覧が、それぞれの感情の顔をクリックするとそれぞれの感情のカード一覧が表示される。

## 実装予定の機能

- プロフィールページのカレンダーにその日一日の投稿で一番多い投稿数がある感情の色の背景にする。
- プロフィールページにレーダーチャートを付けて、これまでの投稿の感情の割合を可視化する。

## データベース設計

<img width="501" alt="スクリーンショット 2022-02-28 0 31 28" src="https://user-images.githubusercontent.com/66903388/155888862-ea2a0506-080a-470a-8442-ddbccc6b7729.png">

## ローカルでの動作方法

### Backend

```
$ git clone https://github.com/Matsushoooo12/EmoMemory-API-v2.git
$ cd EmoMemory-API-v2
$ rails db:migrate
```

### Frontend

```
$ git clone https://github.com/Matsushoooo12/EmoMemory-Frontend-v1.git
$ cd EmoMemory-Frontend-v1
$ rm -rf node_modules
$ npm install
```
