# Overview

This white paper focuses on a demo application that integrates ThingWorx with ChatGPT-4o. We explain the
components of the application and how they collectively facilitate communication between ThingWorx and the
LLM through an API. Ultimately natural language questions from the user are answered in a similar fashion.
Although our example uses a specific LLM service, the application and concepts it illustrates can be easily
adapted to work with other data stores and other LLMs. The demo data used by the application is stored in a
ThingWorx Data Table, for the sake of easy importing. The process covers extracting data from the Data Table,
preparing it, and creating prompts that let ThingWorx talk with the LLM to deliver useful, natural language answers.
The methods outlined here are flexible. Even if your data comes from ThingWorx Value Streams, historians, or other
databases, the overall approach remains the same. You simply extract the relevant data, add context, and feed it
into the LLM. Likewise, if you choose a different LLM service, the main steps—API communication, data
transformation, and response checking—will still apply with only minor changes.
A specific context for using ThingWorx and LLMs is for Statistical Process Control (SPC). In many factories, SPC is
used to track when processes go "out of control" over time. With this setup, you can ask questions like, “What were
the out-of-control events for Machine 5 last month?” The system can then pull together historical and real-time
SPC data to show when and where rules were violated. This helps teams quickly spot problems and make
improvements.

# Authors
David Kessler
Brad Cline

# Disclaimer
By downloading this software, the user acknowledges that it is unsupported, not reviewed for security purposes, and that the user assumes all risk for running it.

Users accept all risk whatsoever regarding the security of the code they download.

This software is not an official PTC product and is not officially supported by PTC.

PTC is not responsible for any maintenance for this software.

PTC will not accept technical support cases logged related to this Software.

This source code is offered freely and AS IS without any warranty.

The author of this code cannot be held accountable for the well-functioning of it.

The author shared the code that worked at a specific moment in time using specific versions of PTC products at that time, without the intention to make the code compliant with past, current or future versions of those PTC products.

The author has not committed to maintain this code and he may not be bound to maintain or fix it.

# License
I accept the MIT License (https://opensource.org/licenses/MIT) and agree that any software downloaded/utilized will be in compliance with that Agreement. However, despite anything to the contrary in the License Agreement, I agree as follows:

I acknowledge that I am not entitled to support assistance with respect to the software, and PTC will have no obligation to maintain the software or provide bug fixes or security patches or new releases.

The software is provided “As Is” and with no warranty, indemnitees or guarantees whatsoever, and PTC will have no liability whatsoever with respect to the software, including with respect to any intellectual property infringement claims or security incidents or data loss.
