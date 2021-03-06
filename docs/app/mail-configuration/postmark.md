---
title: Postmark
---

## Configuring Postmark

First off, make sure you have created an account with [Postmark](https://postmarkapp.com). 

At this moment, sending bulk email with Postmark is in beta. Before using Mailcoach to send out mails with Postmark, contact their support to enable this on your account.

## Configuring Postmark

At Postmark you must [configure a new webhook](https://postmarkapp.com/support/article/1067-how-do-i-enable-delivery-webhooks).

At the webhooks settings screen, on Postmark, you must add the `Open`, `Bounce`, `Spam Complaint` and `Link Click` webhooks and point them to the route you configured. 

The webhook should be sent to `https://<your-domain>/postmark-feedback`

## Configuring Mailcoach

On the Mail configuration settings screen in Mailcoach, you'll have to have to fill in these settings.

- Mails per second: to not overwhelm Postmark with mail requests, send this to a sensible value. In many cases `10` will be sufficient
- Server token: you can get the right value on the [Postmark account details screen](https://account.postmarkapp.com/account/edit)
- SMTP user
- SMTP password
