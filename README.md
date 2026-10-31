# 🚖 Instant - ASI:One Agent Challenge Submission

Instant is an autonomous ride-share coordinator built for the Fetch.ai ecosystem. It intercepts expensive solo cab rides at major transit hubs and uses geospatial matching to group co-passengers arriving on the same train or flight, splitting the fare securely before a cab is even booked.

## 🚀 Core Features & Challenge Criteria
* **Agent Chat Protocol (ACP):** Full conversational workflow completed entirely inside the ASI:One chat interface without relying on external web frontends.
* **ASI:One Native LLM:** Parses complex user intents, extracting train PNRs, arrival hubs, and destination routing.
* **ASI1 Interactive Cards:** Renders rich UI directly in the chat to visually prove the exact money saved (e.g., crossing out a ₹1200 solo fare and highlighting the ₹400 split fare).
* **Agent Payment Protocol:** Simulates a decentralized escrow system to securely lock passenger funds before the final cab booking.

## 🛠️ How to Run & Test (For Judges)
This agent is completely contained within a single Python file and designed to run instantly on the Agentverse Web IDE.

**Step 1: Deploy on Agentverse**
1. Navigate to **Hosted Agents** in the [Agentverse Dashboard](https://agentverse.ai).
2. Click **+ New Agent** and select a blank template.
3. Copy the entire contents of `agent.py` from this repository and paste it into the Web IDE.
4. Click **Run** and copy the generated Agent Address.

**Step 2: Interact on ASI:One**
1. Open the ASI:One interface and search for the agent using the Agent Address.
2. To trigger the mock geospatial database and fare-splitting logic, send this exact prompt:
   > *"I just arrived at KSR Bengaluru, my PNR is 12628 and I need to go to Kumaraswamy Layout."*

**Expected Output:**
The agent will parse the intent, verify the PNR against active travelers, and output an ASI1 Interactive Card matching you with verified riders (Yuvraj Soni and Harshit Chandiramani). The card will explicitly show the ₹800 savings. Clicking "Accept Match" will trigger the Agent Payment Protocol escrow confirmation.
