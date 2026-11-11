# Shashwat Saket 👋

<p align="center">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&size=21&duration=3000&pause=900&color=3B82F6&center=true&vCenter=true&width=750&lines=Machine+Learning+Researcher;Deep+Learning+%26+Representation+Learning;Computational+Neuroscience;Building+Algorithms%2C+Not+Just+Applications" />
</p>

<p align="center">
  <a href="https://linkedin.com/in/shashwatsaket46"><img src="https://img.shields.io/badge/LinkedIn-Connect-0A66C2?style=flat-square&logo=linkedin" /></a>
  <a href="https://github.com/shashwatsaket46"><img src="https://img.shields.io/badge/GitHub-Follow-181717?style=flat-square&logo=github" /></a>
  <a href="mailto:shashwat.saket@nyu.edu"><img src="https://img.shields.io/badge/Email-Contact-EA4335?style=flat-square&logo=gmail&logoColor=white" /></a>
</p>

I'm a Computer Science graduate student at **New York University**, where I spend most of my time working on machine learning research.

My interests have taken me from representation learning and vector quantization to computational neuroscience, where I'm currently exploring how molecular information can help explain neuronal connectivity.

I enjoy working on problems that require more than applying an existing model: understanding the underlying mathematics, developing an approach, implementing it, and figuring out what the experiments actually tell us.

Previously, I worked as a Software Engineer at **CGI Inc.**, building enterprise applications, intelligent automation systems, and ML-powered solutions.

---

## 🔬 Research

### Understanding neural connectivity through biological data

**Graduate Researcher | NYU Neuroinformatics Lab**  
*May 2026 – Present*

Working with Prof. Erdem Varol on the Drosophila visual system, exploring how gene expression and transcriptomic information relate to neuronal connectivity.

One of the interesting questions in this work is whether molecular information can help explain why particular neurons connect to one another.

My work involves:

- Integrating connectome, transcriptomic, and gene-expression datasets.
- Developing computational approaches for neuronal cell-type identification.
- Investigating gene-pair associations between presynaptic and postsynaptic neurons.
- Building transformer-based filtering and analysis pipelines.
- Running large-scale experiments using GPU-accelerated infrastructure.
- Exploring how connectivity patterns vary across neuropils and neural circuits.

A significant part of the work involves turning large, heterogeneous biological datasets into something that can be systematically analyzed and evaluated.

**Current research interests:** Connectomics, computational neuroscience, multimodal learning, graph machine learning, representation learning, and biological data integration.

---

## 🧠 Featured Research

### Reusable Hierarchical Codebooks for Approximate Nearest-Neighbor Search

One of my major research projects focuses on making vector quantization more efficient by reusing codebooks across multiple levels of retrieval.

In conventional approaches, different quantization stages can require independently constructed codebooks. I have been investigating whether a shared hierarchical codebook can support both coarse candidate filtering and finer retrieval, reducing construction overhead while retaining retrieval quality.

The interesting part is not simply building a hierarchy. It is understanding how the choice of construction strategy affects quantization error and, ultimately, nearest-neighbor retrieval accuracy.

#### Three approaches to codebook construction

I explored three different strategies:

| Strategy | Construction idea |
|---|---|
| **Top-Down** | Start with a coarser representation and progressively refine it. |
| **Bottom-Up** | Construct finer representations first and combine them into coarser levels. |
| **Middle-Anchor** | Use an intermediate quantization level as the reference for constructing the hierarchy. |

#### How the retrieval framework works

```mermaid
flowchart TD
    A["High-dimensional input vectors"] --> B["Hierarchical codebook construction"]
    B --> C["Shared quantization structure"]
    C --> D["Coarse retrieval"]
    D --> E["Candidate selection"]
    E --> F["Fine retrieval / reranking"]
    F --> G["Nearest-neighbor results"]

    B -.-> H["Top-Down"]
    B -.-> I["Bottom-Up"]
    B -.-> J["Middle-Anchor"]

    style B fill:#2563eb,color:#fff,stroke:#2563eb
    style G fill:#15803d,color:#fff,stroke:#15803d
```

#### What I investigated

- Hierarchical codebook construction using Lloyd-Max quantization.
- Quantization error propagation between hierarchical levels.
- Error conservation and monotonicity across construction strategies.
- The effect of anchor placement on retrieval quality.
- The relationship between reconstruction error and Recall@1.
- Construction cost versus retrieval accuracy.

#### Experimental evaluation

We evaluated our approaches using GloVe-200 and OpenAI embedding datasets with 1,536 and 3,072 dimensions, including multiple random seeds and ablation experiments.

Some of the findings from the evaluated configurations:

| Observation | Experimental result |
|---|---|
| Top-Down and Middle-Anchor | Recall@1 within approximately 1 percentage point of their corresponding single-tier references |
| Bottom-Up | Recall@1 degradation of up to approximately 12 percentage points |
| GloVe-200 | 2.2% improvement in Recall@1 over Product Quantization in the evaluated setting |
| Codebook construction | Approximately 50×–1,300× lower construction cost in evaluated configurations |

The experiments highlighted something particularly interesting: the order in which a quantization hierarchy is constructed matters. Similar-looking codebook structures can behave quite differently depending on how quantization errors propagate between levels.

**Methods and baselines explored:** Lloyd-Max quantization, Product Quantization (PQ), TurboQuant, and Extended RaBitQ.

<details>
<summary><b>More about the research</b></summary>

The project involved mathematical derivations, implementation of multiple construction strategies, experimental comparisons, and ablation studies.

Rather than evaluating compression in isolation, the experiments considered the effect of quantization decisions on downstream retrieval quality.

The broader goal is to understand when hierarchical codebook reuse is beneficial, where it introduces additional error, and how construction choices influence the efficiency-accuracy trade-off.

*Research manuscript in preparation.*

</details>

---

## 🛠️ Other Things I've Built

### ReservaDirect | Autonomous AI Reservation Agent

Built at the **tech@NYU Hackathon (HOF Office)**.

ReservaDirect connects Google Calendar with real-world restaurant reservations.

The idea was simple: instead of manually searching for restaurants and making calls, let an autonomous agent handle the process.

- Extracts reservation requirements from calendar event descriptions.
- Discovers and ranks relevant restaurants.
- Initiates AI-powered voice calls.
- Handles reservation confirmation.
- Updates calendar events dynamically.

**Technologies:** Python, FastAPI, React, Docker, Voice AI.

<p align="center">
  <a href="https://www.youtube.com/watch?v=ZCsI_wIn5to">
    <img src="https://img.youtube.com/vi/ZCsI_wIn5to/maxresdefault.jpg" width="80%" alt="ReservaDirect demo"/>
  </a>
  <br/>
  <a href="https://www.youtube.com/watch?v=ZCsI_wIn5to">▶ Watch the demo</a>
  ·
  <a href="https://github.com/shashwatsaket46/ReservaDirect">Source code</a>
</p>

### Knowledge Graph-Based RAG

Explored combining knowledge graphs with retrieval-augmented generation to improve contextual retrieval and grounded LLM responses.

Worked on extracting structured relationships, semantic retrieval, and combining graph-based context with language model generation.

### NLP-Based Propaganda Detection

Worked on applying deep learning and natural language processing to identify propaganda patterns in textual data.

Explored text representations, preprocessing pipelines, and classification architectures for unstructured text.

---

## 💼 Professional Experience

### Software Engineer | CGI Inc.
*August 2023 – September 2025*

Before moving further into research, I spent two years working on enterprise software and intelligent automation.

Some of the work I contributed to:

- Developed NLP-based conversational AI modules that automated approximately 40% of targeted enterprise workflows.
- Built Camunda-based ML microservices, improving deployment throughput by 35%.
- Implemented anomaly detection workflows for financial datasets, improving detection accuracy by 25%.
- Worked on backend services, distributed systems, and enterprise application integration.
- Collaborated with engineering teams across ML and backend development.

This experience gave me a practical understanding of what it takes to move an ML idea beyond a notebook and into a working system.

---

## 📄 Publications

- Research publication in *Cluster Computing* (Springer).

My current research interests also include efficient vector search, hierarchical quantization, and multimodal learning for computational neuroscience.

---

## ⚙️ Tools & Technologies

These are some of the tools I have worked with across research and engineering.

**Machine Learning & Deep Learning**

<p>
  <img src="https://skillicons.dev/icons?i=python,pytorch,tensorflow" />
</p>

**Data Science & Research**

<p>
  <img src="https://skillicons.dev/icons?i=r,matlab,anaconda" />
</p>

**Backend & Distributed Systems**

<p>
  <img src="https://skillicons.dev/icons?i=fastapi,spring,nodejs,kafka,postgres" />
</p>

**Infrastructure & Development**

<p>
  <img src="https://skillicons.dev/icons?i=docker,kubernetes,linux,git,github" />
</p>

---

## 📊 GitHub Activity

<p align="center">
  <img height="165" src="https://github-readme-stats.vercel.app/api?username=shashwatsaket46&show_icons=true&hide_border=true&theme=transparent&rank_icon=github" />
  <img height="165" src="https://github-readme-streak-stats.herokuapp.com/?user=shashwatsaket46&hide_border=true&theme=transparent" />
</p>

<p align="center">
  <img src="https://github-readme-activity-graph.vercel.app/graph?username=shashwatsaket46&theme=github-compact&hide_border=true" width="95%" />
</p>

---

## 📫 Get in Touch

I'm always happy to connect with people working on interesting problems in machine learning, algorithms, and computational biology.

- **LinkedIn:** [shashwatsaket46](https://linkedin.com/in/shashwatsaket46)
- **GitHub:** [shashwatsaket46](https://github.com/shashwatsaket46)
- **Email:** [shashwat.saket@nyu.edu](mailto:shashwat.saket@nyu.edu)

---

<p align="center">
  <i>Interested in understanding why algorithms work, not just making them work.</i>
</p>
