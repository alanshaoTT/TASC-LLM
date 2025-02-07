# TASC-LLM

This repository contains open-sourced refined labels for Thai automatic speech recognition (ASR) datasets. These labels were generated using a self-evolving data refinement framework that iteratively cleans a hybrid corpus of weak and precise labels, leading to significant improvements in ASR performance.

## Overview

Low-resource languages like Thai often suffer from limited high-quality annotations and noisy, weakly-labeled data. Our approach refines a hybrid dataset—comprising 500 hours of precise labels and 16k hours of weak labels—using a pre-trained Zipformer model combined with a CER-based filtering mechanism. As a result, the refined labels achieve a 16.63% relative reduction in Character Error Rate (CER) on the CommonVoice Thai dataset and provide the community with 14k hours of curated Thai speech data.

This repository supports the TASC-LLM framework, which integrates:
- **Self-evolving Data Refinement:** Iteratively updates labels by retaining only high-confidence predictions (CER ≤ 10%).
- **LLM-enhanced ASR Architecture:** Projects refined speech features into a Thai language model space.
- **Threshold-aware Sequence Compression:** Dynamically prunes redundant frames to reduce computational cost without sacrificing performance.

## Repository Contents

- **`labels/`**: Contains the refined label files (refined gigaspeech2 and MSR-86K labels).
- **`README.md`**: This file.
