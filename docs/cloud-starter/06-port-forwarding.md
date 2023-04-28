# Using Port Forwarding

Midgard is a lab environment that is behind a NAT. This means that your instance does not have a public IP address and is not directly accessible from the internet. To make your instance accessible from the internet, you can use port forwarding in Midgard.

## Port Forwarding with Midgard

To port forward in Midgard, you can use the `/midgard add portforward` command. Here are the steps to set up port forwarding for your instance:

1. Connect to the Midgard Discord server and go to the `#bot-commands` channel.
2. Decide on the port you want to forward. For example, let's say you want to forward port `8080`.
3. Run the following command to set up port forwarding:
```bash
/midgard add portforward port:8080
```
4. This will create a security group in Midgard and set up a Cloudflare tunnel to expose your instance traffic to an HTTPS endpoint. The default protocol is HTTP. Other protocol options are TCP and SSH, but protocols other than HTTP have to be proxied through the Cloudflare binary.

After running the command, you will receive a response from Midgard with a URL that you can use to access your instance over HTTPS.

The URL will automatically terminate SSL for you.