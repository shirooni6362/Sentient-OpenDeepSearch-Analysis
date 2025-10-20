# Open Deep Search: Comprehensive Technical Analysis


<img width="1280" height="720" alt="Image" src="https://github.com/user-attachments/assets/60bf3ae2-ecee-493f-893e-5161e6a99898" />

## Abstract
This paper presents a comprehensive technical analysis of Open Deep Search, an open-source framework developed by the Sentient Foundation that addresses the capability gap between closed and open-source artificial intelligence systems in search-augmented reasoning. The research examines the dual-component architecture combining sophisticated web search capabilities with agentic reasoning paradigms, achieving 88.3% accuracy on SimpleQA and 75.3% on FRAMES benchmarks—surpassing GPT-4o Search Preview by 9.7 percentage points on complex multi-hop reasoning tasks.
Key Finding: Open Deep Search demonstrates that transparent, open-source approaches can achieve competitive performance with proprietary alternatives while providing advantages in customization, cost control (80-90% savings at scale), and privacy preservation through self-hosting capabilities.


## Citation
@article{oni2025opendeepsearch,
  title={Open Deep Search and the Future of Reasoning Agents: A Comprehensive Technical Analysis of Architecture, Performance, and Ecosystem Implications},
  author={Oni, Shiro},
  journal={Zenodo},
  year={2025},
  month={October},
  doi={10.5281/zenodo.[ASSIGNED-NUMBER]},
  url={https://zenodo.org/record/[RECORD-ID]}
}
```

**DOI**: `10.5281/zenodo.[ASSIGNED-NUMBER]`

**Preprint**: Available on Zenodo and arXiv:2503.20201

## Table of Contents

- [Overview](#overview)
- [Key Contributions](#key-contributions)
- [Research Scope](#research-scope)
- [Performance Highlights](#performance-highlights)
- [Project Structure](#project-structure)
- [Getting Started](#getting-started)
- [Detailed Analysis Sections](#detailed-analysis-sections)
- [Benchmark Results](#benchmark-results)
- [Cost Analysis Summary](#cost-analysis-summary)
- [Technical Requirements](#technical-requirements)
- [Related Resources](#related-resources)
- [Author](#author)
- [License](#license)
- [Acknowledgments](#acknowledgments)

## Overview

The emergence of proprietary search-augmented language models has created a significant capability gap between closed and open-source AI systems. This research provides the first comprehensive technical analysis of Open Deep Search, examining:

- **Architecture**: Modular dual-component design with ReAct and CodeAct reasoning frameworks
- **Performance**: Rigorous evaluation on SimpleQA and FRAMES benchmarks
- **Economics**: Total cost of ownership modeling across deployment scales
- **Ecosystem**: Open Model License integration for sustainable open-source development
- **Production**: Scalability, reliability, and operational considerations
- **Future**: Critical limitations and research directions

### Research Methodology

This analysis synthesizes:
- Primary source documentation from Sentient Foundation
- Academic preprints and benchmark evaluations
- Comparative analysis of proprietary alternatives (Perplexity, OpenAI, Google)
- Economic modeling and cost-benefit analysis
- Production deployment frameworks and best practices

## Key Contributions

### 1. Architectural Documentation
Comprehensive technical documentation of Open Deep Search architecture enabling genuine reproducibility:
- Three-stage search pipeline (query rephrasing, retrieval, augmentation)
- Dual agent frameworks (ReAct for interpretability, CodeAct for performance)
- Plug-and-play model integration supporting 50+ language models
- Tool suite and extension mechanisms

### 2. Benchmark Analysis
Rigorous empirical evaluation with detailed ablation studies:
- **SimpleQA**: 88.3% accuracy (near-parity with GPT-4o at 89.9%)
- **FRAMES**: 75.3% accuracy (exceeds GPT-4o by 9.7 percentage points)
- Component contribution analysis isolating search, reasoning, and augmentation effects
- Cross-system comparative performance assessment

### 3. Economic Modeling
Total cost of ownership analysis across deployment configurations:
- Per-query cost breakdown for API-based and self-hosted deployment
- Break-even analysis (self-hosting advantageous above ~150K queries/month)
- Three-year TCO scenarios showing 80-90% cost savings at scale
- Cost optimization strategies and techniques

### 4. Ecosystem Analysis
First comprehensive evaluation of Open Model License framework:
- Cryptographic fingerprinting technical implementation
- Marketplace dynamics and sustainability modeling
- Multi-agent verification and attribution mechanisms
- Trusted execution environment integration

### 5. Production Guidance
Practical deployment considerations for real-world systems:
- Scalability architecture and horizontal scaling patterns
- Reliability engineering and fault tolerance mechanisms
- Monitoring, observability, and performance analysis frameworks
- Security hardening and operational runbooks

### 6. Critical Assessment
Honest evaluation of limitations and future research directions:
- Technical constraints (latency, multimodal gaps, reasoning depth)
- Benchmark inadequacies and evaluation gaps
- Open research problems in search-augmented reasoning
- Societal implications and responsible development principles

## Research Scope

### Covered Topics

**System Architecture (Section 2)**
- Core design principles and architectural patterns
- Two-component architecture separating search and reasoning
- ReAct vs CodeAct agent framework comparison
- Model-agnostic integration supporting diverse LLMs

**Search Pipeline (Section 3)**
- Query rephrasing for coverage expansion
- Multi-provider retrieval (Serper, SearXNG)
- Deep content augmentation with semantic reranking
- Performance characteristics and optimization

**Reasoning Agents (Section 4)**
- Chain-of-thought and self-consistency foundations
- ReAct implementation with dynamic few-shot learning
- CodeAct implementation with SmolAgents integration
- Tool suite (search, calculator, recursive reasoning)

**Benchmark Evaluation (Section 5)**
- SimpleQA: 4,326 factual questions, adversarially filtered
- FRAMES: 824 multi-hop reasoning scenarios
- Ablation studies isolating component contributions
- Cross-system comparative analysis

**Competitive Landscape (Section 6)**
- Proprietary systems (Perplexity, OpenAI, Google SGE)
- Architectural inference from observable behavior
- Open-source alternatives (OpenPerplex, Perplexica)
- Strategic positioning and competitive advantages

**Cost Analysis (Section 7)**
- Per-query breakdown (API vs self-hosted)
- Infrastructure cost modeling with capital amortization
- Multi-year TCO scenarios across deployment scales
- Optimization strategies reducing costs 40-60%

**Open Model License (Section 8)**
- Cryptographic fingerprinting mechanism
- Economic sustainability and marketplace dynamics
- Multi-agent verification patterns
- Sentient Enclaves integration for private deployment

**Advanced Capabilities (Section 9)**
- Complex reasoning beyond current benchmarks
- Multi-agent orchestration for specialized domains
- Quality assessment frameworks (citation, completeness, coherence)
- Interactive refinement and multimodal directions

**Production Deployment (Section 10)**
- Scalability patterns and capacity planning
- Reliability engineering (redundancy, failover, circuit breakers)
- Monitoring and observability infrastructure
- Security hardening and operational procedures

**Limitations & Future Work (Section 11)**
- Technical gaps (1.6% SimpleQA lag, latency disadvantages)
- Benchmark inadequacies requiring new evaluation frameworks
- Open research problems (optimal search, credibility assessment)
- Societal implications and responsible development

## Performance Highlights

### SimpleQA Benchmark (Factual Question Answering)

| System | Accuracy | Base Model | Searches/Query |
|--------|----------|------------|----------------|
| **ODS-v2 (DeepSeek-R1)** | **88.3%** | DeepSeek-R1 | 1.02 |
| GPT-4o Search Preview | 89.9% | GPT-4o | - |
| ODS-v1 (DeepSeek-R1) | 87.7% | DeepSeek-R1 | 1.08 |
| ODS-v1 (Llama 3.1 70B) | 83.4% | Llama 3.1 70B | 1.05 |
| Perplexity Standard | 64.9% | Sonar | - |

**Gap Analysis**: 1.6 percentage point difference from GPT-4o (near-parity)

### FRAMES Benchmark (Multi-Hop Reasoning)

| System | Accuracy | Base Model | Searches/Query |
|--------|----------|------------|----------------|
| **ODS-v2 (DeepSeek-R1)** | **75.3%** | DeepSeek-R1 | 3.39 |
| GPT-4o Search Preview | 65.6% | GPT-4o | - |
| Perplexity Sonar Reasoning Pro | 65.6% | Sonar | - |
| ODS-v1 (DeepSeek-R1) | 56.7% | DeepSeek-R1 | 1.08 |
| ODS-v1 (Llama 3.1 70B) | 49.5% | Llama 3.1 70B | 1.05 |

**Performance Advantage**: 9.7 percentage points superior to GPT-4o on complex reasoning

### Key Performance Insights

1. **Framework Matters for Complexity**: CodeAct (ODS-v2) outperforms ReAct (ODS-v1) by 18.6 percentage points on FRAMES while showing similar performance on SimpleQA
2. **Augmentation Critical**: Enabling augmentation improves FRAMES accuracy from 27.6% to 75.3% (47.7 percentage point gain)
3. **Adaptive Search Strategy**: ODS-v2 averages 3.39 searches/query on FRAMES vs 1.08 for ODS-v1, demonstrating sophisticated complexity recognition
4. **Model Quality Compounds**: Upgrading from Llama 3.1 70B to DeepSeek-R1 provides 4.3 percentage point gain on SimpleQA and 7.2 points on FRAMES

## Project Structure
```
Open-Deep-Search-Analysis/
├── compiled/
│   └── Open_Deep_Search_Comprehensive_Analysis.pdf
├── paper/
│   ├── figures/
│   │   ├── architecture_diagram.png
│   │   ├── search_pipeline.png
│   │   ├── react_vs_codeact.png
│   │   ├── performance_comparison.png
│   │   ├── cost_analysis.png
│   │   └── oml_fingerprinting.png
│   ├── sections/
│   │   ├── 01_introduction.tex
│   │   ├── 02_architecture.tex
│   │   ├── 03_search_pipeline.tex
│   │   ├── 04_reasoning_agents.tex
│   │   ├── 05_benchmark_evaluation.tex
│   │   ├── 06_competitive_landscape.tex
│   │   ├── 07_cost_analysis.tex
│   │   ├── 08_oml_integration.tex
│   │   ├── 09_advanced_capabilities.tex
│   │   ├── 10_production_deployment.tex
│   │   ├── 11_limitations_future.tex
│   │   └── 12_conclusion.tex
│   ├── main.tex
│   └── references.bib
├── assets/
│   ├── thumbnail.png
│   └── supplementary_materials/
├── scripts/
│   └── compile_latex.sh
├── README.md
├── LICENSE
└── CITATION.cff

## Detailed Analysis Sections

### Section 1: Introduction (pp. 5-7)
Establishes the capability gap between proprietary and open-source search-augmented reasoning systems. Introduces Open Deep Search as a competitive open alternative achieving near-parity with commercial systems.

### Section 2: System Architecture (pp. 7-18)
**Core Principles**: Radical modularity, model agnosticism, transparency, graceful degradation
**Components**: Open Search Tool, Open Reasoning Agent (ReAct & CodeAct)
**Design Philosophy**: Prioritizing flexibility and extensibility over narrow optimization

### Section 3: Search Pipeline (pp. 18-30)
**Three Stages**:
1. Query rephrasing (coverage expansion)
2. Retrieval (Serper/SearXNG integration)
3. Augmentation (web scraping, semantic reranking)

**Key Insight**: Augmentation provides 47.7 percentage point improvement on FRAMES

### Section 4: Reasoning Agents (pp. 30-40)
**ReAct (ODS-v1)**: Explicit thought-action-observation loops, 200 community examples
**CodeAct (ODS-v2)**: Python code generation, superior on complex reasoning
**Performance Delta**: 18.6 percentage points on FRAMES favoring CodeAct

### Section 5: Benchmark Evaluation (pp. 40-54)
**SimpleQA**: 4,326 questions, 81% Wikipedia-sourced, adversarially filtered
**FRAMES**: 824 multi-hop scenarios, tests synthesis across sources
**Ablation Studies**: Isolates contributions of search, reasoning, augmentation, base model

### Section 6: Competitive Landscape (pp. 54-65)
**Proprietary Analysis**: Perplexity, OpenAI, Google SGE
**Architectural Inference**: Single-search limitations, snippet reliance hypothesis
**Strategic Positioning**: Transparency, customization, cost advantages

### Section 7: Cost Analysis (pp. 65-77)
**Break-Even Point**: ~150,000 queries/month for self-hosting
**TCO Scenarios**: 80-90% savings at scale (500K+ queries/month)
**Optimization Strategies**: Caching, model selection, infrastructure rightsizing

### Section 8: Open Model License (pp. 77-88)
**Fingerprinting**: 1,024 secret query-response pairs, 1% performance impact
**Economics**: Usage-based fees enabling creator compensation
**Challenges**: Voluntary compliance, enforcement mechanisms, legal clarity

### Section 9: Advanced Capabilities (pp. 89-97)
**Beyond Benchmarks**: Deep multi-hop reasoning, temporal awareness, contradiction resolution
**Multi-Agent**: Domain specialists (medical, legal, financial) with coordinator
**Quality Dimensions**: Citation accuracy, completeness, coherence, uncertainty handling

### Section 10: Production Deployment (pp. 98-110)
**Scalability**: Horizontal scaling, caching strategies (40-60% throughput gain)
**Reliability**: 3-4 nines availability through redundancy and failover
**Operations**: Monitoring, security hardening, incident response

### Section 11: Limitations & Future Work (pp. 110-117)
**Technical Gaps**: 1.6% SimpleQA lag, 2-4x latency disadvantage, no multimodal support
**Research Problems**: Optimal search strategies, source credibility, error propagation
**Societal Implications**: Democratization vs misuse risk, worker displacement, epistemic authority

### Section 12: Conclusion (pp. 118-125)
**Synthesis**: Open approaches achieve competitive performance with proprietary alternatives
**Contributions**: Technical documentation, rigorous evaluation, honest limitation assessment
**Vision**: Sustainable open AI ecosystems serving diverse needs

## Benchmark Results

### SimpleQA Performance Matrix

| Configuration | Base Model | Accuracy | Δ from GPT-4o | Searches/Query |
|---------------|------------|----------|---------------|----------------|
| ODS-v2 | DeepSeek-R1 | 88.3% | -1.6pp | 1.02 |
| ODS-v1 | DeepSeek-R1 | 87.7% | -2.2pp | 1.08 |
| ODS-v1 | Llama 3.1 70B | 83.4% | -6.5pp | 1.05 |
| Base Model Only | Llama 3.1 70B | 21.2% | -68.7pp | 0 |

**Human Baseline**: ~97% (adjusted for grader errors)

### FRAMES Performance Matrix

| Configuration | Base Model | Accuracy | Δ from GPT-4o | Searches/Query |
|---------------|------------|----------|---------------|----------------|
| ODS-v2 (Pro) | DeepSeek-R1 | 75.3% | +9.7pp | 3.39 |
| ODS-v1 | DeepSeek-R1 | 56.7% | -8.9pp | 1.08 |
| ODS-v1 | Llama 3.1 70B | 49.5% | -16.1pp | 1.05 |
| ODS-v2 (Default) | DeepSeek-R1 | 27.6% | -38.0pp | 3.39 |
| Base Model Only | Llama 3.1 70B | 34.3% | -31.3pp | 0 |

**Key Findings**:
- Augmentation impact: 47.7 percentage points (27.6% → 75.3%)
- Framework impact: 18.6 percentage points (56.7% → 75.3%)
- Adaptive search: 3.39 avg searches vs 1.08 for non-adaptive

### Ablation Study Results

| Component Added | SimpleQA | FRAMES | Δ SimpleQA | Δ FRAMES |
|-----------------|----------|--------|------------|----------|
| Base Model (Llama 3.1 70B) | 21.2% | 34.3% | - | - |
| + Search Tool | 82.4% | 27.6% | +61.2pp | -6.7pp |
| + ReAct Framework | 87.2% | 37.4% | +4.8pp | +9.8pp |
| + Few-Shot Examples | 87.8% | 49.5% | +0.6pp | +12.1pp |
| + DeepSeek-R1 Model | 90.4% | 56.7% | +2.6pp | +7.2pp |
| + CodeAct Framework | 88.3% | 75.3% | -2.1pp | +18.6pp |

**Insight**: Search alone insufficient for complex reasoning; framework + augmentation essential

## Cost Analysis Summary

### Per-Query Cost Breakdown

**API-Based Deployment** (Default Mode):
- Query Rephrasing: $0.002-0.005
- Search API (2-3 calls): $0.002-0.009
- Agent Reasoning: $0.017-0.045
- **Total**: $0.021-0.059 per query

**API-Based Deployment** (Pro Mode with Augmentation):
- Additional Embedding Generation: $0.001-0.003
- Increased Reasoning Costs: $0.025-0.100
- **Total**: $0.032-0.120 per query

**Self-Hosted Deployment**:
- Fixed Monthly Cost: ~$3,600 (2x A100 GPUs, operations)
- Marginal Cost per Query: $0.001-0.003
- **Break-Even**: ~150,000 queries/month

### Three-Year TCO Scenarios

**Small Deployment** (10K → 25K queries/month):
- Perplexity API: $12,600
- ODS API: $18,900
- Self-Hosted: $129,600 (not economical)

**Medium Deployment** (50K → 150K queries/month):
- Perplexity API: $72,000
- ODS API: $108,000
- Self-Hosted: $179,600 (approaching break-even)

**Large Deployment** (100K → 500K queries/month):
- Perplexity API: $180,000
- GPT-4o Search: $720,000
- ODS API: $540,000
- Self-Hosted: $179,600 (**$360K+ savings**)

**Enterprise Deployment** (500K → 2M queries/month):
- Perplexity API: $720,000
- GPT-4o Search: $2,880,000
- Self-Hosted (4x GPU): $459,200 (**$2.4M+ savings**)

### Cost Optimization Strategies

**Immediate Impact** (30-50% reduction):
- Model selection (GPT-3.5 for rephrasing, Claude Sonnet for reasoning)
- Multi-layer caching (search results, embeddings, responses)
- Self-hosted SearXNG for search

**Architectural** (15-25% additional reduction):
- Adaptive mode selection (default vs pro based on complexity)
- Batch processing for non-realtime workloads
- Prompt optimization reducing token consumption

**Infrastructure** (30-50% infrastructure cost reduction):
- Model quantization (8-bit/4-bit)
- Inference optimization (vLLM, TensorRT-LLM)
- Spot instances for batch workloads

## Technical Requirements

### For Reading
- PDF reader supporting 130+ page documents
- Optional: LaTeX editor for source inspection

### For Building from Source
- **LaTeX Distribution**: TeX Live 2020+ or MiKTeX
- **Packages Required**:
  - amsmath, amssymb (mathematical notation)
  - graphicx (figure inclusion)
  - hyperref (cross-references and links)
  - biblatex or natbib (bibliography management)
  - algorithm2e (algorithm pseudocode)
  - tikz (technical diagrams)

### For Implementation (if deploying Open Deep Search)
- **Compute**: 2x NVIDIA A100 80GB GPUs (minimum for self-hosted)
- **RAM**: 128GB+ for moderate deployment
- **Storage**: 100GB+ for search indices and cached data
- **Network**: 1Gbps+ bandwidth for web scraping
- **Software**:
  - Python 3.10+
  - LiteLLM for model integration
  - SearXNG or Serper.dev for search
  - Infinity or Jina AI for embeddings
  - Redis for distributed caching

## Related Resources

### Official Open Deep Search Resources
- **GitHub Repository**: [github.com/sentient-agi/OpenDeepSearch](https://github.com/sentient-agi/OpenDeepSearch)
- **Documentation**: [docs.sentient.xyz](https://docs.sentient.xyz/)
- **Official Website**: [sentient.xyz](https://www.sentient.xyz)

### Referenced Frameworks
- **Sentient Agent Framework**: [github.com/sentient-agi/Sentient-Agent-Framework](https://github.com/sentient-agi/Sentient-Agent-Framework)
- **OML Fingerprinting**: [github.com/sentient-agi/OML-1.0-Fingerprinting](https://github.com/sentient-agi/OML-1.0-Fingerprinting)
- **Sentient Enclaves**: [github.com/sentient-agi/Sentient-Enclaves-Framework](https://github.com/sentient-agi/Sentient-Enclaves-Framework)

### Primary Research Sources
- **Original Preprint**: arXiv:2503.20201
- **SimpleQA Benchmark**: [openai.com/index/introducing-simpleqa](https://openai.com/index/introducing-simpleqa/)
- **FRAMES Benchmark**: [HuggingFace datasets/google/frames-benchmark](https://huggingface.co/datasets/google/frames-benchmark)

### Supporting Libraries
- **LiteLLM**: [litellm.ai](https://litellm.ai) (Unified LLM interface)
- **SmolAgents**: [github.com/huggingface/smolagents](https://github.com/huggingface/smolagents) (HuggingFace agent framework)
- **Crawl4AI**: [github.com/unclecode/crawl4ai](https://github.com/unclecode/crawl4ai) (Web scraping)
- **Infinity**: [github.com/michaelfeil/infinity](https://github.com/michaelfeil/infinity) (Self-hosted embeddings)

### Companion Content
- **YouTube Video**: [Detailed walkthrough and implementation guide]
- **Blog Post**: [Key findings and practical implications]
- **Zenodo Dataset**: DOI: 10.5281/zenodo.[ASSIGNED-NUMBER]

## Author

**Shiro Oni**  
Independent Technical Research Analysis

**Contact**: [Your contact method]  
**Research Interests**: AI safety, open-source AI ecosystems, search-augmented reasoning, agent frameworks

**Other Publications**:
- [List other relevant papers if applicable]

## License

### Paper Content
This research paper is licensed under **Creative Commons Attribution 4.0 International (CC BY 4.0)**.

You are free to:
- Share: copy and redistribute the material
- Adapt: remix, transform, and build upon the material

Under the following terms:
- Attribution: You must give appropriate credit, provide a link to the license, and indicate if changes were made

Full license text: [creativecommons.org/licenses/by/4.0/](https://creativecommons.org/licenses/by/4.0/)

### Code Examples
Code snippets and scripts in this repository are licensed under **MIT License**.
```
MIT License

Copyright (c) 2025 Shiro Oni

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
