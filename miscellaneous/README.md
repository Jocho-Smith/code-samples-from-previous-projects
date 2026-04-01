# small personal favorites


## http.server CLI tool
`python -m http.server`
- Distribute public keys to freshly enrolled machines
- quickly spin up static web pages for debugging/development (also useful to check other browsers or mobile devices with touch)
- easily extensible to test abi:

```python
from http.server import BaseHTTPRequestHandler, HTTPServer
import json

class Handler(BaseHTTPRequestHandler):
    def do_GET(self):
        if self.path == "/api/user":
            data = {"id": 1, "name": "Alice"}
            self.send_response(200)
            self.send_header("Content-Type", "application/json")
            self.end_headers()
            self.wfile.write(json.dumps(data).encode())

server = HTTPServer(("0.0.0.0", 8000), Handler)
server.serve_forever()
```


## 'party trick'

Estimating Pi using monte carlo sampling in **one line** of code (inspired by @MrPSolver)

```python
import numpy as np
from numpy.random import uniform

print(4* np.sum(uniform(size=300000000)**2+uniform(size=300000000)**2 < 1) / 300000000)
```