# EDAスクリプティング入門（EDA Scripting Basics）

本ドキュメントでは、EDA設計フローの自動化や効率化に欠かせないスクリプト言語について解説します。主にSKILL（Cadence）、Tcl（EDA標準）、Python（近年拡張中）に焦点をあて、基本構文から実務例まで紹介します。

---

## 1. はじめに

EDAツールは多数のパラメータや操作を伴うため、手動操作は非効率です。  
スクリプトを用いて作業を自動化・定型化し、設計品質向上と工数削減を実現します。

---

## 2. 主なスクリプト言語

| 言語   | 特徴                                | 主な用途                         |
|--------|-----------------------------------|---------------------------------|
| SKILL  | Cadence独自言語。Lisp系構文。      | Virtuosoでのカスタム処理、GUI制御 |
| Tcl    | 汎用スクリプト言語。EDAで広く利用 | ツール設定、バッチ処理、フロー制御 |
| Python | 汎用プログラミング言語。近年増加  | データ処理、EDAツール連携、自動化 |

---

## 3. SKILL基礎（Cadence環境向け）

- **基本構文**：

```lisp
(defun hello ()
  (println "Hello, Skill!"))
(hello)
•	用途例：
	•	回路図の自動生成
	•	レイアウト図形の作成・編集
	•	カスタムGUIボタン作成
```

## 4. Tcl基礎(EDA標準)

- **基本構文**：

```lisp
puts “Hello, Tcl!”
set a 10
if {$a > 5} {
puts “a is greater than 5”
}
	•	用途例：
	•	スクリプトベースのバッチ実行
	•	EDAツールの設定ファイルやコマンド制御
	•	フローの一括管理
```

⸻

##5. Python基礎（近年注目）

- **基本構文**：


print(“Hello, Python!”)
a = 10
if a > 5:
print(“a is greater than 5”)
	•	用途例：
	•	データ解析（波形、ログ）
	•	EDAツールのAPI制御（例：OpenROAD Python bindings）
	•	自動化ツールのラッパー開発

⸻

##6. 実務例：OpenROADバッチスクリプト（Tcl）

read_verilog mydesign.v
read_liberty mycell.lib
read_lef myprocess.lef
link_design mydesign
place_design
clock_tree_synthesis
route_design
write_def output.def
write_gds output.gds

⸻

##7. スクリプト活用のポイント
	•	処理の再現性向上
	•	エラー発見の容易化（ログ記録）
	•	複数ファイル・条件分岐の一括管理
	•	チーム内共有・標準化

⸻

##8. 学習リソース
	•	Cadence SKILL公式ドキュメント
	•	Tcl公式サイト・EDAツールマニュアル
	•	Python EDAコミュニティ（GitHub, StackOverflow）

⸻

##参考リンク
	•	Cadence SKILL：https://support.cadence.com/skill/
	•	Tcl言語：https://www.tcl.tk/
	•	Python：https://www.python.org/
	•	OpenROAD Tcl API：https://theopenroadproject.org/
