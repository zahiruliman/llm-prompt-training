# 🗺️ Technique 2: Contextual Scaffolding

> **Core Concept:** "Here's Your Briefing" — Provide comprehensive project context for relevant AI responses

---

## 📖 **Understanding the Technique**

### **What is Contextual Scaffolding?**

Contextual Scaffolding is the practice of providing the AI with a complete "project briefing" before asking it to generate content. Think of it as creating a detailed Terms of Reference (ToR) that gives the AI all the background information it needs to produce accurate, relevant results.

**The Reality:** AI has zero knowledge of your specific project, organization, or constraints. Everything must be explicitly stated.

### **Why This is Critical**

| **Without Context** | **With Proper Context** |
|-------------------|----------------------|
| ❌ Generic, template-like outputs | ✅ Project-specific, accurate content |
| ❌ Wrong assumptions about technology | ✅ Aligned with actual technical environment |
| ❌ Missing compliance requirements | ✅ Includes necessary standards (KRISA, PDPA) |
| ❌ Hours of manual corrections | ✅ Ready-to-use professional documentation |

---

## 🏗️ **Essential Context Elements**

### **The Complete Project Briefing Template**

```
📋 PROJECT CONTEXT CHECKLIST
├─ 🎯 Project Background & Objectives
├─ 🔍 Scope Definition (In/Out of scope)
├─ 👥 Target Users & Stakeholders  
├─ ⚙️ Technical Environment & Constraints
├─ 📏 Standards & Compliance Requirements
├─ 🔗 Integration Requirements
└─ 📖 Definitions & Terminology
```

#### **1. 🎯 Project Background & Objectives**
- What is the project and why does it exist?
- What business problem are you solving?
- What are the expected outcomes?

#### **2. 🔍 Scope Definition**
- What functionality is explicitly included?
- What is deliberately excluded from this phase?
- Any phase-based delivery approach?

#### **3. 👥 Target Users & Stakeholders**
- Who will use this system? (Internal staff, public, specific groups)
- What are their technical skill levels?
- Any special accessibility requirements?

#### **4. ⚙️ Technical Environment & Constraints**
- Existing systems that must be integrated
- Technology platforms and standards
- Infrastructure limitations or requirements

#### **5. 📏 Standards & Compliance**
- KRISA compliance requirements
- PDPA and data protection needs
- Industry-specific regulations
- Organizational document templates

#### **6. 🔗 Integration Requirements**
- External systems or APIs
- Data exchange formats
- Authentication methods

#### **7. 📖 Definitions & Terminology**
- Organization-specific acronyms
- Technical terms with specific meanings
- Business process definitions

---

## 🔧 **Application in AIDevX**

### **Best Practice Workflow**

```
Step 1: Assign appropriate persona (Technique 1)
Step 2: Provide comprehensive context briefing
Step 3: State specific deliverable request  
Step 4: Reference context throughout conversation
```

### **Context Integration with AIDevX Assistants**

| **AIDevX Assistant** | **Critical Context Elements** |
|---------------------|------------------------------|
| **Generate Requirements** | Business objectives, user types, compliance needs |
| **SRS > SDS** | Technical environment, integration points, constraints |
| **Create User Manual** | User skill levels, business processes, terminology |

---

## 💡 **Practical Example: Malaysian Banking Context**

### **Scenario:** Creating system design for mobile banking cash withdrawal feature

#### **❌ Ineffective Approach (No Context)**

```
Anda seorang arkitek sistem. Sila jana SRB untuk sistem pengeluaran wang.
(You are a system architect. Please generate the SRB for a cash out system.)
```

**Result:** Generic design with wrong assumptions about regulations, technology, and integration.

#### **✅ Effective Approach (With Comprehensive Context)**

```
You are a Lead Solutions Architect at a major Malaysian bank, tasked with 
designing a new feature for our "MyWallet" e-wallet application.

Please generate the Spesifikasi Rekabentuk Sistem (SRB) for a new 
"Cash Out to ATM" feature.

PROJECT CONTEXT:
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

📋 PROJECT BACKGROUND:
The "Cash Out to ATM" feature allows MyWallet users to generate a secure, 
one-time code on their app to withdraw cash from any of our bank's ATMs 
without a debit card. This addresses customer convenience and reduces 
plastic card dependency.

🎯 KEY OBJECTIVES:
1. Enhance user convenience and drive app engagement
2. Ensure all transactions are secure and comply with financial regulations
3. Maintain seamless integration with existing banking infrastructure

⚙️ TECHNICAL ENVIRONMENT:
- Must integrate with existing Core Banking System (CBS) via internal API Gateway
- Compatible with current Diebold Nixdorf ATM fleet
- All communication must be encrypted end-to-end
- One-time codes must expire after 10 minutes

📏 COMPLIANCE REQUIREMENTS:
- Payment Card Industry Data Security Standard (PCI DSS) compliance
- Bank Negara Malaysia's Risk Management in Technology (RMiT) policy
- Document structure must follow KRISA SRB template

🔗 INTEGRATION POINTS:
- Core Banking System (for balance validation)
- ATM Network Management System
- Mobile App Backend
- SMS Gateway (for backup verification)

Please generate the SRB covering sequence diagrams, API specifications, 
and security considerations.
```

### **Expected Output Quality**

With proper context, the AI produces SRB content that includes:

- ✅ Bank Negara compliance considerations
- ✅ PCI DSS security measures
- ✅ Realistic API endpoint designs
- ✅ Proper integration with CBS systems
- ✅ KRISA-compliant document structure

---

## ⚠️ **Common Pitfalls & Best Practices**

### **✅ DO These Things**

| **Best Practice** | **Example** | **Why It Works** |
|-------------------|-------------|------------------|
| **Structure Your Context** | Use clear headings and sections | AI can parse information systematically |
| **Be Project-Specific** | "Must integrate with existing HRMIS v2.1" | Prevents generic, unusable suggestions |
| **Include Constraints** | "Web application only, no mobile app" | Keeps solutions within realistic boundaries |
| **Define Terminology** | "'E-Notis' refers to our legacy notification system" | Prevents misinterpretation of jargon |

### **❌ AVOID These Mistakes**

| **Pitfall** | **Example** | **Why It Fails** |
|-------------|-------------|------------------|
| **Information Overload** | Pasting entire project documents | AI gets confused by too much irrelevant detail |
| **Assuming Knowledge** | "Use the standard integration approach" | AI doesn't know your "standard" approach |
| **Vague Constraints** | "Must be secure and fast" | Too generic to provide actionable guidance |
| **Missing Context** | Forgetting to mention key integrations | Results in incomplete or wrong solutions |

---

## 🎮 **Practice Activity: Context Detective**

### **Challenge:** Identify Missing Information

#### **Problematic Prompt:**
```
You are a System Analyst. A client wants to build a new booking system. 
Please generate the SKS.
```

### **Your Detective Mission** (Think-Pair-Share):

**Step 1 (Individual - 2 minutes):** List at least 5 missing context elements
**Step 2 (Pair - 4 minutes):** Compare lists and create comprehensive analysis  
**Step 3 (Share - 2 minutes):** Present findings to group

#### **Missing Elements Checklist:**

- [ ] **What type of booking?** (Hotels? Appointments? Resources? Events?)
- [ ] **Who are the users?** (Public customers? Internal staff? Specific groups?)
- [ ] **Integration requirements?** (Payment systems? Existing databases?)
- [ ] **Business objectives?** (What problem is this solving?)
- [ ] **Technology constraints?** (Platform preferences? Legacy systems?)
- [ ] **Compliance requirements?** (Data protection? Industry standards?)
- [ ] **Scope boundaries?** (What's included vs. excluded?)
- [ ] **User skill levels?** (Technical expertise of end users?)

### **Discussion Points**

> 💭 **Reflect:** How would missing context affect SKS quality?  
> 💭 **Consider:** Which missing element would cause the biggest problems?  
> 💭 **Think:** How do you gather this context in real projects?

---

## 📝 **Quick Reference Templates**

### **Context Template for SKB (Business Requirements)**

```
PROJECT CONTEXT for SKB:
━━━━━━━━━━━━━━━━━━━━━━━━━━

📋 BUSINESS BACKGROUND:
- Current business challenge: [describe problem]
- Strategic objectives: [business goals]
- Success criteria: [how you'll measure success]

👥 STAKEHOLDERS:
- Primary users: [who will use the system]
- Business owners: [who requested this]
- Other affected parties: [indirect stakeholders]

🔍 SCOPE:
- Included: [what's in scope for this project]
- Excluded: [what's deliberately out of scope]
- Future phases: [what might come later]

📏 COMPLIANCE:
- Regulatory requirements: [PDPA, industry standards]
- Organizational policies: [internal guidelines]
- Documentation standards: [KRISA compliance]
```

### **Context Template for SKS (System Requirements)**

```
TECHNICAL CONTEXT for SKS:
━━━━━━━━━━━━━━━━━━━━━━━━━

⚙️ TECHNICAL ENVIRONMENT:
- Platform: [web, mobile, desktop, cloud]
- Integration systems: [existing systems to connect]
- Technology stack: [preferred technologies]
- Infrastructure: [hosting, database, etc.]

🔗 INTEGRATION REQUIREMENTS:
- External APIs: [third-party services]
- Internal systems: [existing organizational systems]
- Data sources: [where data comes from]
- Authentication: [SSO, LDAP, etc.]

📊 PERFORMANCE & SECURITY:
- Expected load: [number of users, transactions]
- Security requirements: [encryption, access control]
- Availability needs: [uptime requirements]
- Backup/recovery: [data protection needs]
```

---

## 🎯 **Key Takeaways**

1. **Never Assume** the AI knows your project specifics
2. **Structure Context** clearly with headings and categories
3. **Include All Constraints** — technical, business, and regulatory
4. **Define Terminology** specific to your organization
5. **Keep Context Relevant** — include what's needed, exclude what's not
6. **Remember:** Quality context = Quality output

**Next:** Learn how to show exact formats instead of describing them! → **Technique 3: Few-Shot Prompting**