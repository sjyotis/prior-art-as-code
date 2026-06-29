# Prior Art as Code: A Practical Guide

## Protect your open source project from patent trolls by embedding prior art in your repository

---

## 1. What Is Prior Art?

Prior art is any public evidence that an invention already exists. Under US law (35 U.S.C. § 102(a)(1)), an invention cannot be patented if it was "described in a printed publication" before the filing date. Under European law (EPC Article 54(2)), the state of the art includes "everything made available to the public" before filing. The EPO's G 1/23 decision (2025) clarified that public availability alone is sufficient – no reproducibility required.

**Prior art proves the invention was already known.** That makes any later patent invalid.

---

## 2. Why Prior Art Matters for Open Source

Open source projects are prime targets for patent trolls because:

| Threat | Why It Matters |
|--------|----------------|
| Code is public | Trolls can scan for novel inventions |
| No patent budget | Most open source projects cannot afford to file or defend patents |
| No legal team | Individual contributors are vulnerable to lawsuits |

**The solution is prior art.** It costs nothing, requires no legal fees, and blocks patents before they are filed.

---

## 3. The Problem with Traditional Defensive Publications

| Problem | Why It Fails |
|---------|--------------|
| Separate from code | Hard to find, easy to ignore |
| Expensive | Many services charge fees (IP.com, etc.) |
| Static | Rarely updated |
| Not enabling | Vague descriptions do not convince examiners |
| Unverifiable | No working code to prove the invention works |

**Traditional defensive publications are weak prior art.**

---

## 4. Prior Art as Code: A Better Approach

Prior art as code embeds prior art directly in your source repository. It provides:

| Feature | Benefit |
|---------|---------|
| **Integrated with code** | Documents live alongside the implementation |
| **Timestamped by Git** | Immutable proof of publication date |
| **Enabling disclosure** | Enough detail to re‑implement the invention |
| **Verifiable** | Working code is the evidence |
| **Free** | Public repositories cost nothing |
| **Searchable** | Patent examiners can find it |

**This is stronger prior art.** It is enabling, verifiable, and timestamped.

---

## 5. Example: Thought OS

**Thought OS** is a real open source project that uses this approach. Its repository contains a comprehensive prior art document with various disclosed concepts, including:

- UUID permanence (items keep identity across renames)
- Hardware binding without TPM
- Resurrection from Git history
- Active cache validation

Each concept is described in its own separate document, making it easy to update, reference, and understand individually. The main document indexes them all. This modular approach is recommended for complex projects.

*For reference: [github.com/sjyotis/thought-os](github.com/sjyotis/thought-os)*

---

## 6. The Prior Art Document Itself Is Sufficient

**The prior art document alone, with working code and a timestamp, is sufficient to establish prior art and invalidate later patents.** The law itself provides the protection – 35 U.S.C. § 102(a)(1) and EPC Article 54(2) invalidate any patent that claims an invention already disclosed.

---

## 7. How to Implement Prior Art as Code

### Step 1: Identify Your Novel Inventions

Ask: "What would I be angry about if someone else patented?"

### Step 2: Write an Enabling Description

Include:

- Plain language summary
- Technical specification (data structures, algorithms, protocols)
- Code references (files and line numbers)
- Diagrams (flowcharts, sequence diagrams)

### Step 3: Create Prior Art Documents

For simple projects, a single `PRIOR_ART_DISCLOSURE.md` is enough. For complex projects with multiple independent features, create **separate documents per concept** in a `docs/` folder (e.g., `docs/resurrection-engine.md`, `docs/hardware-binding.md`). Use a main `PRIOR_ART_DISCLOSURE.md` as an index linking to each.

### Step 4: Timestamp with Git

Commit the documents with a message like `docs: add prior art disclosure`. The commit timestamp proves publication date.

### Step 5: Link It in Your README

Make the prior art document easy to find. Patent examiners need to discover it.

### Step 6: Publish Publicly

Push to a public repository (GitHub, GitLab, etc.). Public availability is what matters.

---

## 8. Suggested Platforms for Publication

| Platform | Best For | Notes |
|----------|----------|-------|
| **GitHub** | Source code + documents | The standard for open source; patent examiners search here |
| **GitLab** | Source code + documents | Alternative to GitHub; also searchable |
| **SourceForge** | Source code + documents | Legacy platform, still indexed |
| **IP.com** | Prior art submission | Paid service, submitted to patent offices |
| **Zenodo** | Document publication | Assigns DOI (persistent identifier) |
| **arXiv** | Technical papers | Academic-style prior art |
| **Hacker News** | Project announcements | Creates social timestamp |
| **Dev.to** | Technical articles | Searchable, indexed by Google |

**Best practice:** Publish on GitHub + one other platform (e.g., Zenodo) for redundancy.

---

## 9. Optional: Patent‑Prohibiting License

While the prior art document alone is sufficient to invalidate later patents, you may choose to add an explicit patent‑prohibiting license. Such a license:

- Explicitly forbids patenting of the disclosed concepts
- Provides a separate legal basis (contract law) to challenge a patent
- Sends a clear signal that the technology belongs to no one

It is **optional**. The prior art is the shield. The license is an extra lock on the gate.

---

## 10. Why Prior Art as Code Is Stronger

| Aspect | Traditional Prior Art | Prior Art as Code |
|--------|----------------------|-------------------|
| Cost | Paid | Free |
| Integration | Separate | Integrated with code |
| Timestamp | Manual | Git commits |
| Enabling | Often vague | Detailed, with code |
| Verifiable | Hard | Working code is evidence |
| Modularity | Single document | Separate files per concept |

**Prior art as code is stronger because it provides all the evidence needed.**

---

## 11. Conclusion

Prior art as code is a free, effective way to protect open source projects from patents. It works by:

1. Establishing a public, timestamped, enabling disclosure
2. Referencing the actual working code

**The prior art document itself is sufficient.** The law (35 U.S.C. § 102(a)(1), EPC Article 54(2)) invalidates any later patent claiming the disclosed concepts. A patent‑prohibiting license is optional – it adds an extra layer but is not required.

**Every open source project should consider prior art as code.** It costs nothing. It blocks patents. It protects innovation.

---

**sjyotis**  
June 2026  
thought-os@protonmail.com
