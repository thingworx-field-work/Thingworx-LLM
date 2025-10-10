### 🧠 ThingWorx + LLM Accelerator — Version 2.0 Release Overview

This best practice and demo application showcase how to integrate ThingWorx with large language models (LLMs) such as ChatGPT-4.1 using a secure, modular, and enterprise-ready design.
Version 2.0 builds on the original “ThingWorx + LLM” accelerator, adding advanced analytics capabilities, stronger guardrails, and a redesigned architecture that makes LLM interactions smarter, faster, and easier to extend.

The updated Best Practice Document (V2) walks through every component of the new accelerator and explains how ThingWorx and LLMs communicate through simple, authenticated API calls — no additional packages or libraries required.
It also includes detailed guidance for setup, security, and validation when using enterprise-grade AI services such as Microsoft Azure OpenAI.

### 🔄 What’s New in V2

Analytics Insights Integration: Version 2 connects directly with ThingWorx Analytics to interpret results from Signals, Profiles, Datasets, and Predictive Models. Users can now ask questions such as “Which factors most influence grinder failure?” or “How accurate is the predictive model trained on the Bean Pro dataset?”

Router-Based Architecture: The accelerator now includes a dynamic “router” that allows the LLM to decide which ThingWorx services to execute to answer a user’s question. This approach reduces token cost, improves response accuracy, and increases transparency.

Expanded Service Library: V2 introduces 17 modular services, replacing the 5 from V1. Each is clearly scoped to handle data, analytics, or orchestration tasks, making it easier to customize for specific use cases.

Updated Mashup & UI: The mashup now features two tabs — Data Insights (V1) and Analytics Insights (V2) — following PTC’s corporate design template for a cleaner, more intuitive experience.

Improved Validation & Governance: The document outlines best practices for cross-checking LLM outputs against ThingWorx data, adding human-in-the-loop review, and applying data-protection safeguards throughout the integration.


### 📊 Demo Application

The accelerator project (PTCDTS.TWXLLM) includes:

- A Manager Thing that handles API communication with the LLM and ThingWorx Analytics microservices
- A Data Table and Data Shapes defining example manufacturing data
- A Mashup (PTCDTS.TWXLLM.Insights_MU) providing side-by-side tabs for Data Insights and Analytics Insights
- A Repository containing example Analytics files (DEMO_BEANPRO_DATA.csv, DEMO_BEANPRO_METADATA.json)

You can import the project into ThingWorx 9.5.0 or later, set your LLM credentials, and start running queries immediately.

🧩 Flexible, Secure, and Extensible

The techniques in this release are designed to be adaptable.
Whether your data comes from ThingWorx Value Streams, historians, SQL databases, or custom APIs — or whether you use Azure OpenAI, another hosted LLM, or an on-prem model — the integration pattern remains the same:
extract → contextualize → prompt → validate.

By following these best practices, organizations can safely harness generative AI to make industrial data more understandable and actionable — improving productivity, decision-making, and time-to-insight while keeping sensitive information protected.

### Authors
David Kessler (dkessler@ptc.com)

*This version builds on V1.1, co-authored with Brad Cline (bcline@ptc.com)

### Disclaimer
Users are solely responsible for the use of and reliance on the demo application and the accompanying document which integrates ThingWorx with ChatGPT-4.1, a generative Artificial Intelligence (AI) tool. The project file for the demo application is provided for demonstration purposes only and should not be used in production without thorough testing.

Users acknowledge that PTC Inc. owns the intellectual property rights to this demo application. A limited, free, non-exclusive license is granted to users for demonstration and educational purposes only.

Due to the inherent unpredictability of generative AI tools, users further acknowledge that generated output may be inaccurate or harmful, and that users must apply human judgment and consider associated risks when evaluating generated output.

PTC disclaims liability for any losses or damages arising from the use of the demo application and this document. Users are responsible for outcomes from using the demo and document, and assume responsibility for complying with all relevant laws, including but not limited to data privacy, security, and the EU AI Act.

Your license to commercial versions of PTC products may not include all APIs needed to connect to AI tools and may require additional licensing.

By downloading this software, the user acknowledges that it is unsupported, not reviewed for security purposes, and that the user assumes all risk for running it.

Users accept all risk whatsoever regarding the security of the code they download.

This software is not an official PTC product and is not officially supported by PTC.

PTC is not responsible for any maintenance for this software.

PTC will not accept technical support cases logged related to this Software.

This source code is offered freely and AS IS without any warranty.

The author of this code cannot be held accountable for the well-functioning of it.

The author shared the code that worked at a specific moment in time using specific versions of PTC products at that time, without the intention to make the code compliant with past, current or future versions of those PTC products.

The author has not committed to maintain this code and he may not be bound to maintain or fix it.

### License
I accept the MIT License (https://opensource.org/licenses/MIT) and agree that any software downloaded/utilized will be in compliance with that Agreement. However, despite anything to the contrary in the License Agreement, I agree as follows:

I acknowledge that I am not entitled to support assistance with respect to the software, and PTC will have no obligation to maintain the software or provide bug fixes or security patches or new releases.

The software is provided “As Is” and with no warranty, indemnitees or guarantees whatsoever, and PTC will have no liability whatsoever with respect to the software, including with respect to any intellectual property infringement claims or security incidents or data loss.
