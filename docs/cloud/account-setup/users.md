---
id: users
title: How to manage users in Temporal Cloud
sidebar_label: Users
sidebar_position: 3
description: Invite users, set account level roles, and set Namespace-level positions for users.
toc_max_heading_level: 4
keywords:
- temporal cloud
- temporal cloud account
- introduction
- how-to
- users
- user
- explanation
- namespace
tags:
- temporal-cloud
- temporal-cloud-account
- introduction
- how-to
- users
- user
- explanation
- namespace
---

<!-- THIS FILE IS GENERATED. DO NOT EDIT THIS FILE DIRECTLY -->

- How to invite users to your Temporal Cloud Account
- What are the available Account-level roles?
- What are the Namespace-level permissions?

## Invite users {#invite-users}

:::caution

Access to Temporal Cloud is authorized via single sign-on (SSO), currently limited to Google OAuth.
The email addresses of all users who need access to Temporal Cloud must be registered with Google.

If an email address is not associated with a Google Account, the user must follow the instructions in the [Use an existing email address](https://support.google.com/accounts/answer/27441?hl=en#existingemail) section of [Create a Google Account](https://support.google.com/accounts/answer/27441).

**Important:** Do _not_ create a Gmail account when creating a Google Account.

:::

When you create a user in Temporal Cloud, the prospective user receives an email invitation.
Before accepting the invitation, the user must be logged in to Google using the email address that received the invitation.
The user must then click **Accept Invite** in the message.
Attempting to log in to Temporal Cloud without first accepting the invite doesn't work.

### Roles and permissions

Each user in Temporal Cloud is assigned a Role.
Each user can be assigned permissions for individual Namespaces.

- [Account-level Roles](/cloud/#account-level-roles)
- [Namespace-level permissions](/cloud/#namespace-level-permissions)

<!--- How to invite users in Temporal Cloud using Web UI --->

### Invite users using Web UI

:::info

To invite users, a user must have the Global Admin account-level [Role](/cloud/#account-level-roles).

:::

1. In Temporal Web UI, click **Settings** in the lower-left portion of the window.
1. On the **Settings** page, click **Create Users** in the upper-right portion of the window.
1. On the **Create Users** page in the **Email Addresses** box, type or paste one or more email addresses.
1. In **Account-Level Role**, select a [Role](/cloud/#account-level-roles).
   The Role applies to all users whose email addresses appear in **Email Addresses**.
1. If the account has any Namespaces, they are listed under **Grant access to Namespaces**.
   To add a permission, select the checkbox next to a Namespace, and then select a [permission](/cloud/#namespace-level-permissions).
   Repeat as needed.
1. When all permissions are assigned, click **Send Invite**.

Temporal sends an email message to each user.
To join Temporal Cloud, a user must click **Accept Invite** in the message.

## What are the account-level Roles for users in Temporal Cloud? {#account-level-roles}

When a Global Admin invites a user to join an account, the Global Admin selects one of the following Roles for that user:

- **Global Admin**
  - Has full administrative permissions across the account, including users and usage
  - Has Namespace Admin [permissions](/cloud/#namespace-level-permissions) on all [Namespaces](/namespaces) in the account
- **Developer**
  - Can create and update Namespaces; has full control over [Workflows](/workflows)
  - Has Namespace Admin permissions for each Namespace created by that user
- **Read-Only:** Can only read information

## What are the Namespace-level permissions for users in Temporal Cloud? {#namespace-level-permissions}

A [Global Admin](/cloud/#account-level-roles) can assign permissions for any [Namespace](/namespaces) in an account.
A Developer can assign permissions for a Namespace they create.

For a Namespace, a user can have one of the following permissions:

- **Namespace Admin:** Can <a class="tdlp" href="/cloud/account-setup/namespaces#create-a-namespace">create<span class="tdlpiw"><img src="/img/link-preview-icon.svg" alt="Link preview icon" /></span><span class="tdlpc"><span class="tdlppt">How to manage Namespaces in Temporal Cloud</span><br /><br /><span class="tdlppd">You can create and manage Namespaces from your Temporal Cloud UI.</span><span class="tdlplm"><br /><br /><a class="tdlplma" href="/cloud/account-setup/namespaces#create-a-namespace">Learn more</a></span></span></a> and <a class="tdlp" href="/cloud/account-setup/namespaces#manage-namespaces">edit Namespaces<span class="tdlpiw"><img src="/img/link-preview-icon.svg" alt="Link preview icon" /></span><span class="tdlpc"><span class="tdlppt">How to manage Namespaces in Temporal Cloud</span><br /><br /><span class="tdlppd">You can create and manage Namespaces from your Temporal Cloud UI.</span><span class="tdlplm"><br /><br /><a class="tdlplma" href="/cloud/account-setup/namespaces#manage-namespaces">Learn more</a></span></span></a>; can create, rename, update, and delete [Workflows](/workflows)
- **Write:** Can create, rename, update, and delete Workflows within the Namespace
- **Read-Only:** Can only read information from the Namespace