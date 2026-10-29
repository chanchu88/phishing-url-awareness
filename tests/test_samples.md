# Test Results

Python version used: 3.13 or later (write your actual version) | Operating system: Kali Linux | Date: [enter date]

| # | Input | Expected result | Actual result | Pass/Fail |
|---|---|---|---|---|
| 1 | `https://www.example.com/login` | No listed warning signs | No listed warning signs found. This does NOT prove safety. Never enter passwords from unexpected links. | PASS |
| 2 | `http://192.0.2.10/account` | IP address + HTTP | Uses an IP address instead of a familiar domain. - Uses HTTP. HTTPS alone does not prove trust. | PASS |
| 3 | `http://example.com@sample.invalid/login` | @ symbol + HTTP | - Contains an @ symbol; inspect carefully. - Uses HTTP. HTTPS alone does not prove trust. | PASS |
| 4 | `https://a.b.c.d.e.example.invalid/path` | Many hostname segments | - Contains many hostname segments/subdomains. | PASS |
| 5 | `https://xn--example.invalid/` | Punycode-style hostname | - Contains a punycode-style hostname. | PASS |

## Notes

I learned how to build a Python tool that checks URLs for common phishing warning signs, such as suspicious symbols, IP addresses, and the use of HTTP.
What surprised me was that even a normal-looking URL can be suspicious, and no warning signs do not guarantee that a URL is safe.
