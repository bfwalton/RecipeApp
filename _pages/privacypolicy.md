---
layout: page
permalink: /privacypolicy/
title: Privacy Policy
heading: Privacy policy
seo_title: "Saucier Privacy Policy — No Accounts, No Tracking"
description: "Saucier has no account, analytics or server. Recipes sync through your iCloud; optional USDA nutrition lookups send ingredient names directly to USDA."
updated: 10 October 2026
lead: >-
  The short version: Saucier has no server, account or analytics. Your recipes
  stay on your device and, if enabled, in your own iCloud. Optional USDA
  nutrition lookups send ingredient names directly to USDA.
---

## 1. Who this covers

This policy covers the Saucier app for iPhone and iPad and this website.
Saucier is made by {{ site.author }}. Questions go to
[{{ site.support_email }}](mailto:{{ site.support_email }}).

## 2. What Saucier collects

**Nothing.**

Saucier contains no analytics SDK, no advertising network, no crash-reporting
service and no third-party tracking of any kind. There is no Saucier account, so
you are never asked for an email address, a name or a password.

Saucier operates no server. There is no database holding your recipes, because
there is nowhere for one to be.

## 3. Where your recipes live

Your recipes, photos, notes and categories are stored **on your device**.

If you have iCloud enabled, they also sync through **your own private iCloud
account**, using Apple's CloudKit. That data is held in your personal iCloud
storage, governed by
[Apple's privacy policy](https://www.apple.com/legal/privacy/). Saucier cannot
read it. Neither can anyone else operating Saucier, because no such facility
exists.

If you use iCloud sharing to share a recipe with someone, that recipe is
accessible to the people you share it with, through Apple's sharing mechanism.

Your active cooking timers and weekly meal plan are stored on the device where
you use them. The meal plan does not currently sync over iCloud.

## 4. The on-device assistant

Ask Saucier is built on **Apple Intelligence's on-device foundation model**. Your
questions, your recipes and the answers are processed on your device and are not
transmitted to Saucier or to any third party.

## 5. Nutrition estimates

The default nutrition source uses Apple Intelligence on your device. Its
ingredient lookups and estimates do not leave the device.

If you choose **USDA FoodData Central** instead, Saucier sends each ingredient
name as a search term, along with your FoodData Central API key or the shared
demo key, directly from your device to USDA. It does not send the full recipe,
your notes or your Saucier library. USDA will receive the ordinary network
information associated with that request, such as your IP address. Your chosen
source and any API key you enter are stored in the app's local settings.

## 6. Permissions Saucier may ask for

Each is optional, requested only when you use the feature it belongs to, and
refusing it only disables that feature.

| Permission | Why | Where the data goes |
|---|---|---|
| **Microphone** | To hear a question you ask out loud while cooking | Processed for speech recognition, then discarded. Not stored or transmitted by Saucier. |
| **Speech Recognition** | To turn what you said into text | Uses Apple's Speech framework. Saucier requests on-device recognition wherever your device supports it. Where it does not, iOS may process the audio on Apple's servers under Apple's privacy policy. |
| **Reminders** | To add ingredients to your grocery list | Written to your Reminders app on your device and in your iCloud. Saucier does not read your other reminders. |
| **Notifications** | To tell you when a cooking timer finishes | Scheduled locally on your device. No push server is involved. |
| **Photos** | To let you choose a photo for a recipe | The image you pick is stored with the recipe on your device. |
| **Contacts** | To show the photo of a person you have shared a recipe with | Read on your device for display only. Never transmitted. |

## 7. Network requests Saucier makes

Saucier contacts the internet when you save or reload a recipe from a web
address. Your device fetches that page directly from the site in question,
which sees the request as it would a browser visit. It also contacts USDA if
you choose FoodData Central as your nutrition source, as described above.

Saucier does not route these requests through any server of its own, because
there isn't one.

## 8. This website

This site is hosted on **GitHub Pages**. It sets no cookies, runs no analytics
and embeds no third-party trackers. GitHub may log standard server information
such as IP addresses as part of serving the site; see
[GitHub's privacy statement](https://docs.github.com/site-policy/privacy-policies/github-privacy-statement).

The App Store download button links to Apple's App Store, which has
[its own privacy policy](https://www.apple.com/legal/privacy/).

## 9. Children

Saucier is not directed at children under 13 and collects no personal
information from anyone, including children.

## 10. Your rights

Because Saucier holds no data about you, there is nothing to request, correct or
delete from us. Your own copies are under your control at all times:

- Export your entire library to a `.sauce` file from Settings.
- Delete the app to remove its local data from a device.
- Manage or delete its iCloud data from **Settings → Apple Account → iCloud**.

## 11. Changes to this policy

If this policy changes, the date at the top of this page changes with it, and
the change will be noted in the app's [release notes]({{ '/changelog/' | relative_url }}).
Any future addition of analytics would be announced there rather than introduced
quietly.

## 12. Contact

[{{ site.support_email }}](mailto:{{ site.support_email }})
