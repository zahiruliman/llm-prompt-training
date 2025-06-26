# 🎭 Technique 1: The Persona Pattern

> **Core Concept:** "Wear This Hat" — Assign specific professional roles to guide AI responses

---

## 📖 **Understanding the Technique**

### **What is the Persona Pattern?**

The Persona Pattern is a foundational prompting technique where you instruct the AI to adopt a specific professional role or expertise. Instead of getting generic responses, you're essentially "hiring" a virtual expert for your task.

**Think of it like this:** Rather than asking "anyone" for advice, you're specifically consulting a Senior Business Analyst, Lead System Architect, or Security Specialist.

### **Why Does This Work?**

| **Technical Perspective** | **Practical Impact** |
|---------------------------|---------------------|
| AI models are trained on vast datasets of professional content | **Better focus** on domain-specific knowledge |
| Assigning roles activates relevant patterns in the AI's training | **Appropriate terminology** and professional language |
| Personas constrain the AI's responses to expert-level outputs | **Structured formatting** matching professional standards |

---

## 🎯 **Benefits for BAs and SAs**

When you assign the right persona to AI, you get:

> ✅ **Increased Relevance** — Information specific to your professional domain  
> ✅ **Appropriate Tone** — Formal, professional communication style  
> ✅ **Domain Formatting** — Document structures that match industry standards  
> ✅ **Expert-Level Depth** — Considerations a generalist might miss

---

## 🔧 **Application in AIDevX**

### **Best Practice Workflow**

```
Step 1: Choose AIDevX Assistant (Generate Requirements, SRS > SDS, etc.)
Step 2: Start with persona assignment
Step 3: Provide your specific request
Step 4: Review and refine as needed
```

### **Persona Matching for KRISA Documents**

| **Document Type** | **Recommended Persona** | **Expertise Focus** |
|-------------------|------------------------|-------------------|
| **📄 SKB** (Business Requirements) | Senior Business Analyst | Stakeholder needs, business goals, compliance |
| **📄 SKS** (System Requirements) | Lead System Analyst | Technical specifications, functional requirements |
| **📄 SRB** (System Design) | Solutions Architect | System architecture, technical design patterns |

---

## 💡 **Practical Example: Malaysian Government Context**

### **Scenario:** Creating system requirements for a new government service portal

#### **❌ Ineffective Approach (No Persona)**

```
Tolong tuliskan senarai keperluan untuk laman pendaftaran pengguna.
(Please write a list of requirements for a user registration page.)
```

**Result:** Basic, incomplete requirements missing security and compliance considerations.

#### **✅ Effective Approach (With Persona)**

```
Anda ialah seorang Penganalisis Sistem Kanan (Senior System Analyst) yang 
berkhidmat di unit teknikal sebuah agensi kerajaan Malaysia. Anda mempunyai 
pengalaman luas dalam membangunkan sistem e-Kerajaan yang selamat dan mesra 
pengguna, selaras dengan piawaian KRISA.

Sila jana draf Spesifikasi Keperluan Sistem (SKS) untuk modul Pendaftaran 
Pengguna bagi portal MyServices yang baharu. Pastikan ia merangkumi Keperluan 
Fungsian dan Bukan Fungsian.

(You are a Senior System Analyst working in the technical unit of a Malaysian 
government agency. You have extensive experience in developing secure and 
user-friendly e-Government systems, in line with KRISA standards.

Please generate a draft System Requirement Specification (SKS) for the User 
Registration module of the new MyServices portal. Ensure it covers both 
Functional and Non-Functional Requirements.)
```

### **Sample Output Quality**

The persona-driven approach produces requirements that include:

- ✅ MyKad validation protocols
- ✅ PDPA compliance measures  
- ✅ Single sign-on (SSO) integration
- ✅ WCAG accessibility standards
- ✅ Security encryption requirements

---

## ⚠️ **Common Pitfalls & Best Practices**

### **✅ DO These Things**

| **Best Practice** | **Example** | **Why It Works** |
|-------------------|-------------|------------------|
| **Be Specific** | "Senior Business Analyst specializing in public sector financial systems" | Narrow focus produces expert-level outputs |
| **Match Role to Document** | Business Analyst for SKB, System Analyst for SKS | Aligned expertise for appropriate content |
| **Include Experience Level** | "15 years of experience in Malaysian government projects" | Establishes credibility and depth |

### **❌ AVOID These Mistakes**

| **Pitfall** | **Example** | **Why It Fails** |
|-------------|-------------|------------------|
| **Too Vague** | "Act as a BA" | Lacks focus and expertise depth |
| **Wrong Persona** | "Marketing manager writing technical requirements" | Mismatched expertise leads to poor results |
| **No Context** | "You are an analyst" | Generic responses without domain knowledge |

---

## 🎮 **Practice Activity: Persona Matching**

### **Challenge:** Match the Expert to the Task

**Scenario:** You're working on a new e-procurement system for a government agency.

#### **Tasks to Complete:**

| **Task** | **Options** | **Your Choice** |
|----------|-------------|----------------|
| **Draft SKB** for business objectives | A) Java Developer<br/>B) Senior Business Analyst<br/>C) UI/UX Designer | _____ |
| **Create SKS** for system specifications | A) Project Manager<br/>B) Lead System Analyst<br/>C) Database Administrator | _____ |
| **Design SRB** for system architecture | A) Solutions Architect<br/>B) Business Analyst<br/>C) QA Tester | _____ |

### **Discussion Points**

> 💭 **Think About:** Why does the right persona matter for KRISA compliance?  
> 💭 **Consider:** How would a wrong persona affect document quality?  
> 💭 **Reflect:** What specific expertise does each role bring to documentation?

---

## 📝 **Quick Reference Template**

### **Copy-Paste Persona Starters**

**For SKB (Business Requirements):**
```
You are a Senior Business Analyst with [X] years of experience in Malaysian 
[sector] projects, specializing in KRISA-compliant documentation. Your task 
is to create a comprehensive Spesifikasi Keperluan Bisnes (SKB) that focuses 
on stakeholder needs and business objectives.
```

**For SKS (System Requirements):**
```
You are a Lead System Analyst with extensive experience in Malaysian government 
e-services development. You specialize in creating detailed technical 
specifications following KRISA standards. Your task is to generate a 
Spesifikasi Keperluan Sistem (SKS) with comprehensive functional and 
non-functional requirements.
```

**For SRB (System Design):**
```
You are a Solutions Architect with deep expertise in government-grade system 
design. You have [X] years of experience creating secure, scalable architectures 
for Malaysian public sector applications. Your task is to develop a 
Spesifikasi Rekabentuk Sistem (SRB) following KRISA guidelines.
```

---

## 🎯 **Key Takeaways**

1. **Start Every Request** with a clear, specific persona assignment
2. **Match Expertise** to the document type you're creating  
3. **Be Specific** about experience level and domain knowledge
4. **Align with KRISA** standards for government documentation
5. **Remember:** The right persona is the foundation of quality output

**Next:** Learn how to provide comprehensive context to your chosen persona! → **Technique 2: Contextual Scaffolding**