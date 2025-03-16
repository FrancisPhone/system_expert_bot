# system_expert_bot

## Abstract
Software documentation is essential for understanding and maintaining software systems, however many projects suffer from outdated or incomplete documentation. Traditional reverse engineering extracts structural information but lacks natural language explanations, limiting accessibility. Recent advances in NLP and large language models (LLMs) offer automated documentation, yet comprehensive system-level understanding remains underexplored. This project develops a Software System Expert Bot that leverages NLP, knowledge graphs, and machine learning to generate documentation and answer technical queries on software code, database schemas, and SQL procedures. By integrating LLM-generated documentation, a structured knowledge graph, fine-tuned models, and Retrieval-Augmented Generation (RAG), the bot provides accurate, interactive responses. The outcome is a scalable AI assistant that enhances software documentation and system comprehension.

## Related Papers

### A framework for software re-documentation using reverse engineering approach
This paper presents a framework that uses the Rigi tool, a reverse engineering environment, to extract static information from source code and represent it in Rigi Standard Format (RSF) files. These files are
visualized as directed graphs or tree-like structures, which are then transformed into standard Unified Modeling Language (UML) notation. The framework was applied to a Shopping Management System (ShM), and the generated documentation was evaluated using a Documentation Quality Model (DQM), assessing attributes like understandability, consistency, and completeness. The results demonstrated its effectiveness in producing
usable, up-to-date, and complete documentation, aiding in software maintenance. However, it lacks NLP integration, focusing on structural representations rather than natural language explanations.

### Free and Customizable Code Documentation with LLMs: A Fine-Tuning Approach
This paper introduces an LLM-based application for generating basic documentation, such as README files and GitHub pages, for publicly available code repositories. This tool supports multiple models, including open-source options like Meta’s Llama2 and Google’s Gemini, offering cost-effective solutions by eliminating the need for paid API calls. It also allows fine-tuning with QLoRA (Quantized Low-Rank Adaptation), enabling users to customize models on their specific datasets, though optimal results may require powerful GPU resources. This work is directly relevant to our project’s first method: documenting technical components (codes, database schema, and SQL procedures) using NLP. By extending the LLM-based approach, we can generate comprehensive documentation, building on the fine-tuning capabilities to ensure accuracy for our domain-specific needs. 

### GRAPHCODEBERT: PRE-TRAINING CODE REPRESENTATIONS WITH DATA FLOW
This paper introduces GraphCodeBert, a pre-trained model that leverages data flow graphs to represent the semantic structure of code. These graphs capture ”where-the-value-comes-from” relationships between variables, providing a richer representation than simple token sequences. GraphCodeBert is pre-trained on a large corpus of code and achieves superior performance in tasks like code search, clone detection, and code translation compared to previous models like CodeBERT.

### Tackling Long Code Search with Splitting, Encoding, and Aggregating
This paper introduces SEA (Split, Encode, and Aggregate) method for code search that tackles the challenge of long code snippets. The method consists of three main steps: 1. Splitting: Long code is split into smaller blocks using an AST-based approach, which parses the code into an Abstract Syntax Tree and divides it into non-overlapping subtrees, followed by a sliding window to create overlapping code blocks. 2. Encoding: Each code block is encoded using a pre-trained Transformer-based model like GraphCodeBert to obtain its embedding. 3. Aggregation: The embeddings are aggregated using an attention-based method combined with meanpooling to create a comprehensive representation, assigning weights based on block importance. For code search, a natural language query is encoded similarly, and similarity is calculated to rank code snippets, outperforming baseline and sparse Transformer models.

### RepoAgent: An LLM-Powered Open-Source Framework for Repository-level Code Documentation Generation
The paper introduces RepoAgent, a novel framework leveraging large language models (LLMs) to automate repository-level code documentation generation and maintenance. Its methodology comprises three key stages: Global Structure Analysis, Documentation Generation, and Documentation Update. In the first stage, RepoAgent constructs a project tree using Abstract Syntax Tree (AST) analysis to parse Python code and employs the Jedi library to map bi-directional reference relationships, forming a Directed Acyclic Graph (DAG). The Documentation Generation phase utilizes a sophisticated prompt template, integrating the project tree, code snippets, and reference relationships to produce detailed, structured documentation with practical guidance, processed in a bottom-to-top topological order and rendered via GitBook. Finally, the Documentation Update stage integrates with Git’s pre-commit hook to detect code changes and selectively update affected documentation, ensuring synchronization. Evaluated on nine Python repositories, RepoAgent demonstrates superior performance compared to traditional methods, validated through qualitative case studies and quantitative human preference tests.

