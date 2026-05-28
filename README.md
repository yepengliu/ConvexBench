# ConvexBench: Can LLMs Recognize Convex Functions?

Official implementation of the watermarking algorithms presented in the paper:

["ConvexBench: Can LLMs Recognize Convex Functions?"](https://arxiv.org/abs/2602.01075) by Yepeng Liu, Yu Huang, Yu-Xiang Wang, Yingbin Liang, and Yuheng Bu.

## Introduction
Convex analysis is a modern branch of mathematics with many applications. As Large Language Models (LLMs) start to automate research-level math and sciences, it is important for LLMs to demonstrate the ability to understand and reason with convexity.  We introduce ConvexBench, a scalable and mechanically verifiable benchmark for testing *whether LLMs can identify the convexity of a symbolic objective under deep functional composition.* Experiments on frontier LLMs reveal a sharp compositional reasoning gap: performance degrades rapidly with increasing depth,  dropping from an F1-score of $1.0$ at depth $2$ to approximately $0.2$ at depth $100$. Inspection of models' reasoning traces indicates two failure modes: \textit{parsing failure} and *lazy reasoning*. To address these limitations, we propose an agentic divide-and-conquer framework that (i) offloads parsing to an external tool to construct an abstract syntax tree (AST) and (ii) enforces recursive reasoning over each intermediate sub-expression with focused context. This framework reliably mitigates deep-composition failures, achieving substantial performance improvement at large depths (e.g., F1-Score $= 1.0$ at depth $100$).
