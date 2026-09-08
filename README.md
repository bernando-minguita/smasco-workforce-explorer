# 🏗️ SMASCO Workforce Explorer

[![Version](https://img.shields.io/badge/version-1.0-blue.svg)](https://github.com/yourusername/smasco-workforce-explorer)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Made with ❤️](https://img.shields.io/badge/Made%20with-❤️-red.svg)](https://github.com/yourusername/smasco-workforce-explorer)

> A powerful single‑page web application to explore, manage, and validate workforce data from SMASCO's API.

---

## 📖 Table of Contents

- [Overview](#-overview)
- [Features](#-features)
- [Tech Stack](#-tech-stack)
- [Getting Started](#-getting-started)
- [Usage](#-usage)
- [API Endpoints](#-api-endpoints)
- [Data Persistence](#-data-persistence)
- [Offline Mode](#-offline-mode)
- [Contributing](#-contributing)
- [License](#-license)

---

## 🧭 Overview

**SMASCO Workforce Explorer** is a client‑side dashboard that connects to SMASCO's backend services to retrieve contracts, projects, and worker details. It provides a clean interface for:

- Browsing all workforce data with advanced filtering and sorting.
- Drilling down into individual worker profiles with document expiry tracking.
- Generating payslips on‑demand via a one‑time access token.
- Validating document expiry and viewing status distributions.
- Exporting the full dataset to Excel.

All data is cached locally using IndexedDB, enabling offline access and fast reloads.

---

## ✨ Features

| Feature | Description |
|---------|-------------|
| 🔐 **Secure Authentication** | Log in using your SMASCO customer portal credentials. |
| 📂 **Project/Contract Tree** | Navigate your data hierarchy; collapse/expand contracts and projects. |
| 👷 **Worker Grid** | Sort, filter, and search workers by name, ID, passport, profession, etc. |
| 👤 **Worker Profile Modal** | View detailed personal, document, and project information. |
| 📄 **Payslip Lookup** | Select a worker and a period (year/month) to request and view payslips. |
| 🖨️ **Print Payslip** | Print or save a payslip as PDF from the viewer. |
| ✅ **Validation Dashboard** | Overview of expired/expiring documents and worker status distribution. |
| 📊 **Excel Export** | Generate a master Excel file of all filtered workers. |
| ⚡ **Parallel Extraction** | Multi‑threaded API fetching for faster data population. |
| 💾 **IndexedDB Cache** | All worker details and summaries are cached; refresh from cache or live API. |
| 📱 **Offline Support** | Service worker and cache provide basic offline functionality. |

---

## 🧰 Tech Stack

- **HTML5 / CSS3** – semantic markup, TailwindCSS for styling.
- **JavaScript (ES6+)** – Vanilla JS with async/await.
- **IndexedDB** – local persistence via a custom wrapper.
- **SheetJS (XLSX)** – Excel export.
- **jsPDF / html2canvas** – (optional for PDF export, currently uses print).
- **Lucide Icons** – beautiful icon set.
- **TailwindCSS** – utility‑first CSS framework.
- **Service Worker** – basic offline caching.

---

## 🚀 Getting Started

### Prerequisites

- A modern web browser (Chrome, Edge, Firefox, Safari).
- Valid SMASCO account credentials (username/password).

### Installation

This is a **single HTML file** – no build tools needed!

1. Clone this repository:
   ```bash
   git clone https://github.com/bernando-minguita/smasco-workforce-explorer.git
