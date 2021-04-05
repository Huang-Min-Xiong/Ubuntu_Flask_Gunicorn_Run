#### 安裝 Gunicorn 套件:
- sudo pip install gunicorn

#### Gunicorn 背景執行:
- gunicorn -w 3 -b 127.0.0.1:5000 test:app

#### 隱藏執行結果:
- gunicorn -w 3 -b 127.0.0.1:5000 test:app - -daemon

#### 參數說明:
- -w : 就是worker的個數，簡單來說就是同一個時間能夠處理多少工作量(官方是建議一個CPU可設置2-4個 worker)。

- -b : 設定服務所綁定的端口，格式為HOST:PORT。

- test:app: 為執行的程式名稱，假設檔名為test.py，就要在最後面加上test:app。

#### 查詢Gunicorn背景有哪些服務正在運行中: 
- ps -ef | grep gunicorn

#### 刪除指定Pid隨之子程序也會跟著移除: 
- sudo kill -9 (PID)
