# note

### Warp - Initial Connection
To connect for the very first time you must call register first:
1. Register the client warp-cli register.
1. Connect warp-cli connect.
1. Run curl https://www.cloudflare.com/cdn-cgi/trace/ and verify that warp=on

### Check java directory

```
readlink -f $(which java)
```