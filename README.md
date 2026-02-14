LLM Integration

We integrated Google Gemini AI to provide intelligent analysis for employees.

Smart Features

The AI can analyze employee data and provide:
- Tax bracket estimates and take-home pay calculations
- Cost of living analysis for different locations
- Salary comparisons with market rates
- Career development recommendations
- Productivity tips for tasks

API Endpoints

Send custom prompt:
```
POST /api/llm/generate
Body: {"prompt": "your prompt here"}
```

Analyze employee profile:
```
GET /api/llm/employee-analysis/{id}
```

Get tax information:
```
GET /api/llm/tax-info/{id}
```

Get location benefits:
```
GET /api/llm/location-benefits/{id}?location=New York City
```

Compare salary to market:
```
GET /api/llm/salary-comparison/{id}
```

Get productivity tips:
```
GET /api/llm/task-tips/{id}
```

Setup

You need a Google Gemini API key. Get one free at https://makersuite.google.com/app/apikey

Add your API key to application.properties:
```
gemini.api.key=your-key-here
```

How to Use

First create an employee using the regular employee endpoints. Then use the LLM endpoints with that employee's ID to get AI-powered insights about their taxes, location benefits, or career development.

Test all endpoints at http://localhost:8080/swagger-ui.html