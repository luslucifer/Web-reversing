# Soaper Scraping Guide

Scraping Soaper is as straightforward as it gets—it almost feels like it's inviting us to do it! Let me walk you through how to scrape Soaper step-by-step. 🎯

Our target: **[Soaper](https://soaper.live/)**

----------

## Scraping Steps

### Step 1: Pick Your Page

Open any movie or TV series page. For this example, we’re scraping the following page:

```bash
https://soaper.live/movie_1rGplMrG87.html  

```

----------

### Step 2: Open DevTools

Fire up **Librewolf** (or any browser) and open the **DevTools** (Ctrl+Shift+I or right-click > Inspect).  
Go to the **Network tab**. If no requests are visible, refresh the page. Your Network tab should look like this:

![Open DevTools](https://raw.githubusercontent.com/luslucifer/Web-reversing/main/images/openDevTools.png)

----------

### Step 3: Inspect Responses

Check the response of the URLs under the **Network tab**. You’ll eventually find one returning an `.m3u8` file—our treasure! 🗺️

![Look for URLs](https://raw.githubusercontent.com/luslucifer/Web-reversing/main/images/lookUrls.png)

----------

### Step 4: Copy Headers

Once you find the request, right-click and copy **all headers**.

![Copy Headers](https://raw.githubusercontent.com/luslucifer/Web-reversing/main/images/copyAllHeaders.png)

----------

### Step 5: Extract the Payload

Since it’s a POST request, you’ll also need the payload. Grab it from the **Request section**.

![Copy Payload](https://raw.githubusercontent.com/luslucifer/Web-reversing/main/images/copyPayload.png)

----------

### Step 6: Use ChatGPT to Mimic the Request

Now, paste the headers, URL, and payload into ChatGPT and ask it to mimic the request in `curl`.

![Paste into ChatGPT](https://raw.githubusercontent.com/luslucifer/Web-reversing/main/images/pasteInChatgpt.png)

----------

### Step 7: Test the `curl`

Copy the `curl` command ChatGPT provides and use it in **Postman** or **ThunderClient**. When you send the request, you’ll likely get a compressed encoded response—don’t worry, it’s not encrypted.

![Request with Accept-Encoding](https://raw.githubusercontent.com/luslucifer/Web-reversing/main/images/requesWithAcceptEncodeing.png)

----------

### Step 8: Disable `Accept-Encoding`

Remove the `Accept-Encoding` header from the request and resend it. This time, you’ll get clean, uncompressed data.

![Disable Accept-Encoding](https://raw.githubusercontent.com/luslucifer/Web-reversing/main/images/diableIngAcceptEncoding.png)

----------

### Step 9: Winner Winner Chicken Dinner ! 🎉

Congratulations, you’ve successfully scraped Soaper! Enjoy your decoded response.

![Winner Winner Chicken Dinner](https://raw.githubusercontent.com/luslucifer/Web-reversing/main/images/winer_winer_chicken_dinner.png)

----------

## Stay Connected

Got questions or want to share your progress? We’ve got you covered:

-   **[Join us on Discord](https://discord.gg/aAPmfsRD)**
-   **[Chat on Telegram](https://t.me/vidjoy)**

Let’s keep scraping fun, educational, and super rewarding! 🚀