| Event ID | Meaning                                     | Why It Matters                                                      |
| -------: | ------------------------------------------- | ------------------------------------------------------------------- |
|     4624 | Successful logon                            | Normal authentication; investigate unusual logon types or locations |
|     4625 | Failed logon                                | Brute-force attacks, password spraying                              |
|     4634 | Logoff                                      | User session tracking                                               |
|     4648 | Logon using explicit credentials            | Potential lateral movement or administrative activity               |
|     4672 | Special privileges assigned                 | Privileged account logon                                            |
|     4688 | Process created                             | One of the most valuable events for threat detection                |
|     4697 | Service installed                           | Possible persistence mechanism                                      |
|     4720 | User account created                        | Watch for unauthorized accounts                                     |
|     4728 | User added to security-enabled global group | Privilege escalation indicator                                      |
|     4732 | User added to local group                   | Local administrator changes                                         |
|     4740 | Account locked out                          | Brute-force or password issues                                      |
|     4768 | Kerberos TGT requested                      | Authentication activity                                             |
|     4769 | Kerberos service ticket requested           | Useful for detecting Kerberoasting                                  |
|     4771 | Kerberos pre-authentication failed          | Password attacks                                                    |
|     4776 | NTLM authentication                         | Legacy authentication monitoring                                    |
|     7045 | New service installed                       | Common persistence technique                                        |
