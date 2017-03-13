# DevOps-cookbook

## Python

### String

**index**
```python
s = 'github.com/guoliang-dev'
s.index('g')  # 0 - firs index from left
s.rindex('g')  # 18 - firt index from right
s.index('g', s.index('g') + 1)  # 11 second index from left

# contains? 
try:
    s.index('python')
except ValueError as e:
    print 'cannot find the value: %s' % e
```

**adjust**
```python
s='github'
s.ljust(20, '-')  # 'github--------------'
s.rjust(20, '-')  # '--------------github'
```

**cout occurrences**
```python
s = 'cookbook'
s.count('o') # 4
s.count('o', 0, 2) # 1
```

### I/O

### Datetime



## Windows CMD

### Windows OS quick setup

**auto start**
add app shortcut to: 
```
# auto start for all users
C:\ProgramData\Microsoft\Windows\Start Menu\Programs\Startup
# auto start for one user
C:\Users\<user-id>\AppData\Roaming\Microsoft\Windows\Start Menu\Programs\Startup  #shorcut: shell:startup
```

### I/O

**robocopy**
```bat
robocopy c:/tmp/sf c:/tmp/dest /MIR

```
return code: `1` - `One of more files were copied successfully.` [robocopy return codes](https://blogs.technet.microsoft.com/deploymentguys/2008/06/16/robocopy-exit-codes/)


### Windows Service

```bat
sc \\<remote-server> <service>
sc \\<remote-server> stop <service>
sc \\<remote-server> start <service>

net start <service>
net stop <service>
```
[*net start vs. sc start*](https://superuser.com/questions/315166/net-start-service-and-sc-start-what-is-the-difference)

### Windows Scheduler Job

### PsExec

### HPC



## Database

### SQL

### H2

### SQL Server / T-SQL

### MySQL



## PowerShell



## Bash

### Linux 
```bash
# show user's groups
groups <user-name>

# add user to group
sudo usermod -a -G <group-name> <user-name>

# log off
logoff
```

## Vim

## Regular Expression

**Python**

```python
s = 'SB20170313AWS123456'
m = re.search('SB\\d{6,8}([a-zA-Z]{3,6})\\d{6}', s)
print m.group(1)
```
**JavaScript**
```javascript
s = 'SB20170313AWS123456'
mc = s.match('SB\\d{6,8}([a-zA-Z]{3,6})\\d{6}')
console.log(mc[1])
```

## IDE

### IntelliJ 

**open file in Explorer:** `ctrl + alt + F12`

**recent files popup** `ctrl + e`

**Maximize editor:** `ctrl + shift + F12`

