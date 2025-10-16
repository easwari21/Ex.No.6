# Ex.No.6 Development of Python Code Compatible with Multiple AI Tools

# Date:
# Register no.
# Aim: Write and implement Python code that integrates with multiple AI tools to automate the task of interacting with APIs, comparing outputs, and generating actionable insights with Multiple AI Tools

#AI Tools Required:

# Explanation:
Experiment the persona pattern as a programmer for any specific applications related with your interesting area. 
Generate the outoput using more than one AI tool and based on the code generation analyse and discussing that. 

## AI Tools Required
- ChatGPT (GPT-5 or GPT-4) – for generating and explaining Python code  
- Google Gemini / Bard – for alternate logic and optimization suggestions  
- GitHub Copilot – for debugging and auto-completing code snippets  
- Replit / Jupyter Notebook – for executing and testing AI-generated code  
- Postman / RapidAPI – to explore and test API endpoints and responses  

## Explanation
In this experiment, we explore how AI tools can assist in creating, refining, and verifying Python programs that work with multiple APIs.  
We focus on currency conversion — comparing exchange rate data from two different APIs and analyzing their consistency.

## Title
Framing Prompts for AI-Assisted Project Coding

## Objective
To learn how to design structured prompts for AI tools to generate Python programs that can:
1. Connect with multiple APIs  
2. Compare and analyze API data  
3. Generate insights or next steps automatically  

---

## Stage 1: Generate Python Code for Interacting with Multiple APIs
**Prompt:**  
Write a Python program that connects to two currency APIs — ExchangeRate API and Frankfurter API. Fetch the USD to INR exchange rate from both APIs and print the results.

### OUTPUT
```
import requests

def get_exchangerate_api():
    url = "https://api.exchangerate-api.com/v4/latest/USD"
    data = requests.get(url).json()
    return data["rates"]["INR"]

def get_frankfurter_api():
    url = "https://api.frankfurter.app/latest?from=USD&to=INR"
    data = requests.get(url).json()
    return data["rates"]["INR"]

rate1 = get_exchangerate_api()
rate2 = get_frankfurter_api()

print(f"ExchangeRate API - 1 USD = {rate1} INR")
print(f"Frankfurter API - 1 USD = {rate2} INR")
```
## AI Explanation:
The AI generated a code snippet that uses the requests library to fetch live exchange rates from two APIs.

## Stage 2: Compare Outputs from Different APIs

**Prompt:**
Modify the previous program to calculate and display the difference between the two API results.

# OUTPUT
```
diff = abs(rate1 - rate2)
print(f"Difference in exchange rate: {diff:.4f}")

if diff > 0.20:
    print("Significant difference detected between APIs.")
else:
    print("Both APIs show similar exchange rates.")
```
# AI Explanation:
The AI modified the previous code to include comparison logic and added a threshold value to detect noticeable differences.

## Stage 3: Suggest Insights or Next Steps

**Prompt:**
Extend the program to compute an average exchange rate and suggest which API might be more reliable based on consistency.

# OUTPUT
```
average_rate = (rate1 + rate2) / 2
print(f"Average Exchange Rate: 1 USD = {average_rate:.4f} INR")

if diff > 0.20:
    print("Frankfurter API may be more up-to-date; verify ExchangeRate data.")
else:
    print("Both APIs are consistent. Average rate can be used safely.")
```
# AI Explanation:
The AI added code to calculate the average rate and print logical insights based on the difference between APIs.

## Result:
The Python code for interacting with multiple APIs was generated, executed, and analyzed successfully using multiple AI tools.

# Result: The corresponding Prompt is executed successfully.
