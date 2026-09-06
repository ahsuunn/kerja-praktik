---
name: kp-assistant
description: >-
  Custom skill for writing, structuring, and updating the ITB Kerja Praktik
  report in LaTeX based on Paragon Technology and Innovation internship logs.
---

# Kerja Praktik LaTeX Writing Assistant

This skill provides guidelines and procedures for drafting academic LaTeX content for the Kerja Praktik (KP) report at ITB for PT Paragon Technology and Innovation.

## Daily Log Mapping Matrix

Use `context/log.txt` and `context/parapay.md` to map daily technical activities into report chapters:

| Week | Date Range | Primary Focus | Target Chapter |
| :--- | :--- | :--- | :--- |
| **Week 1** | 02–05 Juni 2026 | Onboarding HR, FATL team onboarding, VPN setup, system analysis | Bab I & Bab II |
| **Week 2** | 08–12 Juni 2026 | Save as Draft feature, FAR payment type disabling | Bab III (Fitur Save as Draft) |
| **Week 3** | 15–19 Juni 2026 | Revision Flow feature foundation & UI components | Bab III (Revision Flow v1) |
| **Week 4** | 22–26 Juni 2026 | Potong Tagihan feature, API integration, Warning modal | Bab III (Modul Potong Tagihan) |
| **Week 5** | 29 Juni – 03 Juli 2026 | Non-allocation lock, contiguous add payment, read-only mode for waiting admin | Bab III (Aturan Bisnis Revisi) |
| **Week 6** | 06–10 Juli 2026 | Major Refactoring to Revision v2, Setor Tunai flow, Customer grouping | Bab III (Arsitektur Revision v2) |
| **Week 7** | 13–17 Juli 2026 | Payment revision endpoints, Unallocated invoice handling, Date pickers | Bab III (Integrasi Endpoint Revisi) |
| **Week 8** | 20–24 Juli 2026 | Non-cash to cash constraints, IndexedDB proof caching, Infinite scroll | Bab III (Optimasi & IndexedDB) |
| **Week 9-10**| 27 Juli – 11 Aug 2026 | Final testing, bug fixing, documentation & handover | Bab III & Bab IV |

## LaTeX Writing Rules & Style Guidelines

1. **Academic Indonesian Tone:**
   - Use standard formal Indonesian (*Bahasa Indonesia Baku*).
   - Use passive/objective voice (e.g., *"Penulis melakukan pengembangan"* or *"Pengembangan fitur dilakukan"* instead of *"Saya buat"*).

2. **Foreign & Technical Term Formatting:**
   - Wrap English or software engineering terms in `\textit{...}` (e.g., `\textit{frontend}`, `\textit{refactoring}`, `\textit{endpoint}`, `\textit{draft}`).

3. **Cross-Referencing:**
   - Always reference figures and tables using `Gambar \ref{fig:...}` or `Tabel \ref{tab:...}`.
   - Use labels: `\label{fig:...}` placed after `\caption{...}`.

4. **Code & Interface Snippets:**
   - Format technical structures cleanly using LaTeX `verbatim` or `framed` blocks.
