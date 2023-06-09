# Growtopia Captcha Solver powered by AI

This API is for solving captchas shown in Growtopia.

<img src="https://cdn.discordapp.com/attachments/978338181613223976/1100802964974735420/Captcha_AI.png" width="31%">
<i>Image credit: Caferius#4337</i>

## Speed
Solver Speed 0.2-0.3 seconds.
API Latency 0-1.1 seconds.
Total Speed 0.2-1.4 seconds.

## Success Rate
Captchas are solved with 99.9997804232% accuracy. (1 fail every 4554 captchas)
It can detect every captcha, even the ones you can't see with your own eyes. (Fails are caused because gt is too strict about answer. Even though the solver finds the answer correctly, it sometimes finds the answer 1-2 pixels off which causes wrong answer.)

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

curl "https://growtopia.tools/api/captcha/?id={captchaid}&key={secretkey}&format=json" 

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

### Check Usages
curl "https://growtopia.tools/api/info?api=captcha&key={secretkey}"

```
{"success": true, "usage": usageleft(int), "subscription": "subscription type(string)"}
```

## Usage/Examples

#### Solver
```python
import requests
from requests.structures import CaseInsensitiveDict

url = "https://growtopia.tools/api/captcha"

headers = CaseInsensitiveDict()
headers["Content-Type"] = "application/x-www-form-urlencoded"

data = "key={yourkey}&id={captchaid}&format=json"


resp = requests.get(url, headers=headers, data=data)

result = resp.json()
```

## Showcase
<img src="https://github.com/Bolwl/Growtopia-AI-Captcha/blob/b3b8555b14cf434f91d3d3d9730b25bf55540401/showcase.gif?raw=true" alt="Captcha Solver Showcase" title="Captcha Solver Showcase" width="500"/>

## License

[MIT](https://choosealicense.com/licenses/mit/)
