# Launching Instances

To launch the a basic instance:

1. Logon to your Midgard Dashboard
2. Navigate to `Project / Compute / Instances` in the navigation panel on the left hand side.
3. Click the `Launch Instance` button to start the Launch Dialog.
4. **Details Dialog:** Your instance must have a `name`; a `description` is optional. You can launch multiple instances at a time by setting the `Count` (e.g. 2 will launch 2 VM’s). Click `Next` to continue.
5. **Source Dialog:** Choose a Boot Source. By default, Midgard booted from image and automatically create a persistent volume for persistence. If you do not need data persistence or choose `No` to create an volume option. Use the Filter widget to help you find the image you need; Use the up-arrow button beside the image you need to select it for launch (eg. `Ubuntu 22.04 LTS`)
6. **Flavor Dialog:** Selected the required instance VCPUs, RAM and boot disk size. Use the up-arrow button beside the flavor you need to select it for launch. Eg. `m1.small`
7. **Networks Dialog:** It is defaulted to private network. Unless you have specific networking requirement, the default option is ideal.
8. **Security Groups:** It is recommended to add the `ssh` security group you created following [Security Groups](01-security-groups.md) in addition to the `default` security group.
9. **Key Pair:** Choose the keypair that will be used to populated the instance `~/.ssh/authorized_keys`.


