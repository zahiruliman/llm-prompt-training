## Technique 5: Iterative Prompting ("Let's Refine This")

### 5.1. Concept

Iterative Prompting is the practice of treating the AI as a collaborative partner to refine its output through a series of specific, follow-up prompts. The core idea is that the first output is a draft, not the final product.

### 5.2. Rationale

-   **From a Technical Perspective:** An initial, complex prompt (e.g., "Generate the full SKS") might have too many competing constraints for the AI to handle perfectly at once. By breaking down the refinement process into smaller, more focused follow-up prompts, you allow the model to concentrate its resources on one adjustment at a time (e.g., "Now, refine the non-functional requirements section...").
-   **From a Practical Perspective:** It is often more efficient to generate a solid "Version 1.0" of an **SKB** or **SKS** and then refine it than it is to craft a single, perfect, all-encompassing prompt. This conversational approach allows for rapid course correction and the incremental improvement of a document, making the process feel more like a collaboration.

### 5.3. Application in AIDevX

This is a universal technique applicable in any chat-based interaction with an AIDevX assistant. The key to success is to be highly specific in your refinement requests. Avoid vague feedback.

#### **Example (Malaysian Context):**

**Objective:** Refine a first-draft **Spesifikasi Keperluan Bisnes (SKB)** to be more specific and aligned with stakeholder needs.

**Initial Prompt & Output:**
*   **Prompt:** `You are a Business Analyst. Our goal is to build a new portal for university students to find and apply for internships. Please generate the initial draft of the Business Requirement Specification (SKB).`
*   **Initial Output:**
    ```
    **Dokumen: Spesifikasi Keperluan Bisnes (SKB) - Draf Awal**

    **1.0 Pengenalan**
    Dokumen ini menghuraikan keperluan bisnes untuk sebuah portal baharu bagi membolehkan pelajar universiti mencari dan memohon latihan industri.

    **2.0 Objektif Bisnes**
    - Memudahkan proses permohonan latihan industri.
    - Meningkatkan padanan antara pelajar dan syarikat.

    **3.0 Skop**
    - Pelajar boleh mencari dan memohon latihan industri.
    - Syarikat boleh menyiarkan tawaran latihan industri.
    - Pentadbir boleh menguruskan pengguna dan siaran.

    **4.0 Pemegang Taruh**
    - Pelajar Universiti
    - Syarikat
    - Pentadbir Portal

    **5.0 Peraturan Bisnes**
    - Portal hendaklah mesra pengguna.
    ```

**Ineffective Refinement:**
```
Boleh perbaiki lagi SKB ini? (Can you improve this SKB?)
```
*   **Result:** The AI might make superficial changes without understanding the specific business goals. The feedback is not actionable.

**Effective Refinement Prompts (A Conversation):**

1.  **Refining Business Rules:**
    ```
    Terima kasih. Draf ini adalah permulaan yang baik. Walau bagaimanapun, peraturan bisnes yang dijana terlalu umum. Sila perhalusi bahagian Peraturan Bisnes untuk memasukkan syarat-syarat khusus ini:
    1.  Hanya pelajar tahun akhir sahaja yang layak memohon.
    2.  Setiap pelajar hanya boleh memohon maksimum 5 syarikat pada satu-satu masa.
    3.  Syarikat mesti mempunyai sekurang-kurangnya 10 orang pekerja tetap untuk layak menyertai program ini.

    (Thank you. This draft is a good start. However, the generated business rules are too generic. Please refine the Business Rules section to include these specific conditions:
    1.  Only final-year students are eligible to apply.
    2.  Each student can only apply to a maximum of 5 companies at a time.
    3.  Companies must have at least 10 permanent employees to be eligible to join the program.)
    ```
2.  **Refining Stakeholder Needs:**
    ```
    Bagus. Sekarang, mari kita perhalusi keperluan pemegang taruh. Sila tambah keperluan khusus untuk Jabatan Hal Ehwal Pelajar (HEP) universiti. Mereka mesti boleh menjana laporan bulanan mengenai jumlah permohonan dan penempatan yang berjaya. Laporan ini mesti dalam format CSV.

    (Good. Now, let's refine the stakeholder requirements. Please add a specific requirement for the university's Student Affairs Department (HEP). They must be able to generate a monthly report on the number of applications and successful placements. This report must be in CSV format.)
    ```
3.  **Refining Scope:**
    ```
    Hampir siap. Sila kemas kini bahagian Skop Projek. Nyatakan dengan jelas bahawa "integrasi dengan sistem HR syarikat adalah di luar skop untuk Fasa 1."

    (Almost done. Please update the Project Scope section. State clearly that "integration with company HR systems is out of scope for Phase 1.")
    ```

*   **Result:** Through a series of specific, iterative prompts, the initial generic **SKB** is transformed into a precise, actionable requirements document that truly reflects the business needs.

### 5.4. Common Pitfalls & Best Practices

**Objective:** To efficiently guide the AI from a rough draft to a final product.

| Best Practice (Do) | Pitfall (Don't) |
| :--- | :--- |
| **Be Specific and Actionable.** Give concrete instructions. "Change the tone to be more formal," "Rewrite these SKS requirements to be testable," "Add a column for 'Risk Level' to the table." | **Be Vague and Ambiguous.** Avoid feedback like "Fix it," "I don't like this SKS," or "Make it better." The AI does not understand subjective dislike. |
| **Focus on One KRISA Section at a Time.** For complex refinements, address one section at a time (e.g., first fix the functional requirements in the SKS, then the non-functional requirements). | **Ask for Too Many Changes at Once.** A prompt like "In this SRB, rewrite the architecture section, add a data model, reformat the tables, and make it shorter" may confuse the AI. |
| **Affirm and Guide.** Use polite, guiding language. Starting with "Thank you, that's a good start. Now, let's refine the SKB's scope..." helps maintain a collaborative flow. | **Start a New Chat for a Small Change.** Don't abandon the conversation and start over for a simple refinement. The AI uses the immediate conversation history to understand the refinement request. |

**Example of a Pitfall:**

> **DON'T:** (After the AI generates a list of requirements for an SKS) "That's not right. Try again."
>
> *   **Why it's a pitfall:** This provides zero useful information. The AI doesn't know *what* was wrong with the requirements in the **SKS** and will likely just generate a slightly different but still incorrect version.

**Example of a Best Practice:**

> **DO:** (After the AI generates a list of requirements for an SKS)
> "Terima kasih. Draf SKS ini baik. Walau bagaimanapun, beberapa keperluan fungsian adalah samar. Sila tulis semula keperluan SKS-FUNC-003 dan SKS-FUNC-005 untuk menjadikannya lebih spesifik dan boleh diuji, selaras dengan prinsip SMART.
>
> Sebagai contoh, gantikan 'sistem mesti cepat' dengan 'sistem mesti memaparkan hasil carian dalam masa kurang dari 3 saat di bawah beban puncak'."
>
> (Thank you. This SKS draft is good. However, some functional requirements are ambiguous. Please rewrite requirements SKS-FUNC-003 and SKS-FUNC-005 to be more specific and testable, in line with SMART principles.
>
> For example, replace 'the system must be fast' with 'the system must display search results in under 3 seconds under peak load'.)
>
> *   **Why it's a best practice:** The feedback is specific, references the exact requirements to fix in the **SKS**, and provides an example of what "better" looks like. The AI knows exactly what to do.

### 5.5. Interactive Workshop Activity: "Jom Perhalusi" (Let's Refine)

-   **Duration:** 5 Minutes
-   **Format:** Group Discussion.
-   **Task:**
    1.  The trainer displays a weak AI output on the screen: a vague functional requirement from a draft **SKS**: `SKS-FUNC-015: The system shall allow the administrator to manage users.`
    2.  The trainer asks the group for verbal feedback, framing it as a real-time refinement session.
    3.  **Trainer:** "This requirement is too vague to be implemented or tested. What specific follow-up prompts could we give `AIDevX` to break this down into clear, testable requirements for our SKS?" (Expected answers: "Please break down 'manage users' into specific functions like Create User, Edit User, Deactivate User, and Reset Password.", "Please rewrite this as three separate requirements for adding, editing, and deleting users.").
    4.  This quick, interactive dialogue teaches the group how to think in terms of specific, actionable follow-up prompts to improve the quality of their KRISA documents. 