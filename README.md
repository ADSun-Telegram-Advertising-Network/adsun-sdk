# Adsun SDK — Telegram Mini App Ads

[Adsun](https://adsun.io) is a Telegram advertising network for Mini Apps, bots and channels.
This SDK lets you monetize a Telegram Mini App with **rewarded video**, **interstitial** and **task** ads.

- ⚡ One script tag, no build step
- 🎁 Rewarded ads with server-side Reward URL (fraud-safe)
- 🖥 Interstitial (full-screen) ads at natural breaks
- ✅ Task ads for Telegram channels, bots and apps
- 📊 Real-time stats in the Adsun publisher panel
- 🌍 Global demand: 15M+ daily impressions, 213 countries
- React, Vue, Unity (WebGL) and vanilla JS examples

## Quick start

```html
<script src="https://api.adsun.io/sdk.js"></script>
<script>
  const ad = Adsun.init({ blockId: "YOUR_BLOCK_ID" });
  ad.addEventListener("onReward", () => refreshRewardState());
  ad.show().catch(() => restoreApp());
</script>
```

1. Sign up as a publisher at https://adsun.io/register?type=partner
2. Add your Mini App and create an ad block
3. Copy the block ID into `Adsun.init`
4. Set a Reward URL on your server to grant rewards

## Telegram bot ads

Show native ad messages inside your bot:

```
GET https://api.adsun.io/advbot?tgid={USER_ID}&blockid={BLOCK_ID}&language={LANG}&token={TOKEN}
```

Returns `text_html`, `click_url`, `button_name`, `image_url` — send with `parse_mode=HTML`.

## FAQ

**What is Adsun?** A Telegram ad network that connects Mini App, bot and channel publishers with advertisers.
**Is Adsun an AdsGram alternative?** Yes — Adsun supports rewarded, interstitial, task and bot ads for Telegram, with an AdsGram-style bot endpoint.
**Which frameworks are supported?** Any web Mini App: vanilla JS, React, Vue, Unity WebGL.

## Links
- Website: https://adsun.io
- Monetization guide: https://adsun.io/telegram-mini-app-monetization
- Advertiser guide: https://adsun.io/how-to-advertise-on-telegram
