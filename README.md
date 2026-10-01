# Bryton Café – QR Menu

Customers scan a QR code → the menu opens in their phone browser (no app install).
Bilingual (ID / EN toggle), photos, prices, categories, search, sold-out labels.

| File | What it is |
|---|---|
| `index.html` | The customer menu (what the QR opens) |
| `menu.json` | All your menu data — items, prices, categories |
| `images/` | Food & drink photos (+ `logo.png`) |
| `editor.html` | Your editor: add / edit / remove items and photos |
| `qr.html` | Makes the printable QR code |
| `qrcode.js` | QR code library used by `qr.html` (MIT licence) |

---

## 1. One-time setup (about 10 minutes)

1. Sign in to **github.com** (use the `brytoncafbiz-ui` account).
2. **New repository** → name it `bryton-menu` → **Public** → **Create repository**.
3. Click **uploading an existing file** → drag in **all files and the `images` folder** from this zip → **Commit changes**.
4. Go to **Settings → Pages** → *Source*: **Deploy from a branch** → Branch: **main**, folder **/(root)** → **Save**.
5. After 1–2 minutes your menu is live at:
   **https://brytoncafbiz-ui.github.io/bryton-menu/**
6. (Optional) Upload your logo as `images/logo.png` (square image). Until then a "B" badge is shown.

## 2. Print the QR code

Open **https://brytoncafbiz-ui.github.io/bryton-menu/qr.html** → check the link → **Download PNG** (for your printer/vendor) or **Print**.
The QR never changes when you edit the menu — print it once.

## 3. Change the menu (anytime)

1. Open **https://brytoncafbiz-ui.github.io/bryton-menu/editor.html** (best on a laptop; works on a phone/tablet too).
2. Edit items:
   - **+ Add item** — name (ID/EN), description, category, price, photo
   - **Add photo** — pick a photo from your gallery; it's auto-resized for fast loading
   - **Options** — different prices like Hot / Iced, Regular / Large
   - **Available** untick → shows "Habis / Sold out" (good for today only)
   - **Hide from menu** → removes it from the menu without deleting
   - **Delete item** → removes permanently
   - Tags: Best seller / New / Spicy
3. Tap **Download changes** → you get `menu.json` + any new photos.
4. On GitHub, in the `bryton-menu` repository:
   - Open the **images** folder → **Add file → Upload files** → add the new photos → **Commit changes**
   - Go back to the main folder → **Add file → Upload files** → add `menu.json` → **Commit changes**
5. Wait ~1 minute and refresh the menu on your phone.

Tip: the editor keeps your unsaved edits as a draft in that browser. Photos you added but haven't downloaded are lost if you close the page, so download before closing.

## Notes

- Prices are whole Rupiah numbers in `menu.json` (e.g. `25000`), shown as **Rp 25.000**.
- The editor page is public but harmless: it can't change the live menu — only a GitHub upload can.
- Best photo shape: square or 4:3, food in the centre.
