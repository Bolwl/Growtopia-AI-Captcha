# Growtopia Captcha Solver powered by AI

This API is for solving captchas shown in Growtopia.

<img src="https://cdn.discordapp.com/attachments/978338181613223976/1100802964974735420/Captcha_AI.png" width="31%">
<i>Image credit: Caferius#4337</i>


## How to purchase?
<b>Dm Bolwl#9999 on discord to purchase key.</b>

| Request Amount | Price|
| :-------- | :------- |
| `1,500 request `| `3DL` |
| `2,500 request `| `450WL` |
| `10,000 request `| `15DL` |
| `50,000 request `| `70DL` |
| `100,000 request `| `125DL` |

<b>For monthly keys dm Bolwl#9999 on discord.</b>

## API Reference

#### Solver

```http
  GET /api/captcha
```

| Parameter | Type     | Description                |
| :-------- | :------- | :------------------------- |
| `key` | `string` | **Required**. Your API key. |
| `id` | `string` | **Required**. Captcha ID |
| `format` | `string` | ***Not* Required**. Response format. `txt` or `json`. Default: `json` |

### Json Response
Example for successful answer.
```
{"success": true, "answer": "0.123"}
```
Example for failed answer.
```
{"success": false, "reason": "Unauthorized"}
```

### TXT Response
Example for successful answer.
```
Answer|0.123
```
Example for failed answer.
```
Answer|Failed
```

## Usage/Examples

#### Solver
```python
import requests
from requests.structures import CaseInsensitiveDict

url = "https://growtopia.tools/api/captcha"

headers = CaseInsensitiveDict()
headers["Content-Type"] = "application/x-www-form-urlencoded"

data = "key={yourkey}&id={captchaid}"


resp = requests.get(url, headers=headers, data=data)

result = resp.json()
```

## License

[MIT](https://choosealicense.com/licenses/mit/)
