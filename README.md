# 📊 AI DAX Generator

### Generate Power BI DAX Expressions Using Artificial Intelligence

An AI-powered application that helps Power BI developers and data analysts generate DAX expressions from natural-language business requirements. Powered by Google's Gemini API, the application uses a predefined Power BI model schema to generate context-aware DAX code.

🚀 **Live Application:** [Try AI DAX Generator](https://r6gzcmgqtru79ndvjzj4hg.streamlit.app/)

📂 **GitHub Repository:** [View Source Code](https://github.com/ay3944013-glitch/AI-DAX-GENERATOR-)

---

## 📌 Project Overview

Writing complex DAX expressions in Power BI can be time-consuming, especially when working with multiple tables, columns, relationships, and filter contexts.

The **AI DAX Generator** simplifies this process by allowing users to describe their business requirements in plain English and receive ready-to-use DAX expressions.

The application uses a predefined Power BI model schema to guide the AI in generating expressions based on the available model objects.

It is designed to help data analysts and Power BI developers save time, improve productivity, and simplify DAX development.

## ✨ Key Features

* **AI-Powered DAX Generation:** Generate DAX expressions from natural-language business requirements.
* **Multiple DAX Objects:** Create measures, calculated columns, and calculated tables.
* **Schema-Aware Generation:** Use a predefined Power BI model schema to guide the generated expressions.
* **Custom Object Naming:** Provide a name for the measure or other DAX object.
* **Expected Result or Test Case:** Optionally describe the expected output to provide additional context.
* **DAX Explanation:** Understand the logic behind the generated expression.
* **Assumptions:** Review assumptions made during generation.
* **Validation Guidance:** Receive suggestions for verifying the expression in Power BI.
* **Download DAX:** Download generated expressions as a text file.
* **Interactive Interface:** Use a simple, browser-based application built with Streamlit.

## 🌐 Live Demo

Try the application without setting up the project locally.

### 👉 [Launch AI DAX Generator](https://r6gzcmgqtru79ndvjzj4hg.streamlit.app/)

### How to Use

1. Open the live application.
2. Review the available Power BI model schema.
3. Select the DAX object you want to create:

   * Measure
   * Calculated Column
   * Calculated Table
4. Enter a name for the DAX object.
5. Describe your business requirement in plain English.
6. Optionally provide an expected result or test case.
7. Click **Generate DAX**.
8. Review the generated expression and its explanation.
9. Download the DAX expression and test it in Power BI.

## 🛠️ Technology Stack

| Technology                | Purpose                                          |
| ------------------------- | ------------------------------------------------ |
| Python                    | Core programming language                        |
| Streamlit                 | Interactive web application interface            |
| Google Gemini API         | AI-powered DAX generation                        |
| Google Gen AI SDK         | Communication with the Gemini API                |
| python-dotenv             | Loading environment variables from a `.env` file |
| Power BI                  | Platform for using and validating generated DAX  |
| Git and GitHub            | Version control and source code management       |
| Streamlit Community Cloud | Application deployment                           |

## ⚙️ Installation and Setup

Follow these steps to run the project locally.

### Prerequisites

* Python 3.10 or a compatible version for the installed dependencies.
* Git.
* A Google Gemini API key.
* A predefined Power BI model schema.

### Step 1: Clone the Repository

```bash
git clone https://github.com/ay3944013-glitch/AI-DAX-GENERATOR-.git
```

Navigate to the project directory:

```bash
cd AI-DAX-GENERATOR-
```

### Step 2: Create a Virtual Environment

```bash
python -m venv venv
```

Activate the environment.

**Windows:**

```bash
venv\Scripts\activate
```

**macOS/Linux:**

```bash
source venv/bin/activate
```

### Step 3: Install Dependencies

```bash
pip install -r requirements.txt
```

### Step 4: Configure the Gemini API Key

Create a file named `.env` in the project root directory.

Add your Gemini API key:

```env
GEMINI_API_KEY=your_gemini_api_key
```

Optionally, specify the Gemini model using the `GEMINI_MODEL` environment variable if needed.

Obtain your API key through [Google AI Studio](https://aistudio.google.com/).

**Security Note:** Never commit your `.env` file or expose your API key in a public repository.

### Step 5: Verify the Power BI Schema

Ensure that `powerbi_schema.txt` exists in the project root and contains the relevant Power BI model information.

The application uses this file to guide DAX generation.

### Step 6: Run the Application

Start the Streamlit application:

```bash
streamlit run app.py
```

Open the local URL displayed in your terminal to access the application.

## 🧠 How It Works

The application follows a straightforward AI-assisted workflow:

1. **User Input:** The user selects a DAX object type and describes a business requirement.
2. **Schema Context:** The application loads the predefined Power BI model schema.
3. **Prompt Construction:** The business requirement and schema are combined with instructions for generating DAX.
4. **AI Processing:** The Gemini API generates the DAX expression and supporting explanation.
5. **Output Extraction:** The application extracts the DAX expression from the AI response.
6. **Results:** The generated expression is displayed with explanatory and validation information.
7. **Download:** The user can download the DAX expression as a text file.

### Workflow

```text
Business Requirement
        |
        v
Streamlit Application
        |
        v
Power BI Model Schema
        |
        v
Prompt Construction
        |
        v
Google Gemini API
        |
        v
Generated DAX Expression
        |
        v
Explanation and Validation Guidance
        |
        v
Download and Use in Power BI
```

## 📂 Project Structure

```text
AI-DAX-GENERATOR-/
│
├── app.py                 # Streamlit application and user interface
├── gemini_service.py      # Gemini API integration
├── geminimodel.py         # Additional model-related module
├── powerbi_schema.txt     # Power BI model schema
├── requirements.txt       # Python dependencies
└── .gitignore             # Git exclusion rules
```

## 💡 Example Use Case

Suppose you have a Power BI sales model containing a sales amount column and an appropriate sales table.

You can enter the following requirement:

**Business Requirement:**

> Create a measure to calculate total sales.

**Example DAX Expression:**

```dax
Total Sales =
SUM ( Sales[SalesAmount] )
```

*Note: This is an illustrative example. The actual table and column names must match your Power BI model schema.*

The application can generate a corresponding expression based on the supplied schema and provide an explanation of its logic.

## 🎯 Benefits

* Reduces the time required to write DAX manually.
* Helps simplify complex analytical calculations.
* Supports faster Power BI development.
* Makes DAX logic easier to understand through explanations.
* Encourages schema-aware expression generation.
* Provides a convenient way to download and reuse generated expressions.

## ⚠️ Limitations

* Generated DAX depends on the quality of the business requirement and the accuracy of the supplied model schema.
* The application uses a predefined schema rather than automatically discovering the user's Power BI model.
* Generated expressions should be tested in Power BI before being used in production reports.
* AI-generated results may require corrections for complex business logic or model-specific requirements.
* A valid Gemini API configuration is required when running the application locally.

## 🔮 Future Improvements

Potential enhancements include:

* Support for uploading Power BI model schemas.
* Improved DAX syntax and reference validation.
* Additional examples and reusable DAX templates.
* Generation history and saved expressions.
* More detailed error handling and troubleshooting.
* Automated testing against sample Power BI models.

## 👨‍💻 Author

**Ankit Yadav**

GitHub: [ay3944013-glitch](https://github.com/ay3944013-glitch)

Project: [AI DAX Generator](https://github.com/ay3944013-glitch/AI-DAX-GENERATOR-)

Live Demo: [Open Application](https://r6gzcmqgtru79ndvjzj4hg.streamlit.app/)

---

⭐ If you find this project useful, consider giving the repository a star!

**Built to simplify DAX development with AI and Power BI.**
