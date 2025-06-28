# 🔍 Technique 6: Reverse Engineering Prompting

> **Core Concept:** "Learn from Examples" — Teach AI to replicate professional document styles and formats  
> **Presentation Reference:** Also known as "Professional Style Replication" in training presentations

---

## 📖 **Understanding the Technique**

### **What is Reverse Engineering Prompting?**

This advanced technique involves teaching the AI a document's entire stylistic and structural format. You provide a complete example document as a "style template." The AI reverse-engineers its structure—headings, paragraph styles, list formats, table designs, and other text-based features. You can then provide new, unrelated content and instruct the AI to generate a new document that matches the *style* of the original template.

**The Master Craftsman's Approach:** Think of a master craftsman learning traditional techniques by studying exemplary work. They examine every detail, understand the patterns, and then apply those principles to create new pieces. Similarly, we teach AIDevX to study professional government documents and replicate their style for new content.

### **Why This is Critical for Government Projects**

**From a Technical Perspective:** Different government agencies and ministries have established documentation standards that must be followed precisely. Rather than trying to describe these complex formatting requirements in words, we can provide actual examples. The AI analyzes the structural patterns, heading hierarchies, table formats, and language conventions to create new documents that maintain institutional consistency.

**From a Practical Perspective:** Analysts and project managers often need to create new documents (e.g., an **BRS**) that must match the look and feel of existing documents from their ministry or department. Describing this style manually is nearly impossible. This technique allows you to say, "Here is how our ministry formats official documents. Now, take my raw notes and create a new BRS that follows this exact professional standard."

### **The Professional Style Replication Process**

Professional government documentation requires:

1. **Consistency** - All documents follow established ministry standards
2. **Authority** - Professional presentation builds stakeholder confidence  
3. **Compliance** - Proper formatting ensures regulatory acceptance
4. **Efficiency** - Reusable style templates accelerate document creation
5. **Quality** - Professional appearance reflects content quality

---

## 🔧 **Step-by-Step Application Workflow**

### **The Master Craftsman's Methodology:**

1. **Isolate the Style Template:** Copy the full text of a well-formatted government document that represents the style you want to replicate. This document should be complete, with proper headings, numbering, tables, and ministry-standard formatting.

2. **Create the Master Prompt:** Structure a prompt with two main parts:
   - **The Style Template:** Paste the copied document text, clearly enclosed in markers like `<style_template> ... </style_template>`
   - **The New Content:** Provide the new, raw information for the new document, enclosed in markers like `<new_content> ... </new_content>`

3. **Give Clear Instructions:** Explicitly instruct the AI to "generate a new document using the provided new content, but format it strictly according to the structure and style found in the style template."

4. **Include Government Context:** Specify the ministry, document type, and compliance requirements to ensure appropriate professional standards.

---

## 💡 **Real Example: Ministry Document Style Replication**

### **Scenario:** Using established Ministry of Health documentation style for new patient data system BRS

#### **The Professional Style Replication Prompt:**

```
You are a Senior Business Analyst at the Ministry of Health Malaysia. Your task 
is to create a formal Spesifikasi Keperluan Bisnes (BRS) document that follows 
our ministry's established documentation standards.

First, carefully analyze the document style provided in the <style_template> tags. 
Pay attention to:
- Ministry header format and document numbering
- Numbered main sections (1.0, 2.0) and lettered subsections (A, B)
- Table formatting and data presentation style
- Professional language tone appropriate for ministry documentation
- PDPA compliance language integration

Then, take the raw notes from the <new_content> tags and generate a new BRS 
document that strictly follows the ministry's professional style and structure.

<style_template>
# PROPOSAL PROJEK: SISTEM E-CUTI HOSPITAL

**KEMENTERIAN KESIHATAN MALAYSIA**
**TARIKH:** 15 Julai 2023
**DOKUMEN NO:** KKM/BRS/BRS/2023/15
**KLASIFIKASI:** SULIT

## 1.0 PENGENALAN

Dokumen ini menghuraikan cadangan untuk membangunkan Sistem E-Cuti Hospital 
bagi menggantikan proses permohonan cuti secara manual di semua hospital kerajaan.

A. Latar Belakang Masalah
- Proses sedia ada menggunakan borang kertas yang tidak efisien
- Tiada sistem berpusat untuk menjejaki baki cuti kakitangan perubatan
- Ketiadaan integrasi dengan sistem HR hospital menyukarkan pengurusan

B. Objektif Projek
- Membangunkan platform digital untuk semua urusan cuti kakitangan perubatan
- Mengurangkan masa proses kelulusan cuti dari 5 hari kepada 24 jam
- Memastikan pematuhan dengan Akta Kerja 1955 dan peraturan KKM

## 2.0 SKOP PROJEK

Projek ini merangkumi pembangunan fungsi-fungsi berikut:
- **Permohonan Cuti:** Membolehkan kakitangan mohon cuti secara dalam talian
- **Alur Kerja Kelulusan:** Sistem kelulusan automatik mengikut hierarki hospital
- **Penjejakan Baki:** Papan pemuka untuk memapar baki cuti real-time
- **Integrasi HR:** Sambungan dengan sistem HR sedia ada (HRMIS)

### 2.1 Pematuhan dan Keselamatan

Sistem ini mesti mematuhi:
- **PDPA 2010:** Perlindungan data peribadi kakitangan
- **Garis Panduan Keselamatan Siber KKM:** Enkripsi data dan audit trail
- **Prosedur Standard Hospital:** Integrasi dengan SOP sedia ada

| Fasa Projek | Anggaran Masa | Pemilik |
|------------|---------------|---------|
| Fasa 1: Analisis & Reka Bentuk | 2 Bulan | Pasukan IT KKM |
| Fasa 2: Pembangunan Sistem | 4 Bulan | Vendor Teknologi |
| Fasa 3: UAT & Latihan | 2 Bulan | Hospital Percontohan |
| Fasa 4: Pelaksanaan Nasional | 3 Bulan | Semua Hospital KKM |

## 3.0 KEPERLUAN SUMBER

### 3.1 Sumber Manusia
- Ketua Projek (1 orang) - Pegawai IT Gred 41
- Penganalisis Sistem (2 orang) - Pegawai IT Gred 29
- Koordinator Hospital (5 orang) - Satu untuk setiap hospital percontohan

### 3.2 Bajet Anggaran
Jumlah bajet yang diperlukan: RM 850,000
- Pembangunan sistem: RM 600,000
- Perkakasan dan infrastruktur: RM 150,000
- Latihan dan sokongan: RM 100,000

**Disediakan oleh:** Ahmad bin Hassan, Penganalisis Sistem Kanan
**Disemak oleh:** Dr. Siti Aminah, Ketua Penolong Pengarah IT
**Diluluskan oleh:** Dato' Dr. Rahman, Pengarah Bahagian IT
</style_template>

<new_content>
Title: Business Requirements Specification for Hospital Patient Data Integration System

Document Details: 
- Document number should be KKM/BRS/BRS/2023/28
- Date: August 20, 2023
- Classification: CONFIDENTIAL

Introduction:
We need to create an integrated patient data system that connects all government hospitals nationwide. Currently, patient records are isolated in individual hospitals, making it difficult for doctors to access complete medical histories when patients visit different hospitals.

Background Problems:
- No centralized patient database across hospitals
- Doctors cannot access patient history from other hospitals
- Medical emergencies delayed due to incomplete information
- Duplicate medical tests due to lack of shared records

Project Objectives:
- Create unified patient database accessible by all government hospitals
- Reduce medical errors through complete patient history access
- Eliminate duplicate tests and procedures
- Improve emergency medical response time by 40%
- Ensure full compliance with medical data protection laws

Project Scope:
The system should include:
- Patient registration and medical record management
- Real-time data sharing between hospitals
- Medical history access and search functionality
- Emergency medical information quick access
- Integration with existing Hospital Information Systems (HIS)

Compliance Requirements:
- PDPA 2010 for patient data protection
- Medical data confidentiality standards
- Ministry of Health cybersecurity guidelines
- Audit requirements for medical record access

Timeline:
Phase 1: System design and architecture (3 months)
Phase 2: Development and testing (6 months) 
Phase 3: Pilot implementation at 3 hospitals (2 months)
Phase 4: National rollout to all government hospitals (4 months)

Resources needed:
- Project Manager (1 person) - IT Officer Grade 44
- Systems Analysts (3 people) - IT Officer Grade 32
- Medical consultants (2 people) - specialists to ensure clinical requirements
- Hospital coordinators (10 people) - one for each pilot and key hospitals

Budget estimate: RM 2.5 million total
- System development: RM 1.8 million
- Hardware and infrastructure: RM 500,000
- Training and support: RM 200,000

Document prepared by: Nurul Huda binti Ahmad, Senior Systems Analyst
Reviewed by: Dr. Mohd Azmi, Deputy Director of Medical Informatics  
Approved by: Dato' Dr. Faridah, Director of Hospital Information Systems
</new_content>
```

### **Expected Professional Output Quality:**

```
# SPESIFIKASI KEPERLUAN BISNES: SISTEM INTEGRASI DATA PESAKIT HOSPITAL

**KEMENTERIAN KESIHATAN MALAYSIA**
**TARIKH:** 20 Ogos 2023
**DOKUMEN NO:** KKM/BRS/BRS/2023/28
**KLASIFIKASI:** SULIT

## 1.0 PENGENALAN

Dokumen ini menghuraikan keperluan bisnes untuk membangunkan Sistem Integrasi 
Data Pesakit Hospital yang akan menghubungkan semua hospital kerajaan di Malaysia.

A. Latar Belakang Masalah
- Tiada pangkalan data pesakit berpusat merentas hospital kerajaan
- Doktor tidak dapat mengakses sejarah perubatan pesakit dari hospital lain
- Kecemasan perubatan tertangguh akibat maklumat tidak lengkap
- Ujian perubatan berulang disebabkan tiada perkongsian rekod

B. Objektif Projek
- Mewujudkan pangkalan data pesakit bersatu yang boleh diakses oleh semua hospital kerajaan
- Mengurangkan ralat perubatan melalui akses sejarah pesakit yang lengkap
- Menghapuskan ujian dan prosedur berulang
- Meningkatkan masa respons kecemasan perubatan sebanyak 40%
- Memastikan pematuhan penuh dengan undang-undang perlindungan data perubatan

## 2.0 SKOP PROJEK

Projek ini merangkumi pembangunan fungsi-fungsi berikut:
- **Pengurusan Pendaftaran dan Rekod Perubatan:** Sistem berpusat untuk semua data pesakit
- **Perkongsian Data Masa Nyata:** Capaian segera antara hospital
- **Pencarian Sejarah Perubatan:** Fungsi carian komprehensif untuk rekod pesakit
- **Akses Maklumat Kecemasan:** Capaian pantas untuk situasi kritikal
- **Integrasi HIS:** Sambungan dengan Sistem Maklumat Hospital (HIS) sedia ada

### 2.1 Pematuhan dan Keselamatan

Sistem ini mesti mematuhi:
- **PDPA 2010:** Perlindungan data peribadi pesakit
- **Piawaian Kerahsiaan Data Perubatan:** Mengikut garis panduan KKM
- **Garis Panduan Keselamatan Siber KKM:** Enkripsi data dan audit trail
- **Keperluan Audit:** Rekod akses maklumat perubatan

| Fasa Projek | Anggaran Masa | Pemilik |
|------------|---------------|---------|
| Fasa 1: Reka Bentuk dan Seni Bina Sistem | 3 Bulan | Pasukan IT KKM |
| Fasa 2: Pembangunan dan Ujian | 6 Bulan | Vendor Teknologi |
| Fasa 3: Pelaksanaan Rintis di 3 Hospital | 2 Bulan | Hospital Percontohan |
| Fasa 4: Pelaksanaan Nasional Semua Hospital | 4 Bulan | Semua Hospital KKM |

## 3.0 KEPERLUAN SUMBER

### 3.1 Sumber Manusia
- Ketua Projek (1 orang) - Pegawai IT Gred 44
- Penganalisis Sistem (3 orang) - Pegawai IT Gred 32
- Perunding Perubatan (2 orang) - Pakar untuk keperluan klinikal
- Koordinator Hospital (10 orang) - Seorang untuk setiap hospital percontohan dan utama

### 3.2 Bajet Anggaran
Jumlah bajet yang diperlukan: RM 2,500,000
- Pembangunan sistem: RM 1,800,000
- Perkakasan dan infrastruktur: RM 500,000
- Latihan dan sokongan: RM 200,000

**Disediakan oleh:** Nurul Huda binti Ahmad, Penganalisis Sistem Kanan
**Disemak oleh:** Dr. Mohd Azmi, Timbalan Pengarah Informatik Perubatan
**Diluluskan oleh:** Dato' Dr. Faridah, Pengarah Sistem Maklumat Hospital
```

**Professional Result:** The AI perfectly replicates the Ministry of Health's documentation style while adapting the content for the new patient data system. All formatting, language tone, compliance references, and structural elements match the established ministry standards.

---

## ⚠️ **Common Pitfalls & Best Practices**

### **✅ DO These Things**

| **Best Practice** | **Example** | **Why It Works** |
|-------------------|-------------|------------------|
| **Provide Clean, Complete Templates** | Use well-formatted ministry documents with proper headers, numbering, tables | AI learns precise formatting patterns |
| **Use Clear Separation Markers** | `<style_template>` and `<new_content>` tags | Prevents confusion between style and content |
| **Include Government Context** | Specify ministry, document classification, compliance requirements | Ensures appropriate professional standards |
| **Match Document Types** | Use BRS template for BRS creation, SRB template for SRB creation | Maintains document type consistency |
| **Preserve Ministry Standards** | Include proper approvals, document numbers, classification levels | Ensures institutional compliance |

### **❌ AVOID These Mistakes**

| **Pitfall** | **Example** | **Why It Fails** |
|-------------|-------------|------------------|
| **Messy or Inconsistent Templates** | Documents with poor formatting or mixed styles | AI replicates poor quality patterns |
| **Mixing Content with Style** | Including template instructions within style examples | Confuses AI's pattern recognition |
| **Generic Templates** | Using non-government documents as templates | Misses ministry-specific formatting requirements |
| **Incomplete Examples** | Templates missing headers, approval sections, or classifications | Results in incomplete document structure |

---

## 🎮 **Practice Activity: Master Craftsman Workshop**

### **Challenge:** Replicate Professional Government Style

#### **Government Documentation Scenario:**
You've been provided with a well-formatted Ministry of Transport project proposal document and need to create a new Jabatan Kerja Raya (JKR) infrastructure BRS using the same professional style and formatting standards.

#### **Your Mission:**
Working in pairs, create a complete reverse engineering prompt that will teach AIDevX to replicate the ministry's documentation style for a new highway maintenance system BRS.

**Required Elements:**
1. **Style Template Analysis** - Identify key formatting patterns in the provided template
2. **Content Transformation** - Convert raw notes about highway maintenance into professional requirements
3. **Government Standards** - Maintain ministry classification, approval hierarchies, and compliance references
4. **Professional Quality** - Ensure output matches government documentation standards

### **Your Task: Create the Master Prompt**

Write a comprehensive reverse engineering prompt that includes:
- ✅ Clear role definition (Senior Business Analyst at JKR)
- ✅ Proper template analysis instructions
- ✅ Style pattern recognition guidance (headers, numbering, tables, language)
- ✅ Government context preservation (classification, approvals, compliance)
- ✅ Professional output requirements

### **Success Criteria:**
Your prompt should enable AI to create a government-ready BRS that:
- Maintains exact ministry formatting standards
- Preserves professional language tone and structure
- Includes proper document classification and approval sections
- Addresses JKR-specific compliance and operational requirements
- Demonstrates master craftsman attention to detail

**Professional Outcome:** Master the art of style replication to ensure all government documents maintain institutional consistency and professional standards.

---

## 📝 **Quick Reference Templates**

### **Government Document Style Replication Template**

```
You are a [Expert Role] at [Ministry/Agency Name]. Your task is to create a 
formal [Document Type] that follows our ministry's established documentation standards.

ANALYSIS INSTRUCTIONS:
Carefully analyze the document style in the <style_template> tags, paying attention to:
- Ministry header format and document numbering system
- Section numbering hierarchy (1.0, 1.1, A, B, etc.)
- Table formatting and data presentation style  
- Professional language tone appropriate for government documentation
- Compliance language integration and regulatory references
- Approval signature format and classification levels

REPLICATION TASK:
Take the raw content from <new_content> tags and generate a new [Document Type] 
that strictly follows the ministry's professional style and structure while 
ensuring:
- Government-appropriate language and tone
- Proper compliance and regulatory references
- Ministry-standard formatting and presentation
- Professional approval and classification sections

<style_template>
[Paste complete government document with full formatting]
</style_template>

<new_content>
[Raw content to be transformed into professional government document]
</new_content>
```

### **Ministry BRS Style Replication Template**

```
You are a Senior Business Analyst at [Ministry Name]. Create a formal BRS 
document following our ministry's established standards.

Analyze the style template for:
- Official ministry header and document identification
- Structured section numbering and subsection hierarchy
- Professional table formatting for project phases and resources
- Government-appropriate language and compliance integration
- Standard approval and review signature sections

Transform the raw business requirements into a professional BRS that maintains:
- Ministry documentation standards and formatting
- Appropriate government language and tone
- Regulatory compliance references (PDPA, ministry guidelines)
- Professional approval hierarchy and document classification

<style_template>
[Complete ministry BRS or similar formal document]
</style_template>

<new_content>
[Raw business requirements and project information]
</new_content>
```

---

## 🎯 **Key Takeaways**

1. **Study Professional Examples** - Use high-quality government documents as style templates
2. **Separate Style from Content** - Keep template analysis and new content completely separate
3. **Preserve Government Standards** - Maintain ministry formatting, classification, and approval requirements
4. **Focus on Consistency** - Ensure all documents follow established institutional patterns
5. **Include Compliance Elements** - Replicate regulatory references and government-specific language
6. **Master the Craft** - Pay attention to every detail of professional government documentation
7. **Quality Templates = Quality Output** - The better your template, the better your results
8. **Remember:** Professional style replication ensures institutional consistency and builds stakeholder confidence

**Professional Principle:** Master craftsman attention to detail in style replication ensures all government documents maintain the highest professional standards and institutional credibility.

**Mastery Complete:** You now have all six AI prompting techniques for professional government document creation! 🎯