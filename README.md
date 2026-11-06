# Index1D API Examples

Ví dụ code tích hợp API của Index1D (ép index) và CheckIndex (check index).

## Cài đặt

Không cần thư viện ngoài — dùng requests (Python), cURL (PHP), fetch (Node.js).

## Python — Check index

```python
import requests

API_KEY = "YOUR_API_KEY"
urls = [
    "https://example.com/page-1",
    "https://example.com/page-2",
]

resp = requests.post(
    "https://checkindex.qzz.io/api/check",   # ← thay endpoint thật
    json={"urls": urls},
    headers={"Authorization": f"Bearer {API_KEY}"},
)
print(resp.json())
```

## PHP — Check index

```php
<?php
$apiKey = 'YOUR_API_KEY';
$urls = ['https://example.com/page-1', 'https://example.com/page-2'];

$ch = curl_init('https://checkindex.qzz.io/api/check'); // ← thay endpoint thật
curl_setopt_array($ch, [
    CURLOPT_RETURNTRANSFER => true,
    CURLOPT_POST => true,
    CURLOPT_HTTPHEADER => [
        'Content-Type: application/json',
        "Authorization: Bearer $apiKey",
    ],
    CURLOPT_POSTFIELDS => json_encode(['urls' => $urls]),
]);
print_r(json_decode(curl_exec($ch), true));
```

## Liên hệ

- Telegram: [@thien1d](https://t.me/thien1d) — nhận API key và tài liệu đầy đủ
- Website: https://index1d.top
