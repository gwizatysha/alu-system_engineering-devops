# Load balancer

Scripts that double the web servers and put them behind HAProxy.

| File | Description |
| --- | --- |
| `0-custom_http_response_header` | Configures Nginx on web-01 / web-02 with an `X-Served-By` header set to the server hostname |
| `1-install_load_balancer` | Installs HAProxy on lb-01 and round-robins traffic to web-01 and web-02 |

Run the first script on both web servers and the second on lb-01, as root.
