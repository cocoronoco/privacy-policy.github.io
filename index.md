import base64

# index.md content (Markdown with embedded CSS link)
index_md = """---
layout: default
title: プライバシーポリシー
---

<link rel="stylesheet" href="style.css">

<div class="container">

# プライバシーポリシー

このプライバシーポリシーは、[あなたの拡張機能名]（以下「本拡張機能」）の利用におけるユーザー情報の取り扱いについて説明するものです。

最終更新日: 2024年4月29日

## 1. データの収集と利用
本拡張機能は、ユーザーの個人を特定できる情報（氏名、住所、メールアドレス、電話番号など）を一切収集しません。また、ブラウジング履歴やウェブサイトのコンテンツなどの機密性の高い情報を外部サーバーに送信することもありません。

## 2. データの保存
本拡張機能の設定や一時的なデータ（もしあれば）は、すべてユーザーのローカルデバイス上のブラウザストレージ（`chrome.storage.local` 等）にのみ保存されます。これらのデータが開発者や第三者に共有されることはありません。

## 3. 権限（パーミッション）の使用について
本拡張機能が要求する権限は、機能を提供するために最低限必要なものに限定されています。
- **[例: storage]**: ユーザーの設定を保存するために使用します。
- **[例: activeTab]**: 現在開いているタブに対して機能を提供するために使用します。
これらの権限を通じて取得されたデータが、外部に漏洩したり収集されたりすることはありません。

## 4. Google User Data Policyへの準拠
本拡張機能は、Chromeウェブストアの[ユーザーデータに関するポリシー](https://developer.chrome.com/docs/webstore/program-policies/user-data-faq)（Limited Use要件を含む）を遵守しています。
- ユーザーの利益を第一の目的としてデータを取り扱います。
- 広告配信、クレジットスコアの算出、またはその他の不適切な目的でユーザーデータを利用することはありません。

## 5. 第三者への開示
本拡張機能はデータを収集しないため、第三者にデータを販売または提供することはありません。

## 6. ポリシーの変更
本プライバシーポリシーは、必要に応じて更新されることがあります。重要な変更がある場合は、拡張機能のアップデート情報などを通じてお知らせします。

## 7. お問い合わせ
本ポリシーに関するご質問がある場合は、以下の連絡先までお問い合わせください。

- 開発者: [あなたの名前 または 組織名]
- メールアドレス: [あなたのメールアドレス]

</div>
"""

# style.css content
style_css = """
body {
    font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif;
    line-height: 1.6;
    color: #333;
    background-color: #f8f9fa;
    margin: 0;
    padding: 0;
}

.container {
    max-width: 800px;
    margin: 40px auto;
    padding: 40px;
    background-color: #fff;
    box-shadow: 0 4px 6px rgba(0,0,0,0.1);
    border-radius: 8px;
}

h1 {
    color: #0056b3;
    border-bottom: 2px solid #0056b3;
    padding-bottom: 10px;
    margin-bottom: 30px;
    font-size: 24pt;
}

h2 {
    color: #2c3e50;
    border-left: 5px solid #0056b3;
    padding-left: 15px;
    margin-top: 40px;
    font-size: 16pt;
}

p, li {
    font-size: 11pt;
    margin-bottom: 15px;
}

a {
    color: #0056b3;
    text-decoration: none;
}

a:hover {
    text-decoration: underline;
}

footer {
    text-align: center;
    margin-top: 40px;
    font-size: 0.9em;
    color: #666;
}
"""

with open("index.md", "w", encoding="utf-8") as f:
    f.write(index_md)

with open("style.css", "w", encoding="utf-8") as f:
    f.write(style_css)
