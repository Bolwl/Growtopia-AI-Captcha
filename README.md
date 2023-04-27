# Growtopia Captcha Solver powered by AI

This API is for solving captchas shown in Growtopia.

<img src="https://cdn.discordapp.com/attachments/978338181613223976/1100802964974735420/Captcha_AI.png" width="31%">
<i>Image credit: Caferius#4337</i>

## API Reference

#### Solver

```http
  GET /api/captcha
```

| Parameter | Type     | Description                |
| :-------- | :------- | :------------------------- |
| `token` | `string` | ***Not Required for now (Free until May 1st)***. Your API key. |
| `id` | `string` | **Required**. Captcha ID |

The result will be in json format. Example for successful answer.
```
{"success": true, "answer": "0.123"}
```
Example for failed answer.
```
{"success": false, "reason": "Unauthorized"}
```

## Usage/Examples

#### Solver
```python
import requests
from requests.structures import CaseInsensitiveDict

url = "https://growtopia.tools/api/captcha"

headers = CaseInsensitiveDict()
headers["Content-Type"] = "application/x-www-form-urlencoded"

data = "token={yourtoken}&id={captchaid}"


resp = requests.get(url, headers=headers, data=data)

result = resp.json()
```

## License

[MIT](https://choosealicense.com/licenses/mit/)
