---
title: Email monitoring
pcx_content_type: how-to
weight: 1
---

# Monitor your inbox

Once you have chosen a [domain to scan](/cloudflare-one/email-security/setup/api-deployment/office365-api/#connect-your-domains), Email Security allows you to monitor the traffic scanned from your email inboxes.

To monitor your inbox:

1. Log in to the [Cloudflare dashboard](https://dash.cloudflare.com/).
2. Select **Zero Trust**.
3. Select **Email Security**.
4. Under **Email Security**, select **Monitoring**. 

The dashboard will display the following metrics:

- Email activity
- Disposition evaluation
- Detection details
- Impersonations
- Phish submissions
- Auto-move events
- Detection settings metrics

## Email activity

Email activity aggregates statistics about emails scanned and dispositions assigned (the number of email flagged due to a detection) within a given timeframe.

To view the live number of email scanned and dispositions scanned, enable **Live mode**.

## Disposition evaluation

Email traffic that flows through Email Security is given a final disposition, which represents Email Security's evaluation of that specific message.

Disposition evaluation displays the following dispositions:

- **Malicious**: Traffic invoked multiple phishing verdict triggers, met thresholds for bad behavior, and is associated with active campaigns.
- **Spoof**: Traffic associated with phishing campaigns that is either non-compliant with your email authentication policies ([SPF](https://www.cloudflare.com/en-gb/learning/dns/dns-records/dns-spf-record/), [DKIM](https://www.cloudflare.com/en-gb/learning/dns/dns-records/dns-dkim-record/), [DMARC](https://www.cloudflare.com/en-gb/learning/dns/dns-records/dns-dmarc-record/)) or has mismatching `Envelope From` and `Header From` values.
- **Suspicious**: Traffic associated with phishing campaigns (and is under further analysis by our automated systems).
- **Spam**: Traffic associated with non-malicious, commercial campaigns.
- **Bulk**: Traffic associated with [Graymail](https://en.wikipedia.org/wiki/Graymail_%28email%29), that fall in between the definitions of spam and suspicious. For example, a marketing email that intentionally obscures its unsubscribe link.

## Detection details

Detection details displays information about:

- **Malicious** disposition:
   * **Email threat types**: Top malicious threat types, and their number relative to the total amount of malicious threats received.
   * **Targeted users**: Top number of emails targeted, and their number relative to the total amount of malicious targets.
   * **Malicious links**: A graph displaying the total number of malicious links and their distribution throughout the month.
   * **Malicious attachments**: Number of malicious attachments, and the top types of malicious files received.
- **Suspicious** disposition:
   * **Suspicious threat types**: Top suspicious threat types, and their number relative to the total amount of threats received.
   * **Suspicious targets**: Top number of emails targeted, and their number relative to the total amount of malicious targets.
   * **Suspicious links**: A graph displaying the total number of suspicious links and their distribution throughout the month.
- **Spoof** disposition:
   * **Spoof users (impersonated names)**: Top number of impersonated names, and their number relative to the total number of detection received.
   * **Spoof targets**: Top number of targeted emails.
   * **Sender v. envelope mismatch**: This field indicates the number of mismatches between the email address the message was sent from, and the email address the message was _actually_ sent from. 

## Impersonations

Impersonations are a form of phishing attack where the actor pretends to be someone else to steal sensitive information.

**Impersonations** displays the number of targeted users, and a chart describing the total number of impersonation attempts.

To view all targeted users, select **View all targeted users**.
To view all impersonation emails, select **View all impersonation emails**.
To view impersonated users, select **View impersonated users**.

Refer to [Trusted domains](/cloudflare-one/email-security/detection-settings/trusted-domains/) to add a trusted domain, and [Impersonation registry](/cloudflare-one/email-security/detection-settings/impersonation-registry/) to add a user to the impersonation registry.


## Phish submissions

Phishing is a type of attack that involves stealing sensitive information with the aim of using and selling the information.

A phish submission happens when a user or an administrator reports a phishing attack. Refer to [Phish submissions](/cloudflare-one/insights/email-monitoring/phish-submissions/) to learn how to submit a phish.

Phish submissions displays the following information:

- **All submissions**: The total number of phish submissions.
- **User submissions**: The number of phish submissions reported by your users.
- **Admin submissions**: The number of phish submissions reported by an administrator.

Select **Review submissions** to review a filtered list of phish submissions reported by your team.

## Auto-move events

Auto-move events are emails moved to different inboxes based on the disposition Email Security assigned.

This panel shows you the total number of auto-moves and the source folder from which these retractions are originating from.

Refer to [Auto-moves](/cloudflare-one/email-security/auto-moves/) to configure auto-move events.

## Detection settings metrics

Detection settings metric displays information about:

- **Allowed traffic**: Traffic that Email Security will exempt emails that match certain patterns from normal detection scanning.
- **Blocked traffic**: Traffic that Email Security automatically blocks from senders.
- **Domain age**: The number of days since domain registration.

Select **Configure** to configure policy and rules for [allowed traffic](/cloudflare-one/email-security/detection-settings/allow-policies/), [blocked traffic](/cloudflare-one/email-security/detection-settings/blocked-senders/) and [domain age](/cloudflare-one/email-security/detection-settings/additional-detections/).