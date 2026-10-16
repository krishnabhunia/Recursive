# Recursive — Windows Forms prototype

## What this repository actually contains
A .NET Framework 4.8 Windows Forms desktop skeleton intended for recursive path/file operations, currently without the underlying traversal logic.

**Technology:** C#, WinForms, .NET Framework 4.8, ZetaLongPaths package.

## Confirmed components
| File | Role |
|---|---|
| `Recursive/Form_Fetch_ALL_Details.cs` | Form and empty Start/link-click handlers |
| `Recursive/Form_Fetch_ALL_Details.Designer.cs` | UI controls/layout |
| `Recursive/Program.cs` | Desktop program entry |
| `Recursive.sln` | Visual Studio build target |

## System architecture
~~~mermaid
flowchart LR
 User[User / developer] --> Entry[WinForms executable]
 Entry --> Logic[Application code]
 Logic --> Resource[UI event handlers]
~~~

## Execution and data flow
~~~mermaid
sequenceDiagram
 participant U as User
 participant A as Windows application
 participant R as UI handlers
 U->>A: Open / interact
 A->>R: Read or invoke functionality
 R-->>A: Current result
 A-->>U: Display / report
~~~

## Installation and setup
1. On Windows install Visual Studio, .NET desktop development workload and .NET Framework 4.8 targeting pack.
2. Open Recursive.sln, restore NuGet packages including ZetaLongPaths, and build the solution.
3. Run in Visual Studio to inspect the form; functionality is not implemented in the Start/link handlers.

~~~mermaid
flowchart TD
 A[Clone GitHub project] --> B[Prepare platform and dependencies]
 B --> C[Open/run project]
 C --> D{Check project behavior}
 D -->|Pass| E[Inspect features and tests]
 D -->|Fail| F[Review setup and known limitations]
 F --> B
~~~

## Current functionality and usage
The application opens a Windows Forms UI. Current code in btn_Start_Click and ll_Path_LinkClicked is empty; it should not be represented as a working recursive scanner.

## Validation protocol
- A PR workflow validates documentation structure and GitHub-local links.
- Windows GitHub Actions attempts a .NET Framework 4.8 build; no automated desktop interaction tests exist.
- Check the specific PR **Checks** tab for run results; documentation is not proof of working application features.
- Manual smoke test should follow the sequence above and compare observed behavior with the source.

## Gaps and limitations
- Prototype only: no recursive file search or processing implementation is committed.
- No unit tests or CLI interface; UI event actions are empty.
- Do not promise results, file traversal, or performance until these are built and tested.
- Geographic maps and benchmark graphs are intentionally not invented: this project does not provide verified geospatial or measured performance information.
- Runtime/source fixes should be isolated from this documentation-focused PR.
