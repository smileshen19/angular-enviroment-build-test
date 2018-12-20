Angular Enviroment build Test

測試：
執行npm run build_dev / npm run build_dev比較結果

說明：
1.angular.json內，build -> configurations內定義設定 dev 與 prod
2.在ng build時帶入參數 -configuration=dev/prod會對應angular.json內的設定
3.建立基本的build script: build_basic，不同env設定皆跑這段script，帶不同configuration參數
4.使用package.json內config:env定義帶進script:build_basic的參數
5.npm run "腳本名稱" --"專案名稱":"package.json內config區塊的參數名稱"="帶入的參數"
6.npm run build_basic --angular7-enviroment-build-test:env=dev
