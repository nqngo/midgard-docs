# Welcome to Midgard

Welcome to **Midgard**. **Midgard** is a private OpenStack cloud for VAIT testing, training, and development purpose. At the moment, **Midgard** offers the following capacities:

- Virtual Machines.
- Persistent Volume Storages.
- Managed Docker instance.
- API Access: OpenStack CLI, CloudFormation, Terraform, OpenStack Heat.

The following features are under development and can be only be tested via the API:
- Managed Kubernetes.

Default quota:

- _Max instances_: 4
- _Max VCPUS_: 4
- _Max RAM_: 8GB
- _Max persistent storage_: 120GB

As this is a private lab, service uptime is not guaranteed and your project might be decommisioned to support other users.

## Limitations

1. **Midgard** has no public IP addresses. You will not be able to provide direct access to your instance through WAN. If you require ingress through WAN, it is recommended that you expose a `cloudflared` tunnel or setup your own reversed proxy.
2. **Midgard** is a self-serviced Infrastructure-as-a-Service platform. You are responsible for the setup, maintenance, upgrade of your own instances.

## How to request Access

To request access, please provide the correct information on `#vait-cloud` channel using the following template:

```
Github: <your_username>
Fullname: <your_fullname>
Reason for Access: <your_reason_for_access>
```

Eg:

```
Github: nqngo
Fullname: Nhat Ngo
Reason for Access: Testing k3s for homelab use.
```

Once your request is approved, you will receive a private message from the cloud maintainer. Please setup your access following the instruction on [Accessing the Lab](access-the-lab).

