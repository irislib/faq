# Iris FAQ

[Iris](https://iris.to/) is a Nostr Android, iOS and web client for better social networks.

Please note that this FAQ section is a work-in-progress. The information may have already changed due to the frequent app and network updates.

If you cannot find the answer to your question, you can always reach out to other Iris and Nostr users for assistance. 

There is a growing number of Nostr resources that may also instruct in using Iris (e.g. [nostr.how](https://www.nostr.how/clients/iris)).

## Getting started

### Alby support
Iris web client works with the [Alby](https://www.getalby.com) extension. According to Alby, also with multiple keys.

### Avatar
Gif avatars work on Iris.

### Profile banner size
1500x500 pixels is the preferred size. 

### Dark/light theme
You can change the theme on settings. Iris will remember your selection even on other clients.

### Login options
Supports npub and window.nostr login as well as Alby and nos2x browser extensions. You can also paste your public key (npub) if you don't want to make any changes (e.g. follow, write notes, like, read DMs etc.).

### Android version
Google Play store [version](https://play.google.com/store/apps/details?id=to.iris.twa). [(apk)](https://github.com/irislib/iris-messenger/releases)

### Username
Iris supports profile URLs in the following formats ([examples](https://iris.to/post/note1wn6axvzvnzn8hr45j95qlxpag4u7xcdx79rtk0uet8s5hhqynfhsdfppve)): 
 - https://iris.to/bob (bob is an iris.to/username, not publicly available yet)
 - https://iris.to/alice@example.com (if you have a NIP05; not your email)
 - https://iris.to/example.com (if you have a NIP05 _@example.com)
 - https://iristo/npub (nostr public key)
 
The username that you can change in "edit profile" is not unique. However, nip05 names such as alice@example.com are unique. 

### Browser version

Iris works on most common browsers: [iris.to](https://iris.to/). 

### iOS app
You can install the browser app version on your home screen or use the Testflight [version](https://testflight.apple.com/join/5xdoDCmG).

### Testflight
Iris is in Testflight public testing. Join [here](https://testflight.apple.com/join/5xdoDCmG).

## Using Iris

### Audio player
Notes can play audio.

### Badge
Indicates that the user is NIP05 verified.

### Block
User blocks are private. When you block someone on Iris, DMs will be locally removed as well, and any further DMs rejected.
Block lists are stored encrypted to self in event kind 16462.

### Color badges on user names
- Blue =  a followed verified user (NIP05)
- White = you don't follow but  1-10 of your following follows the user (hover over the icon and Iris shows the count)
- Yellow = you don't follow but over 10 of your following follows the user (hover over the icon and Iris shows the count)

### Feed and spam
Iris rejects events from authors that your social network has not interacted with. The downside is that discovery of new users is more difficult, and sometimes you see fewer posts than on other clients.

### Flag (public)
The users you choose to report are blocked on your feed and the list of your flagged users is public.

### Followers
Nostr doesn't save individual follows as events, only the most recent version of your contact list. You'd have to save the "followed" event locally either manually or by your client.

### Image links
You can post image URLs and the media is shown in the notes. 

### Global feed
Global feed shows notes from everyone in your extended network of follows.

### Embedded media formats
Youtube, IG, Tidal and Spotify play on notes.

Brave browser issue: Spotify embed may cause Brave to ask to install a Widevine DRM BS extension.

### Likes
Click the number next to the heart in a note to see who liked it.

### New user / not logged in
If a user's name is not found, a deterministic Adjective Animal name is shown instead of the public key (e.g. Grubby Magpie)

### Log in with the public key
If you use a public key to log in you have a read-only view of certain information but cannot add, edit or delete information.

### Notes
There're no restrictions on who sees your posted notes. All notes are public. Clients can change what the user views (see the feed and spam section) but it does not change the fact that nostr handles all notes as public for now (unless they are DM content), and you should consider everything as public. 

For a quote note (you can also have more than one), copy the NoteID (from the note menu) and paste it on the new note into the position where you want the quoted note.

Mentioning users When writing a note, type @ and wait for the menu to come out and choose the preferred user by clicking it from the menu.

### Markdown
This is not supported yet.

### New follower notifications
Iris shows notifications for new followers but doesn't save the notification yet. The notification is only shown when Iris has locally cached someone's contact list and gets a new version of it (updates were made elsewhere).

### Search notes
You can paste note ids (bech32, beginning with “note”) into the search box to find them.

### Upload images
You can use the attach media option when writing a note, or upload to [imgur](https://imgur.com/upload), [nostr.build](https://www.nostr.build/) or a similar service and then insert the link to the note.

### Upload media
Video and audio uploads are supported on notes.

### Report notes
You can publicly report users' posts. It publishes a delete event for the reported note in Nostr.

### Undo and delete
In the note menu, there’s a delete option for notes. It’s up to relays and other clients to respect it so consider it more as a wish than anything else. Hidden or ignored is not deleted. This is how nostr protocol works. Unboosting and unliking work the same way (not available yet).

### Webtorrent magnet links
Notes preview and play Magnet webtorrent media links (may not work on mobile devices).

## Lightning

### Lightning address
`lightning:iris@getalby.com` format is supported. Add your lightning wallet in the edit profile section.

### Receiving lightning
Issue a Lightning invoice or you can also use `lightning:iris@getalby.com` format.

### Zapping
Your mobile wallet needs to be registered on the device for the link to be recognised when you click it.

Lightning wallets are starting to implement the zapping feature. You could try
www.walletofsatoshi.com for mobile or https://getalby.com for desktop, for example.

Currently, The ⚡️ is a lightning: link to the user's address. There is no listing of zaps yet. 

## Privacy and security

### Key safety on browser apps
Browser applications are not signed by the developer unlike native apps and browser extensions. Someone could hack the server or DNS and serve malicious code that steals your private key. XSS is also a risk, although not common in applications that use a framework like react.

### Privacy on uploaded images
Image loading is done via proxy to resize and avoid IP leaking unless it's from a whitelisted (e.g. imgur.com and nostr.build)

### Private message privacy (DMs)
Only the message content is encrypted: sender, recipient and timestamp are visible to everyone.

## Network, storage and relays

### Caching
Iris caches profiles, follows and the latest 1000 notes for a faster and better user experience.

### Features disappeared or missing?

If you force refresh on your browser that might help (cmd/ctrl +R in some browsers) or quitting the app may also help clear the local cache ([iOS](https://support.apple.com/en-us/HT201330)).

### Keyword search
Keyword search works with relays that have implemented it.

### Local storage
Iris stores a few of the latest messages, contacts and metadata, but could store more in the future.

### NIP05 verification failed
If your NIP05 is not showing check whether you have technical errors in the NIP05 implementation (e.g. CORS error).

if your NIP05 shows as valid on one client, but invalid on the other it could be a local cache issue. Try cmd/cntr + R to do a force refresh on the browser, or quit and restart the app.

### Relays
The relays Iris uses can change over time since they reflect the content you're viewing.

### Relay requests
Iris asks for 1000 latest events from known users initially. Some relays don't like the large authors filter (100-2000). Then it subscribes to all upcoming messages but discards those that are from unknown authors. When you open someone's profile, all their events are queried.

### Umbrel
Iris may not work with ws: but only with wss: (using webcrypto api). Browsers don't let you connect to a non-secure address (ws) if the page is loaded from a secure origin (https).

### Timestamps
Iris saves the notifications and DM threads' last seen timestamp for easier client synchronisation.

### What is NIP-5
The NIP05 address is just an easier way to find your public key profile. Just like email addresses, many people can have the same NIP05 username (e.g. Bob), but not on the same domain (e.g. bob@domain.com).

## Questions and support

### Iris developer
[Martti Malmi](https://iris.to/npub1g53mukxnjkcmr94fhryzkqutdz2ukq4ks0gvy5af25rgmwsl4ngq43drvk) develops Iris full-time.

### Iris name
Iris is the Greek goddess of the rainbow and the messenger of gods. Iris means rainbow in ancient Greek. The iris of the eye is named so because of its many colors. Eyes are essential for human communication. Iris users could be called [iridians](https://en.wiktionary.org/wiki/iridian).

### Iris Telegram group
Join the Iris.to telegram group: https://t.me/+u-qC51vCUWQ3NmRk

### Language options
If you would like to contribute to better translations, please [visit](https://docs.google.com/spreadsheets/d/19VSmmqqq5zpOcKIS2H8bHcVeG3Bby5aW8Q_4LykPUao/edit?usp=sharing).
