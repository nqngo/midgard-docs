# Security Groups

Security Groups are Midgard's way of specifying what network traffic can reach into -and out of- your Virtual Machine (VM). By default a VM brought up in the Midgard Cloud can reach out to the world via the network, but the world can’t reach in.

You need to specify any network traffic to be allowed to reach the VM via the Rules in a Security Group. Security groups can be applied to VMs at launch and can be applied or removed at any other time in the VMs life.

## Inspecting your Security Groups

1. Logon to your Midgard Dashboard
2. Navigate to `Project / Network / Security Groups` in the navigation panel on the left hand side.
3. You will now see a list of the Security Groups that are available in your project.
4. Click the `Manage Rules` option in the Action Menu button on the `default` group.
5. A list of `Rules` is displayed that are part of this Security Group.

## Creating a Security Group

1. Logon to your Midgard Dashboard
2. Navigate to `Project / Network / Security Groups` in the navigation panel on the left hand side.
3. Click the button `+ Create Security Group`.
4. Give your Security Group a meaningful Name and optionally a Description. For the purpose of this tutorial we recommend the name `SSH`.
5. Click Create Security Group to finalise this step. You have now created a Security Group and you are ready to configure it with the right Rules.

## Adding `ssh` Access

1. After clicking the create security group button above, you will automatically see the rules for this group. Two Egress rules should be visible.

    Egress means traffic/data sent out of our virtual machine. What we are concerned with, is who is trying to come in. So to allow our own connections, we need to add an Ingress rule for SSH access.

2. To add the SSH rule, click the `+ Add Rule` button.
3. In the Add Rule dialog, select the Rule SSH in the `Rule` selector.
4. Click the Add button to complete this step. You have created a Security Group and configured it with the SSH rule.

## Applying Security Groups

Security Groups are applied to Virtual Machines to allow them to receive network traffic. Typically you apply Security Groups when you Launch your VM, but you can add security groups to your running VM at a later time too; Or indeed remove security groups from your VMs.

### Applying a Security Group at Launch

When you launch an instance using the Midgard dashboard, the Launch Instance dialog will guide you and will ask you to apply one or more security groups. You will need to have created those group before the following the launch dialog.

If you’re following the Cloud Starter: you’ll learn about Launching and the Dialog in [Launching Virtual Machines](launching-instances.md).

### Applying a security group on a running instance

If an instance is already running you can add security groups to the running instance to make it respond to additional network traffic, or remove security groups when they’re no longer required. You do this using the option `Edit Security Groups` in the `Action` button menu for your instance.

If you’re following the Cloud Starter: you’ll learn about more about Changing things on your instance in [Rebooting, Deleting, Rebuilding, Resizing](changing-instances.md)