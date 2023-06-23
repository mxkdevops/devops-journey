# Daily log for coding linux command

### 23/06/2023 09: 39 . Creating a linux user with groups and set him temporary password

# Create a new user
sudo useradd -m -G dev,sudo newuser

# Set a temporary password for the new user
sudo passwd newuser

# Set password expiration and enforce change upon first login
sudo chage -d 0 newuser

# check the content of passwd file
cat /etc/passwd
