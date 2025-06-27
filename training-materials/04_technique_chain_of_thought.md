# 🧠 Technique 4: Chain of Thought Prompting

> **Core Concept:** "Think Step-by-Step" — Guide AI through logical reasoning before generating final output  
> **Presentation Reference:** Also known as "Blueprint Planning Method" in training presentations

---

## 📖 **Understanding the Technique**

### **What is Chain of Thought Prompting?**

Chain of Thought (CoT) prompting is a technique where we explicitly instruct the AI to break down a complex problem into a sequence of logical steps *before* providing the final answer. Instead of asking for the result directly, we ask the AI to "show its work" and reason through the problem first.

**The Architect's Approach: Plan Before Building:** Think of creating a complex KRISA document like designing a building. An architect never starts construction without detailed blueprints. Similarly, for complex documents like SRB or multi-section SKS, we need AIDevX to create a blueprint first.

### **Why This is Critical for Government Projects**

**From a Technical Perspective:** For complex tasks like generating a full **SRB**, a direct answer requires the AI to make multiple logical inferences at once. This can lead to errors. Chain of Thought prompting constrains the model to follow a deliberate, sequential reasoning path. Each step builds on the previous one, which dramatically reduces the likelihood of logical fallacies or missed sections.

**From a Practical Perspective:** This technique allows us to validate the AI's "thinking" before it commits to an answer. It's especially useful for planning the structure of a large KRISA document or analyzing a complex business process before writing the **SKB**. It helps uncover flawed assumptions in the AI's approach early on, allowing us to course-correct.

### **When You Need Blueprint Planning:**
- Large KRISA documents (SRB with multiple technical sections)
- Complex business processes (multi-department workflows)
- System integration projects (connecting 3+ existing systems)
- Documents requiring stakeholder validation before writing

---

## 🔧 **Application in AIDevX**

This is highly effective as a preliminary step for a complex task. Use it to plan the structure of a document before asking an assistant like "Generate SRB Document" to write the full content, or to analyze a problem before generating the requirements for an **SKS**.

### **Comparison: Direct vs Blueprint Approach**

| **Direct Request (Risky)** | **Blueprint Planning (Professional)** |
|---------------------------|---------------------------------------|
| *"Generate complete SRB for mobile payment system"* | *"Before creating the SRB, first blueprint the architecture by identifying: components, integrations, data flow, and security layers"* |
| **Result:** Generic document, missing critical elements | **Result:** Validated structure, comprehensive coverage |

---

## 💡 **Real Example: FPX Payment Integration Project**

### **Scenario:** Bank Rakyat wants to integrate FPX payment into their mobile banking app

#### **❌ Ineffective Approach (Direct Request)**

```
Sila jana SRB untuk ciri pembayaran bil mudah alih.
(Please generate the SRB for a mobile bill payment feature.)
```

**Result:** The AI will generate a generic SRB, but will likely miss many specific architectural components, integration points, and security considerations relevant to a telco payment system. The structure may not fully align with KRISA.

#### **✅ Effective Approach (Blueprint Planning Method)**

```
You are a Lead Solutions Architect at Bank Rakyat Malaysia. Before creating 
the technical SRB document, please blueprint the FPX integration by analyzing:

STEP 1: Component Architecture
- Which existing bank systems will be involved?
- What new components need development?

STEP 2: Integration Touch Points  
- How will mobile app connect to core banking?
- What APIs are required for FPX gateway?
- Where does transaction logging happen?

STEP 3: Data Security Framework
- What customer data flows through the system?
- How do we ensure PDPA compliance?
- What encryption standards apply?

STEP 4: System Flow Design
- Map the complete transaction flow from user initiation to confirmation
- Identify all validation and verification points
- Detail error handling and rollback procedures

After you have clearly outlined this blueprint plan, I will review it before 
you proceed to generate the full SRB content for each section.
```

### **Expected Blueprint Output Quality**

```
Baik, saya faham. Sebelum menjana SRB penuh, berikut adalah rangka blueprint 
perancangan dan analisis saya.

**BLUEPRINT PLAN: FPX INTEGRATION ARCHITECTURE**

STEP 1: COMPONENT ARCHITECTURE
- **Mobile App Frontend:** Customer interface for payment initiation
- **API Gateway:** Single entry point, handles authentication and routing
- **Payment Service:** Core payment processing logic, communicates with external gateways
- **Notification Service:** Handles SMS/Push notifications for TAC and payment status
- **Ledger Service:** Records all financial transactions permanently
- **Audit Service:** Compliance logging for Bank Negara requirements

STEP 2: INTEGRATION TOUCH POINTS
- **Core Banking System:** Get account balance, validate customer (READ/WRITE)
- **FPX Gateway:** Initiate online banking payments (WRITE)
- **Bank Negara RENTAS:** Real-time gross settlement (WRITE)
- **SMS Gateway:** Send transaction authorization codes (WRITE)
- **Fraud Detection System:** Risk assessment and monitoring (READ/WRITE)

STEP 3: DATA SECURITY FRAMEWORK
- All API communications via HTTPS (TLS 1.2+)
- Customer data encryption at rest using AES-256
- Payment tokenization - no card details stored locally
- PDPA compliance for personal data handling
- PCI DSS Level 1 certification requirements
- End-to-end audit trails for regulatory compliance

STEP 4: SYSTEM FLOW DESIGN
1. Customer initiates payment through mobile app
2. System validates account and available balance
3. Payment request routed to FPX gateway
4. Customer redirected to bank login portal
5. Upon successful authentication, payment processed
6. Transaction confirmed and recorded in ledger
7. Customer receives confirmation via SMS and app notification
8. All transactions logged for audit and compliance

Setelah blueprint ini dipersetujui, saya akan meneruskan untuk menjana 
kandungan SRB terperinci bagi setiap seksyen.
```

**Professional Result:** The AI produces a logical, KRISA-compliant plan for the SRB. This allows the user to verify the architecture and approach *before* the AI generates the detailed content, ensuring the final SRB is comprehensive and technically sound.

---

## ⚠️ **Common Pitfalls & Best Practices**

### **✅ DO These Things**

| **Best Practice** | **Example** | **Why It Works** |
|-------------------|-------------|------------------|
| **Use for Complex KRISA Documents** | Apply for SRB creation, complex SKS planning, multi-department SKB analysis | Ensures comprehensive coverage of all components |
| **Guide the Thought Process** | Provide key areas to consider mapping to KRISA document sections | Produces structured, relevant analysis |
| **Include Government Context** | Reference Bank Negara, PDPA, ministry-specific requirements | Ensures regulatory compliance in planning |
| **Validate Before Generation** | Review blueprint before requesting full document creation | Prevents wasted effort on flawed foundations |

### **❌ AVOID These Mistakes**

| **Pitfall** | **Example** | **Why It Fails** |
|-------------|-------------|------------------|
| **Use for Simple Tasks** | "Think step-by-step: What is an SKS?" | Adds unnecessary complexity to straightforward questions |
| **Vague Instructions** | "Think step-by-step" without guidance | AI has to guess what aspects are important |
| **Skip Validation Step** | Generate full document without reviewing blueprint | May produce comprehensive but incorrect solutions |
| **Generic Planning** | No Malaysian government or regulatory context | Misses critical compliance and integration requirements |

---

## 🎮 **Practice Activity: Blueprint Planning Workshop**

### **Challenge:** Plan Before Building

#### **Government Project Scenario:**
The Ministry of Health is developing a nationwide patient referral system that connects district hospitals with specialist centers. The system must handle patient data transfer, appointment scheduling, and inter-hospital communication while ensuring PDPA compliance and integration with existing Hospital Information Systems (HIS).

#### **Your Mission:**
Working in pairs, create a blueprint planning prompt for AIDevX that breaks down this complex SKS into logical components.

**Required Blueprint Elements:**
1. **System Architecture Components** - What major system modules are needed?
2. **Integration Mapping** - How will district hospitals connect to specialist centers?
3. **Data Flow Analysis** - What patient information flows between systems and how?
4. **Compliance Framework** - What PDPA and medical data protection measures are required?
5. **Workflow Design** - How does a patient referral move from initiation to completion?

### **Your Task: Create the Blueprint Prompt**

Write a comprehensive Chain of Thought prompt that includes:
- ✅ Appropriate expert persona (Solutions Architect for healthcare systems)
- ✅ Ministry of Health project context
- ✅ Specific step-by-step blueprint instructions
- ✅ Government compliance requirements (PDPA, medical data protection)
- ✅ Integration with existing hospital systems

### **Success Criteria:**
Your blueprint prompt should guide AI to create a comprehensive plan that addresses:
- All major system components and their relationships
- Integration touchpoints with existing hospital systems
- Data security and patient privacy requirements
- Workflow processes from referral initiation to completion
- Compliance with healthcare regulations and KRISA standards

**Deliverable:** One complete blueprint planning prompt ready for AIDevX

### **Professional Outcome**
Demonstrate mastery of the architect's approach: planning complex government systems before implementation.

---

## 📝 **Quick Reference Templates**

### **Blueprint Planning Template for SRB (System Design)**

```
You are a [Expert Persona] working on [Government Project Context].

Before creating the full SRB document, please develop a comprehensive blueprint 
by analyzing the following components step-by-step:

STEP 1: SYSTEM ARCHITECTURE ANALYSIS
- Identify all major system components and their responsibilities
- Map relationships and dependencies between components
- Define technology stack and platform requirements

STEP 2: INTEGRATION MAPPING
- List all external systems that must integrate
- Define APIs, data exchange formats, and communication protocols
- Identify authentication and authorization requirements

STEP 3: DATA ARCHITECTURE DESIGN
- Map all data entities and their relationships
- Define data flow patterns and storage requirements
- Address PDPA compliance and data protection measures

STEP 4: SECURITY AND COMPLIANCE FRAMEWORK
- Detail security layers and protection mechanisms
- Address government regulatory requirements
- Define audit trails and monitoring requirements

STEP 5: OPERATIONAL CONSIDERATIONS
- Performance and scalability requirements
- Disaster recovery and business continuity
- Maintenance and support frameworks

After presenting this blueprint, await confirmation before generating the 
detailed SRB content.
```

### **Blueprint Planning Template for SKS (System Requirements)**

```
You are a [Expert Persona] analyzing [Government Project Context].

Before generating functional requirements, please blueprint the system by 
thinking through these logical steps:

STEP 1: USER ROLE ANALYSIS
- Identify all user types and their system access needs
- Map user journeys and interaction patterns
- Define permission levels and access controls

STEP 2: BUSINESS PROCESS MAPPING
- Break down core business processes into system workflows
- Identify decision points and approval mechanisms
- Map exception handling and error scenarios

STEP 3: INTEGRATION REQUIREMENTS
- List all external systems requiring connectivity
- Define data exchange requirements and formats
- Address real-time vs batch processing needs

STEP 4: COMPLIANCE AND SECURITY ANALYSIS
- Map PDPA and regulatory requirements to system features
- Define audit and logging requirements
- Address data retention and privacy controls

After this analysis, I will review before you generate the detailed functional 
requirements for the SKS.
```

---

## 🎯 **Key Takeaways**

1. **Use Blueprint Planning** for complex KRISA documents requiring comprehensive analysis
2. **Guide the Reasoning Process** with specific steps mapped to document requirements
3. **Include Government Context** with regulatory and compliance considerations
4. **Validate Before Building** - review blueprints before generating full content
5. **Break Down Complexity** into manageable, logical components
6. **Address Integration Early** in the planning phase for government systems
7. **Remember:** Good blueprints lead to excellent government-ready documentation

**Professional Principle:** Blueprint planning ensures comprehensive coverage and allows validation before detailed writing, preventing costly revisions.

**Next:** Learn how to refine and perfect your AI outputs! → **Technique 5: Iterative Prompting** *(also presented as "Professional Refinement Process")* 