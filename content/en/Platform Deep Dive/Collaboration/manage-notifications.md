---
title: "Manage Notifications"
linkTitle: "Notifications"
weight: 40
description: >
  Explore Cobalt notifications.
---

{{% pageinfo %}}
You can manage notifications for specific [pentests](#manage-pentest-notifications) and [findings](#manage-finding-notifications).
{{% /pageinfo %}}

By default, you get notifications for some activities related to your organization and pentests—both through email and in the Cobalt app. If you're not receiving email notifications, see our [troubleshooting tips](#troubleshoot-email-notifications).

{{%expand "View examples of activities." %}}
<br>
You get notified when someone has:

- Created or deleted a pentest
- Posted an update for a pentest
- Reported a vulnerability
- Changed a finding state
- Invited users to the organization

{{% /expand %}}
<br>

Your [user role](/platform-deep-dive/collaboration/user-roles/) determines which notifications you get.

## Manage Pentest Notifications

When you collaborate on a pentest, you get notifications depending on your notification preferences.

On the pentest page, select the bell icon ![Bell icon](/icons/Bell.png "Bell icon"), and set your preference:

- **Notifications on all activity**, unless you've explicitly unfollowed a [finding](#manage-finding-notifications). This is the default option.
- **Notifications on @ mentions and findings you participate in**
- **Mute notifications, except on findings you [follow](#manage-finding-notifications)**

![Manage notification preferences for a pentest](/deepdive/PentestNotifications.png "Manage notification preferences for a pentest")

## Manage Finding Notifications

You get notifications for a finding when someone:

- Assigned you to the finding.
- Mentioned you in a comment.
- Left a comment on the finding—if you subscribed to [pentest notifications](#manage-pentest-notifications).

If you're not participating, you can subscribe to notifications for a finding.

1. On the pentest page, go to **Findings**, and select a finding.
1. Under **Notifications**, select **Follow**.<br><br>
   ![Follow a finding](/deepdive/FollowFinding.png "Follow a finding")

To unsubscribe from a thread, select **Unfollow**.

## View All Notifications

To view notifications for all organizations you belong to, select the bell icon ![Bell icon](/icons/Bell.png "Bell icon") in the upper-right corner. The number of unread notifications, if any, appears on the bell icon.

![Navigate to the Notifications page](/deepdive/ViewAllNotifications.png "Navigate to the Notifications page")

You only see recent notifications in the popover. To view all notifications, select the three-dot icon {{% three-dots %}} > **Go to notifications page**.

- To mark all notifications as read, select **Mark all as read**.
- To mark a single notification as read, select the dot icon •.

## View Team Activity

To view the latest activity of your team members and pentesters, navigate to the **Activity** page. Both organization users and [Pentest Team Members](/platform-deep-dive/collaboration/user-roles/#pentest-team-member) can view this page.

![View team activity](/deepdive/ViewActivity.png "View team activity")

## Troubleshoot Email Notifications

### You're Not Receiving Emails from Cobalt

Do the following:

- Check with your IT administrator to ensure that the `cobalt.io` email domain:
  - Isn't included in the list of blocked senders.
  - Doesn't trigger a [Sender Policy Framework (SPF)](/getting-started/glossary/#sender-policy-framework) hard rejection. This failure occurs when the recipient mail server rejects emails from IP addresses not specified in the SPF record.
- Check the filters of your mailbox. Verify that the rules you've enabled don't affect emails from the `cobalt.io` email domain.
- Verify that emails from Cobalt aren't being marked as spam or junk.
- Make sure that you've confirmed your email address in Cobalt. To do that, click the link in the email invitation.

### You're Receiving Emails with Delay

This may happen because your organization has enabled [graylisting](/getting-started/glossary/#graylisting) for emails. To remedy this, add the `cobalt.io` email domain to the allowlist.

Refer to the documentation of your email management system for instructions. For example, read [how to configure permitted senders in Mimecast](https://community.mimecast.com/s/article/email-security-gateway-permitted-senders-policy-configuration?).
