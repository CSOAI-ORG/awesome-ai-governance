# Awesome AI Governance [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> A curated list of frameworks, tools, standards, and resources for governing AI systems responsibly.

AI governance is no longer optional. As AI systems move from labs into production — powering decisions about credit, healthcare, hiring, and safety — organizations need concrete tools to ensure these systems are fair, transparent, accountable, and aligned with human values.

This list covers the full stack of AI governance: from high-level policy frameworks and risk management standards, to practical tooling for bias detection, explainability, model monitoring, and compliance. Whether you're a compliance officer implementing the EU AI Act, an ML engineer building responsible AI pipelines, or a researcher studying algorithmic fairness — you'll find something useful here.

**Contributions welcome!** See [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines.

---

## Contents

- [Governance Frameworks](#governance-frameworks)
- [Risk Management](#risk-management)
- [Standards & Regulations](#standards--regulations)
- [Fairness & Bias](#fairness--bias)
- [Explainability & Interpretability](#explainability--interpretability)
- [Privacy & Security](#privacy--security)
- [Model Evaluation & Benchmarking](#model-evaluation--benchmarking)
- [Monitoring & Observability](#monitoring--observability)
- [Audit & Compliance Tools](#audit--compliance-tools)
- [Ethics & Responsible AI](#ethics--responsible-ai)
- [Organizations & Initiatives](#organizations--initiatives)
- [Research & Papers](#research--papers)
- [Courses & Learning](#courses--learning)
- [Books](#books)
- [Newsletters & Communities](#newsletters--communities)

---

## Governance Frameworks

Frameworks that provide structured approaches to AI governance across the AI lifecycle.

- [NIST AI Risk Management Framework (AI RMF 1.0)](https://www.nist.gov/itl/ai-risk-management-framework) - The gold standard US framework. Four core functions: Govern, Map, Measure, Manage. Freely available with companion playbook and profiles.
- [OECD AI Principles](https://oecd.ai/en/ai-principles) - The first intergovernmental standard on AI (2019). Adopted by 46+ countries. Five value-based principles and five recommendations for policymakers.
- [UNESCO Recommendation on the Ethics of AI](https://www.unesco.org/en/artificial-intelligence/recommendation-ethics) - The first global standard-setting instrument on AI ethics. Adopted by 193 member states. Covers human rights, environment, gender, and data governance.
- [Microsoft Responsible AI Standard v2](https://www.microsoft.com/en-us/ai/responsible-ai) - Practical goals and requirements across six principles: fairness, reliability & safety, privacy & security, inclusiveness, transparency, accountability.
- [Google AI Principles](https://ai.google/responsibility/principles/) - Seven principles guiding Google's AI development, with published progress reviews and governance structures.
- [IBM AI Governance Framework](https://www.ibm.com/watson/responsible-ai) - Enterprise framework covering ethics boards, risk assessment methodologies, and AI FactSheets.
- [Singapore Model AI Governance Framework](https://www.pdpc.gov.sg/help-and-resources/2020/01/model-ai-governance-framework) - Practical guidance for private sector organizations. Includes implementation and self-assessment guide.
- [Canada Algorithmic Impact Assessment (AIA)](https://www.canada.ca/en/government/system/digital-government/digital-government-innovations/responsible-use-ai/algorithmic-impact-assessment.html) - Mandatory questionnaire for Canadian federal agencies deploying automated decision systems. Scores impact level and recommends mitigations.
- [Council of AI GSPC](https://doi.org/10.5281/zenodo.18383474) - Production governance scorecard: 22 axis · 15 measured. Open methodology + public score artifacts (Zenodo DOI).
- [Beijing AI Principles](https://www.baai.ac.cn/news/beijing-ai-principles-en.html) - Developed by the Beijing Academy of AI. Covers research, development, use, and governance of AI.
- [Tokyo Guidelines for AI Governance](https://www.soumu.go.jp/main_sosiki/joho_tsusin/eng/presentation.html) - Japan's Soft Law approach to AI governance emphasizing human-centric AI.

## Risk Management

Tools and methodologies for identifying, assessing, and mitigating AI risks.

- [MIT AI Risk Repository](https://airisk.mit.edu/) - Living database of 1000+ AI risks extracted from literature, taxonomized into causal and domain frameworks. Searchable and regularly updated.
- [AI Incident Database (AIID)](https://incidentdatabase.ai/) - Crowdsourced collection of AI failure incidents. Searchable by harm type, sector, and system. Essential for risk identification.
- [AI Vulnerability Database (AVID)](https://avidml.org/) - Structured vulnerability database for AI systems covering security, ethics, and performance failures. Includes enumeration and taxonomy.
- [OWASP Top 10 for LLM Applications](https://owasp.org/www-project-top-10-for-large-language-model-applications/) - The definitive list of critical vulnerabilities in LLM apps: prompt injection, data leakage, supply chain, insecure output handling, and more.
- [OWASP AI Exchange](https://owaspai.org/) - Comprehensive AI security and privacy guidance. Covers threat modeling, controls, and risk assessment for AI systems.
- [Giskard](https://github.com/Giskard-AI/giskard) - Open-source vulnerability scanner for AI models. Automatically detects performance, bias, and security issues. Python library + CI/CD integration.
- [Robust Intelligence (CISCO)](https://www.robustintelligence.com/) - AI firewall and continuous validation platform. Tests models against adversarial attacks, data drift, and performance degradation.
- [Adversa AI](https://adversa.ai/) - Adversarial robustness testing and red-teaming platform for AI/ML systems.
- [Microsoft Counterfit](https://github.com/Azure/counterfit) - Open-source automation tool for security testing AI systems. Supports multiple attack frameworks (ART, TextAttack, etc.).
- [IBM Adversarial Robustness Toolbox (ART)](https://github.com/Trusted-AI/adversarial-robustness-toolbox) - Python library with adversarial attacks, defenses, and robustness metrics for all major ML frameworks.
- [CleverHans](https://github.com/cleverhans-lab/cleverhans) - Adversarial example library for benchmarking ML systems against attacks. Supports JAX, PyTorch, and TF.
- [AI Verify](https://aiverify.sg/) - Singapore's open-source AI governance testing framework. Technical tests + process checks aligned to their Model Governance Framework.

## Standards & Regulations

Key regulatory frameworks and technical standards shaping AI governance globally.

### Regulations

- [EU AI Act](https://artificialintelligenceact.eu/) - The world's first comprehensive AI regulation. Risk-based approach: prohibited, high-risk, limited-risk, minimal-risk. Full applicability 2026/2027.
- [EU AI Act Implementation Timeline](https://artificialintelligenceact.eu/implementation-timeline/) - Track key dates for prohibitions, GPAI obligations, high-risk requirements, and penalties.
- [US Executive Order 14110](https://www.whitehouse.gov/briefing-room/presidential-actions/2023/10/30/executive-order-on-the-safe-secure-and-trustworthy-development-and-use-of-artificial-intelligence/) - Biden's EO on Safe, Secure, and Trustworthy AI. Directs NIST, DoD, DOE, and other agencies on AI safety standards.
- [US OMB Memo M-24-10](https://www.whitehouse.gov/wp-content/uploads/2024/03/M-24-10-Advancing-Governance-Management-and-Accountability-in-AI-Agency-Use.pdf) - Requirements for US federal agencies on AI governance, including impact assessments and rights-impacting AI.
- [UK AI Safety Institute](https://www.aisi.gov.uk/) - Government body for evaluating advanced AI systems. Publishes safety research and evaluation methodologies.
- [China Interim Measures for Generative AI](http://www.cac.gov.cn/2023-07/13/c_1690898327029107.htm) - Cyberspace Administration of China rules for generative AI services. Requires security assessments and content labeling.
- [Brazil AI Bill](https://www.camara.leg.br/proposicoesWeb/fichadetramitacao?idProposicao=2236340) - Proposed comprehensive AI legislation following a risk-based approach similar to the EU AI Act.
- [Canada AIDA](https://ised-isde.canada.ca/site/innovation-better-canada/en/artificial-intelligence-and-data-act) - Artificial Intelligence and Data Act. Part of Bill C-27. Regulates high-impact AI systems.
- [Colorado SB 24-205](https://leg.colorado.gov/bills/sb24-205) - First comprehensive US state AI law. Requires developers and deployers of high-risk AI to use reasonable care to avoid algorithmic discrimination.

### Technical Standards

- [ISO/IEC 42001:2023](https://www.iso.org/standard/81284.html) - First international AI management system standard. Certifiable. Covers policy, risk assessment, and continuous improvement for AI systems.
- [ISO/IEC 23894:2023](https://www.iso.org/standard/77304.html) - AI risk management guidance standard. Complements ISO 31000 for AI-specific risks.
- [ISO/IEC 23053:2022](https://www.iso.org/standard/74438.html) - Framework for AI systems using ML. Establishes common terminology and understanding.
- [ISO/IEC TR 24028:2020](https://www.iso.org/standard/77608.html) - Overview of trustworthiness in AI systems covering reliability, transparency, privacy, and accountability.
- [IEEE 7000-2021](https://standards.ieee.org/ieee/7000/6781/) - Model process for addressing ethical concerns during system design. Integrates ethics into engineering lifecycle.
- [IEEE 7001-2021](https://standards.ieee.org/ieee/7001/6929/) - Transparency of autonomous systems. Measurable levels of transparency for different stakeholders.
- [IEEE CertifaiEd](https://engagestandards.ieee.org/ieeecertifaied.html) - Certification program for AI ethics based on IEEE ethics standards.
- [NIST AI 100-1](https://nvlpubs.nist.gov/nistpubs/ai/NIST.AI.100-1.pdf) - AI RMF 1.0 official publication.
- [NIST AI 600-1](https://www.nist.gov/publications/artificial-intelligence-risk-management-framework-generative-artificial-intelligence) - Generative AI Profile for the AI RMF. Specific risks and actions for GenAI systems.
- [CEN-CENELEC JTC 21](https://www.cencenelec.eu/areas-of-work/cen-cenelec-topics/artificial-intelligence/) - European standards body developing harmonized standards to support EU AI Act conformity.

## Fairness & Bias

Tools and research for detecting, measuring, and mitigating bias in AI systems.

### Open Source Tools

- [Fairlearn](https://github.com/fairlearn/fairlearn) - Microsoft's Python toolkit for assessing and improving fairness. Metrics, mitigation algorithms, and visualization dashboards.
- [AIF360](https://github.com/Trusted-AI/AIF360) - IBM's comprehensive bias detection and mitigation toolkit. 70+ fairness metrics, 10+ mitigation algorithms. Supports pre/in/post-processing.
- [Aequitas](https://github.com/dssg/aequitas) - University of Chicago bias audit toolkit. Generates bias reports for ML models across protected groups. Used by governments.
- [What-If Tool](https://pair-code.github.io/what-if-tool/) - Google's interactive visual tool for probing ML models. Explore counterfactuals, fairness metrics, and feature importance without coding.
- [Fairness Indicators](https://github.com/tensorflow/fairness-indicators) - TensorFlow tool for computing fairness metrics at scale. Integrates with TensorBoard.
- [LiFT](https://github.com/linkedin/LiFT) - LinkedIn Fairness Toolkit. Scala/Spark library for measuring and mitigating bias in large-scale ML workflows.
- [Themis](https://github.com/LASER-UMASS/Themis) - Discrimination testing tool for software systems. Measures causal and group discrimination.
- [RESPONSIBLEAI](https://github.com/microsoft/responsible-ai-toolbox) - Microsoft's Responsible AI Toolbox. Integrated dashboard combining Fairlearn, InterpretML, Error Analysis, and Causal Inference.
- [holisticai](https://github.com/holistic-ai/holisticai) - Bias and mitigation toolkit with focus on practical industry use cases. Clean API covering classification, regression, clustering, and recommendation.

### Datasets for Bias Testing

- [Adult (Census Income)](https://archive.ics.uci.edu/dataset/2/adult) - Classic fairness benchmark. Predict income with gender/race as sensitive attributes.
- [COMPAS](https://github.com/propublica/compas-analysis) - ProPublica's recidivism dataset. The dataset that sparked the modern algorithmic fairness debate.
- [German Credit](https://archive.ics.uci.edu/dataset/144/statlog+german+credit+data) - Credit risk dataset with gender and age as potential sensitive attributes.
- [MIMIC-IV](https://mimic.mit.edu/) - Critical care dataset used extensively for healthcare AI fairness research.
- [HateXplain](https://huggingface.co/datasets/Hate-speech-CNERG/hatexplain) - Hate speech detection dataset with human rationales and target group annotations.
- [Bias in Bios](https://github.com/Microsoft/biosbias) - Biography dataset for studying gender bias in occupation classification.

## Explainability & Interpretability

Tools for understanding and explaining AI model decisions.

### Model-Agnostic Methods

- [SHAP](https://github.com/shap/shap) - The gold standard for feature attribution. Unified framework based on Shapley values. Works with any model. TreeSHAP is exceptionally fast.
- [LIME](https://github.com/marcotcr/lime) - Local Interpretable Model-agnostic Explanations. Explains individual predictions by fitting local surrogate models.
- [Anchors](https://github.com/marcotcr/anchor) - High-precision model-agnostic explanations. Finds IF-THEN rules that "anchor" a prediction.
- [Alibi](https://github.com/SeldonIO/alibi) - Seldon's open-source Python library covering black-box and white-box explanations, counterfactuals, and influence functions.
- [InterpretML](https://github.com/interpretml/interpret) - Microsoft's toolkit. Includes Explainable Boosting Machine (EBM) — an interpretable glass-box model that rivals black-box accuracy.
- [DALEX](https://github.com/ModelOriented/DALEX) - Model-agnostic exploration and explanation. Strong on comparative analysis across models. R and Python.
- [OmniXAI](https://github.com/salesforce/OmniXAI) - Salesforce's comprehensive explainability library. Supports tabular, vision, NLP, and time-series. Multiple explanation methods in one API.

### Model-Specific & Neural Methods

- [Captum](https://github.com/pytorch/captum) - PyTorch's official interpretability library. Integrated gradients, occlusion, GradCAM, Layer Conductance, and more.
- [Lucent](https://github.com/tensorflow/lucid) - Feature visualization for neural networks. Descendant of GoogLean's Lucid library.
- [Transformer Interpretability](https://github.com/hila-chefer/Transformer-Explainability) - Attention-based and gradient-based explanation methods specifically for transformer architectures.
- [BertViz](https://github.com/jessevig/bertviz) - Interactive visualization of attention in transformer models (BERT, GPT-2, etc.).
- [ecco](https://github.com/jalammar/ecco) - NLP model introspection. Visualizes input saliency, layer evolution, and neuron activations.

### Explanation Management

- [AI Explainability 360](https://github.com/Trusted-AI/AIX360) - IBM's toolkit with 10+ explanation algorithms and explanation metrics. Includes formal taxonomy of explainability.
- [Quantus](https://github.com/understandable-machine-intelligence-lab/Quantus) - Evaluation framework for explanation quality. 30+ metrics measuring faithfulness, robustness, localization, and complexity.

## Privacy & Security

Tools and frameworks for privacy-preserving AI and AI security.

### Privacy-Preserving ML

- [Opacus](https://github.com/pytorch/opacus) - PyTorch library for training models with Differential Privacy. Maintained by Meta AI.
- [TensorFlow Privacy](https://github.com/tensorflow/privacy) - Differential privacy tools for TensorFlow. DP-SGD Optimizer and privacy accounting.
- [PySyft](https://github.com/OpenMined/PySyft) - OpenMined's stack for private, secure computation. Federated learning, differential privacy, and encrypted computation.
- [Flower](https://flower.ai/) - Friendly federated learning framework. Works with PyTorch, TensorFlow, JAX, Hugging Face.  Framework-agnostic.
- [NVIDIA FLARE](https://github.com/NVIDIA/NVFlare) - Enterprise federated learning. Used in healthcare (including multi-hospital studies). Privacy filters and secure aggregation.
- [CrypTen](https://github.com/facebookresearch/CrypTen) - Privacy-preserving ML framework by Meta using secure multiparty computation.
- [TF Encrypted](https://github.com/tf-encrypted/tf-encrypted) - Encrypted deep learning in TensorFlow. Secure computation with cryptographic protocols.
- [duet](https://github.com/OpenMined/PySyft) - OpenMined's peer-to-peer privacy-preserving data science framework (part of PySyft ecosystem).

### AI Security

- [Garak](https://github.com/NVIDIA/garak) - LLM vulnerability scanner. Probes for hallucination, data leakage, prompt injection, jailbreaks, and toxicity. "nmap for LLMs."
- [Promptfoo](https://github.com/promptfoo/promptfoo) - LLM eval and red-teaming CLI. Test prompts against security vulnerabilities, compare models, and catch regressions.
- [Rebuff](https://github.com/protectai/rebuff) - Prompt injection detection SDK. Multi-layer defense: heuristics, LLM-based detection, and vector DB canary tokens.
- [LLM Guard](https://github.com/protectai/llm-guard) - Security toolkit for LLM interactions. Input/output sanitization, PII detection, injection prevention, and toxicity filtering.
- [NeMo Guardrails](https://github.com/NVIDIA/NeMo-Guardrails) - NVIDIA's toolkit for adding programmable guardrails to LLM-based conversational systems.
- [Guardrails AI](https://github.com/guardrails-ai/guardrails) - Input/output validation framework. Define structured contracts for LLM outputs with automatic correction.
- [Lakera Guard](https://www.lakera.ai/) - Real-time AI firewal