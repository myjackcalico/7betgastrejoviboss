# Boss's Day gift reveal

A static, single-page site, so no build step or framework is needed.

## Structure

```
index.html        page, styles and scripts
assets/           song, ticket images and the ticket PDF
vercel.json       adds an X-Robots-Tag: noindex header to every file
```

## Deploy to Vercel

1. Create a **private** GitHub repository. It contains real tickets and a copyrighted song.
2. Push these files to it:
   ```
   git init
   git add .
   git commit -m "Gift reveal"
   git branch -M main
   git remote add origin https://github.com/<you>/<repo>.git
   git push -u origin main
   ```
3. In Vercel choose **Add New → Project**, import the repository, and keep:
   - Framework Preset: **Other**
   - Build Command: *(empty)*
   - Output Directory: *(empty / root)*
4. Click **Deploy**.

## Personalising the link

Append names to the URL (boss's name in the vocative case):

```
https://<your-project>.vercel.app/?boss=Jovita&from=Pardavim%C5%B3%20skyrius
```

## Privacy

- `<meta name="robots">` tags and the `X-Robots-Tag` header ask search engines not to index the page or its files.
- This keeps the page out of search results, but anyone who has the link can still open it. Share the link only with the recipient.

## Autoplay

The page tries to start the song as soon as it loads. Chrome only allows that if the visitor has interacted with the site before. Otherwise the song starts on the first tap, click or key press anywhere on the page.
