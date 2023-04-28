# Moving Data

You may need to move data from your VM to your local machine or upload files to your VM for various reasons. In this document, we will cover how to use `scp` or `rsync` to move data from your VM or upload files to your VM.

## Moving Data from the VM

To move data from your VM to your local machine, you can use the `scp` command. Here are the steps to move data from your VM:

1. Ensure you can connect to your VM using SSH. See the previous [Launching a VM](02-launching-vms.md) document for more details.
2. Use the `scp` command to copy the data from your VM to your local machine. For example, to copy a file named `data.txt` to your local machine, run the following command on your local machine:
```bash
scp midgard:/path/to/data.txt /path/to/local/directory/
```

Note that `midgard` is the hostname of your VM, and `/path/to/data.txt` is the path to the data file on your VM. `/path/to/local/directory/` is the path to the local directory where you want to copy the data.

## Uploading Files to the VM

To upload files to your VM, you can use the `scp` or `rsync` command. Here are the steps to upload files to your VM using `scp`:

1. Ensure you can connect to your VM using SSH. See the previous [Launching a VM](02-launching-vms.md) document for more details.
2. Use the `scp` command to copy the files from your local machine to your VM. For example, to copy a file named `file.txt` from your local machine to your VM, run the following command on your local machine:
```bash
scp /path/to/file.txt midgard:/path/to/directory/
```

Note that `midgard` is the hostname of your VM, and `/path/to/directory/` is the path to the directory where you want to upload the file on your VM. `/path/to/file.txt` is the path to the file on your local machine that you want to upload.

Alternatively, here are the steps to upload files to your VM using `rsync`:

1. Ensure you can connect to your VM using SSH. See the previous [Launching a VM](02-launching-vms.md) document for more details.
2. Use the `rsync` command to copy the files from your local machine to your VM. For example, to copy a directory named `data` from your local machine to your VM, run the following command on your local machine:
```bash
rsync -avz /path/to/data/ midgard:/path/to/directory/
```

Note that `midgard` is the hostname of your VM, and `/path/to/directory/` is the path to the directory where you want to upload the directory on your VM. `/path/to/data/` is the path to the directory on your local machine that you want to upload.

After completing these steps, your data or files will be moved from your VM to your local machine or uploaded to your VM.
