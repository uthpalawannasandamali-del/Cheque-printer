# ASIAN LANKA — Cheque Printing & Management

Full-stack HNB cheque printing and handover system for the Kaduwela branch.

## Features

- Cheque editor with automatic LKR amount-in-words conversion
- Live 203 × 76 mm cheque preview and review-before-print confirmation
- Genuine pre-printed cheque and voucher output modes
- Millimetre field alignment and one-page calibration test print
- On-device cheque photo OCR with candidate confirmation
- Database-backed cheque register with search and duplicate-number checks
- Handover records with optional NIC, phone, invoice and signature
- Mouse, finger and stylus signature capture
- A4 PDF handover receipts with optional fields omitted when blank

## Run

```bash
npm install
npm run db:push
npm run dev
```

The app runs on port 3000. For production:

```bash
npm run build
npm start
```

Printer alignment is stored in the current browser because it is printer-specific. Cheque and handover records are stored in the configured MySQL database. Uploaded cheque photos remain on the current device. Captured signatures are embedded in the downloaded PDF; the database stores only whether a signature was captured.
