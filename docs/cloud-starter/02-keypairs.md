# Key Pairs

A Public-Private keypair is used in the Nectar instead of a password, to log on to any Virtual Machine (VM) you launch in Midgard.

A Public-Private keypair is a pair of files, your Private key and your Public key. They uniquely belong to each other (just like a lock and key). Your Private key file is yours, and yours alone (just like your car or house keys!). You should securely store it on a location on your computer that is only accessible to you. Your Public key can be used to authorise and authenticate you in a remote computer account.

When you launch an instance, Midgard places the Public key from your Midgard account into your VM for you. This way you can use SSH to connect to your VM using the three essential connection elements:

- Computer’s IP address
- The user account,
- The private key that is securely stored on your computer.

## Creating a Key Pair

1. Logon to your Midgard Dashboard
2. Navigate to `Project / Compute / Key Pair` in the navigation panel on the left hand side.
3. Click the button `+ Create Key Pair`.
4. Name your new key pair, select `SSH Key` as your `Key Type` and click `Create Key Pair`.
5. The new OpenStack keypair will automatically download to your local machine; make sure you don't lose it, or you won't be able to access the new instance.

## Importing an existing Key Pair

If you have an existing SSH public key, you can import it into Midgard by:

2. Navigate to `Project / Compute / Key Pair` in the navigation panel on the left hand side.
3. Click the button `Import Public Key`.
4. Name your new key pair, select `SSH Key` as your `Key Type`
5. Upload your SSH public key file or paste the content directly in box.
6. Click `Import Public Key`.
