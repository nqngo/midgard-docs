# Installing Softwares

When you launch a VM in the cloud, it comes with a base image that includes a minimal set of software. However, you will often need to install additional software to run your applications or perform various tasks on the VM. In this document, we will cover how to install software on a VM running _Ubuntu 22.04_ and how to expose a simple web app to the internet.

## Installing Software

To install software on a VM running Ubuntu 22.04, you can use the `apt` package manager. Here are the steps to install software on your VM:

1. Connect to your VM using SSH. You can use the `ssh` command with the `midgard` hostname in your `~/.ssh/config` file. See the previous [Launching a VM](02-launching-vms.md) document for more details.
2. Update the package list: `sudo apt update`
3. Install the software you need. For example, to install Node.js and npm, run: `sudo apt install nodejs npm`

You can repeat step 3 for any other software you need to install on your VM.

## Example: Exposing a Simple Web App

To expose a simple web app to the internet, you can use the built-in `http-server` package for Node.js. Here are the steps to expose a simple web app:

1. Install `http-server`: `sudo npm install -g http-server`
2. Create a simple web page. You can use the following example as a starting point:
```html
<!DOCTYPE html>
<html>
  <head>
    <title>Hello, world!</title>
  </head>
  <body>
    <h1>Hello, world!</h1>
    <p>This is a simple web page.</p>
  </body>
</html>
```
3. Save this code as `index.html` in a directory of your choice.
4. Start the `http-server` with the directory containing `index.html` as the root: `http-server /path/to/directory`
5. The web app will be accessible on port 8080 of your VM.

Note that this is a simple web app for demonstration purposes only. For a real-world application, you will need to configure your web app properly for security and performance.

If you want to access the web app from your local machine, you can use SSH port forwarding to forward traffic from a local port to the VM's port 8080. For example, to forward traffic from port 8080 on your local machine to port 8080 on the VM, run the following command on your local machine:

```bash
ssh -L 8080:localhost:8080 midgard
```

Then you can access the web app from your local machine at `http://localhost:8080`. Note that in this example, the web app is only accessible from your local machine on port 8080. To make it accessible from the internet, see the [Port Forwarding](06-port-forwarding.md) section.
