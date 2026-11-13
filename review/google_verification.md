# PostAll – Google OAuth verification (YouTube)

## OAuth consent screen (Branding)
- App name: PostAll
- User support email: (his Gmail – choose in dropdown)
- App logo: review/icon.png (120x120)
- App home page: https://postall.cryptohunter2009.com/
- Privacy policy: https://postall.cryptohunter2009.com/privacy.html
- Terms of service: https://postall.cryptohunter2009.com/terms.html
- Authorized domain: cryptohunter2009.com  (verify in Search Console – google9d35954e473ae6d8.html is already in the site)
- Developer contact email: (his Gmail)

## OAuth client (Web application)
- Authorized redirect URI to ADD: https://postall.cryptohunter2009.com/oauth/youtube.html
- After adding it: set app_settings.google_redirect_uri = that URL (Supabase), so the server uses it.

## Scopes and justification
**https://www.googleapis.com/auth/youtube.upload**
PostAll is a one-click social media publishing tool. The user writes one caption, picks a video, ticks the platforms (YouTube, Facebook, Instagram, TikTok) and clicks "Post to All". PostAll uses youtube.upload only to upload that video, with the user's title/description, to the YouTube channel the user connected, and only when the user clicks "Post to All". PostAll never uploads anything on its own and never edits or deletes existing videos.

**https://www.googleapis.com/auth/youtube.readonly**
Used once right after the user connects, to call channels.list (mine=true) and read the channel id and title. PostAll shows the channel name under Accounts → Connected and in "Where to post" so the user can see which channel the video will go to. No other YouTube data is read or stored.

Why narrower scopes are not enough: there is no narrower scope for uploading videos than youtube.upload, and channels.list(mine=true) needs youtube.readonly to show the user which channel is connected.

## Demo video (record on laptop after branding is saved, ~2 min, English UI, unlisted on YouTube)
1. Open https://postall.cryptohunter2009.com/ and log in.
2. Accounts → YouTube → Connect.
3. Google screen: choose account/channel. Keep the address bar visible so the client_id is readable. The consent screen must say "PostAll" and list both YouTube permissions.
4. Allow → back in PostAll, the channel appears under Connected (this is youtube.readonly).
5. Post tab → pick a short video → caption → tick only the YouTube channel → Post to All.
6. Show "Posted" in PostAll, then open YouTube Studio and show the uploaded video (this is youtube.upload).
7. Accounts → Remove the YouTube connection (shows the user can disconnect).

## Meta backup: business_management video (only if Meta rejects it)
1. Facebook Login screen → "Continue as …" → on the business step, choose the business portfolio "Islamic Motivational Videos".
2. Select the Pages that belong to that business portfolio → Save.
3. Back in PostAll, show that those business-owned Pages appear under Connected.
4. Post to one of those business Pages and open the Page to show the post.
Note for reviewer: "These Pages are owned by a business portfolio; they are only returned to PostAll through business_management. PostAll does not change any business settings."
