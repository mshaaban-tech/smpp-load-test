## Examples
-   [Go by Example](https://gobyexample.com/)

## Commands

```shell
# Init project
go mod init github.com/muhammadshaban/smpp-load-test

# Install requirements
go mod tidy

# Build
go build -o build/load_test

# Run load test
./build/load_test \
    -ip 127.0.0.1 -port 8005 \
    -username SHORTCODE -password SHORTCODE_PASSWORD -systemid SHORTCODE_SYSTEMID \
    -sender SHORTCODE_SENDER -recepient "966534510820" \
    -sessions 1 -throughput 1 -amount 1

```

```shell
# Parse pcap file
tshark \
    -r output.pcap \
    -X'lua_script:pcap_parse.lua'

tcpdump -i any  "port 8005" -w output.pcap
tshark -i any -f "port 8005" -c 5 -w output.pcap

tcpdump -i eth0 "host 212.118.129.59" -w output.pcap

# Get round trip time
time nc -z 127.0.0.1 8005

```
