# nginx_proxy_pass

## Synopsis

因為後端　API PORT 號太多，改去　PORT　號的方式。
舉例：
呼叫端改用呼叫 http://xxx.com/dal/CustomerInfo  透過 nginx 指向 http://aaa.com:50344/ & http://bbb.com:50344/

## Code Example

無

## Motivation

proxy_pass 去掉後端的 PORT 號

## Installation

nginx.conf 一般會放在 /etc/nginx 

api.conf api.upstream web.conf web.upstream 檔案放在 /etc/nginx/default.d

## API Reference

無

## Tests

無

## Contributors

無

## License

無

## Others
因為 log 檔增長太快, 設定排程每天 1am 砍 *.gz
crontab -e
 * 1 * * * sudo find /var/log/nginx -type f -name '*.gz' -exec rm {} +
