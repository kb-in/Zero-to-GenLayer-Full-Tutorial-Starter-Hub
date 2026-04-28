“Zero to GenLayer — Full Tutorial + Starter Hub”

GOAL:
Create a full educational + practical tutorial website that teaches a user how to go from ZERO to building a working GenLayer dApp.

IMPORTANT:
- Pure frontend (HTML, CSS, JS)
- No backend required
- Must work on iPad/mobile
- Clean Web3 dark UI

---

STRUCTURE:

1. HERO
Title: “Zero to GenLayer 🚀”
Subtitle: “Learn, Build, Deploy — AI Smart Contracts in minutes”

Buttons:
- Start Tutorial
- Open Studio

---

2. QUICK START HUB (cards with links)

- Studio (https://studio.genlayer.com)
- Faucet (https://faucet.genlayer.com)
- Docs (https://docs.genlayer.com)
- Boilerplate (GitHub)

Each card:
- icon
- short explanation
- button

---

3. CORE CONCEPTS (MANDATORY FOR MISSION)

Create simple explanation cards:

- Optimistic Democracy
Explain like:
“Validators run AI independently and agree on result”

- Equivalence Principle
Explain:
“Defines what counts as the same result”

---

4. STEP-BY-STEP TUTORIAL (MAIN PART)

Create visual steps:

Step 1 → Open Studio  
Step 2 → Create contract  
Step 3 → Paste code  
Step 4 → Deploy  
Step 5 → Call function  

---

5. FULL WORKING CONTRACT (IMPORTANT)

Include a REAL GenLayer contract (not fake)

Example:

# { "Depends": "py-genlayer:test" }

from genlayer import *

class YesNoOracle(gl.Contract):
    answers: gl.DynArray[bool]

    def __init__(self):
        self.answers = gl.DynArray[bool]()

    @gl.public.write
    def ask(self, question: str):

        def call_ai():
            result = gl.exec_prompt(f"Answer YES or NO: {question}")
            return "YES" in result.upper()

        answer = gl.eq_principle_strict_eq(call_ai)
        self.answers.append(answer)

    @gl.public.view
    def get(self, index: int) -> bool:
        return self.answers[index]

Add COPY BUTTON

---

6. FRONTEND INTERACTION (VERY IMPORTANT)

Show how frontend works with genlayer-js:

Display example JS code:

- writeContract()
- readContract()
- waitForTransactionReceipt()

Explain simply:
“This is how your website talks to blockchain”

---

7. ARCHITECTURE SECTION

Show flow:

User → Frontend → Contract → AI → Validators → Blockchain → Result

---

8. MINI PROJECT IDEA (REQUIRED)

Include 1 real idea like:

“AI Oracle dApp”
User asks question → blockchain returns YES/NO

---

9. LEARNING PATH

Beginner → Contract → Deploy → Frontend → Build your own dApp

---

10. FINAL CTA

“Now you are ready to build 🚀”

Buttons:
- Open Studio
- View Docs
- Start Building

---

FEATURES:
- Smooth scroll
- Sticky navbar
- Responsive design
- Clean UI
- Copy buttons
- Section animations

---

OUTPUT:
- Single index.html file
- Fully styled
- Ready to deploy on Netlify/Vercel
