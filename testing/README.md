# Snort IDS Testing

This directory documents the testing performed for the custom Snort rules in this lab.

Each screenshot shows the test action and the corresponding Snort alert.

## Tests

### 01 - ICMP Ping Detection

**Rule:** SID 100001

**Test:**

    ping <snort-lab-ip>

The rule detects ICMP traffic and generates an alert when a ping is received.

### 02 - FTP File Download

**Rule:** SID 100002

**Test:**

    ftp <snort-lab-ip>
    get myfile.txt

The rule detects the `RETR myfile.txt` command and generates an alert.

### 03 - FTP Login Attempt

**Rule:** SID 100003

**Test:**

    ftp <snort-lab-ip>

The rule detects an FTP login attempt using the configured NetID.

### 04 - HTTP Secret Plans Request

**Rule:** SID 100004

**Test:**

    http://<snort-lab-ip>/Secret-Plans.txt

The rule detects requests for the specified URI.

### 05 - Netcat Cat Command

**Rule:** SID 100005

**Test:**

    ncat <snort-lab-ip> 4444
    cat /etc/passwd

The rule detects the `cat` command in traffic directed to TCP port 4444.

## Screenshots

- `snort-screenshot-01.png` - ICMP ping test
- `snort-screenshot-02.png` - FTP file download test
- `snort-screenshot-03.png` - FTP login attempt test
- `snort-screenshot-04.png` - HTTP URI test
- `snort-screenshot-05.png` - Netcat and `cat` command test
