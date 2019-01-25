OCR-GoogleCloudVision
====

画像ファイルから、手書き文字認識を行います。    

[Google-Cloud-Vision-APIのサンプルコード document_text/doctext.pyと、detect/beta_snippets.py](https://github.com/GoogleCloudPlatform/python-docs-samples/tree/master/vision/cloud-client/)を使用しています。


## Description
[Cloud Vision API ドキュメント](https://cloud.google.com/vision/docs/)  


## Demo
画像ファイルを読み込み文字認識を行っています。  
Gif画像では、手書き文字を認識しています。  
確信度は、0から1の数値で表されます。
![result](https://github.com/zashio/OCR-GoogleCloudVision/blob/master/GoogleOCRDemo.gif)  


## Requirement
- Python3.6.6  
- Jupyterで実行する場合、Anaconda3  


## Usage

### Google Cloud Platformを利用するために
[Google Cloud Platformの簡単スタートアップガイド](http://goo.gl/ua5fQw)の、サービス共通編(P9-P20)を終え、プロジェクトを作成してください。

### ソースコードのコピー
- コンソールを開き、任意の場所で以下を実行し、全てのファイルをダウンロードしてください。  
`git clone https://github.com/zashio/OCR-GoogleCloudVision.git`  
- OCR-GoogleCloudVisionフォルダ内に移動し、コンソール上で以下を実行し、必要なライブラリをインストールしてください。  
`pip install -r requirements.txt`   

### 認証について  
ソースコード中の、
`os.environ["GOOGLE_APPLICATION_CREDENTIALS"]= "C:***/***/***.json"`  
を、訂正する必要があります。  
[認証の概要](https://cloud.google.com/docs/authentication/getting-started)中の、「サービスアカウントを作成する」を実行し、認証用jsonファイルを入手してください。  
<div align="center">
<img src=https://github.com/zashio/OCR-GoogleCloudVision/blob/master/CreateServiceAccountKey.png "GetJson">
</div>
  
「作成」を押してダウンロードされたjsonファイルを、任意の場所に保存して  
`os.environ["GOOGLE_APPLICATION_CREDENTIALS"]= "C:***/***/***.json"`  
中の`***/***/***`にその場所へのパスを記載してください。  
これは、環境変数に書き込んでおくのがスマートではありますが、このようにソースコード中で指定することもできます。  
  
### .ipynbを使う場合
- 任意の環境(デモGifではJupyterLab)で"detect_handwritten_note.ipynb"を開き、  
`os.environ["GOOGLE_APPLICATION_CREDENTIALS"]= "C:***/***/***.json"`  
を訂正したのち、上から実行してください。  
- 引数`file_name`に文字認識を行う画像ファイルを指定してください。  
  
### .pyを使う場合
- 任意のエディタで"detect_handwritten.py"を開き、以下を訂正してください。  
`os.environ["GOOGLE_APPLICATION_CREDENTIALS"]= "C:***/***/***.json"`  
- コマンドライン上で、以下を実行してください。  
`python detect_handwritten.py ***.jpg`  
- `***.jpg`の部分に、文字認識を行う画像ファイルを指定してください。  

## Install
必要なライブラリは、'requirements.txt'に記述してあります。  
そのため、以下のコマンドをOCR-GoogleCloudVisionフォルダ内で実行していただくことにより、必要なライブラリがすべてインストールされます。  
`pip install -r requirements.txt`  
※Anaconda環境にてPythonのインストールを行った場合は、pipコマンドとcondaコマンドを併用してのインストールはおやめください。


## Contribution  
お待ちしております。  
フォークして、新しいブランチを作ってそこに変更点をプッシュしておいてください。  
プルリクエストもお願いします。  

## Licence  
This source is licensed under the Apache License, Version2.0

## Author
zashio
