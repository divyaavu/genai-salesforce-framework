# GEN-AI Plugin – Code Framework

A modular repository demonstrating how to structure a **VS Code extension** integrated with **LLM-based automation for Salesforce**.  
It includes organized source code, reusable libraries, and a complete **training data workspace** with Salesforce page examples and JSONL datasets used for fine-tuning or instruction-based model experiments.

---

## Overview

This project provides a **reference implementation** for integrating generative AI into developer workflows.  
It showcases:
- A maintainable VS Code plugin structure
- AI-driven data preparation (prompt/response style JSONL)
- Realistic domain data (Salesforce pages)
- A clear folder layout for extension, assets, libraries, and datasets

---

## Highlights

- **Modular architecture** separating extension logic, assets, and training data  
- **Salesforce domain coverage** — includes page templates (`*.txt`) for core modules like *Incident, Opportunity, Orders,* and *Individuals*  
- **Training & validation datasets** formatted in `.jsonl` for model evaluation  
- **Lightweight and easy to scan** for code reviews or interview demonstrations  

---

## Repository Structure

CodeFramework/
├─ ai-extensionsgen/ # Core VS Code extension logic
├─ assets/
│ └─ images/ # Icons and visuals (plugin UI assets)
├─ lib/
│ ├─ marked/ # Markdown rendering library
│ └─ prism/ # Syntax highlighting library
├─ src/ # Scripts and style modules
├─ training/ # Domain-specific training data
│ ├─ AppLauncherPage.txt
│ ├─ HomePage.txt
│ ├─ IncidentPage.txt
│ ├─ OpportunityPage.txt
│ ├─ OrdersPage.txt
│ ├─ ... # Additional Salesforce page samples
│ ├─ training_data_chat.jsonl # Prompt-response training dataset
│ └─ validation_data_chat.jsonl # Validation dataset
├─ manifest.json # Extension manifest
├─ package.json # Dependency and metadata config
└─ panel.html # Example UI view


---

## Data Overview

### Salesforce Page Samples (`training/*.txt`)
Each text file represents a page or feature within Salesforce, containing realistic content for model context or automation prompts.  
These serve as input materials for LLM prompt engineering and automation testing.

### JSONL Datasets
- **`training_data_chat.jsonl`** – example training set defining system/user messages for generating Selenium page object classes or Salesforce-based automation templates.  
- **`validation_data_chat.jsonl`** – parallel validation set to evaluate accuracy and consistency.

Each line follows the JSONL schema:

```json
{
  "messages": [
    {"role": "system", "content": "You are an expert in generating Selenium Java page object classes using provided DOM information."},
    {"role": "user", "content": "Generate page object for Opportunity Page"}
  ]
}




The data can be used for experimenting with LLM fine-tuning, code generation, or intelligent test script creation.



