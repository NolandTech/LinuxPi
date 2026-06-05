Generate Key (windows)
`ssh-keygen -t ed25519 -f C:\Users\NolandC\.ssh\yourkeyname`

Generate Key (Linux)
`ssh-keygen -t ed25519`

open pub file and copy and past into (windows):
`C:\Users\YourUsername\.ssh\authorized_keys`

open Pub file copy and past into linux:
`~/.ssh/authorized_keys`

Add to Keyring Windows 

Start key ring
`Start-Service ssh-agent`

Add key:
`ssh-add C:\Users\<User Name>\.ssh\yourkeyname`

Add to Keyring (Linux)

Start Keyring:
`eval "$(ssh-agent -s)"`

Add Key:
`ssh-add ~/.ssh/your_key_name`


Set keyring to start automatically (windows)
`Set-Service -Name ssh-agent -StartupType Automatic`