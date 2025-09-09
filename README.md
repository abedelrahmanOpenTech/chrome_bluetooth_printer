# BLE Printer Demo - Fixed Solution

A web-based demo to **scan, connect, and print** text or HTML elements as images using **Bluetooth Low Energy (BLE) thermal printers**. Fully runs in the browser using **Web Bluetooth API** and **ESC/POS commands**.

---

## Features

- **Scan for BLE printers** with common name prefixes (`GT`, `PRT`, `BT`, `Printer`).
- **Connect** to a printer and find writable characteristics automatically.
- **Print text**:
  - Bold text
  - Centered or left-aligned
  - Line feeds
- **Print HTML div as image**:
  - Converts div to canvas using `html2canvas`
  - Converts canvas to **monochrome ESC/POS bytes**
  - Sends data to the printer in chunks
- **Live status updates** (info, connected, error)

---

## Demo Layout

1. **Header** – Title and subtitle.
2. **Video Preview** – Demo video embedded.
3. **Controls** – Scan printers, print text, print div.
4. **Printer List** – Discovered BLE printers (click to connect).
5. **Preview Div** – Div content to print as image.
6. **Status Box** – Shows current status of printer actions.

---

## How to Use

1. Open the demo in a **BLE-compatible browser** (Chrome desktop/Android).
2. Click **Scan Printers** and allow Bluetooth access.
3. Click a printer from the list to **connect**.
4. After connecting:
   - **Print Text** prints sample text.
   - **Print Div as Image** prints the div content as an image.

---

## Dependencies

- [html2canvas](https://html2canvas.hertzen.com/) (v1.4.1) – Converts divs to canvas.

```html
<script src="https://cdn.jsdelivr.net/npm/html2canvas@1.4.1/dist/html2canvas.min.js"></script>
