
### Creating a New User

To create a new user on your system, use the `adduser` command. This is an interactive tool that automatically sets up the user's home directory and prompts you to create a secure password.

```sh
sudo adduser yourusername
````

The terminal will ask you to enter and confirm a new password. It will also ask for some optional details (like Full Name or Room Number)—you can just press `Enter` to skip those.

### Granting Sudo Privileges

By default, a new user is a standard user and cannot run administrative commands. To fix this, you must add them to the `sudo` group.


```sh
sudo usermod -aG sudo yourusername
```

This command **adds your user to the `sudo` group**, which grants permission to run commands as root using `sudo`.

#### Breaking it Down:

- **`usermod`** → Modifies an existing user account.
    
- **`-aG`** → Appends (`-a`) your user to a new **secondary group** (`-G`), without removing them from their existing groups. _(Warning: Forgetting the `-a` will remove the user from all other groups!)_
    
- **`sudo`** → The group that holds administrative privileges (as defined in `/etc/sudoers`).
    
- **`yourusername`** → The user account you are modifying.
    

#### Why is this necessary?

If a user isn't in the **`sudo` group** (or explicitly allowed in `/etc/sudoers`), they will receive a **"user is not in the sudoers file"** or **"Permission denied"** error instead of a password prompt when attempting to run system commands.

#### Do you need to do this again?

Nope! This is a **one-time setup**. Your user will permanently have `sudo` privileges unless they are explicitly removed from the group.

### Verifying the Setup

To verify that the permissions were applied correctly, switch to the new user (or log out and log back in) and run:


```sh
groups
```

If `sudo` appears in the output list, you are all set! 🚀