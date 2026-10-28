# Lab Report: Comparing Telnet and SSH Traffic in Wireshark

## 1. Aim

Compare a local Telnet session with a local SSH session using Wireshark and observe the difference between plaintext application data and encrypted session contents.

## 2. Environment

- Date performed: `TODO`
- Operating system / Linux distribution: `TODO`
- VM or workstation: `TODO`
- Wireshark version: `TODO`
- Capture interface: `TODO`
- Telnet service status / port: `TODO`
- SSH service status / port: `TODO`

## 3. Procedure

### Telnet

1. Started Wireshark and selected the loopback interface.
2. Connected to the local Telnet service.
3. Authenticated with a dedicated lab account and ran `whoami`.
4. Applied the `telnet` display filter.
5. Followed the TCP stream and recorded the observed visibility.

### SSH

1. Started a fresh Wireshark capture on loopback.
2. Connected to the local SSH service.
3. Authenticated with a dedicated lab account and ran `whoami`.
4. Applied the `ssh` display filter.
5. Followed the TCP stream and compared the result with Telnet.

> Edit this section if your actual steps differed. Do not report steps as completed until you have performed them.

## 4. Results

| Observation | Telnet | SSH |
|---|---|---|
| Display filter used | `telnet` | `ssh` |
| Was application data readable? | `TODO — record your observation` | `TODO — record your observation` |
| Security implication | `TODO` | `TODO` |

## 5. Screenshots

Insert or link your genuine screenshots here after adding them to `screenshots/`.

- Telnet filter: `screenshots/02-telnet-filter.png`
- Telnet stream: `screenshots/03-telnet-stream.png`
- SSH filter: `screenshots/04-ssh-filter.png`
- SSH stream: `screenshots/05-ssh-stream.png`

## 6. Reflection questions

1. **What information was visible when you followed the Telnet TCP stream?**  
   `TODO — answer from your own capture.`

2. **What changed when you followed the SSH TCP stream?**  
   `TODO — answer from your own capture.`

3. **Why is sending authentication information over an unencrypted session dangerous?**  
   `TODO`

4. **What security property does SSH provide that Telnet does not?**  
   `TODO`

5. **Why should packet captures containing credentials never be uploaded to a public GitHub repository?**  
   `TODO`

## 7. Conclusion

`TODO — summarize what your evidence showed and why SSH is preferred for secure remote administration.`

## 8. Limitations and safety

Record any service, permission, interface, or capture limitations encountered. Use only authorized local systems and synthetic test data. Do not include passwords, tokens, private keys, or other secrets in this report.
