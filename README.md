
Forbidden Buster is a tool designed to automate various techniques in order to bypass HTTP 401 and 403 response codes and gain access to unauthorized areas in the system. **This code is made for security enthusiasts and professionals only. Use it at your own risk.**

## Features

- Probes HTTP 401 and 403 response codes to discover potential bypass techniques.
- Utilizes various methods and headers to test and bypass access controls.
- Customizable through command-line arguments.
  
## Installation & Usage
Install requirements

```bash
pip3 install -r requirements.txt
```

Run the script

```bash
python3 forbidden_bypass.py -u http://example.com
```

## Arguments
Forbidden Buster accepts the following arguments:

```bash
  -h, --help            show this help message and exit
  -u URL, --url URL     Full path to be used
  -m METHOD, --method METHOD
                        Method to be used. Default is GET
  -H HEADER, --header HEADER
                        Add a custom header
  -d DATA, --data DATA  Add data to requset body. JSON is supported with escaping
  -p PROXY, --proxy PROXY
                        Use Proxy
  --rate-limit RATE_LIMIT
                        Rate limit (calls per second)
  --include-unicode     Include Unicode fuzzing (stressful)
  --include-user-agent  Include User-Agent fuzzing (stressful)
```

Example Usage:
```bash
python3 forbidden_bypass.py --url "http://example.com/secret" --method POST --header "Authorization: Bearer XXX" --data '{\"key\":\"value\"}' --proxy "http://proxy.example.com" --rate-limit 5 --include-unicode --include-user-agent
```

## Credits
- **Hacktricks** - Special thanks for providing valuable techniques and insights used in this tool.
- **SecLists** - Credit to danielmiessler's SecLists for providing the wordlists.
- **kaimi** - Credit to kaimi's "Possible IP Bypass HTTP Headers" wordlist.

