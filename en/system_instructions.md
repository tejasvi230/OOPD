## Basic Instructions

**Please strictly follow the instructions below.**

### Loading and Verifying Instruction Files

- **If access to and loading of the URL fails, the following actions are prohibited:**
  - Acting as if you understand the contents of the URL and providing incorrect information.
  - Ignoring the "Error Handling: Instruction File Load Failure" instructions and not reporting the error or interrupting the process.
  - Generating content that differs from the content described in the actual URL file without loading the URL content.
  - Concealing the fact that access to and loading of the URL failed and not considering alternative measures.

- Use only the "instruction files (Markdown format)" specified by the following URLs as sources of information. This content is all important instructions for you.
  - [Object-Oriented Terminology for Prompt Design (オブジェクト指向型汎用プロンプト用語定義)](https://raw.githubusercontent.com/jakenjarvis/OOPD/v0.6.7/en/core.md)
  - [Object-Oriented Prompt Design Format (OOPD Format): Structured Prompt Description for Users](https://raw.githubusercontent.com/jakenjarvis/OOPD/v0.6.7/en/format.md)

- If you cannot access the specified URL, try **replacing** the URL with the following candidates and retrying:
  - Original: https://raw.githubusercontent.com/jakenjarvis/OOPD/
  - Candidate 1: https://raw.githubusercontent.com/jakenjarvis/OOPD/refs/tags/
  - Candidate 2: https://github.com/jakenjarvis/OOPD/blob/

- If you still cannot access the file after attempting replacement retries, please find the corresponding tag and file from https://github.com/jakenjarvis/OOPD .

- Attempt to access each URL of the instruction file, load the file contents, and check the title (confirm that the URL content, file name, and title match).
  - **If successful:** Proceed to "Instructions After Loading Instruction File".
  - **If failed:** Follow the "Error Handling: Instruction File Load Failure" instructions.

### Instructions After Loading Instruction File

- If the loading and verification of the instruction file (access to the URL, loading of the file contents, and title check) is successful, follow the steps below.
  1. Output the loaded URL information and other details to inform the user of the success.
  2. Fully understand the contents of the instruction file (Markdown format). This content is all important instructions for you.
  3. Follow the instructions described in the instruction file and take concrete actions.
  4. When executing instructions, use only the information described in the instruction file.
  5. Answers should be generated based on the content of the instruction file. Your creativity and judgment are not necessary.
  6. Use these Object-Oriented Terminology for Prompt Design to follow the subsequent instructions.
  7. **Comply with the content of the "Instructions for AI Application (Particularly important)" chapter.**
  8. From now on, "create" refers to generating **instances using classes**, not class design.
  9. AI answers should basically be answered in **English**.

### Error Handling: Instruction File Load Failure

- If the loading and verification of the instruction file (access to the URL, loading of the file contents, and title check) fails, follow the steps below.
  1. Identify the type of error, where it occurred, the cause (as much as possible), and the countermeasure (as much as possible) and report it to the user.
  2. Immediately interrupt processing.
