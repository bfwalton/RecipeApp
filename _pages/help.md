---
layout: page
permalink: /help/
title: Help & Support
heading: Help and support
seo_title: "Saucier Support — Help With Saving, Sync and Importing"
description: "Support for Saucier on iPhone and iPad: fixes for saving recipes, iCloud sync, Ask Saucier, timers and importing — plus how to get in touch."
lead: >-
  One person answers this inbox, usually within a couple of days.
  <a href="mailto:help@saucier-app.com">help@saucier-app.com</a>
---

## Get in touch

Email **[{{ site.support_email }}](mailto:{{ site.support_email }})** with the
problem, your device, and your iOS version. A screenshot helps more than almost
anything else.

Bug reports, feature requests and "this is confusing and here is why" are all
genuinely welcome — Saucier is a side project, and what people write in is what
decides the next thing built.

## Common problems

### A recipe saved with missing or wrong ingredients

Some pages publish messy recipe data, and some publish none at all. Two things
to try:

1. Open the recipe, tap **Edit**, and fix the lines by hand. Saucier re-reads
   edited ingredient lines, so corrected amounts still scale and convert
   properly.
2. Use **Reload from Website** on the recipe. If the site has since fixed its
   page, this pulls a fresh copy.

If a particular site is consistently wrong, send the link — those are the
reports that improve the parser for everyone.

### Nothing happens when I share a page to Saucier

Check that Saucier is enabled in the share sheet: tap **Share**, scroll the row
of apps to the end, tap **More**, and make sure Saucier is switched on. You can
drag it up the list while you are there.

As a fallback, copy the link and open Saucier — it offers to save a recipe link
it finds on your clipboard.

### My recipes are not syncing between devices

Saucier syncs through your own iCloud account, so:

- Both devices must be signed in to **the same Apple Account**.
- **iCloud Drive** must be on in Settings.
- Saucier must be allowed to use iCloud in **Settings → Apple Account → iCloud**.
- Sync needs a connection on both devices, and is not instant — give it a minute
  on a good network.

### I cannot find the Ask Saucier button

Ask Saucier needs Apple Intelligence available and switched on for your device
and region. Saucier deliberately hides the button when the model is unavailable,
because a chat that cannot answer is worse than no chat.

Check **Settings → Apple Intelligence & Siri**. If you have just turned it on,
the model assets may still be downloading; Saucier picks that up next time you
return to the app.

### Voice does not hear me

Voice needs two permissions — **Microphone** and **Speech Recognition** — in
**Settings → Saucier**. If either was declined, the microphone button stays
visible but cannot do anything, so Saucier shows the reason on screen next to
it.

### A timer did not go off

Timers fire as notifications, so Saucier needs **Notifications** allowed in
**Settings → Saucier**. Check that Focus or a Sleep schedule is not silencing
them, and that **Time Sensitive** notifications are permitted.

Timers do not survive the app being force-quit from the app switcher.

### Ingredients are not reaching my grocery list

Saucier writes to the **Reminders** app, so it needs full Reminders access in
**Settings → Saucier**. Ingredients go to your grocery list in Reminders rather
than to a list inside Saucier.

### An import did not work

Saucier reads Paprika's `.paprikarecipes` and `.paprikarecipe` exports and its
own `.sauce` files, and identifies them by their contents rather than their
extension. If a file is rejected, it is genuinely not one of those formats —
send it over and it can be looked at.

[More about importing →]({{ '/import-recipes/' | relative_url }})

## Getting your data out

Your recipes are yours and are not held anywhere you cannot reach:

- **Settings → Export** writes your whole library to a `.sauce` file.
- Any single recipe can be shared as a file or as its original link.
- Everything is stored on your device and in your own iCloud account.

## More

- [Frequently asked questions]({{ '/FAQ/' | relative_url }})
- [What's new]({{ '/changelog/' | relative_url }})
- [Privacy policy]({{ '/privacypolicy/' | relative_url }})
- [Terms of service]({{ '/termsofservice/' | relative_url }})
