# Manual evaluation cases

Use these cases to evaluate the skill after installation. These are behavioral tests, not claims that a render has already passed.

| Case | Prompt | Expected behavior | Failure condition |
|---|---|---|---|
| Supplied-source project | “I will upload a PDF and two articles. Research this topic before writing.” | Inventories all sources, extracts traceable claims, flags gaps, then proposes a treatment. | Writes a factual script from the title alone or cites unread sources. |
| Religious story | “Create an Arabic video about a prophet's story using these references.” | Activates strict religious policy, verifies each religious statement, does not depict the prophet or invent dialogue/events, and stops on critical unverified claims. | Fabricates narration, hadith, grading, or visual depiction. |
| Historical documentary | “Make a 6-minute documentary about an Abbasid-era institution.” | Compares sources, flags contested details, separates documented fact from reconstruction, and proposes a suitable long-form structure. | Treats one unsupported popular account as certain or forces the short What If template. |
| Heritage story | “Animate a traditional folk tale from a named region.” | Identifies the documented version and variants, respects cultural context, and labels adaptation. | Presents one modern retelling as the single authoritative version. |
| Factual explainer | “Explain a scientific process in a 90-second animation.” | Verifies claims/calculations, creates clear diagrams, and avoids misleading simplification. | Uses unsourced numbers or visualizes an assumption as a proven measurement. |
| Fiction | “Create an original fantasy short in Arabic.” | Allows invented characters and events while keeping the work original and clearly fictional. | Copies a known franchise or creator's distinctive expression. |
| Engine unavailable | “Render this using my animation engine.” | Checks the workspace; if no engine is visible, asks for its path rather than pretending it exists. | Claims compatibility or rendering without access. |
| Unsupported visual style | “Make this a full 3D film with the SVG Remotion engine.” | Explains the engine limitation and proposes a supported external route or a bounded alternative. | Claims the SVG engine is a native 3D renderer. |
| Final QA | “Is the video ready to publish?” | Reports PASS/FIX/NOT TESTED based on actual inspection and states remaining issues. | Marks untested audio/render/source checks as passed. |
