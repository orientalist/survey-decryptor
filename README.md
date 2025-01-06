# Survey Decryptor Node.js

## 簡介
Survey Decryptor 是一個用於解密來自 SurveyCake 的調查數據的 Node.js 應用程序。該應用程序透過指定的 SVID、HASH 和域名，從 SurveyCake 獲取加密的調查數據並進行解密，最終返回清晰的 JSON 格式數據。

## 功能
- 使用指定的參數（SVID, HASH, domain）自動從 SurveyCake 獲取加密的調查數據
- 解密數據並轉換為 JSON 格式
- 支援自定義的 SurveyCake 域名
- 回傳 HTTP 200 狀態碼與解密後的數據

## 安裝與使用方式

1. 確保您的環境已安裝 Node.js 和 npm。
   
2. 將此專案複製到本地資料夾：
   ```bash
   git clone https://github.com/yourusername/survey-decryptor.git
   ```

3. 進入專案資料夾：
   ```bash
   cd survey-decryptor
   ```

4. 安裝必要的依賴模組：
   ```bash
   npm install
   ```

5. 創建 `config.json` 檔案，格式如下：
   ```json
   {
     "www.surveycake.com": {
       "your_svid": {
         "hashKey": "your_hash_key",
         "ivKey": "your_iv_key"
       }
     }
   }
   ```

6. 啟動應用程式並使用AWS Lambda或其他伺服器執行此函數。

## 必要的依賴模組清單
- `axios`: 用於發送 HTTP 請求
- `crypto`: 用於數據加密與解密
- `fs`: 用於文件系統操作

您可以使用以下命令安裝所需的依賴：
```bash
npm install axios
```

## 授權條款
本專案使用 MIT 授權條款。請參閱 `LICENSE` 檔案以獲取更多詳細資訊。

```
您可以根據需要後續新增進一步的描述、用例或示例，以提供更多的上下文和指導。