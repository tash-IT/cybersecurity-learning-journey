# Linux file system hierarchy
- Linux organizes system in a hieracrchical structure.
## Key directories:
| Directory | Purpose |
| / | Root directory |
| /etc | System configuratiobn files |
| /home | User personal directories |
| /tmp | Temporary files(created on reboot) |
| /root | Home directory for root user |
| /dev | Device files (Hardware interfaces) |

## Security Best Practices
1. Always use sude instead of root login
2. Regularly update system (sudo apt update && sudo apt upgrade)
3. Use strong passwords
4. Configure firewall: 
      sudo apt install ufw
      sudo ufw enable
      sudo ufw allow ssh (Secure Shell)

## Root vs sudo vs su
* Root(The master account) = The ultimate admin, can read, edit or delete files and change system settings without restrictiona
* sudo(Superuser Do) = allows authorized users to run commands as root temporarily.
    sudo su  **changesto rootbut keeps current environment
    sudo -i  **logs in as root with root's environment (cleaner)
* su(switch user) = Switches to another user(default: root if no username is given)
     su - **switches to root (requires root password)
     su - username **Logs in as root with root's environment

## File and Directory permissions
- Every file/directory has 3 sets of permissions: Owner(user) - full access{rwx}
             Group - read and execute {r-x}
             Others(everyone else) - read-only {r--}

- Permission meanings
r(read) - View file contents
w(write) - modify file
x(execute) - run file/enter dir

