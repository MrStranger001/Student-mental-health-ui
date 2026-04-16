🌿 Student Mental Health UI (Sanctuary OS)Sanctuary OS is an immersive, privacy-first emotional support tool designed for students. Unlike traditional wellness apps, it focuses on instant relief through high-fidelity audio synthesis and kinetic visual environments.
🚀 Core FeaturesBinaural Atmospheric Engine: A custom-built audio synthesizer using the Web Audio API. It generates Brownian Noise (Velvet Rain) and 110Hz Binaural Hums mathematically to induce a deep "Flow State" without external audio files.Kinetic Forest Environment: A multi-layered, parallax background where greenery (ferns and leaves) sways dynamically based on the user's mood and breathing pace.Resilience Bank: A secure, local-first "message vault" that allows users to save motivational notes to their future selves.10 Pillars of Gratitude: A structured reflection system designed to rewire the brain for positivity through daily micro-habits.Star Resonance Visuals: A celestial breathing guide that expands from a central star to a full-diameter glow, syncing the user's breath with light.

🛠 Tech Stack
Frontend: React.js (Vite)
Styling: Tailwind CSS (Glassmorphism & Custom Animations)
Audio: Web Audio API (Oscillators, Biquad Filters, Gain Nodes)
State Management: React Hooks (useState, useEffect, useRef)
Persistence: Browser LocalStorage (Zero-Login Privacy)

🧠 Technical Challenges & Solutions
1. The "Harsh Audio" ProblemChallenge: Standard White Noise was too sharp and irritating for stressed users.Solution: Implemented a Brownian Noise Algorithm that integrates random values to create a deeper, softer "patter" sound. I applied a Low-Pass Biquad Filter at $550\text{Hz}$ to remove high-frequency hiss.
2. 2. Browser Autoplay PoliciesChallenge: Modern browsers block audio from starting automatically.Solution: Built a Hardware Unlock System. The AudioContext is suspended until the user's first meaningful interaction (selecting a mood or clicking the "Breathe" circle), ensuring 100% sound reliability.
3. Kinetic PerformanceChallenge: Animating many high-resolution images can lag a student's laptop.Solution: Used CSS Keyframe Transforms on a few layered SVG/Emoji elements. This offloads the animation to the GPU, keeping the CPU free for audio processing.
