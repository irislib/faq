# Iris FAQ

[Iris](https://iris.to/) is a Nostr Android, iOS and web client for better social networks.

Please note that this FAQ section is a work-in-progress. The information may have already changed due to the frequent app and network updates.

If you cannot find the answer to your question, you can always reach out to other Iris and Nostr users for assistance. 

There is a growing number of Nostr resources that may also instruct in using Iris (e.g. [nostr.how](https://www.nostr.how/clients/iris)).

## Getting started

### Alby support
Iris web client [works](https://iris.to/post/note1a9m6zcfjsrmulxxqkpe7wj8h580vh5yqrg3389dj5qcvduztlyjsavrv4y) with the [Alby](https://www.getalby.com) extension also with multiple keys.

### Avatar
Gif avatars [work](https://iris.to/post/note1jq69869gcds9pqvgxchsmegju9gnn208zgut84z5epwhnhh23d6sfkyjvm) on Iris.

### Profile banner size
1500x500 pixels is the preferred size. 

### Dark/light theme
You can change the theme on settings. Iris will remember your selection even on other clients.

### Login options
Supports npub and window.nostr login as well as Alby and nos2x browser extensions. You can also paste your public key (npub) if you don't want to make any changes (e.g. follow, write notes, like, read DMs etc.).

### Android version
Google Play store [version](https://play.google.com/store/apps/details?id=to.iris.twa). [(apk)](https://github.com/irislib/iris-messenger/releases)

### Username (nostr)
Iris supports profile URLs in the following formats ([examples](https://iris.to/post/note1wn6axvzvnzn8hr45j95qlxpag4u7xcdx79rtk0uet8s5hhqynfhsdfppve)): 
 - `https://iris.to/bob` (bob is an `iris.to/username`)
 - `https://iris.to/alice@example.com` (if you have a NIP05; not your email)
 - `https://iris.to/example.com` (if you have a NIP05 _@example.com)
 - `https://iristo/npub` (nostr public key)
 
The username that you can change in "edit profile" is not unique. However, NIP05 identifiers such as `alice@example.com` are unique. 

### Iris username

Iris username helps users to find your nostr profile easier.

The format is `iris.to/username` (for example: [iris.to/sirius](https://iris.to/sirius)).

You can also use `username@iris.to` format (NIP05; e.g. `sirius@iris.to`) in user searches.

You cannot change your Iris username. They are unique, more than 3 characters long and using letters and numbers only. You can use underscore (\_) but no other special characters are allowed.

Namesquatting, impersonation, vulgar or otherwise offensive usernames may result in you losing your username (also spamming or otherwise abusive username usage).

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
Indicates that the user has a NIP05 identifier.

### Backups and Restore

You can download (and copy) your profile data and the following list.

You can restore your previous data either by uploading the file (.json) or pasting the same data into the field.

Restoring your old following data will merge it with your current version. The profile data is restored only if it's the latest version (event). All other events are republished (not posted as new).

### Block
User blocks are private. When you block someone on Iris, DMs will be locally removed as well, and any further DMs rejected.
Block lists are stored encrypted to self in event kind 16462.

### Color badges on user names
- Blue =  a followed user
- White = you don't follow but  1-10 of your following follows the user (hover over the icon and Iris shows the count)
- Yellow = you don't follow but over 10 of your following follows the user (hover over the icon and Iris shows the count)

### Feed and spam
Iris rejects events from authors that your social network has not interacted with (actions such as follow, like, reply etc. that refer to the npub in question). 

For example, if you have a follower and let's call your follower a spammer: If nobody has ever liked, followed, replied or interacted in any (nostr event) way with the spammer then you will not see it.

Your network starts from you and who you follow and goes forward from there. Who follows you is not automatically part of your network unless any interaction happens.

The result is that you get less spam. Your follower count number is lower for the same reason. The downside is that discovery of new users is more difficult, and sometimes you see fewer posts than on other clients.

### Flag (public)
The users you choose to report are blocked on your feed and the list of your flagged users is public.

### Follower count

Your follower count may seem lower on Iris than other clients. Iris rejects events from authors that your social network has not interacted with. You get way less spam and your follower count number is lower for the same reason.

### Following list
Nostr doesn't save individual follows as events, only the most recent version of your contact list. You'd have to save the "followed" event locally either manually or by your client. Keeping more than one nostr client session open (not logged out) is not advised since this may reset your following list.

### Image links
You can post image URLs and the media is shown in the notes. 

### Global feed
Global feed shows notes from everyone in your extended network of follows.

### Embedded media formats
Youtube, IG, Spotify, Tidal and Twitch play on notes.

Brave browser issue: Spotify embed may cause Brave to ask to install a Widevine DRM BS extension.

### Likes
Click the number next to the heart in a note to see who liked it.

### New user / not logged in
If a user's name is not found, a deterministic Adjective Animal name is shown instead of the public key (e.g. Grubby Magpie)

### Log in with the public key
If you use a public key to log in you have a read-only view of certain information but cannot add, edit or delete information.

### Markdown
This is not supported yet.

### Notes
There're no restrictions on who sees your posted notes. All notes are public. Clients can change what the user views (see the feed and spam section) but it does not change the fact that nostr handles all notes as public for now (unless they are DM content), and you should consider everything as public. 

For a [quote note](https://iris.to/post/note10ekxar0vvwnt6l098eemfypv3ty0ehtf47lfd8ljz9fv9tvz23psggdn00) (you can also have more than one), copy the NoteID (from the note menu) and paste it on the new note into the position where you want the quoted note.

Mentioning users When writing a note, type @ and wait for the menu to come out and choose the preferred user by clicking it from the menu.

Posting notes [works](https://iris.to/post/note1e8znafpc9sxgq447t6llsc0thp3eh80mh5zy6g6wqhygu8pf8ggq6maj9q) also by pressing cmd/ctrl + return on your keyboard.

### New follower notifications
Iris shows notifications for new followers but doesn't save the notification yet. The notification is only shown when Iris has locally cached someone's contact list and gets a new version of it (updates were made elsewhere).

### Notifications

Iris shows [notifications](https://iris.to/post/note1esk3s2mkjmtxmew83407ywxt68yg0dcel4vu9knv3u450p86akwsgf2dwk) in one place (the ❤️ on the menu).

### Search notes

You can [search](https://iris.to/post/note1gd35qpaj2tke6ku8rjf4mtnjuafk4y5ghmrvspfse0s2a3stlrcqs5yn95) users by
⚡️ npub
⚡️ NIP05 (`jack@cash.app`)
⚡️ @ (and start typing the name)

Notes by the NoteID (starting with note1)
⚡️ with hashtags and keywords

There's also [support](https://iris.to/post/note1hr7ye9vud7g0jxe3mma0j75gamusrzwhtejth5erqm9v9h5u9j7q3lawa8) for Chinese, Japanese and Korean languages.
Iris search is based on https://nostr.band with its content, results and features.

### Upload images
You can use the attach media option when writing a note, or upload to [imgur](https://imgur.com/upload), [nostr.build](https://www.nostr.build/) or a similar service and then insert the link to the note.

### Upload media
Video and audio uploads are supported on notes.

### Report notes
You can publicly report users' posts. It publishes a delete event for the reported note in Nostr.

### Undo and delete
In the note menu, there’s a delete option for notes. It’s up to relays and other clients to respect it so consider it more as a wish than anything else. Hidden or ignored is not deleted. This is how nostr protocol works. Unboosting and unliking work the same way (not available yet).

### View as

Iris allows you to view other accounts with their public key (a nostr protocol feature) if you're using a browser extension login. Visit the user's profile and open the user's profile menu and select the "[View as...](https://iris.to/post/note19nlkcm50kv4jfujhnprrgwa0m07s0wj7gqh663pu87sfgytgs6jqu32st4)" option.

### Webtorrent magnet links
Notes preview and play Magnet webtorrent media links (may not work on mobile devices).

## Lightning

### Lightning address
`lightning:iristoapp@getalby.com` format is supported. Add your lightning wallet in the edit profile section.

### Receiving lightning
Issue a Lightning invoice or you can also use `lightning:iristoapp@getalby.com`format.

### Zapping
Your mobile wallet needs to be registered on the device for the link to be recognised when you click it.

Lightning wallets are starting to implement the zapping feature. You could try
www.walletofsatoshi.com for mobile or https://getalby.com for desktop, for example. The technical term is [NIP-57](https://github.com/nostr-protocol/nips/blob/master/57.md).

Currently, The ⚡️ is a lightning: link to the user's address ([see how it works](https://iris.to/post/note10uvvg0drlevur3y3cy6xgncwyg7ww28222yrkpfjy6kcc9w9d72qjnn5qp)). There is no listing of zaps yet. 

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
If your NIP05 is not showing on your profile, check whether you have technical errors in the NIP05 implementation (e.g. CORS error).

if your NIP05 shows as valid on one client, but invalid on the other it could be a local cache issue. Try cmd/cntr + R to do a force refresh on the browser, or quit and restart the app.

### Relays
The relays Iris uses can change over time since they reflect the content you're viewing.

### Relay requests
Iris asks for 1000 latest events from known users initially. Some relays don't like the large authors filter (100-2000). Then it subscribes to all upcoming messages but discards those that are from unknown authors. When you open someone's profile, all their events are queried.

### Umbrel
Iris may not work with ws: but only with wss: (using webcrypto api). Browsers don't let you connect to a non-secure address (ws) if the page is loaded from a secure origin (https).

### Timestamps
Iris saves the notifications and DM threads' last seen timestamp for easier client synchronisation.

### What is NIP-05
The NIP-05 identifier is an easier way to find your public key profile. Just like email addresses, many people can have the same NIP05 name (e.g. Alice), but not on the same domain (e.g. `alice@domain.com`).

## Troubleshooting

### Why what I am posting from one device is not always visible to others?

It could be that your other client's relays have not picked it up. 

Copy the noteid from one client and paste it into the Iris search box on the other and see whether it comes up. 

If you're sure that it is published you could try to "Resend to relays" from the note menu. 

It could also be that you're not logged in with your private key, you're offline or not connected to the relays. A quick way to see whether you're logged in with your private key (nsec) is to see whether the DMs are open and whether you can read their content.

### Why my picture is not showing up on other devices?

See the previous [answer](https://github.com/irislib/faq#why-what-i-am-posting-from-one-device-is-not-always-visible-to-others) first.

Iris uploads the pictures to a third-party service (e.g. www.nostr.build ) so it's a possibility that something is not working on their end. Yet, if you can get the picture URL from the original post (for example, "Copy raw data" from the note menu) and paste it on a browser you can verify whether it's available and visible.

## Questions and support

### Iris developer
[Martti Malmi](https://iris.to/npub1g53mukxnjkcmr94fhryzkqutdz2ukq4ks0gvy5af25rgmwsl4ngq43drvk) develops Iris full-time.

### The name Iris
Iris is the Greek goddess of the rainbow and the messenger of gods. Iris means rainbow in ancient Greek. The iris of the eye is named so because of its many colors. Eyes are essential for human communication. Iris users could be called [iridians](https://en.wiktionary.org/wiki/iridian).

### Iris Telegram group
Join the Iris.to telegram group: https://t.me/+u-qC51vCUWQ3NmRk

### Language options
If you would like to contribute to better translations, please [visit](https://docs.google.com/spreadsheets/d/19VSmmqqq5zpOcKIS2H8bHcVeG3Bby5aW8Q_4LykPUao/edit?usp=sharing).
