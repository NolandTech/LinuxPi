`sudo chmod -R 755 `
`sudo chown -R 1000:1000 `

### chmod — it changes **file/folder permissions**.
Stands for **change mode**

`sudo chmod -R 755 /path/to/directory

 `-R` Means **recursive** (works for all sub-directories)
 `755` This is the permission **code** in octal:
`/path/to/directory` 

| Number | Meaning                                      |
| ------ | -------------------------------------------- |
| 7      | Owner can **read, write, execute** (`4+2+1`) |
| 5      | Group can **read, execute** (`4+0+1`)        |
| 5      | Others can **read, execute** (`4+0+1`)       |
- **Read = 4**
- **Write = 2**
- **Execute = 1**

**Add the numbers for each user category:**
- Owner: `4+2+1 = 7` → full access
- Group: `4+0+1 = 5` → read + execute
- Others: `4+0+1 = 5` → read + execute


`sudo chmod -R u+rwx,g+rwx,o+r /directory `

`u+rwx,g+rwx,o+r`

This is the **symbolic mode** for permissions:

|Symbol|Who it applies to|What it does|
|---|---|---|
|`u`|user (owner)|`+rwx` → add read, write, execute|
|`g`|group|`+rwx` → add read, write, execute|
|`o`|others|`+r` → add read only|

| Number | Permissions | Binary (r=4, w=2, x=1) |
| ------ | ----------- | ---------------------- |
| 0      | ---         | 000                    |
| 1      | --x         | 001                    |
| 2      | -w-         | 010                    |
| 3      | -wx         | 011                    |
| 4      | r--         | 100                    |
| 5      | r-x         | 101                    |
| 6      | rw-         | 110                    |
| 7      | rwx         | 111                    |

### chown
Stands for **change owner** — it changes the **owner and/or group** of files or folders.

`sudo chown -R your_user:your_group /directory`

`your_user:your_group`

- **`your_user`** → new **owner** of the files
- **`your_group`** → new **group** of the files
- `/directory`


