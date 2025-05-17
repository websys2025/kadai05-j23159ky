## 外部APIの呼び出しのミニレポート
### Q3-1. 郵便番号APIについて説明せよ。
* エンドポイントと機能
エンドポイント: https://zipcloud.ibsnet.co.jp/api/search
郵便番号を入力するとそれに対応した住所を返すAPI

* リクエストとレスポンスのフォーマット
 https://zipcloud.ibsnet.co.jp/api/search?zipcode=3150045
    {
      "zipcode": "1000001",
       "prefcode": "13",
        "address1": "東京都",
       "address2": "千代田区",
        "address3": "千代田",
      }
address1: 都道府県
address2: 市区町村
address3: 町域

### Q3-2. 各自で調査したAPIについて説明せよ。
* APIの名称と参照URL
* API：Open-Meteo API（オープン・メテオ）
* URL：https://open-meteo.com/

* エンドポイントと機能
エンドポイント: https://api.open-meteo.com/v1/forecast

* リクエストとレスポンスのフォーマット
リクエスト(GET)
* 東京の緯度（35.6895）・経度（139.6917）で、現在の天気を取得する
https://api.open-meteo.com/v1/forecast?latitude=35.6895&longitude=139.6917&current_weather=true

 * {
 "latitude": 35.6895,
  "longitude": 139.6917,
  "current_weather": {
    "temperature": 21.4,
    "windspeed": 8.2,
    "weathercode": 1,
    "is_day": 1,
    "time": "2025-05-17T06:00"
   }
}

temperature: 現在の気温（℃）
windspeed: 風速（km/h）
weathercode: 天気の状態を表すコード（例：0=快晴、1=晴れ など）

time: データの取得時刻
### Q3-3. 感想
* 今回の課題で苦労したこと
APIにてデータ取得失敗時の処理

* 演習を通して理解できたこと
WEBAPIの利便性と使用したAPIの使用方法
  
* Web APIの利便性や課題など
urlを入力し、使用方法を調べるだけで気軽に利用できる点が良いと感じた。
