# 📋 Technique 3: Few-Shot Prompting

> **Core Concept:** "Show, Don't Just Tell" — Demonstrate exact formats with examples rather than descriptions  
> **Presentation Reference:** Also known as "Professional Template Methodology" in training presentations

---

## 📖 **Understanding the Technique**

### **What is Few-Shot Prompting?**

Few-Shot Prompting means providing the AI with one or more concrete examples of the exact output format you want, rather than trying to describe it in words. You're essentially "teaching by example" within your prompt.

**The Master Craftsman's Approach:** Think of a master craftsman training an apprentice. Instead of explaining how to shape wood, they show the apprentice a perfect example and say "make it exactly like this." AIDevX works the same way - it learns patterns from examples more effectively than from descriptions.

**Think of it like this:** Instead of explaining how to format a requirement specification, you show the AI 2-3 perfectly formatted examples and then ask it to continue in the same pattern.

### **Why Template Examples Transform Output Quality**

Government documents require precise formatting, consistent structure, and specific terminology. Describing these requirements often leads to interpretation errors. Showing exact examples eliminates ambiguity and ensures professional consistency.

| **Describing Format** | **Showing Examples** |
|----------------------|---------------------|
| ❌ "Each requirement should have an ID, statement, and priority" | ✅ Shows exact ID format: `SKS-FUNC-001` |
| ❌ AI guesses at formatting style | ✅ AI copies precise structure |
| ❌ Inconsistent outputs requiring cleanup | ✅ Perfect formatting every time |
| ❌ Ambiguous instructions | ✅ Clear, unambiguous patterns |

**Professional Principle:** One perfect example is worth a thousand words of description.

---

## 🎯 **Benefits for KRISA Documentation**

Few-Shot Prompting is particularly powerful for:

> ✅ **Requirements Tables** — Consistent ID schemes and formatting  
> ✅ **Use Case Descriptions** — Standardized structure and terminology  
> ✅ **Test Case Templates** — Repeatable format with exact fields  
> ✅ **Data Dictionary Entries** — Uniform data definitions  
> ✅ **API Documentation** — Consistent endpoint specifications

---

## 🔧 **Application in AIDevX**

### **Best Practice Workflow**

```
Step 1: Assign persona + provide context (Expert Persona Strategy + Project Intelligence Framework)
Step 2: State the deliverable you need
Step 3: Show 2-3 perfect examples of the format
Step 4: Ask AI to generate more following the pattern
Step 5: Review and refine if needed
```

### **Optimal Number of Examples**

| **Examples** | **When to Use** | **Impact** |
|-------------|----------------|------------|
| **1 Example** | Simple, straightforward formats | May miss variations or edge cases |
| **2-3 Examples** | ✅ **Recommended** — Standard practice | Captures pattern variations effectively |
| **4+ Examples** | Complex formats with many variations | May overwhelm the prompt unnecessarily |

---

## 💡 **Professional Template Methodology in Action: KRISA Requirements**

### **The Challenge:** Generate functional requirements for Jabatan Imigresen's new visa application system that meet government documentation standards.

#### **❌ Ineffective Approach (Format Description - Unreliable)**

```
"Generate functional requirements in government format with ID numbers, 
clear statements, and priority levels"
```

**Result:** Inconsistent formatting, unclear requirement structure

#### **✅ Effective Approach (Template Example - Professional)**

```
You are a Lead System Analyst specializing in government enterprise architecture 
with extensive experience in Malaysian government e-services development.

Generate functional requirements for Jabatan Imigresen's online visa application 
system following KRISA standards.

Use this EXACT KRISA format:

TEMPLATE PATTERN:
---
**ID Keperluan:** SKS-FUNC-XXX
**Pernyataan:** Sistem hendaklah membenarkan [Actor] untuk [Action] dengan [Condition]
**Keutamaan:** [Tinggi/Sederhana/Rendah]
**Compliance Note:** [PDPA/Security/Integration requirement]
---

EXAMPLE 1:
---
**ID Keperluan:** SKS-FUNC-001  
**Pernyataan:** Sistem hendaklah membenarkan Pemohon Visa untuk submit aplikasi visa elektronik menggunakan MyKad atau passport verification
**Keutamaan:** Tinggi
**Compliance Note:** Must comply with PDPA for personal data handling
---

EXAMPLE 2:
---
**ID Keperluan:** SKS-FUNC-002
**Pernyataan:** Sistem hendaklah membenarkan Pegawai Imigresen untuk review dokumen aplikasi dengan automated document verification
**Keutamaan:** Tinggi  
**Compliance Note:** Integration with existing Immigration database required
---

Now generate 8 functional requirements for online visa fee payment module.
```

**Result:** Perfectly formatted, government-standard requirements ready for official documentation

### **Extended Example: Transform Raw Notes**

**Raw Input:**
```
The system admin needs to manage user roles. They should create new roles, 
edit permissions, and delete unused roles. This is high priority.
```

**Template Teaching Approach:**
```
You are a Senior System Analyst specializing in KRISA-compliant documentation 
for Malaysian government systems.

Transform the following raw notes into professional SKS functional requirements 
using this EXACT template:

TARGET KRISA FORMAT:
---
**Requirement ID:** SKS-FUNC-XXX
**Statement:** The system shall allow [Actor] to [Action]  
**Priority:** [High/Medium/Low]
**Category:** [Security/Functional/Performance]
**Compliance:** [PDPA/Security framework reference]
---

EXAMPLE 1:
---
**Requirement ID:** SKS-FUNC-015
**Statement:** The system shall allow System Administrator to create new user roles with specific permission sets
**Priority:** High
**Category:** Security
**Compliance:** Role-based access control per government security standards
---

EXAMPLE 2:
---
**Requirement ID:** SKS-FUNC-016
**Statement:** The system shall allow System Administrator to modify permission levels for existing user roles
**Priority:** High
**Category:** Security
**Compliance:** Audit trail required for all permission changes
---

Raw notes to transform: [Insert raw notes here]
```

### **Expected Output Quality**

The template methodology produces consistently formatted requirements:

```
---
**Requirement ID:** SKS-FUNC-017
**Statement:** The system shall allow System Administrator to deactivate unused user roles while preserving audit history
**Priority:** High
**Category:** Security
**Compliance:** Data retention policy compliance for role management
---
```

---

## ⚠️ **Common Pitfalls & Best Practices**

### **✅ DO These Things**

| **Best Practice** | **Example** | **Why It Works** |
|-------------------|-------------|------------------|
| **Use Consistent Examples** | All examples follow identical structure | AI learns the pattern correctly |
| **Show Realistic Content** | Actual requirement statements, not placeholders | Demonstrates appropriate language and detail |
| **Include Government Context** | Malaysian ministry/agency specific examples | Ensures compliance and contextual relevance |
| **Clear Separators** | Use `---` or borders between examples | Makes pattern boundaries obvious |
| **Include Compliance Notes** | PDPA, security, integration requirements | Ensures government standards compliance |

### **❌ AVOID These Mistakes**

| **Pitfall** | **Example** | **Why It Fails** |
|-------------|-------------|------------------|
| **Inconsistent Examples** | Different ID formats in each example | AI gets confused about the true pattern |
| **Placeholder Content** | "Requirement goes here" instead of real text | AI may generate generic placeholder text |
| **Too Many Variations** | Each example uses different structure | Dilutes the pattern you want to establish |
| **No Clear Boundaries** | Examples run together without separation | AI can't distinguish where examples end |
| **Missing Government Context** | Generic examples without Malaysian compliance | Lacks regulatory and domain specificity |

---

## 🎮 **Practice Activity: Professional Template Teaching**

### **Challenge:** Transform Raw Notes into Government-Standard Requirements

#### **Government Project Scenario:**
You're working on a digital document management system for Ministry of Education. Raw stakeholder feedback needs transformation into professional SKS requirements.

#### **Given Raw Information:**
```
Teachers need to upload lesson plans and share them with other teachers. 
The head of department should approve plans before sharing. Students should 
be able to access approved plans for their subjects. The system needs to 
track who accessed what documents and when for audit purposes.
```

#### **Target KRISA Format:**
```
**Requirement ID:** SKS-FUNC-XXX
**Statement:** The system shall allow [Actor] to [Action] [Conditions]
**Priority:** [High/Medium/Low]
**Category:** [Core/Supporting/Compliance]
**Ministry Context:** [Education-specific requirement details]
```

### **Your Task:** Create a Complete Professional Prompt

Write a comprehensive prompt that includes:
- ✅ Appropriate expert persona for government SKS generation
- ✅ Ministry of Education project context
- ✅ 2-3 perfect template examples using the target format
- ✅ Clear instruction to transform the raw notes

### **Success Criteria:**
Your prompt should produce requirements that are:
- Consistently formatted using the exact KRISA template
- Professionally written in proper government requirement language
- Include Ministry of Education specific context and compliance
- Ready for immediate use in an official SKS document

### **Professional Outcome**
Demonstrate mastery of template methodology for government documentation standards.

---

## 📝 **Quick Reference Templates**

### **For Functional Requirements (SKS) - KRISA Standard**

```
Use this EXACT format for every functional requirement:

TEMPLATE PATTERN:
---
**ID Keperluan:** SKS-FUNC-XXX
**Pernyataan:** Sistem hendaklah membenarkan [Actor] untuk [Action] dengan [Condition]
**Keutamaan:** [Tinggi/Sederhana/Rendah]
**Compliance Note:** [PDPA/Security/Integration requirement]
---

EXAMPLE:
---
**ID Keperluan:** SKS-FUNC-001
**Pernyataan:** Sistem hendaklah membenarkan Pegawai untuk log masuk menggunakan MyKad dan kata laluan
**Keutamaan:** Tinggi
**Compliance Note:** Must comply with government authentication standards
---
```

### **For Use Case Descriptions - Government Standard**

```
Use this EXACT format for every use case:

TEMPLATE PATTERN:
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
**Use Case ID:** UC-XXX
**Use Case Name:** [Descriptive Name]
**Actor:** [Primary User Role]
**Description:** [Brief purpose statement]
**Preconditions:** [What must be true before this use case]
**Main Flow:** 
1. [Step 1]
2. [Step 2]
3. [Step 3]
**Postconditions:** [What is true after successful completion]
**Compliance:** [PDPA/Security/Integration considerations]
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

EXAMPLE:
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
**Use Case ID:** UC-001
**Use Case Name:** Submit Visa Application
**Actor:** Citizen/Visa Applicant
**Description:** Allows citizen to submit electronic visa application with document verification
**Preconditions:** User has valid MyKad or passport, required documents uploaded
**Main Flow:** 
1. User logs in using MyKad authentication
2. User fills visa application form with personal details
3. System validates information against Immigration database
4. User uploads required supporting documents
5. System performs document verification checks
6. User submits application and receives confirmation
**Postconditions:** Application stored in system, reference number generated, notification sent
**Compliance:** PDPA compliance for personal data handling, integration with Immigration database
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

### **For Test Cases - Quality Assurance Standard**

```
Use this EXACT format for every test case:

TEMPLATE PATTERN:
┌─────────────────────────────────────────────────────────────┐
│ **Test Case ID:** TC-XXX                                   │
│ **Requirement ID:** [Linked requirement]                   │
│ **Test Objective:** [What this test verifies]              │
│ **Test Steps:**                                             │
│ 1. [Action step]                                            │
│ 2. [Action step]                                            │
│ 3. [Verification step]                                      │
│ **Expected Result:** [What should happen]                  │
│ **Test Data:** [Required test data]                        │
│ **Compliance Check:** [PDPA/Security verification]         │
└─────────────────────────────────────────────────────────────┘

EXAMPLE:
┌─────────────────────────────────────────────────────────────┐
│ **Test Case ID:** TC-001                                   │
│ **Requirement ID:** SKS-FUNC-001                           │
│ **Test Objective:** Verify MyKad authentication login      │
│ **Test Steps:**                                             │
│ 1. Navigate to login page                                   │
│ 2. Enter valid MyKad number (123456-78-9012)              │
│ 3. Enter correct password                                   │
│ 4. Click Login button                                       │
│ 5. Verify successful login and dashboard access            │
│ **Expected Result:** User successfully logged in, redirected to main dashboard │
│ **Test Data:** Valid MyKad: 123456-78-9012, Password: TestPass123 │
│ **Compliance Check:** Verify no sensitive data logged in system logs │
└─────────────────────────────────────────────────────────────┘
```

---

## 🎯 **Key Takeaways**

1. **Show Perfect Examples** instead of describing formats in words
2. **Use 2-3 Examples** to establish clear patterns for government documents
3. **Keep Examples Consistent** in structure and KRISA compliance
4. **Include Realistic Content** with Malaysian government context rather than placeholders
5. **Separate Examples Clearly** with visual boundaries for pattern recognition
6. **Include Compliance Notes** for PDPA, security, and integration requirements
7. **Use Government-Specific Context** with ministry/agency examples
8. **Remember:** Perfect examples = Perfect government-ready output formatting

**Professional Principle:** Template methodology ensures consistent, government-standard documentation that meets KRISA compliance requirements.

**Next:** Learn how to guide AI through step-by-step thinking! → **Technique 4: Chain of Thought Prompting** *(also presented as "Blueprint Planning Method")*