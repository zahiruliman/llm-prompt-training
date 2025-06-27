# 🎭 Technique 1: The Persona Pattern

> **Core Concept:** "Wear This Hat" — Assign specific professional roles to guide AI responses  
> **Presentation Reference:** Also known as "Expert Persona Strategy" in training presentations

---

## 📖 **Understanding the Technique**

### **What is the Persona Pattern?**

The Persona Pattern is a foundational prompting technique where you instruct the AI to adopt a specific professional role or expertise. Instead of getting generic responses, you're essentially "hiring" a virtual expert for your task.

**Think of it like this:** Rather than asking "anyone" for advice, you're specifically consulting a Senior Business Analyst, Lead System Architect, or Security Specialist.

**Professional Consultant Approach:** When you hire a consultant for a critical government project, you choose someone with specific expertise, experience, and domain knowledge. The same principle applies to AIDevX - you must define the expert persona who will create your KRISA documents.

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

### **Strategic Persona Selection for KRISA Documents**

| **Document Type** | **Recommended Persona** | **Expertise Focus** |
|-------------------|------------------------|-------------------|
| **📄 SKB** (Business Requirements) | Senior Business Analyst with extensive experience in Malaysian public sector digital transformation projects | Deep understanding of government stakeholder needs, knowledge of regulatory compliance requirements, experience with citizen service design |
| **📄 SKS** (System Requirements) | Lead System Analyst specializing in government enterprise architecture | Technical expertise in integration with existing government systems, understanding of security and compliance frameworks, experience with KRISA methodology |
| **📄 SRB** (System Design) | Solutions Architect with focus on Malaysian government technology stack | Knowledge of approved technology standards, experience with government-scale system design, understanding of inter-agency integration requirements |

**Professional Principle:** The more specific and relevant your expert persona, the more professional and applicable your document output.

---

## 💡 **Practical Example: Malaysian Government Context**

### **Impact of Expert Persona Selection**

#### **❌ Ineffective Approach (No Persona)**

```
"Write requirements for a login system."
```

**Result:** Generic, one-size-fits-all requirements lacking government context

#### **✅ Effective Approach (With Expert Persona)**

```
"You are a Senior System Analyst with 15 years of experience in Malaysian 
government digital services, specializing in KRISA-compliant documentation 
and PDPA compliance.

Generate functional requirements for the MyKad-based authentication module 
of the new citizen services portal, ensuring alignment with National 
Cybersecurity Policy and Bank Negara guidelines."
```

**Result:** Government-specific, compliance-ready, professionally structured requirements

### **Extended Example: Ministry of Health E-Prescription System**

**Real-World Scenario:** The Ministry of Health is developing a nationwide e-prescription system that will connect hospitals, clinics, and pharmacies across Malaysia. This system must integrate with existing hospital management systems, comply with medical data protection regulations, and support both MyKad and foreign patient identification.

**Project Complexity:**
- 500+ healthcare facilities to integrate
- Real-time prescription verification across systems  
- Medical data privacy compliance (PDPA + healthcare regulations)
- Integration with National Pharmaceutical Database
- Multi-language support (Bahasa Malaysia, English, Chinese, Tamil)

**Expert Persona Selection Challenge:**

**DOCUMENT 1: SKB (Business Requirements)**
*Who should define the business objectives and stakeholder needs?*

**✅ CORRECT:** Senior Business Analyst with 10+ years in Malaysian healthcare digitization projects  
**❌ INCORRECT:** Healthcare IT Specialist with programming background  
**❌ INCORRECT:** Medical Doctor with basic IT knowledge

**DOCUMENT 2: SKS (System Requirements)**  
*Who should detail the technical specifications and integration requirements?*

**✅ CORRECT:** Lead System Analyst specializing in healthcare enterprise systems integration  
**❌ INCORRECT:** Project Manager with general technology oversight experience  
**❌ INCORRECT:** Database Administrator with hospital system experience

**DOCUMENT 3: SRB (System Design)**
*Who should architect the technical solution and system design?*

**✅ CORRECT:** Solutions Architect with expertise in large-scale government healthcare technology  
**❌ INCORRECT:** Senior Business Analyst with healthcare domain knowledge  
**❌ INCORRECT:** Software Testing Lead with healthcare system experience

### **Sample Output Quality**

The persona-driven approach produces requirements that include:

- ✅ MyKad validation protocols
- ✅ PDPA compliance measures  
- ✅ Single sign-on (SSO) integration
- ✅ WCAG accessibility standards
- ✅ Security encryption requirements
- ✅ Healthcare-specific audit trails
- ✅ Multi-language support requirements
- ✅ Real-time prescription verification protocols

---

## ⚠️ **Common Pitfalls & Best Practices**

### **✅ DO These Things**

| **Best Practice** | **Example** | **Why It Works** |
|-------------------|-------------|------------------|
| **Be Specific** | "Senior Business Analyst specializing in public sector financial systems" | Narrow focus produces expert-level outputs |
| **Match Role to Document** | Business Analyst for SKB, System Analyst for SKS | Aligned expertise for appropriate content |
| **Include Experience Level** | "15 years of experience in Malaysian government projects" | Establishes credibility and depth |
| **Specify Domain Knowledge** | "Specializing in KRISA-compliant documentation and PDPA compliance" | Ensures relevant regulatory understanding |

### **❌ AVOID These Mistakes**

| **Pitfall** | **Example** | **Why It Fails** |
|-------------|-------------|------------------|
| **Too Vague** | "Act as a BA" | Lacks focus and expertise depth |
| **Wrong Persona** | "Marketing manager writing technical requirements" | Mismatched expertise leads to poor results |
| **No Context** | "You are an analyst" | Generic responses without domain knowledge |
| **Missing Government Context** | "You are a system analyst" (without Malaysian government focus) | Lacks regulatory and compliance awareness |

---

## 🎮 **Practice Activity: Expert Persona Matching**

### **Challenge:** Match the Expert to the Task

**Scenario:** You're working on a new e-procurement system for a government agency.

#### **Tasks to Complete:**

| **Task** | **Options** | **Your Choice** |
|----------|-------------|----------------|
| **Draft SKB** for business objectives | A) Java Developer<br/>B) Senior Business Analyst<br/>C) UI/UX Designer | **B** |
| **Create SKS** for system specifications | A) Project Manager<br/>B) Lead System Analyst<br/>C) Database Administrator | **B** |
| **Design SRB** for system architecture | A) Solutions Architect<br/>B) Business Analyst<br/>C) QA Tester | **A** |

### **Discussion Points**

> 💭 **Think About:** Why does the right persona matter for KRISA compliance?  
> 💭 **Consider:** How would a wrong persona affect document quality?  
> 💭 **Reflect:** What specific expertise does each role bring to documentation?  
> 💭 **Analyze:** How does expert selection impact the quality and compliance readiness of your KRISA documents?

---

## 📝 **Quick Reference Template**

### **Copy-Paste Persona Starters**

**For SKB (Business Requirements):**
```
You are a Senior Business Analyst with [X] years of experience in Malaysian 
public sector digital transformation projects, specializing in KRISA-compliant 
documentation. You have deep understanding of government stakeholder needs, 
knowledge of regulatory compliance requirements, and experience with citizen 
service design. Your task is to create a comprehensive Spesifikasi Keperluan 
Bisnes (SKB) that focuses on stakeholder needs and business objectives.
```

**For SKS (System Requirements):**
```
You are a Lead System Analyst specializing in government enterprise architecture 
with extensive experience in Malaysian government e-services development. You have 
technical expertise in integration with existing government systems, understanding 
of security and compliance frameworks, and experience with KRISA methodology. 
Your task is to generate a Spesifikasi Keperluan Sistem (SKS) with comprehensive 
functional and non-functional requirements.
```

**For SRB (System Design):**
```
You are a Solutions Architect with focus on Malaysian government technology stack 
and deep expertise in government-grade system design. You have [X] years of 
experience creating secure, scalable architectures for Malaysian public sector 
applications with knowledge of approved technology standards and understanding 
of inter-agency integration requirements. Your task is to develop a Spesifikasi 
Rekabentuk Sistem (SRB) following KRISA guidelines.
```

---

## 🎯 **Key Takeaways**

1. **Start Every Request** with a clear, specific persona assignment
2. **Match Expertise** to the document type you're creating  
3. **Be Specific** about experience level and domain knowledge
4. **Align with KRISA** standards for government documentation
5. **Include Malaysian Government Context** for compliance readiness
6. **Remember:** The right persona is the foundation of quality output

**Professional Principle:** Expert persona selection directly impacts the quality and compliance readiness of your KRISA documents.

**Next:** Learn how to provide comprehensive context to your chosen persona! → **Technique 2: Contextual Scaffolding** *(also presented as "Project Intelligence Framework")*