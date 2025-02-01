# Job Hunter

An AI-powered tool to help tailor your job application materials using CrewAI agents.

## Overview

Job Hunter is a Python-based application that uses multiple AI agents to analyze job postings, customize resumes, and prepare interview materials. The system employs a crew of specialized agents working together to create a comprehensive job application package.

NOTE: This package is almost idfentical to the example from this short course on deeplearning.ai: [Multi AI Agent Systems with crewAI](https://learn.deeplearning.ai/courses/multi-ai-agent-systems-with-crewai)

## Features

- Job posting analysis and requirement extraction
- Resume tailoring based on job requirements
- Interview preparation materials generation
- Automated document creation and management

## Project Structure

```
job_hunter/
├── create_resume.py        # Main application script
├── interview_materials.md  # Generated interview prep content
├── tailored_resume.md     # Job-specific customized resume
├── resume.md              # Original resume template
└── db/                    # Database storage
    ├── chroma.sqlite3
    └── b0fbbecc-646e-42cf-8139-21a3f0de62c2/
```

## Agents

The application uses four specialized AI agents:

1. **Tech Job Researcher**: Analyzes job postings to extract key requirements and qualifications
2. **Personal Profiler**: Creates comprehensive candidate profiles based on provided materials
3. **Resume Strategist**: Tailors resumes to match job requirements while maintaining authenticity
4. **Interview Preparer**: Generates relevant interview questions and talking points

## Requirements

- Python 3.11.x
- OpenAI API key
- Required Python packages:
  - crewai
  - python-dotenv
  - crewai-tools

## Setup

1. Clone the repository
2. Create a `.env` file with your OpenAI API key:
   ```
   OPENI_API_KEY=your_api_key_here
   SERPER_API_KEY==your_api_key_here # https://serper.dev
   ```
3. Install the required dependencies:
   ```bash
   pip install -r requirements.txt
   ```

## Usage

1. Update your resume in `resume.md`
2. Run the application:
   ```bash
   python create_resume.py
   ```
3. The script will generate:
   - A tailored resume (`tailored_resume.md`)
   - Interview preparation materials (`interview_materials.md`)

## Input Parameters

The system requires the following inputs:
- Job posting URL
- GitHub profile URL
- Personal writeup/bio

## Output Files

- **tailored_resume.md**: A customized version of your resume highlighting relevant skills and experiences for the specific job
- **interview_materials.md**: Comprehensive interview preparation document including potential questions and talking points

## Note

The system is designed to enhance your existing resume and create preparation materials while maintaining authenticity. It will not fabricate or add false information to your resume.

## Contributing

Feel free to submit issues and enhancement requests.

## License

MIT