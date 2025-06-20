# tcpcheck - A tool to check TCP connections
A tool I created to check TCP connections, which I use frequently across multiple devices. So I created this repository so that you can install it with `go install`.

## Installation
```
go install github.com/Towsif12/tcpcheck@latest
```
If you want to build it yourself, feel free to clone the repository and run `go build`

## Usage
```
tcpcheck 127.0.0.1 3306
```
![Usage](usage.png)

## 🆕 New Features

### ⏱ Timestamp
💡 *Feature suggested by [@iurynovarino](https://github.com/iurynovarino)*

Each connection attempt now includes a full timestamp with date and time in the format:

![image](https://github.com/user-attachments/assets/2e69c157-4dc0-455a-ae30-d0006c2c068e)


### 💤 Delay Option (`-t`) 
💡 *Feature suggested by  [@Tacioandrade](https://github.com/Tacioandrade)*

You can define the interval between connection attempts using the `-t` flag.  
The value is in **seconds** and supports decimals (e.g., `0.5`, `1.2`, etc).  
The default delay is `0.5` seconds.

#### 📌 Usage:
```bash
tcpcheck [-t seconds] <IP> <Port>
```

#### 📌 Examples:
```bash
tcpcheck 192.168.1.1 80
# Uses the default delay of 0.5s

tcpcheck -t 2 192.168.1.1 80
# Uses a delay of 2 seconds

tcpcheck -t 0.1 192.168.1.1 80
# Uses a delay of 100ms
