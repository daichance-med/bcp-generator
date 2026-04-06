# BCP自動生成アプリ v3
### 在宅医療機関向け　業務継続計画（BCP）たたき台自動生成アプリ

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)

---

## 📋 概要

ExcelファイルをアップロードするだけでBCP（業務継続計画）のたたき台が自動生成されるローカル動作のHTMLアプリです。

**在宅医療機関のBCP策定が義務化**された背景を受け、策定支援を目的として開発しました。  
事業所情報を一度入力すれば、BCP本文・ステージ対応表・アクションカード・場所別カード・スタッフ出勤表・備品リストが一括で生成されます。

---

## ✨ 特徴

- **完全ローカル動作** — サーバーへのデータ送信なし。個人情報はブラウザ内のみで処理
- **インターネット不要** — オフライン環境でも動作
- **4種の事業所種別に対応** — 外来+訪問ハイブリッド / 訪問専門 / 外来専門 / 訪問看護ステーション
- **6タブ構成** — BCP本文（8章）/ ステージ対応表 / アクションカード / 場所別カード（5災害×4場所）/ スタッフ出勤表 / 備品リスト
- **全タブ一括PDF保存** — 印刷ボタン1つで全タブをPDF化

---

## 📱 アクセス用QRコード

スマートフォンのカメラでスキャンするとアプリに直接アクセスできます。

<div align="center">

| アプリを開く | テンプレートExcelをダウンロード |
|:---:|:---:|
| ![App QR](https://api.qrserver.com/v1/create-qr-code/?size=180x180&color=1F4E79&bgcolor=ffffff&data=https%3A%2F%2Fdaichance-med.github.io%2Fbcp-generator%2FBCP_generator_v3.html) | ![Template QR](https://api.qrserver.com/v1/create-qr-code/?size=180x180&color=1F4E79&bgcolor=ffffff&data=https%3A%2F%2Fgithub.com%2Fdaichance-med%2Fbcp-generator%2Fraw%2Fmain%2FBCP_Template_v3.xlsx) |
| **[► アプリを開く](https://daichance-med.github.io/bcp-generator/BCP_generator_v3.html)** | **[► テンプレートをダウンロード](https://github.com/daichance-med/bcp-generator/raw/main/BCP_Template_v3.xlsx)** |

</div>

> ⚠️ **iOSユーザーの方へ：** ローカルHTMLファイルをそのまま開くと動作しない場合があります。上記QRコードまたはURLからアクセスしてください。

---

## 🚀 使い方

### STEP 1: Excelに入力
`BCP_Template.xlsx` を開き、黄色いセルに事業所情報を入力して保存

### STEP 2: アプリを開く
`BCP_generator_v3.html` をブラウザで開く（Chrome / Edge / Safari 推奨）

### STEP 3: Excelをアップロード
「タップしてExcelを選択」から入力済みExcelを選択

### STEP 4: 事業所種別を選択
4種の中から該当する種別を選ぶ

### STEP 5: BCP文書を印刷/保存
BCP上部の「印刷/保存」ボタン、または「全タブ印刷/保存」でPDF一括保存

---

## 📁 ファイル構成

```
bcp-generator/
├── BCP_generator_v3.html   # アプリ本体（これをブラウザで開く）
├── BCP_Template_v3.xlsx    # 入力テンプレート（4シート構成）
│   ├── 事業所情報入力        # 黄色セルに記入
│   ├── スタッフリスト         # 氏名・通勤距離等を記入
│   ├── 業務優先度分類        # 任意入力。記入するとBCP第3章に院独自の業務分類表を生成
│   └── 📖 使い方ガイド
└── README.md
```

---

## 📊 生成されるBCP文書

| タブ | 内容 |
|---|---|
| 📄 BCP本文（8章） | 策定目的・リスク分析・業務優先度・患者対応・連携体制・アクションリスト・発動フロー。**第3章は施設種別に応じた業務優先度を自動出力。「業務優先度分類」シート入力で院独自の詳細表に変化** |
| 📊 ステージ対応表 | 被害状況に応じた4段階ステージと対応方針 |
| 🃏 アクションカード | 5災害のサマリーカード（簡易携帯版） |
| 📍 場所別カード | 5災害×4場所（訪問先・施設・移動中・自宅）= 20枚 |
| 👥 スタッフ出勤表 | 通勤距離に応じた参集可否判定（◎○△▲） |
| 🛒 備品リスト | 優先度A/B/C別の推奨備品・参考価格・保有状況 |

---

## 🏥 対応事業所種別

| 種別 | 対応内容 |
|---|---|
| 🏥🚗 外来+訪問ハイブリッド | 全セクション生成 |
| 🚗 訪問専門クリニック | 訪問関連セクションを中心に生成 |
| 🏥 外来専門クリニック | 外来関連セクションを中心に生成 |
| 💉 訪問看護ステーション | 「当ステーション」「管理者」等の文言に自動変換 |

---

## 📚 参考資料

本ツールは以下の公的ガイドラインを参考に作成しました。

- [厚生労働省「医療施設の災害対応のための事業継続計画（BCP）」](https://www.mhlw.go.jp/stf/seisakunitsuite/bunya/kenkou_iryou/kenkou/kekkaku-kansenshou/infulenza/kenkyu_00001.html)
- [J-SPEED（災害診療記録）公式サイト](https://www.j-speed.org/)

---

---

## 🔗 関連アプリ

| アプリ | リポジトリ |
|---|---|
| 在宅BCPハザードマップアプリ | [daichance-med/hazard-map-app](https://github.com/daichance-med/hazard-map-app) |
| BCP自動生成アプリ v3 | [daichance-med/bcp-generator](https://github.com/daichance-med/bcp-generator) |


## 👨‍💻 開発者

**daichance.med**  
福井内科消化器科クリニック（神奈川県小田原市）

---

## 📄 ライセンス

MIT License — 自由に利用・改変・再配布可能です。  
商用利用の場合はご連絡をお願いします。
