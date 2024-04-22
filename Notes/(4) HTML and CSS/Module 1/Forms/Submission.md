After filling out all the details in the fields of an Authentication System, the details travel to the server to get processed. 

### How?
The details travel to the server as a part of an HTTP request which acts as a link between the client and the server. 

There are two HTTP methods which deliver such data.

* ##### GET
It is more insecure and unreliable than POST and is thus, not recommended. The data travels through as a part of the URL. 
For instance, the submission of an Authentication form would create the URL, `http://www.example.com/username=admin&password=welcome`

<br>

* ##### POST
It is a recommended option. The data is in the HTTP request's payload.
```html
POST/ HTTP/1.1
Host: example.com
Content-type: application/form
Content-length: 32

username=admin&password=welcome
```


### Application
It can be implemented in HTML forms using its `action` and `method` attributes.

| Attribute | What it does |
|--|--|
| `action` | Where to send the data |
| `method` | How to send the data |

* ##### `action`
Its value is a URL. It takes the base address as the current address which for instance, is `http://www.example.com/profile`.

| Semantics | What it means |
|--|--|
| `action="/login"` | `http://www.example.com/login` |
| `action="login"` | `https://www.example.com/profile/login` |


* ##### `method`
It can have, broadly, two values. `GET` and `POST`.