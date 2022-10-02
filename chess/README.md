# chess

https://hackerchess-web.h4ck.ctfcompetition.com/admin.php

# urls

https://hackerchess-web.h4ck.ctfcompetition.com/admin.php
https://hackerchess-web.h4ck.ctfcompetition.com/admin.php

# info

- base64 encoded json
- PHPSESSID
- js load_baseboard()

```js
function load_baseboard() {
  const url = "load_board.php"
  let xhr = new XMLHttpRequest()
  const formData = new FormData();
  formData.append('filename', 'baseboard.fen')

  xhr.open('POST', url, true)
  xhr.send(formData);
  window.location.href = "index.php";
}
```

# thoughts

the chess is bogus, they cheat!

time 2 sqlmap :3c

- sqli
- form manipulation
- burp suite