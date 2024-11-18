---
icon: bell-on
cover: >-
  https://images.unsplash.com/photo-1514464750060-00e6e34c8b8c?crop=entropy&cs=srgb&fm=jpg&ixid=M3wxOTcwMjR8MHwxfHNlYXJjaHwxfHxub3RpZmljYXRpb258ZW58MHx8fHwxNzMxNjc5ODExfDA&ixlib=rb-4.0.3&q=85
coverY: -45
layout:
  cover:
    visible: true
    size: hero
  title:
    visible: true
  description:
    visible: true
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: true
---

# Notifications

Notifications are a way to get notified immediately when an intrusion is detected. You can receive notifications via email or Slack instant messaging.

## Create a notification

To create a notification, go to the **Notifications** menu item in the left sidebar. Click on the **Create** button and fill in the following fields:

* **Notification name**: A memorable name for the notification.
* **Type**: The type of notification. Currently, only email and Slack are supported.

Click on the **Configure notification provider** button to configure the notification provider.

### Email

* **SMTP server address**: The SMTP server endpoint to use for sending emails. For Gmail, you can use `smtp.gmail.com`.
* **SMTP server port**: The port to use for the SMTP server. For Gmail, you can use `587` for TLS or `465` for SSL.
* **Use SSL/TLS**: Whether to use SSL/TLS for the SMTP connection. For Gmail, this should be enabled.
* **Username**: The username to use for the SMTP server. For Gmail, this is your email address.
* **Password**: The password to use for the SMTP server. For Gmail, this is an [app password](https://support.google.com/accounts/answer/185833?hl=en).
* **Recipient email**: The email address to send notifications to.
* **Sender name**: The name to use as the sender of the email.
* **Sender email**: The email address to use as the sender of the email.

Click **OK** to save the notification provider configuration.

### Slack

* **API token**: The Slack API token to use for sending messages. You can create a new token by clicking the **Generate** button.
* **Channel ID**: The Slack channel ID to send messages to.

Click **OK** to save the notification provider configuration.

Verify the information in `Configuration` is correct and click **Save** to create the notification.

## Edit a notification

To edit a notification, click on the notification in the list and click on the **Edit** button. You can change the notification name and the notification provider configuration as you did when creating the notification.

## Delete a notification

To delete a notification, click on the **Delete** button in the `Actions` column of the notification list.
