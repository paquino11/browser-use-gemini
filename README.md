# Browser Use with Gemini 2.0 Flash Example

This project demonstrates how to use Browser Use with Gemini 2.0 Flash to navigate to [Google Flights](https://www.google.com/travel/flights) and book flights. It uses:
- [langchain_google_genai](https://pypi.org/project/langchain-google-genai/) for the AI model
- [browser-use](https://pypi.org/project/browser-use/) for browser automation

---

## Table of Contents

- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Configuration](#configuration)
- [Usage](#usage)
- [Project Structure](#project-structure)
- [License](#license)

---

## Prerequisites

1. **Python 3.9 or later** (recommended).
2. A valid **Google API Key** with access to Google Generative AI (Gemini). 
3. (Optional) **Google Chrome** installed. You can customize the Chrome executable path if needed.

---

## Installation

1. **Clone this repository**:

   ```bash
   git clone https://github.com/your-username/your-repo-name.git
   cd your-repo-name
   ```

2. Create and activate a virtual environment (optional but recommended):

   ```bash
   # On Linux/MacOS
   python3 -m venv venv
   source venv/bin/activate

   # On Windows
   python -m venv venv
   venv\Scripts\activate
   ```

3. Install dependencies:

   ```bash
   pip install -r requirements.txt
   ```

## Configuration

1. Set up the .env file:

   ```bash
   cp .env.example .env
   ```

2. Update the GOOGLE_API_KEY value in your .env file:

   ``` 
   GOOGLE_API_KEY=your_real_google_api_key
   ```

3. (Optional) Specify a custom Chrome path:

   If you want to use a custom Chrome installation path, open demo.py and uncomment or modify:

   ```python
   # browser = Browser(
   #     config=BrowserConfig(
   #         chrome_instance_path='/path/to/your/chrome', 
   #     )
   # )
   ```

## Usage
Run the demo:
```bash
python demo.py
```
What it does:

- Initializes a language model using Gemini 2.0 (gemini-2.0-flash).
- Spins up a browser automation instance.
- Navigates to Google Flights.
- Attempts to book a flight from Gothenburg to London for the specified dates (2025-03-01 to 2025-03-10).
- If everything is configured correctly, you should see the browser open and carry out the flight booking steps.

