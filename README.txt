PRETTY BELISS WEBSITE – HOW TO PUBLISH
1. Open index.html in a text editor. Near the bottom find SHEET_CSV_URL and paste the Google Sheet "published CSV" link between the quotes.
2. Upload this folder to a new GitHub repo (Add file > Upload files).
3. In Vercel: Add New > Project > Import that repo > Deploy.
4. Domain: Vercel project > Settings > Domains > add prettybeliscosmetics.com, then copy the DNS values Vercel shows into GoDaddy DNS.
Sheet headings used: Name, Shade, In stock, Qty, Price, MRP, Category, Dupe of, Type, Photo.

EDITING THE SITE DESIGN
- Moving top bar: search for "LINE 1 : moving tag bar" in index.html. Each <span> is one tag.
- Offer banners: search for "BIG OFFER SCREEN". There are 3 slides; edit the heading, paragraph, button text and the
  "10% OFF" line in each <article class="hsSlide">. Keep one <i> per slide inside #hsDots.
- Header quick links: search for "essential jump links". Change the link text/hrefs there.
- Story note (under the offer slides): search for "STORY NOTE". Edit the text in .dnText, the tagline in
  .dnTag, and the flower strip in .dnTop.
- Product reels (the moving video row above the shop): search for "PRODUCT REELS" in the script and fill the
  REELS list. Each line is one tile:
    title   = short caption shown on the cover
    src     = your Instagram reel link (YouTube or a direct .mp4 link also work)
    poster  = the cover picture; the four current covers live in the reels/ folder (reel-1.jpg ... reel-4.jpg) —
              replace a file with your own picture of the same name, or point poster at a new image
    product = exact product name from the sheet that the tile should open. Leave it blank and clicking the
              tile scrolls to the shop and shows a small note offering to find that piece on WhatsApp instead
              (it never opens a random product).
  The row moves on its own (one card every ~3 seconds, loops, pauses when the mouse is over it) and clicking
  a tile jumps straight to that product's page. Add a fifth/sixth line to the list for more tiles; the row
  shows the list twice so the loop stays seamless.
- Flowers: the big rotating blooms come from the mini <svg><use href="#bloom"> symbol right after <body>
  (edit that one shape to change every flower on the site). The <div class="hsDeco"> line inside each offer
  slide adds the two corner blooms and the falling petals; the .bloom lines inside the story note and the
  footer add theirs. Delete a line to remove that flower, or change the colours in the .bloom / .dn .bloom /
  footer .fbloom rules.
- Three-dot side menu: search for "SIDE QUICK MENU". Each <a href="#..."> is one jump link (shop, offers,
  about us, how to order, FAQs, contact us, WhatsApp support).
- Colours: edit the CSS variables at the top of the <style> block (--burgundy, --mauve, --gold, --blush...).
- Fonts: the Google Fonts link in <head> uses Cormorant Garamond (headings) and Jost (body text).
