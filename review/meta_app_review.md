# PostAll – Meta App Review text

App: PostAll (29547148994889321) – https://ranaadnan42.github.io/postall/

## Reviewer instructions (test steps)
1. Open https://ranaadnan42.github.io/postall/ and log in with the PostAll test account (credentials in the "test credentials" field).
2. Open the "Accounts" tab and click "Connect" under Facebook + Instagram. Complete Facebook Login for Business and allow the requested permissions.
3. The connected Facebook Pages and linked Instagram professional accounts appear under "Connected".
4. Open the "Post" tab, select a photo or video, write a caption, tick one or more Facebook Pages / Instagram accounts under "Where to post", and click "Post to All".
5. The post is published to the selected Page(s) and Instagram account(s). The "History" tab shows the result for each destination.

## Permission usage

**pages_show_list** – After the user connects Facebook, PostAll lists the Pages the user manages so the user can choose which Pages to post to. Shown in Accounts → Connected and in Post → "Where to post".

**pages_manage_posts** – PostAll publishes the photo/video and caption the user creates in the app to the Facebook Pages the user selects, only when the user clicks "Post to All".

**pages_read_engagement** – Required with pages_manage_posts to read the Page details (name, id, Page access token) and confirm the published post so PostAll can show its status in History.

**business_management** – Pages owned by a business portfolio are only returned through business assets; PostAll uses it to list and post to the Pages the user manages through their business portfolio. PostAll does not change any business settings.

**instagram_basic** – Reads the Instagram professional account linked to the user's Page (username and id) so the user can choose it as a posting destination.

**instagram_content_publish** – Publishes the user's photo/video and caption as a post/Reel to the Instagram professional account the user selects, only when the user clicks "Post to All".

**public_profile** – Shows the name of the connected Facebook user in the Accounts tab so the user knows which account is connected.

## Data handling
- Data processors / service providers: Supabase (database and server functions hosting).
- Purpose: only to provide the posting service the user requests.
- Data is not sold or shared with third parties; not used for ads.
- Users can disconnect accounts (Accounts → Remove) and request deletion: https://ranaadnan42.github.io/postall/privacy.html
- Responsible entity: Islamic Motivational Videos (verified business portfolio), Pakistan.
- No requests from public authorities for user data in the past 12 months.
