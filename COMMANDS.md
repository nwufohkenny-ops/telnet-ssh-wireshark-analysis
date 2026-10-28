# Commands and Wireshark Filters

Use these commands only in your authorized local lab. Service-management commands vary by Linux distribution.

## 1. Confirm the environment

```bash
uname -a
wireshark --version
ip addr
```

Check that the required local services are installed and running using the tools appropriate to your distribution. Do not install or enable services on a machine you do not administer.

## 2. Start Wireshark

```bash
wireshark &
```

Select the loopback interface, commonly `lo`, and start a capture.

## 3. Telnet portion

Connect only to the local lab service:

```bash
telnet localhost
```

Authenticate with a dedicated lab account and run a harmless command:

```bash
whoami
```

Wireshark display filter:

```text
telnet
```

Select a relevant packet and use **Follow → TCP Stream**. Record whether application data appears readable. Never use a real password or production account.

End the session:

```text
exit
```

## 4. SSH portion

Start a fresh capture on loopback, then connect to the local SSH service:

```bash
ssh localhost
```

If prompted about the host key, verify it and accept it only if appropriate for this controlled lab. Authenticate with your dedicated lab account and run:

```bash
whoami
```

Wireshark display filter:

```text
ssh
```

Follow the TCP stream and compare what is visible with the Telnet stream.

## 5. Notes

- Capture only traffic needed for this exercise.
- Use the loopback interface for local sessions.
- Service availability, ports, and packet details may vary.
- Do not include credentials in notes, screenshots, or public captures.
- If a command fails, record the actual error and environment; do not claim a successful result.
