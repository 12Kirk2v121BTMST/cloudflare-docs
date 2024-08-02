---
title: Auto-move events
pcx_content_type: how-to
weight: 4
---

# Auto-move events

Auto-move events are events where emails are automatically moved to different inboxes based on the disposition Email Security assigned to them.

Email security shows you the total number of auto-moves, and the source folder from which these moves are originating from.

To configure auto-move events:

1. Log in to the [Cloudflare dashboard](https://dash.cloudflare.com/).
2. Select **Zero Trust**.
3. Select **Email security**.
4. Select **Settings**.
5. Select **Moves**.
6. Under **Auto-moves**, select **Configure**.
7. Assign actions based on malicious, spoof, suspicious, spam, and bulk dispositions. Select among:
   - **Soft delete - user recoverable**: Moves the message to the user’s **Recoverable Items - Deleted** folder. Messages can be recovered by the user.
   - **Hard delete - admin recoverable**: Completely deletes messages from a user’s inbox.
   - **Move to trash**: Moves messages to the trash or deleted items email folder.
   - **Move to junk**: Moves the message to the junk or spam folder.
   - **No action**: Messages stay in the origin folder.
8. Select **Post-delivery** moves:
   - **(Recommended) Post-delivery response**: Enabling this option allows Email Security to rescan delivered emails at multiple time intervals for previously unknown phishing sites or campaigns.
   - **(Recommended) Phish submission response**: Enabling this option allows Email Security to move emails that your users reported as phishing and Email Security determined to be malicious.
9. Select **Save**.