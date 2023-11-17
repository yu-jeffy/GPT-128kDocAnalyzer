# GPT-128kDocAnalyzer

A GPT-4-1106 powered document analyzer that leverages the expanded 128k token limit to process and summarize extensive documents. Compatible with .pdf, .txt, .csv, and .docx file types.

## About

GPT-128kDocAnalyzer is a Python application designed to analyze and extract insights from large documents using OpenAI's GPT-4-1106 model. With the capability to handle up to 128k tokens in plaintext mode, this tool is ideal for summarizing long documents that would typically exceed the token limits of standard language models.

The program offers two analysis modes: plaintext and vector. The plaintext mode is suitable for larger documents, potentially translating to hundreds of pages of text, while the vector mode is optimized for smaller documents, allowing for more nuanced reasoning and the use of an agent to assist in document analysis.

An approximate calculation suggests that 128k tokens could equate to roughly 64,000 words (assuming an average of 2 tokens per word). With an average of 250-300 words per page in a typical PDF document, this would translate to approximately 213-256 pages.

...

<p align="center">
  <img src="readme_example.gif" alt="Demo GIF">
</p>

...

## Set-Up

### Prerequisites
- Python 3.10.2 or higher
- An OpenAI API key for accessing GPT-4
- The necessary Python packages installed

### Installation
1. Clone the repository to your local machine:
   ```sh
   git clone https://github.com/your-username/GPT-128kDocAnalyzer.git
   ```
2. Navigate to the cloned repository's directory:
   ```sh
   cd GPT-128kDocAnalyzer
   ```
3. Install the required Python packages:
   ```sh
   pip install -r requirements.txt
   ```
4. Create a `.env` file in the root directory of the project and add your OpenAI API key:
   ```sh
   OPENAI_API_KEY=your_openai_api_key
   ```
   Replace `your_openai_api_key` with your actual key.

## Usage

### Running the Analyzer
1. Run the `main.py` script:
   ```sh
   python main.py
   ```
2. When prompted, enter the file path to the document you wish to analyze.
3. Choose the analysis type by typing "plaintext" or "vector".
4. Enter your custom prompt for the GPT-4 model when prompted.
5. The program will process your document and return the analysis based on the chosen mode.


### Understanding the Output
- In plaintext mode, the output will be a direct response from the GPT-4 model based on your prompt and the content of the document.
- In vector mode, the output will be the result of a more complex analysis involving vector embeddings and an agent to assist in document analysis.


## Example Prompts

When using GPT-128kDocAnalyzer, crafting an effective prompt is crucial for obtaining the best results from the model. Below are some example prompts that you can use or modify according to your needs:

### Example 1: General Summary
```
Summarize this document.
```
Use this prompt when you need a concise summary of the document's content without any specific formatting or structure.

### Example 2: Market Research Summary
```
Provide a comprehensive summary of this market research document. Organize and breakdown into sections. Be insightful, professional, direct.
```
This prompt is tailored for market research documents where you need a structured summary with insights and professional tone.

### Example 3: Legal Document Analysis
```
Analyze the legal implications of the terms outlined in this contract and highlight any potential risks or unusual clauses.
```
Ideal for legal documents, this prompt directs the model to focus on the implications of contractual terms and identify any areas of concern.

### Example 4: Technical Manual Explanation
```
Explain the technical processes described in this manual in layman's terms, focusing on the steps for operating the machinery safely and efficiently.
```
Use this prompt to translate technical jargon from manuals into accessible language, emphasizing safe and effective operation procedures.


## Limitations and Considerations
- The plaintext mode, while capable of handling larger documents, may still require prompt engineering to ensure the most effective summarization or analysis.
- The vector mode is limited to a smaller token size but can provide more nuanced reasoning through the use of an agent.
- The actual number of pages that can be analyzed will depend on various factors such as the complexity of the text, formatting, and the average number of words per page.

## License
This project is licensed under the MIT License - see the LICENSE file for details.


