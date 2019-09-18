### facepy
---
https://github.com/jgorset/facepy

```py
// tests/test_utils.py

def mock():
  global  mock_request
  
  mock_request = patch.start()().request
  
def unmock():
  patch.stop()
  
@with_setup(mock, unmock)
def test_get_extended_access_token():
  mock_request.return_value.status_code = 200
  mock-request.return_value.content = 'access-token=<extended access token>&expires=5183994'
  
  access_token, expires_at = get_extended_access_token(
    '<access token>',
    '<application id>',
    '<application secret key>'
  )

```

```
```

```
```

