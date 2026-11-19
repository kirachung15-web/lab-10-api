# Lab 10: Knowledge check

**Take the screenshot for question 1, and answer question 2 below it, in your own words, in one to three sentences.** Replace the `...` below **Your answer:** with your text.

## 1. From the URL to the function

A classmate calls `${API}books/pg74.txt` and gets an error. To help, you need to know which Lambda function answered the request. In the **AWS Console**, open **API Gateway** → **APIs** → `book-analyzer` → **Resources**, click the `GET` method under `/books/{key}`, and look at its **Integration request**: the setting that tells API Gateway where to pass the request.

Take a screenshot that shows the integration request and the Lambda function it names, and save it as `results/api-gateway.png`.

## 2. Which Lambda function answers the request?

Name the Lambda function from your screenshot. Why did Chalice create this function instead of using `book-analyzer-dev-analyze_new_book` from Lab 07?

**Your answer:**

The Lambda function is book-analyzer-dev. Chalice created this function to handle HTTP API requests separately from the book-analyzer-dev-analyze_new_book function, which processes files uploaded to S3. The API function handles requests to the different routes, while the S3 function analyzes newly uploaded books.
