## Technique 4: Chain of Thought Prompting ("Think Step-by-Step")

### 4.1. Concept

Chain of Thought (CoT) prompting is a technique where we explicitly instruct the AI to break down a complex problem into a sequence of logical steps *before* providing the final answer. Instead of asking for the result directly, we ask the AI to "show its work" and reason through the problem first.

### 4.2. Rationale

-   **From a Technical Perspective:** For complex tasks like generating a full **SRB**, a direct answer requires the AI to make multiple logical inferences at once. This can lead to errors. CoT prompting constrains the model to follow a deliberate, sequential reasoning path. Each step builds on the previous one, which dramatically reduces the likelihood of logical fallacies or missed sections.
-   **From a Practical Perspective:** This technique allows us to validate the AI's "thinking" before it commits to an answer. It's especially useful for planning the structure of a large KRISA document or analyzing a complex business process before writing the **SKB**. It helps uncover flawed assumptions in the AI's approach early on, allowing us to course-correct.

### 4.3. Application in AIDevX

This is highly effective as a preliminary step for a complex task. Use it to plan the structure of a document before asking an assistant like "Generate SRB Document" to write the full content, or to analyze a problem before generating the requirements for an **SKS**.

#### **Example (Malaysian Context):**

**Objective:** Plan the structure and key considerations for the **Spesifikasi Rekabentuk Sistem (SRB)** for a new telecommunication company's mobile bill payment feature.

**Ineffective Prompt (Direct Question):**
```
Sila jana SRB untuk ciri pembayaran bil mudah alih. (Please generate the SRB for a mobile bill payment feature.)
```
*   **Result:** The AI will generate a generic SRB, but will likely miss many specific architectural components, integration points, and security considerations relevant to a telco payment system. The structure may not fully align with KRISA.

**Effective Prompt (Chain of Thought):**
```
You are a Lead Solutions Architect at a leading Malaysian telecommunications company. I need to create the **Spesifikasi Rekabentuk Sistem (SRB)** for a new "Pay Bill" feature in our self-service mobile app, based on the approved SKS-2023-088.

Before you generate the full SRB document, first, propose a detailed table of contents for the SRB that is compliant with the KRISA template. Then, for the "Rekabentuk Senibina" (Architecture Design) section, please outline your thinking process by breaking down the problem step-by-step. In your breakdown, please consider:
1.  **Component Breakdown:** Identify the key components of the solution (e.g., Mobile App Frontend, API Gateway, Payment Service, Notification Service, Ledger Service).
2.  **Integration Points:** Detail the required integrations (e.g., Core Billing System, FPX Gateway, Credit Card Processor, SMS Gateway for TAC).
3.  **Data Model:** Describe the main data entities involved (e.g., User, Bill, Payment, Transaction).
4.  **Security Considerations:** List the critical security measures to be implemented (e.g., End-to-end encryption, Tokenization of card details, Fraud detection logic).

After you have clearly outlined this plan, I will review it before you proceed to generate the full content for each section.
```
*   **Result:** The AI will first produce a logical, KRISA-compliant plan for the SRB. This allows the user to verify the architecture and approach *before* the AI generates the detailed content, ensuring the final SRB is comprehensive and technically sound.

**Example Output (The AI's Plan):**
```
Baik, saya faham. Sebelum menjana SRB penuh, berikut adalah rangka perancangan dan proses pemikiran saya.

**Cadangan Jadual Kandungan SRB (Pematuhan KRISA):**
1.0 Pengenalan
2.0 Reka Bentuk Peringkat Tinggi
    2.1 Gambar Rajah Kontekstual
    2.2 Reka Bentuk Senibina
3.0 Reka Bentuk Terperinci
    3.1 Reka Bentuk Pangkalan Data
    3.2 Reka Bentuk Antara Muka Pengguna
    3.3 Reka Bentuk Komponen
4.0 Pertimbangan Keselamatan

**Proses Pemikiran untuk Seksyen 2.2: Reka Bentuk Senibina**

1.  **Pecahan Komponen (Component Breakdown):**
    *   **Mobile App Frontend:** Antara muka pengguna untuk pelanggan.
    *   **API Gateway:** Titik masuk tunggal untuk semua permintaan, mengendalikan pengesahan dan penghalaan.
    *   **Payment Service:** Logik teras untuk memproses pembayaran, berkomunikasi dengan gerbang pembayaran luar.
    *   **Notification Service:** Mengendalikan penghantaran notifikasi (SMS/Push) untuk TAC dan status pembayaran.
    *   **Ledger Service:** Komponen khusus untuk merekod semua urus niaga kewangan secara kekal.

2.  **Titik Integrasi (Integration Points):**
    *   **Sistem Pengebilan Teras (Core Billing System):** Untuk mendapatkan maklumat bil semasa. (READ)
    *   **Gerbang FPX (FPX Gateway):** Untuk memulakan pembayaran perbankan dalam talian. (WRITE)
    *   **Pemproses Kad Kredit (Credit Card Processor):** Untuk caj kad kredit/debit. (WRITE)
    *   **Gerbang SMS (SMS Gateway):** Untuk menghantar kod TAC (Transaction Authorization Code). (WRITE)

3.  **Model Data (Data Model):**
    *   **Pengguna (User):** Menyimpan maklumat pelanggan (ID Pelanggan, Nama).
    *   **Bil (Bill):** Menyimpan maklumat bil (ID Bil, Jumlah, Tarikh Akhir).
    *   **Pembayaran (Payment):** Merekod setiap percubaan pembayaran (ID Pembayaran, Status, Kaedah).
    *   **Transaksi (Transaction):** Rekod lejar muktamad bagi setiap pembayaran yang berjaya.

4.  **Pertimbangan Keselamatan (Security Considerations):**
    *   Semua komunikasi API mesti melalui HTTPS (TLS 1.2+).
    *   Data sensitif seperti nombor kad kredit tidak akan disimpan; sebaliknya, token dari pemproses pembayaran akan digunakan.
    *   Mekanisme pengesanan penipuan asas akan dilaksanakan (e.g., had transaksi).

Setelah pelan ini dipersetujui, saya akan meneruskan untuk menjana kandungan terperinci bagi setiap seksyen SRB.
```

### 4.4. Common Pitfalls & Best Practices

**Objective:** To improve the quality and logic of answers for complex tasks.

| Best Practice (Do) | Pitfall (Don't) |
| :--- | :--- |
| **Use it for Complex KRISA Documents.** Apply this technique for tasks that require planning and analysis, like creating an **SRB** from an **SKS**, or defining the business process models for an **SKB**. | **Use it for Simple Tasks.** For simple, direct questions (e.g., "What is an SKS?"), asking the AI to "think step-by-step" is unnecessary and adds noise. |
| **Guide the Thought Process.** Provide key areas for the AI to consider in its step-by-step thinking, ideally mapping to sections of the target KRISA document. | **Use a Vague Instruction.** Simply saying "Think step-by-step" is less effective than guiding *how* it should think (e.g., "Think step-by-step. First, identify the user roles from the SKB. Second, propose the system modules..."). |

**Example of a Pitfall:**

> **DON'T:** "Think step by step and tell me the requirements for a reporting module for our SKS."
>
> *   **Why it's a pitfall:** This is too vague. While it might produce a slightly more structured list than a direct query, it doesn't guide the AI's analysis. The AI has to guess what aspects of reporting are important for this specific **SKS**.

**Example of a Best Practice:**

> **DO:** (After setting persona and context for an e-Procurement system's SKS)
> "Before you generate the full list of functional requirements for the 'Vendor Evaluation' module of the **SKS**, please formulate a plan by thinking step-by-step. Your plan must detail the process flow from a system perspective:
> 1.  **Criteria Configuration:** How will the system allow administrators to configure evaluation criteria and weightage?
> 2.  **Document Submission & Validation:** How will the system handle the upload and validation of vendor documents against these criteria?
> 3.  **Scoring & Consolidation:** How will the system calculate, consolidate, and rank the vendor scores automatically?
>
> After you have presented this system process flow, await my confirmation before generating the detailed functional requirements for the **SKS** based on your proposed logic."
>
> *   **Why it's a best practice:** This prompt forces the AI to first design a logical system process. The user can then validate this logic to ensure it's correct *before* the AI wastes effort generating detailed SKS requirements based on a potentially flawed process.

**Example Output (The AI's Plan):**
```
Baik, saya faham. Berdasarkan permintaan anda, berikut adalah pelan aliran proses sistem untuk modul "Penilaian Vendor" sebelum saya menjana keperluan fungsian terperinci untuk SKS.

**Pelan Aliran Proses Sistem: Modul Penilaian Vendor**

1.  **Konfigurasi Kriteria (Criteria Configuration):**
    *   Sistem akan menyediakan antara muka untuk Pentadbir Sistem (System Administrator).
    *   Pentadbir akan dapat mencipta, mengemas kini, dan memadam kriteria penilaian (e.g., 'Kestabilan Kewangan', 'Pematuhan Teknikal').
    *   Setiap kriteria akan mempunyai medan untuk nama, keterangan, dan peratusan pemberat (weightage).
    *   Data ini akan disimpan dalam jadual `EvaluationCriteria`.

2.  **Penyerahan & Pengesahan Dokumen (Document Submission & Validation):**
    *   Vendor akan memuat naik dokumen yang diperlukan melalui portal vendor.
    *   Sistem akan memetakan setiap muat naik dokumen kepada kriteria yang berkaitan.
    *   Sistem akan mengesahkan jenis fail (e.g., PDF, DOCX) dan saiz fail (<10MB).
    *   Status penyerahan akan ditukar dari 'Pending' ke 'Submitted'.

3.  **Pemarkahan & Konsolidasi (Scoring & Consolidation):**
    *   Penilai Dalaman (Internal Evaluators) akan diberikan akses untuk melihat dokumen yang diserahkan.
    *   Sistem akan menyediakan antara muka pemarkahan di sebelah dokumen, di mana penilai boleh memasukkan skor (e.g., 1-5) untuk setiap kriteria.
    *   Setelah semua penilai melengkapkan pemarkahan, sistem akan secara automatik mengira skor purata wajaran untuk setiap vendor.
    *   Sistem akan menjana satu laman ringkasan yang menyenaraikan semua vendor mengikut kedudukan skor akhir mereka.

Sila sahkan sama ada aliran proses ini sejajar dengan keperluan anda sebelum saya meneruskan untuk menulis keperluan fungsian SKS yang terperinci.
```

### 4.5. Interactive Workshop Activity: "Rancang Dulu" (Plan First)

-   **Duration:** 10 Minutes
-   **Format:** Pair Activity.
-   **Task:**
    1.  The trainer presents a high-level objective from an **SKB**:
        -   `"The business needs a new workflow for employees to claim work-related expenses (e.g., travel, meals) through an internal portal to improve efficiency and tracking."`
    2.  In pairs, participants do **not** write the full SKS. Their only task is to write the "Chain of Thought" part of a prompt that would be used to generate the functional requirements for the **SKS**.
    3.  They should create a numbered list that instructs the AI on how to break down the problem logically from a *system* perspective before generating the final requirements list. (e.g., 1. Outline the data entities required. 2. Detail the claim submission process steps. 3. Detail the approval workflow steps. 4. Describe the notification requirements...).
    4.  A pair can share their "plan" with the group to see how different teams would approach the problem. 