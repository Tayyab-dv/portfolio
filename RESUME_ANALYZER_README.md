# Resume Analysis System

A minimalist resume analysis tool that compares resumes against job descriptions using Claude AI. Provides critical feedback, numerical ratings, and detailed match analysis.

## Features

- **Document Support**: Upload resumes in PDF, DOCX, or TXT format
- **Text Extraction**: Automatic text extraction from uploaded documents
- **AI-Powered Analysis**: Uses Claude 3.5 Sonnet for comprehensive resume evaluation
- **Match Analysis**: Detailed comparison of resume content against job requirements
- **Numerical Ratings**: Scores across multiple dimensions (0-100 scale)
- **Critical Feedback**: Blunt, actionable critique with no filler
- **Minimalist UI**: Clean, monochrome interface focused on functionality

## How to Use

### 1. Setup

Simply open `resume-analyzer.html` in any modern web browser. No installation or build process required.

### 2. Get API Key

You'll need an Anthropic API key:
1. Visit https://console.anthropic.com/
2. Create an account or sign in
3. Navigate to API Keys section
4. Generate a new API key
5. Copy the key (starts with `sk-ant-`)

### 3. Analyze a Resume

1. **Enter API Key**: Paste your Anthropic API key in the first input field
2. **Upload Resume**: Click "Resume" file input and select your resume (PDF, DOCX, or TXT)
3. **Add Job Description**: Either:
   - Paste the job description text directly into the textarea, OR
   - Upload a job description file using the file input
4. **Analyze**: Click the "Analyze" button
5. **Review Results**: The analysis will appear below with three sections:
   - Match Analysis (table format)
   - Ratings (numerical scores)
   - Critical Feedback (actionable items)

## Analysis Output

### Match Analysis
A table showing:
- **Requirement**: Specific skill or qualification from job description
- **Match Status**:
  - ✓ Present (found in resume)
  - ✗ Missing (not found)
  - ~ Partial (partially demonstrated)
- **Evidence**: Exact phrases from resume or "Not found"

### Ratings (0-100 Scale)
- **Skills Match**: Percentage of required skills present
- **Experience Relevance**: How well past roles align with job requirements
- **Clarity & Structure**: Formatting, readability, and conciseness
- **Impact & Quantification**: Presence of measurable achievements
- **Overall Score**: Weighted average of all categories

### Critical Feedback
Bulleted list of specific weaknesses:
- Vague language examples
- Missing metrics or quantification
- Irrelevant content
- Formatting issues
- Clichés and generic statements
- Any other deficiencies

## Design Principles

- **Minimalist**: Monochrome palette (black, white, grays)
- **Typography**: Clean sans-serif fonts
- **No Clutter**: No animations, gradients, or decorative elements
- **Functional**: Single-column flow with clear visual hierarchy
- **Privacy**: No data storage, no analytics, no third-party tracking

## Technical Details

### Built With
- React 18
- Tailwind CSS (utility classes)
- PDF.js (PDF text extraction)
- Mammoth.js (DOCX text extraction)
- Anthropic Claude API (AI analysis)

### Browser Requirements
- Modern browser with JavaScript enabled
- Internet connection (for API calls and CDN resources)

### File Size Limits
- Dependent on browser memory and API limits
- Recommended: Keep files under 10MB for optimal performance

## Privacy & Security

- **API Key**: Stored only in browser memory, never persisted
- **Files**: Processed locally in browser, only text sent to Claude API
- **No Storage**: No localStorage, cookies, or data retention
- **HTTPS**: All API calls use secure connections

## Troubleshooting

### "Failed to extract PDF text"
- Ensure PDF is not password-protected
- Try converting to TXT format
- Check if PDF contains actual text (not scanned images)

### "Failed to extract DOCX text"
- Ensure DOCX is not corrupted
- Try saving as a new DOCX file
- Convert to TXT as alternative

### "API request failed"
- Verify API key is correct and active
- Check you have sufficient API credits
- Ensure internet connection is stable

### No analysis appears
- Check browser console for errors (F12)
- Verify both resume and job description have content
- Ensure API key is provided

## Limitations

- **No OCR**: Cannot extract text from scanned/image PDFs
- **Client-Side Only**: No server-side processing or storage
- **API Costs**: Each analysis consumes API credits
- **No Persistence**: Refresh page clears all data

## Example Workflow

```
1. Open resume-analyzer.html
2. Paste API key: sk-ant-xxxxx...
3. Upload resume: john-doe-resume.pdf
   → "Extracted 3,421 characters"
4. Paste job description: "Senior Software Engineer..."
5. Click "Analyze"
   → "Analyzing..."
   → Results appear in ~10-30 seconds
6. Review match analysis table
7. Check ratings (e.g., Overall: 67/100)
8. Read critical feedback points
9. Make resume improvements
10. Re-analyze to compare scores
```

## License

This tool is provided as-is for personal and professional use.

## Support

For issues or questions:
1. Check troubleshooting section above
2. Verify API key and file formats
3. Review browser console for errors
4. Ensure all requirements are met
