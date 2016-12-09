![bit_rise_logo](https://github.com/jgabrielfreitas/TelegramBitriseBot/blob/master/bitrise-logo.png)

# Telegram BitriseBot
> bot to work with CI and CD status on Telegram

#### Usage

Just do a `HTTP GET` for: 

https://api.telegram.org/bot266721295:AAG39D0MCOVVHBFp32-y624Pb7PtHU6z6FM/sendMessage?chat_id=[GROUP_OR_USER_ID]&text=[YOUR_MESSAGE]

Param | Content
--- | ---
chat_id | user or group id
text | message

###### example:

* cURL
```cURL
$ curl -X GET "https://api.telegram.org/bot266721295:AAG39D0MCOVVHBFp32-y624Pb7PtHU6z6FM/sendMessage?chat_id=[CHAT_ID]&text=Hello%20World"
```

* Python
```python
import requests

url = "https://api.telegram.org/bot266721295:AAG39D0MCOVVHBFp32-y624Pb7PtHU6z6FM/sendMessage"

querystring = {"chat_id":"[CHAT_ID]","text":"Hello%20World"}

response = requests.request("GET", url, params=querystring)

print(response.text)
```

* Go
```go
package main

import (
	"fmt"
	"net/http"
	"io/ioutil"
)

func main() {

	url := "https://api.telegram.org/bot266721295:AAG39D0MCOVVHBFp32-y624Pb7PtHU6z6FM/sendMessage?chat_id=-1001064749324&text=Hello%2520World"

	req, _ := http.NewRequest("GET", url, nil)

	res, _ := http.DefaultClient.Do(req)

	defer res.Body.Close()
	body, _ := ioutil.ReadAll(res.Body)

	fmt.Println(res)
	fmt.Println(string(body))

}
```

###### And works like magic :sparkles:

![captura de tela 2016-12-09 as 15 27 42](https://cloud.githubusercontent.com/assets/7410639/21058202/13de4670-be24-11e6-955a-92f309758b85.png)

#### LICENSE
```

The MIT License (MIT)

Copyright (c) 2016 João Gabriel de Freitas

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE

```
