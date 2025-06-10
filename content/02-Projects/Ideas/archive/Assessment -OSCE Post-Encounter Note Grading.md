
## Tags

#project #idea #focus/assessment #focus/teaching #form/machine-learning #samr/augmentation #tech/LLM #tech/zero-shot-learning #tech/GPT #use-case/clinical-skills-evaluation

## Germ of the Idea

Implement AI-based automated grading system for OSCE post-encounter notes using zero-shot large language model architecture, based on the successful UT Southwestern deployment that achieved 91% reduction in human effort and 89.7% agreement with expert graders.

## Overview

### Problem Statement

Manual grading of OSCE post-encounter notes requires specially trained evaluators, creates significant labor and time investments, and often results in weeks-long delays in providing feedback to students. Current assessment processes are labor-intensive, potentially inconsistent across evaluators, and difficult to scale.

### Proposed Solution

Deploy zero-shot GPT-4 based grading system that converts evaluation rubrics into prompts for automated assessment of student post-encounter notes, requiring no prior domain-specific training data and enabling rapid adaptation to new evaluation criteria.

### Success Metrics

- 90%+ reduction in human grading effort (measured by gradable items)
- Turnaround time reduction from weeks to days
- 85%+ agreement with human expert graders at rubric item level
- Cohen's kappa ≥ 0.75 for inter-rater reliability
- Spearman's correlation ≥ 0.80 with total examination scores

## Literature Support

### Key Supporting Papers

- [[Jamieson2024]] - Primary reference demonstrating successful implementation
- Need additional papers on OSCE assessment reliability
- Research on AI grading validation methodologies

### Research Gaps

- Limited multi-institutional validation studies
- Need for long-term impact assessment on student learning
- Comparison studies with traditional grading methods

## Technical Requirements

### AI/ML Components Needed

- **Primary**: GPT-4 or equivalent large language model
- **Alternative**: Fine-tuned local models (Llama-2-7B) via knowledge distillation
- Zero-shot prompt engineering system
- Rubric-to-prompt conversion algorithms
- Claim verification framework for yes/no assessment tasks
- Agreement validation and quality control systems

### Data Requirements

- Historical OSCE post-encounter notes with expert grades
- Current evaluation rubrics for all OSCE stations
- Station-specific assessment criteria
- Student performance benchmarks
- Inter-rater reliability data from human evaluators

### Integration Points

- [[OSCE Management System]]
- [[Simulation Center Recording Platform]]
- [[Student Assessment Database]]
- [[Learning Management System]]
- [[SimulationIQ or equivalent platform]]

## Technical Architecture

### Core System Components

#### Rubrics-to-Prompts Engine

- Converts evaluation rubrics into structured prompts
- Transforms rubric items into yes/no claim-verification tasks
- Handles multiple acceptable answers per rubric item
- Maintains consistency across different question types

#### Zero-Shot Assessment Module

- GPT-4 based evaluation engine
- Minimal prompt engineering approach
- No prior domain-specific training required
- Adaptable to new rubrics without retraining

#### Quality Control System

- Human review for low-scoring students (bottom 20%)
- Senior evaluator adjudication for disagreements
- Statistical validation against human graders
- Continuous performance monitoring

#### Alternative Local Deployment

- Fine-tuned Llama-2-7B models
- Knowledge distillation from GPT-4
- Enhanced data privacy and security
- Institutional control over model performance

## Implementation Strategy

### Phase 1: Pilot Deployment (Months 1-3)

- Deploy for single OSCE session (preclerkship level)
- Conservative threshold (bottom 20% for human review)
- Limited to lower-stakes examinations initially
- Extensive validation against human graders

### Phase 2: Scaled Implementation (Months 4-6)

- Expand to multiple OSCE sessions
- Include clerkship-level assessments
- Optimize thresholds based on pilot results
- Implement automated quality controls

### Phase 3: Advanced Features (Months 7-9)

- Deploy local fine-tuned models
- Implement real-time performance monitoring
- Add predictive analytics for student performance
- Integrate with broader assessment ecosystem

## Validation Protocol

### Pre-Deployment Validation

- Retrospective analysis of historical notes
- Agreement analysis with expert human graders
- Statistical validation (Cohen's kappa, Spearman correlation)
- Cross-validation across different OSCE stations

### Ongoing Quality Assurance

- Continuous monitoring of AI vs. human agreement
- Regular calibration with expert evaluators
- Error analysis and system improvement
- Student outcome tracking and validation

## Risk Management

### Conservative Deployment Strategy

- Initial focus on lower-stakes examinations
- Mandatory human review for borderline cases
- Preservation of traditional grading as backup
- Extensive faculty training and buy-in

### Quality Controls

- Statistical thresholds for automated acceptance
- Senior evaluator oversight for disagreements
- Regular audit of AI grading decisions
- Student appeal process for contested grades

## Operational Benefits

### Efficiency Gains

- 91% reduction in manual grading effort
- Weeks-to-days turnaround time improvement
- Scalable to larger student populations
- Consistent grading standards

### Educational Advantages

- Faster feedback delivery to students
- More detailed and consistent evaluations
- Faculty time reallocation to teaching
- Enhanced assessment standardization

## Stakeholders

- [[Simulation Center Director]] - Implementation oversight
- [[OSCE Coordinators]] - Operational management
- [[Clinical Skills Faculty]] - Validation and quality assurance
- [[Students]] - Primary beneficiaries of faster feedback
- [[IT Support]] - Technical implementation and maintenance
- [[Assessment Committee]] - Academic standards oversight
- [[Senior Evaluators]] - Quality control and adjudication

## Budget Considerations

### Technology Costs

- GPT-4 API usage fees (per assessment)
- Local model training and deployment infrastructure
- Integration development and maintenance
- Quality assurance and monitoring systems

### Personnel Savings

- Reduced manual grading time (91% efficiency gain)
- Reallocation of faculty effort to teaching
- Decreased administrative overhead
- Faster feedback delivery value

## Related Projects

- [[Assessment - SOAP Note Grading]]

---

**Created**: {{date}} **Last Updated**: {{date}}