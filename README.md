Update secretsdump.py
========

New flags (for LOCAL, VSS and DRSUAPI methods get credentials from ntds.dit):
- -sid - Replace RID to SID
- -account-type - Display account type (User, Machine, Trust)

```
secretsdump.py essos.local/'daenerys.targaryen':'BurnThemAll!'@meereen.essos.local -history -user-status -pwd-last-set -just-dc-ntlm -outputfile essos_dcsync.local
```
