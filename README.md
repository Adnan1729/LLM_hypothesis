# LLM Scientific Hypothesis Generation Research

## Research Agenda

This research stream explores the intersection of Large Language Models (LLMs) and scientific discovery, focusing on understanding and potentially harnessing LLMs' capabilities for hypothesis generation.

### Thematic Question
How can we understand and potentially harness LLMs' hallucination mechanisms for "creative" hypothesis generation in the domain of scientific discovery?

### Specific Question
How do LLMs select between multiple hypotheses?

## Reports

### Report 1: Interpreting LLM-Generated Scientific Hypotheses (February 2025)

#### Technical Summary

This study investigates the mechanisms behind LLM-generated scientific hypotheses by analyzing how different sections of research paper abstracts influence the generation process. Using TinyLlama-1.1B-Chat and attribution analysis, we examined the relationship between abstract structure and hypothesis generation.

#### Key Findings

1. **Sectional Influence Distribution**
   
   | Section     | Attribution % |
   |-------------|--------------|
   | Conclusions | 23.7%        |
   | Methods     | 21.3%        |
   | Background  | 19.7%        |
   | Results     | 18.5%        |
   | Objectives  | 16.9%        |

2. **Consistency Analysis**
   
   | Section     | CV    | IQR    |
   |-------------|-------|--------|
   | Background  | 0.32  | -      |
   | Methods     | 0.47  | -      |
   | Results     | 0.60  | -      |
   | Objectives  | 0.58  | -      |
   | Conclusions | 0.95  | 45.45  |

3. **Key Correlations**
   - Strong negative correlation (-0.95) between objectives and conclusions
   - Strong positive correlation (0.89) between results and objectives
   - Moderate negative correlation (-0.51) between background and methods

#### Methodology
![Experimental Setup](media/image1.png)

#### Key Insights

1. **Structured Pattern**: LLM hallucination in hypothesis generation follows a structured pattern rather than occurring randomly.

2. **Controlled Hallucination**: The strong negative correlation between objectives and conclusions suggests a form of "controlled hallucination" where the model bridges gaps between research aims and reported findings.

3. **Section Length Impact**: No direct correlation between section length and attribution scores, indicating that content quality and positioning are more critical than length.

#### Next Steps
Future work will focus on investigating the relationship between hypothesis generation, ranking, and attribution analysis, as outlined in the experimental setup below:

![Next Experimental Setup](media/image14.png)

## Repository Structure

```
.
├── reports/
│   └── report_070225.docx
│   └── jupyter_070225.docx
├── data/
├── analysis/
└── README.md
```

## Contributing

Please read our contributing guidelines before submitting pull requests.

## Citation

If you use this research in your work, please cite:

```bibtex
@article{mahmud2025interpreting,
  title={Interpreting LLM-Generated Scientific Hypotheses: Framework and Initial Findings},
  author={Mahmud, Adnan},
  year={2025}
}
```

## License

This project is licensed under the MIT License - see the LICENSE file for details.
