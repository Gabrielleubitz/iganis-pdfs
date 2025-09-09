<p align="center">
<svg width="80" height="80" viewBox="0 0 100 100" xmlns="http://www.w3.org/2000/svg">
  <defs>
    <mask id="leftSlotMask">
      <rect x="0" y="0" width="100" height="100" fill="#fff"/>
      <rect x="35" y="18" width="6" height="20" rx="3" fill="#000"/>
    </mask>
    <mask id="rightSlotMask">
      <rect x="0" y="0" width="100" height="100" fill="#fff"/>
      <rect x="57" y="60" width="6" height="20" rx="3" fill="#000"/>
    </mask>
  </defs>
  <ellipse cx="50" cy="52" rx="44" ry="34" fill="#0F2D44" transform="rotate(-18 50 52)"/>
  <rect x="30" y="10" width="18" height="80" rx="6" fill="#86B7FF" mask="url(#leftSlotMask)"/>
  <rect x="52" y="6"  width="18" height="86" rx="6" fill="#5B93E6" mask="url(#rightSlotMask)"/>
</svg>
</p>
<h1 align="center">Iganis PDFs</h1>

A robust, locally hosted web-based PDF manipulation tool using Docker. It enables you to carry out various operations on PDF files, including splitting, merging, converting, reorganizing, adding images, rotating, compressing, and more. This locally hosted web application has evolved to encompass a comprehensive set of features, addressing all your PDF requirements.

All files and PDFs exist either exclusively on the client side, reside in server memory only during task execution, or temporarily reside in a file solely for the execution of the task. Any file downloaded by the user will have been deleted from the server by that point.

![stirling-home](images/stirling-home.jpg)

## Features

- 50+ PDF Operations
- Parallel file processing and downloads
- Dark mode support
- Custom download options
- Custom 'Pipelines' to run multiple features in a automated queue
- API for integration with external scripts
- Optional Login and Authentication support (see [here](https://docs.iganipdf.com/Advanced%20Configuration/System%20and%20Security) for documentation)
- Database Backup and Import (see [here](https://docs.iganipdf.com/Advanced%20Configuration/DATABASE) for documentation)
- Enterprise features like SSO (see [here](https://docs.iganipdf.com/Advanced%20Configuration/Single%20Sign-On%20Configuration) for documentation)

## PDF Features

### Page Operations

- View and modify PDFs - View multi-page PDFs with custom viewing, sorting, and searching. Plus, on-page edit features like annotating, drawing, and adding text and images. (Using PDF.js with Joxit and Liberation fonts)
- Full interactive GUI for merging/splitting/rotating/moving PDFs and their pages
- Merge multiple PDFs into a single resultant file
- Split PDFs into multiple files at specified page numbers or extract all pages as individual files
- Reorganize PDF pages into different orders
- Rotate PDFs in 90-degree increments
- Remove pages
- Multi-page layout (format PDFs into a multi-paged page)
- Scale page contents size by set percentage
- Adjust contrast
- Crop PDF
- Auto-split PDF (with physically scanned page dividers)
- Extract page(s)
- Convert PDF to a single page
- Overlay PDFs on top of each other
- PDF to a single page
- Split PDF by sections

### Conversion Operations

- Convert PDFs to and from images
- Convert any common file to PDF (using LibreOffice)
- Convert PDF to Word/PowerPoint/others (using LibreOffice)
- Convert HTML to PDF
- Convert PDF to XML
- Convert PDF to CSV
- URL to PDF
- Markdown to PDF

### Security & Permissions

- Add and remove passwords
- Change/set PDF permissions
- Add watermark(s)
- Certify/sign PDFs
- Sanitize PDFs
- Auto-redact text

### Other Operations

- Add/generate/write signatures
- Split by Size or PDF
- Repair PDFs
- Detect and remove blank pages
- Compare two PDFs and show differences in text
- Add images to PDFs
- Compress PDFs to decrease their filesize (using qpdf)
- Extract images from PDF
- Remove images from PDF
- Extract images from scans
- Remove annotations
- Add page numbers
- Auto-rename files by detecting PDF header text
- OCR on PDF (using Tesseract OCR)
- PDF/A conversion (using LibreOffice)
- Edit metadata
- Flatten PDFs
- Get all information on a PDF to view or export as JSON
- Show/detect embedded JavaScript




# 📖 Get Started

Follow the installation instructions in this repository to get started with the PDF tool.


## Supported Languages

IGANI-PDF currently supports 40 languages!

| Language                                     | Progress                               |
| -------------------------------------------- | -------------------------------------- |
| Arabic (العربية) (ar_AR)                        | ![61%](https://geps.dev/progress/61)   |
| Azerbaijani (Azərbaycan Dili) (az_AZ)        | ![62%](https://geps.dev/progress/62)   |
| Basque (Euskara) (eu_ES)                     | ![36%](https://geps.dev/progress/36)   |
| Bulgarian (Български) (bg_BG)                | ![68%](https://geps.dev/progress/68)   |
| Catalan (Català) (ca_CA)                     | ![67%](https://geps.dev/progress/67)   |
| Croatian (Hrvatski) (hr_HR)                  | ![60%](https://geps.dev/progress/60)   |
| Czech (Česky) (cs_CZ)                        | ![69%](https://geps.dev/progress/69)   |
| Danish (Dansk) (da_DK)                       | ![61%](https://geps.dev/progress/61)   |
| Dutch (Nederlands) (nl_NL)                   | ![60%](https://geps.dev/progress/60)   |
| English (English) (en_GB)                    | ![100%](https://geps.dev/progress/100) |
| English (US) (en_US)                         | ![100%](https://geps.dev/progress/100) |
| French (Français) (fr_FR)                    | ![88%](https://geps.dev/progress/88)   |
| German (Deutsch) (de_DE)                     | ![97%](https://geps.dev/progress/97)   |
| Greek (Ελληνικά) (el_GR)                     | ![67%](https://geps.dev/progress/67)   |
| Hindi (हिंदी) (hi_IN)                          | ![67%](https://geps.dev/progress/67)   |
| Hungarian (Magyar) (hu_HU)                   | ![99%](https://geps.dev/progress/99)   |
| Indonesian (Bahasa Indonesia) (id_ID)        | ![62%](https://geps.dev/progress/62)   |
| Irish (Gaeilge) (ga_IE)                      | ![68%](https://geps.dev/progress/68)   |
| Italian (Italiano) (it_IT)                   | ![98%](https://geps.dev/progress/98)   |
| Japanese (日本語) (ja_JP)                    | ![92%](https://geps.dev/progress/92)   |
| Korean (한국어) (ko_KR)                      | ![67%](https://geps.dev/progress/67)   |
| Norwegian (Norsk) (no_NB)                    | ![66%](https://geps.dev/progress/66)   |
| Persian (فارسی) (fa_IR)                      | ![64%](https://geps.dev/progress/64)   |
| Polish (Polski) (pl_PL)                      | ![72%](https://geps.dev/progress/72)   |
| Portuguese (Português) (pt_PT)               | ![68%](https://geps.dev/progress/68)   |
| Portuguese Brazilian (Português) (pt_BR)     | ![76%](https://geps.dev/progress/76)   |
| Romanian (Română) (ro_RO)                    | ![57%](https://geps.dev/progress/57)   |
| Russian (Русский) (ru_RU)                    | ![88%](https://geps.dev/progress/88)   |
| Serbian Latin alphabet (Srpski) (sr_LATN_RS) | ![94%](https://geps.dev/progress/94)   |
| Simplified Chinese (简体中文) (zh_CN)         | ![93%](https://geps.dev/progress/93)   |
| Slovakian (Slovensky) (sk_SK)                | ![51%](https://geps.dev/progress/51)   |
| Slovenian (Slovenščina) (sl_SI)              | ![71%](https://geps.dev/progress/71)   |
| Spanish (Español) (es_ES)                    | ![74%](https://geps.dev/progress/74)   |
| Swedish (Svenska) (sv_SE)                    | ![65%](https://geps.dev/progress/65)   |
| Thai (ไทย) (th_TH)                           | ![59%](https://geps.dev/progress/59)   |
| Tibetan (བོད་ཡིག་) (bo_CN)                     | ![65%](https://geps.dev/progress/65) |
| Traditional Chinese (繁體中文) (zh_TW)        | ![99%](https://geps.dev/progress/99)   |
| Turkish (Türkçe) (tr_TR)                     | ![99%](https://geps.dev/progress/99)   |
| Ukrainian (Українська) (uk_UA)               | ![70%](https://geps.dev/progress/70)   |
| Vietnamese (Tiếng Việt) (vi_VN)              | ![57%](https://geps.dev/progress/57)   |
| Malayalam (മലയാളം) (ml_IN)              | ![73%](https://geps.dev/progress/73)   |

## 🤝 Contributing

- [Contribution Guidelines](CONTRIBUTING.md)
- [Translation Guide (How to add custom languages)](devGuide/HowToAddNewLanguage.md)
- [Developer Guide](devGuide/DeveloperGuide.md)
