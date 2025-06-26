# 📋 Technique 3: Few-Shot Prompting

> **Core Concept:** "Show, Don't Just Tell" — Demonstrate exact formats with examples rather than descriptions

---

## 📖 **Understanding the Technique**

### **What is Few-Shot Prompting?**

Few-Shot Prompting means providing the AI with one or more concrete examples of the exact output format you want, rather than trying to describe it in words. You're essentially "teaching by example" within your prompt.

**Think of it like this:** Instead of explaining how to format a requirement specification, you show the AI 2-3 perfectly formatted examples and then ask it to continue in the same pattern.

### **Why This Works Better Than Descriptions**

| **Describing Format** | **Showing Examples** |
|----------------------|---------------------|
| ❌ "Each requirement should have an ID, statement, and priority" | ✅ Shows exact ID format: `SKS-FUNC-001` |
| ❌ AI guesses at formatting style | ✅ AI copies precise structure |
| ❌ Inconsistent outputs requiring cleanup | ✅ Perfect formatting every time |
| ❌ Ambiguous instructions | ✅ Clear, unambiguous patterns |

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
Step 1: Assign persona + provide context (Techniques 1 & 2)
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

## 💡 **Practical Example: Malaysian Government SKS**

### **Scenario:** Generate functional requirements for HR system leave module

#### **❌ Ineffective Approach (Describing Format)**

```
Anda seorang Penganalisis Sistem. Tuliskan keperluan fungsian untuk modul 
permohonan cuti. Setiap keperluan mesti ada ID, pernyataan keperluan, dan 
keutamaan (Tinggi, Sederhana, atau Rendah).

(You are a System Analyst. Write functional requirements for the leave 
application module. Each requirement must have an ID, requirement statement, 
and priority (High, Medium, or Low).)
```

**Result:** Inconsistent formatting, varying ID schemes, mixed languages, manual cleanup required.

#### **✅ Effective Approach (Few-Shot Examples)**

```
You are a Senior System Analyst creating a Spesifikasi Keperluan Sistem (SKS) 
for a new integrated HRM system for our company, Maju Holdings Berhad.

Please generate the Functional Requirements for the Leave Application module.

Use this EXACT format for every requirement:
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

---
**ID Keperluan:** SKS-FUNC-XXX
**Pernyataan:** Sistem hendaklah membenarkan [Actor] untuk [Action]
**Keutamaan:** [Tinggi/Sederhana/Rendah]
---

EXAMPLE 1:
---
**ID Keperluan:** SKS-FUNC-045
**Pernyataan:** Sistem hendaklah membenarkan Kakitangan untuk memohon cuti 
tahunan melalui sistem dalam talian
**Keutamaan:** Tinggi
---

EXAMPLE 2:
---
**ID Keperluan:** SKS-FUNC-046
**Pernyataan:** Sistem hendaklah menghantar notifikasi e-mel kepada Pengurus 
apabila kakitangan di bawah seliaannya memohon cuti
**Keutamaan:** Tinggi
---

Now generate 5 more requirements covering leave balance viewing, application 
cancellation, and public holiday display.
```

### **Expected Output Quality**

The few-shot approach produces consistently formatted requirements:

```
---
**ID Keperluan:** SKS-FUNC-047
**Pernyataan:** Sistem hendaklah membenarkan Kakitangan untuk melihat baki 
cuti tahunan semasa mereka
**Keutamaan:** Tinggi
---
**ID Keperluan:** SKS-FUNC-048
**Pernyataan:** Sistem hendaklah membenarkan Kakitangan untuk membatalkan 
permohonan cuti yang berstatus 'Menunggu Kelulusan'
**Keutamaan:** Sederhana
---
```

---

## ⚠️ **Common Pitfalls & Best Practices**

### **✅ DO These Things**

| **Best Practice** | **Example** | **Why It Works** |
|-------------------|-------------|------------------|
| **Use Consistent Examples** | All examples follow identical structure | AI learns the pattern correctly |
| **Show Realistic Content** | Actual requirement statements, not placeholders | Demonstrates appropriate language and detail |
| **Include Edge Cases** | Show both simple and complex examples | Helps AI handle variations properly |
| **Clear Separators** | Use `---` or borders between examples | Makes pattern boundaries obvious |

### **❌ AVOID These Mistakes**

| **Pitfall** | **Example** | **Why It Fails** |
|-------------|-------------|------------------|
| **Inconsistent Examples** | Different ID formats in each example | AI gets confused about the true pattern |
| **Placeholder Content** | "Requirement goes here" instead of real text | AI may generate generic placeholder text |
| **Too Many Variations** | Each example uses different structure | Dilutes the pattern you want to establish |
| **No Clear Boundaries** | Examples run together without separation | AI can't distinguish where examples end |

---

## 🎮 **Practice Activity: Template Teaching**

### **Challenge:** Transform Raw Notes into Structured Requirements

#### **Given Raw Information:**
```
The system admin needs to manage user roles. They should create new roles, 
edit permissions for existing roles, and delete roles that are no longer 
needed. This is a high-priority feature for security and access control.
```

#### **Target KRISA Format:**
```
**Requirement ID:** SKS-FUNC-XXX
**Statement:** The system shall allow [Actor] to [Action]
**Priority:** [High/Medium/Low]
**Category:** [Security/Functional/Performance]
```

### **Your Task:** Create a Complete Prompt

Write a comprehensive prompt that includes:
- ✅ Appropriate persona for SKS generation
- ✅ Brief project context
- ✅ 2-3 perfect few-shot examples  
- ✅ Clear instruction to transform the raw notes

### **Success Criteria:**
Your prompt should produce requirements that are:
- Consistently formatted using the exact template
- Professionally written in proper requirement language
- Appropriately categorized and prioritized
- Ready for immediate use in an SKS document

---

## 📝 **Quick Reference Templates**

### **For Functional Requirements (SKS)**

```
Use this EXACT format for every functional requirement:

---
**ID:** SKS-FUNC-XXX
**Statement:** Sistem hendaklah membenarkan [Actor] untuk [Action]
**Priority:** [Tinggi/Sederhana/Rendah]
**Category:** [Core/Supporting/Optional]
---

EXAMPLE 1:
---
**ID:** SKS-FUNC-001
**Statement:** Sistem hendaklah membenarkan Pengguna untuk log masuk 
menggunakan MyKad dan kata laluan
**Priority:** Tinggi
**Category:** Core
---
```

### **For Use Case Descriptions**

```
Use this EXACT format for every use case:

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
**Use Case ID:** UC-XXX
**Use Case Name:** [Descriptive Name]
**Actor:** [Primary User]
**Description:** [Brief purpose statement]
**Preconditions:** [What must be true before this use case]
**Main Flow:** 
1. [Step 1]
2. [Step 2]
3. [Step 3]
**Postconditions:** [What is true after successful completion]
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

### **For Test Cases**

```
Use this EXACT format for every test case:

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
└─────────────────────────────────────────────────────────────┘
```

---

## 🎯 **Key Takeaways**

1. **Show Examples** instead of describing formats in words
2. **Use 2-3 Examples** to establish clear patterns
3. **Keep Examples Consistent** in structure and style
4. **Include Realistic Content** rather than placeholders
5. **Separate Examples Clearly** with visual boundaries
6. **Remember:** Perfect examples = Perfect output formatting

**Next:** Learn how to guide AI through step-by-step thinking! → **Technique 4: Chain of Thought**