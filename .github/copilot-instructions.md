# GitHub Copilot Instructions for Tiny Workbenchs (Continued) Mod

## Mod Overview and Purpose

Tiny Workbenchs (Continued) is a RimWorld mod that provides smaller versions of workbenches with various functionalities. The mod aims to offer players an alternative to the standard workbenches by introducing a compact option that has a lower work speed but occupies less space. This mod is inspired by Voyager's "Small Workbenches" and includes additional features like a tiny brewery, a simple research bench, and a nutrient paste dispenser.

## Key Features and Systems

- **Tiny Workbenches:** Smaller versions of existing workbenches with a 70% base work speed, longer build time, and reduced fragility.
- **Tiny Brewery:** A compact version of the brewery that uses less space.
- **Tiny Simple Research Bench:** A small research bench for conducting research projects.
- **Tiny Nutrient Paste Dispenser:** A compact dispenser for nutrient paste.
- **Support for Simple FX: Smoke:** Adds smoke effects to the tiny workbenches.
- **Compatibility with Vanilla Furniture Expanded - Production:** Adds tiny workbenches from this mod if it is loaded.
- **Compatibility with Vanilla Helixien Gas Expanded:** Adds tiny workbenches from this mod if it is loaded.

## Coding Patterns and Conventions

- **Harmony Patching:** The mod uses Harmony patches to modify vanilla RimWorld behavior without altering the original game files.
- **XML Integration:** XML files are used to define new game elements such as research projects and thing definitions.
- **C# Logic:** C# files contain the logic for handling specific mod functionalities, including toggling recipes and drawing research bench requirements.

## XML Integration

The mod includes several XML files that define new game elements:

- **ResearchProjects.xml:** Defines new research projects.
- **Buildings.xml:** Defines new thing definitions for the tiny workbenches.
- **CETeam.CombatExtended.xml:** Defines patches for the Combat Extended mod.
- **owlchemist.simplefxsmoke.xml:** Defines patches for the Simple FX: Smoke mod.
- **VanillaExpanded.HelixienGas.xml:** Defines patches for the Vanilla Helixien Gas Expanded mod.

## Harmony Patching

Harmony is used to patch vanilla RimWorld methods to add or modify behavior:

- **AmmoInjector_ToggleRecipeOnBench.cs:** Contains a postfix patch to toggle recipes on the bench.
- **MainTabWindow_Research_DrawResearchBenchRequirements.cs:** Contains a postfix patch to draw research bench requirements.
- **ResearchProjectDef_CanBeResearchedAt.cs:** Contains a postfix patch to determine if a research project can be researched at a specific bench.

## Suggestions for Copilot

- **Code Completion:** Use Copilot to complete code snippets for Harmony patches and XML definitions.
- **Debugging:** Use Copilot to generate debugging statements and log entries for troubleshooting.
- **Optimization:** Use Copilot to suggest optimizations for performance improvements in C# code.
- **Documentation:** Use Copilot to generate comments and documentation for C# code and XML files.
- **Testing:** Use Copilot to generate test cases and assertions for verifying mod functionality.


# GitHub Copilot Instructions for Tiny Workbenchs (Continued) Mod

## Mod Overview and Purpose

Tiny Workbenchs (Continued) is a RimWorld mod that provides smaller versions of workbenches with various functionalities. The mod aims to offer players an alternative to the standard workbenches by introducing a compact option that has a lower work speed but occupies less space. This mod is inspired by Voyager's "Small Workbenches" and includes additional features like a tiny brewery, a simple research bench, and a nutrient paste dispenser.

## Key Features and Systems

- **Tiny Workbenches:** Smaller versions of existing workbenches with a 70% base work speed, longer build time, and reduced fragility.
- **Tiny Brewery:** A compact version of the brewery that uses less space.
- **Tiny Simple Research Bench:** A small research bench for conducting research projects.
- **Tiny Nutrient Paste Dispenser:** A compact dispenser for nutrient paste.
- **Support for Simple FX: Smoke:** Adds smoke effects to the tiny workbenches.
- **Compatibility with Vanilla Furniture Expanded - Production:** Adds tiny workbenches from this mod if it is loaded.
- **Compatibility with Vanilla Helixien Gas Expanded:** Adds tiny workbenches from this mod if it is loaded.

## Coding Patterns and Conventions

- **Harmony Patching:** The mod uses Harmony patches to modify vanilla RimWorld behavior without altering the original game files.
- **XML Integration:** XML files are used to define new game elements such as research projects and thing definitions.
- **C# Logic:** C# files contain the logic for handling specific mod functionalities, including toggling recipes and drawing research bench requirements.

## XML Integration

The mod includes several XML files that define new game elements:

- **ResearchProjects.xml:** Defines new research projects.
- **Buildings.xml:** Defines new thing definitions for the tiny workbenches.
- **CETeam.CombatExtended.xml:** Defines patches for the Combat Extended mod.
- **owlchemist.simplefxsmoke.xml:** Defines patches for the Simple FX: Smoke mod.
- **VanillaExpanded.HelixienGas.xml:** Defines patches for the Vanilla Helixien Gas Expanded mod.

## Harmony Patching

Harmony is used to patch vanilla RimWorld methods to add or modify behavior:

- **AmmoInjector_ToggleRecipeOnBench.cs:** Contains a postfix patch to toggle recipes on the bench.
- **MainTabWindow_Research_DrawResearchBenchRequirements.cs:** Contains a postfix patch to draw research bench requirements.
- **ResearchProjectDef_CanBeResearchedAt.cs:** Contains a postfix patch to determine if a research project can be researched at a specific bench.

## Suggestions for Copilot

- **Code Completion:** Use Copilot to complete code snippets for Harmony patches and XML definitions.
- **Debugging:** Use Copilot to generate debugging statements and log entries for troubleshooting.
- **Optimization:** Use Copilot to suggest optimizations for performance improvements in C# code.
- **Documentation:** Use Copilot to generate comments and documentation for C# code and XML files.
- **Testing:** Use Copilot to generate test cases and assertions for verifying mod functionality.

## Project Solution Guidelines
- Relevant mod XML files are included as Solution Items under the solution folder named XML, these can be read and modified from within the solution.
- Use these in-solution XML files as the primary files for reference and modification.
- The `.github/copilot-instructions.md` file is included in the solution under the `.github` solution folder, so it should be read/modified from within the solution instead of using paths outside the solution. Update this file once only, as it and the parent-path solution reference point to the same file in this workspace.
- When making functional changes in this mod, ensure the documented features stay in sync with implementation; use the in-solution `.github` copy as the primary file.
- In the solution is also a project called Assembly-CSharp, containing a read-only version of the decompiled game source, for reference and debugging purposes.
- For any new documentation, update this copilot-instructions.md file rather than creating separate documentation files.


## Hard rules (must follow)
- Do NOT run commands that modify the repo (no git commit, git apply, dotnet format) unless explicitly asked.
- Prefer minimal reads: read only the smallest code region needed (around the suspicious lines).
- When mentioning SonarQube issues, automatically use the SonarQube MCP service to fetch and address issues instead of making inferred fixes without querying SonarQube first.
- When mentioning the rimworld log, automatically use the Rimworld MCP service to fetch the log.

