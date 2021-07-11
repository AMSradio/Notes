# STEPS and Resources to connect via SSH Key
## What is an SSH KEY?
Main community help page:
https://oregon.bootcampcontent.com/help/#new-to-git-and-gitlab
Under "User Account" table, you will see SSH info under "Authentication"
https://oregon.bootcampcontent.com/help/topics/authentication/index.md

## REVIEW EXISTING SSH KEYS
If you have existing SSH keys, you may be able to use them to help secure connections with GitLab
repositories. By default, SSH keys on Linux and macOS systems are stored in the user's home directory,
in the .ssh/ subdirectory. The following table includes default filenames for each SSH key algorithm:

Algorithm: ED25519 (preferred)
Public Key: id_ed25519.pub
Private Key: id_ed25519

Algorithm: RSA (at least 2048-bit key size)
Public Key: id_rsa.pub
Private Key: id_rsa

Algorithm: DSA (deprecated)
Public Key: id_dsa.pub
Private Key: id_dsa

Algorithm: ECDSA
Public Key: id_ecdsa.pub
Private Key: id_ecdsa

For recommendations, see options for SSH keys:
https://oregon.bootcampcontent.com/help/ssh/README.md#options-for-ssh-keys

## GENERATING A NEW SSH KEY PAIR
ED25519 SSH keys
The book Practical Cryptography With Go
suggests that ED25519 keys are more secure and performant than RSA keys.
As OpenSSH 6.5 introduced ED25519 SSH keys in 2014, they should be available on any current
operating system.
You can create and configure an ED25519 key with the following command:
ssh-keygen -t ed25519 -C "<comment>"
    replace comments with something like your email
    passphrase is optional but is extra security if wated
You'll see a response similar to:
Generating public/private ed25519 key pair.
Enter file in which to save the key (/home/user/.ssh/id_ed25519):
    - to ensure you're saving to the right folder, navigate to the area, right click, and "git bash here"
## RSA SSH Keys
If you use RSA keys for SSH, the US National Institute of Standards and Technology recommends
that you use a key size of at least 2048 bits.
By default, the ssh-keygen command creates an 1024-bit RSA key.
You can create and configure an RSA key with the following command, substituting if desired for the minimum recommended key size of 2048:
ssh-keygen -t rsa -b 2048 -C "email@example.com"
    put your email in the quotes
You'll see a response similar to what was mentioned earlier except it will start with Generating public/private rsa key pair... followed by confirming where to save the key like last time

for more info go to the "options for ssh keys" link above

## Adding an SSH key to your GitLab account
Copy your public SSH key by one of the following commands:
MAC: pbcopy < ~/.ssh/id_ed25519.pub
Linux: xclip -sel clip < ~/.ssh/id_ed25519.pub
Windows: cat ~/.ssh/id_ed25519.pub | clip
    if using an RSA, substitute accordingly
In GITLAB navigate to settings and SSH Keys on the left
Paste the key you copied withe "clip" command from before. Use a descriptive name like "Work Laptop"
add an expiry date if applicable- it's optional
Click Add key Button

## Test it out
To test whether your SSH key was added correctly, run the following command in
your terminal (replacing gitlab.com with your GitLab's instance domain):
ssh-T git@gitlab.com
    replace everything after the @ with your instance
