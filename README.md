# Rename Object for Maya MEL

## 1. 概要
Autodesk Maya用のMelスクリプトです。  
任意で選択した1個もしくは複数(2個以上)のオブジェクトの名前を一度に変更できます。  
名前変更の方法は次の①、②の内いずれかを選択できる様になっております。  

①文字列削除による名前変更(後述の[3-4])  
オブジェクト名の文字列の中の一部の文字列を削除する事により名前を変更します。

②文字列置き換えによる名前変更(後述の[3-5])  
B. オブジェクト名の文字列の中の一部の文字列もしくは全ての文字列を別の文字列に置き換える事により名前を変更します。


動作確認済みのOS : Windows10 Pro  
動作確認済みのMaya : Maya2013, Maya2014, Maya2015, Maya2016, Maya2017  
文字コード : Shift_JIS  
※文字コードにShift_JISを利用しているのは、スクリプト実行時の日本語の文字化け防止の為になります。下記の公式サイトの記載に沿いました。  
◆日本語または簡体字中国語のテキストを含んだ Maya ファイルを用意する  
https://knowledge.autodesk.com/ja/support/maya/learn-explore/caas/CloudHelp/cloudhelp/2016/JPN/Maya/files/GUID-88109151-076A-4AB1-836A-85370B32A256-htm.html



## 2. Melスクリプトの実行方法

[2-1] Melスクリプトファイルを、お好みの適当なディレクトリ下に配置します。
 
[2-2] Mayaを起動し、ウィンドウメニューからスクリプトエディタを開きます。

[2-3] スクリプトエディタのファイルメニューから、ソーススクリプトをクリックします。

[2-4] 読み込むMelスクリプトファイルの選択画面になるので、1で配置したMelスクリプトを選んで読み込みます。  
※[2-3]と[2-4]を行わずに、Melスクリプトファイルをスクリプトエディタ内の入力欄にドラッグドロップしてもOKです。

[2-5] 読み込まれたスクリプトが表示されている入力欄内で、Ctrl ＋ Enterキーを押す。これで実行されます。  
  

## 3. スクリプトのWindow内の各項目について
###[3-1] Rename Object  
Windowのタイトル（このMelスクリプトの名前を意味します）を表示しています。

### [3-2] Edit  
ここをクリックすると、次の①、②のメニューが表示されます。  
① Clear Result of rename by string delete (文字列削除による名前変更の結果をクリア)  
ここをクリックすると、下記 [3-4]の④の内容をクリアできます。  

② Clear Result of rename by string substitute (文字列置き換えによる名前変更結果をクリア)  
ここをクリックすると、下記 [3-5]の⑥の内容をクリアできます。  

### [3-3] Information  
ここをクリックすると、次の①のメニューが表示されます。  
① About RenameObject (RenameObject について)  
ここをクリックすると、このMelスクリプトのバージョン情報と作成者について表示します。  

### [3-4] Rename by string delete (文字列削除による名前変更)  
文字列削除による名前変更の為の設定と実行、および結果表示を行うタブです。  

① Setting of rename by string delete (文字列削除による名前変更の設定)  

② Search string (検索文字列)  
削除対象として検索する文字列を入力します。  

③ Rename by string delete (文字列削除による名前変更)  
このボタンを押すと、文字列削除による名前変更処理が実行されます。  
削除されるのは、②で入力した検索文字列と一致した部分のみです。  

④ Result of rename by string delete(文字列削除による名前変更の結果)  
文字列削除による名前変更関連処理のメッセージを表示するボックスになります。  
ボックスの内容は、[3-2]からクリアできます。  

### [3-5] Rename by string substitute (文字列置き換えによる名前変更)  
文字列置き換えによる名前変更の為の設定と実行、および結果表示を行うタブです。  

① Setting of rename by string substitute (文字列置き換えによる名前変更の設定)  

② Target in name of object (オブジェクトの名前の対象)  
オブジェクトの名前変更において、文字列を置き換える対象を、Whole(全体）、Part(一部)、のいずれかから選択できます。  
Wholeを選択した場合は、オブジェクトの名前全てが次の④で入力された文字列に置き換わります。  
Partを選択した場合は、次の③で入力された文字列がオブジェクト名の中に存在するか検索し、
見つかった時点で④で入力された文字列に置き換わります。  

③ Search string (検索文字列)  
置き換え対象として検索する文字列を入力します。  
②でPartが選択されている場合のみ入力できます。  

④ Substitute string (置き換え文字列)  
置き換え先の文字列を入力します。  
②での選択内容に関わらず入力できます。  

⑤ Rename by string substitute (文字列置き換えによる名前変更)  
このボタンを押すと、文字列置き換えによる名前変更処理が実行されます。  
②の選択内容により、置き換えられる文字列は変わります。  

⑥ Result of rename by string substitute (文字列置き換えによる名前変更の結果)  
文字列置き換えによる名前変更関連処理のメッセージを表示するボックスになります。  
ボックスの内容は、[3-2]からクリアできます。  

### [3-6] Close window ( ウィンドウを閉じる) ボタン  
このボタンを押すと、このMel スクリプトのGUI ウィンドウを閉じて、終了できます。  
