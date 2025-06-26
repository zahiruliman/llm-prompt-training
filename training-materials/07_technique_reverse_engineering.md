## Technique 6: Reverse Engineering Document Styles

### 6.1. Concept

This advanced technique involves teaching the AI a document's entire stylistic and structural format. You provide a complete example document as a "style template." The AI reverse-engineers its structure—headings, paragraph styles, list formats, table designs, and other text-based features. You can then provide new, unrelated content and instruct the AI to generate a new document that matches the *style* of the original template.

### 6.2. Rationale

Analysts and project managers often need to create new documents (e.g., an SKB) that must match the look and feel of a different, existing document (e.g., a formal project proposal). Describing this style is nearly impossible. This technique allows you to say, "Here is a sample of what our formal documents look like. Now, take my raw notes about business requirements and write a new SKB that follows this exact style." It separates content from presentation, allowing you to generate professional, consistently formatted documents for any purpose.

### 6.3. Step-by-Step Workflow

1.  **Isolate the Style Template:** Copy the full text of a well-formatted document that represents the style you want to replicate. This document should be complete, with headings, lists, tables, etc.
2.  **Create the Master Prompt:** Structure a prompt with two main parts:
    *   **The Style Template:** Paste the copied document text, clearly enclosed in markers like `<style_template> ... </style_template>`.
    *   **The New Content:** Provide the new, raw information for the new document, enclosed in markers like `<new_content> ... </new_content>`.
3.  **Give a Clear Instruction:** Explicitly instruct the AI to "generate a new document using the provided new content, but format it strictly according to the structure and style found in the style template."

### 6.4. Example: Using a Project Proposal's Style to Draft an SKB

**Objective:** To use the formal style of an existing "Project Proposal" document to draft a new "Spesifikasi Keperluan Bisnes (SKB)" from raw notes.

**The Master Prompt:**

```
You are a Senior Business Analyst. Your task is to create a formal Spesifikasi Keperluan Bisnes (SKB) document.

First, carefully analyze the document style provided in the `<style_template>` tags. Pay attention to the use of a main title, numbered main sections (1.0, 2.0), lettered subsections (A, B), bullet points for lists, and the structure of tables.

Then, take the raw notes from the `<new_content>` tags and generate a new SKB document that strictly follows the style and structure of the template.

<style_template>
# PROPOSAL PROJEK: SISTEM E-CUTI

**TARIKH:** 1 Ogos 2023
**DOKUMEN NO:** JPM/PRO/2023/07

## 1.0 PENGENALAN

Ini adalah cadangan untuk membangunkan Sistem E-Cuti bagi menggantikan proses permohonan cuti secara manual.

A. Latar Belakang Masalah
- Proses sedia ada menggunakan borang kertas yang tidak efisien.
- Tiada sistem berpusat untuk menjejaki baki cuti.

B. Objektif Cadangan
- Membangunkan satu platform digital untuk semua urusan cuti.
- Mengurangkan masa proses kelulusan cuti sebanyak 50%.

## 2.0 SKOP CADANGAN

Cadangan ini merangkumi fungsi-fungsi berikut:
- Permohonan Cuti
- Kelulusan Cuti
- Laporan Cuti

| Fasa | Anggaran Masa |
| :--- | :--- |
| Fasa 1: Pembangunan | 3 Bulan |
| Fasa 2: UAT & Latihan | 1 Bulan |

</style_template>

<new_content>
Title: Spesifikasi Keperluan Bisnes: Portal Insentif Penyelidikan. 
The document number is MAMPU/SKB/2023/11, dated August 5, 2023.
Our introduction explains that this document defines the business requirements for a new portal to manage research grant applications for government researchers. The problem is that the current process is slow and lacks transparency. The objective is to create a centralized portal to streamline applications and provide real-time status tracking for applicants.
For the second section, on user requirements, we need to specify two main user groups. The first group is 'Researchers', who need to be able to submit new applications and track the status of existing applications. The second group is the 'Secretariat', who must be able to manage applications and generate reports. For the project timeline, we estimate that Phase 1 (Development) will take 4 months and Phase 2 (Pilot Testing) will take 2 months.
</new_content>
```

**Resulting Output (Formatted using the template's style):**
```
# SPESIFIKASI KEPERLUAN BISNES: PORTAL INSENTIF PENYELIDIKAN

**TARIKH:** 5 Ogos 2023
**DOKUMEN NO:** MAMPU/SKB/2023/11

## 1.0 PENGENALAN

Ini adalah dokumen spesifikasi keperluan bisnes (SKB) untuk membangunkan Portal Insentif Penyelidikan.

A. Latar Belakang Masalah
- Proses permohonan geran penyelidikan sedia ada adalah lambat dan tidak telus.
- Tiada platform berpusat untuk pemohon menjejaki status permohonan mereka.

B. Objektif
- Membangunkan satu portal berpusat untuk menguruskan permohonan geran.
- Menyediakan penjejakan status masa nyata untuk pemohon.

## 2.0 KEPERLUAN PENGGUNA

Keperluan merangkumi dua (2) kumpulan pengguna utama:
- **Penyelidik:** Boleh mengemukakan permohonan baharu dan menjejaki status permohonan sedia ada.
- **Sekretariat:** Boleh menguruskan permohonan dan menjana laporan.

| Fasa | Anggaran Masa |
| :--- | :--- |
| Fasa 1: Pembangunan | 4 Bulan |
| Fasa 2: Ujian Rintis | 2 Bulan |
```

### 6.5. Common Pitfalls & Best Practices

| Best Practice (Do) | Pitfall (Don't) |
| :--- | :--- |
| **Provide a Good, Clean Template.** The quality of the output depends heavily on the quality of the style template. Ensure it is well-structured and free of errors. | **Provide a Messy or Inconsistent Template.** If the template has inconsistent heading levels or formatting, the AI's output will also be inconsistent. |
| **Use Clear Markers.** Use distinct tags like `<style_template>` and `<new_content>` to clearly separate the style guide from the new information. | **Mix Content and Style.** Don't mix instructions for new content inside the template. Keep the two parts completely separate for the best results. |

### 6.6. Interactive Workshop Activity: "Ajar Templat Ini" (Teach This Template)

-   **Duration:** 10 Minutes
-   **Format:** Pair Activity.
-   **Task:**
    1.  The trainer provides a **Style Template** (e.g., a simple meeting minutes format) and a block of **New Content** (raw notes about a project discussion).
    2.  In pairs, participants must write a single, complete prompt that uses the "Reverse Engineering" technique.
    3.  The prompt should instruct the AI to use the meeting minutes style to generate a formal "Project Decision Log" based on the provided discussion notes. This teaches them to apply a known style to a new type of content. 