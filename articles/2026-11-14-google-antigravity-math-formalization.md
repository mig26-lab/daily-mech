# Google’s Antigravity /teamwork Multi-Agent Systems Formalize Landmark Mathematical Proofs

![AI and mathematical concepts](https://cdn.pixabay.com/photo/2018/05/08/21/28/artificial-intelligence-3382507_1280.jpg)
*Image from Pixabay under free Content License. Source: [Pixabay](https://pixabay.com/illustrations/artificial-intelligence-3382507/)*

On November 13, 2026, Google Research detailed results from its Antigravity platform’s /teamwork multi-agent harness. Specialized teams of AI agents, powered by Gemini models, produced machine-checked formalizations of major mathematical results, including a full formalization of the Weil conjectures and a proof of the 2013 Courtade–Kumar conjecture.

The Weil conjectures concern the number of solutions to polynomial equations over finite fields. Pierre Deligne’s 1974 proof was a landmark in algebraic geometry. Google’s Teamwork-LEAP system generated approximately 1.8 million lines of Lean code across 28,800 subagent invocations to produce an end-to-end, machine-checked formalization. A separate effort synthesized over 919,000 lines of Lean for a formalization related to Hilbert’s tenth problem over rings of integers.

Researchers from Google, CUHK, USC, and CMU used the Long Proof pattern (Stellar Colosseum) inside Antigravity to prove the Courtade–Kumar conjecture in full generality. The system also assisted with formalizations connected to Navier–Stokes equations and other open problems.

## How the Multi-Agent System Operates

Antigravity’s /teamwork feature coordinates specialized agents. One pattern breaks long proofs into sub-tasks; others handle formalization, verification, and software engineering. Agents operate under human guidance for high-level direction while executing the bulk of the formalization work. Gemini models (including Argon) generate and check Lean proofs, which a computer can then verify independently.

This differs from single-model approaches. Division of labor across agents allows sustained progress on proofs that exceed typical context windows or single-session reasoning limits. The published results emphasize machine-checked output rather than informal claims.

## Broader Implications for Formal Verification

Formal verification has long been limited by the human effort required to translate mathematical arguments into proof assistants such as Lean. Multi-agent systems that generate and refine large volumes of Lean code lower that barrier. Potential applications extend beyond pure mathematics to cryptographic protocol verification (DeepMind has separately used similar techniques on Signal’s encryption code), software correctness, and safety-critical systems.

Google’s results sit alongside other 2026 formalization efforts. Independent groups have also formalized parts of the Weil conjectures and related conjectures with AI assistance, though the scale reported by Google (1.8 million lines for the Weil conjectures) stands out. Independent review of the generated Lean libraries will be necessary to confirm completeness and absence of gaps.

## Limitations and Next Steps

The systems still require human oversight for problem selection, intermediate checks, and final validation. Computational cost is not fully disclosed. The Lean formalizations prove the statements as formalized; they do not automatically generate new mathematical insights beyond what the agents derive under guidance.

Google positions the work as evidence that multi-agent harnesses can accelerate scientific and engineering tasks when paired with strong foundation models. The company has also used similar setups for molecular structure identification from NMR data (reported ~95% accuracy in one test) and software optimization (a Rust rewrite of an AV1 decoder that ran 20–30% faster than the C++ original).

For the AI and formal methods communities, these results demonstrate that agent teams can produce verifiable artifacts at a scale previously associated with large human collaborations. Whether the same techniques reliably transfer to other domains remains an open question that will be tested in the coming months.

## Sources and References

1. Google Research blog: Advancing science & engineering with Antigravity’s /teamwork (November 13, 2026). https://research.google/blog/advancing-science-engineering-with-antigravitys-teamwork-feature/
2. Interesting Engineering: Google Antigravity agents tackle 90-year-old math problem and rewrite software (November 13–14, 2026).
3. Lean Weekly and contemporaneous formalization reports on Weil conjectures and related efforts (November 2026).
4. Google DeepMind prior work on AlphaProof Code for Signal protocol verification.

*Article compiled from public announcements and contemporaneous reporting. Images sourced from Pixabay under free license.*