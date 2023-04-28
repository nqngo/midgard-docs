# Welcome to Midgard
<figure markdown>
  ![Midgard Logo](assets/logo.png){: style="height:300px;"}
</figure>

Welcome to **Midgard**, a private OpenStack cloud for VAIT testing, training, and development purposes. Currently, **Midgard** offers the following capacities:

- Virtual Machines
- Automatic SSL termination via [Cloudflare Tunnel](https://developers.cloudflare.com/cloudflare-one/connections/connect-apps/)

Default quota:

| Property   | Value |
| ---------- | ----- |
| Instances  | 1     |
| VCPUS      | 2     |
| RAM        | 4GB   |

Please note that **Midgard** is a private lab and its service uptime is not guaranteed. Your project may be decommissioned to support other users, and it will be automatically deleted after 30 days. If you require a longer retention period, please renew your project before the 30-day period by running `/midgard renew`.

## Limitations

Please be aware of the following limitations when using **Midgard**:

1. **Midgard** does not have public IP addresses, so you will not be able to provide direct access to your instance. You will need to use `cloudflared` tunnel to access your instance unless it is served over HTTPS.
2. **Midgard** is a self-serviced Infrastructure-as-a-Service platform. You are responsible for setting up, maintaining, and upgrading your own instances.

## Quick Start

To request access, simply use the following slash command in the VAIT Discord:

```shell
/midgard register
```

Once your request is provisioned, **@Midgard Cloud** bot will notify you about your access.