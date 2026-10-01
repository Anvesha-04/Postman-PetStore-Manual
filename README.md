<p align="center">
  <b>🔎 Manual API Testing Project</b><br>
  <i>Request Design • API Execution • Response Validation • Defect Reporting • Re-testing</i>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Testing-Manual%20API%20Testing-1f6feb?style=for-the-badge" alt="Manual API Testing">
  <img src="https://img.shields.io/badge/Tool-Postman-ff6c37?style=for-the-badge&logo=postman&logoColor=white" alt="Postman">
  <img src="https://img.shields.io/badge/Format-REST%20API-6f42c1?style=for-the-badge" alt="REST API">
  <img src="https://img.shields.io/badge/Practice-Swagger%20Petstore-2ea44f?style=for-the-badge" alt="Swagger Petstore">
  <img src="https://img.shields.io/badge/Status-Learning%20Project-f59e0b?style=for-the-badge" alt="Learning Project">
</p>

> 💡 **Project at a glance:** A hands-on manual API testing project using Postman to build requests, inspect responses, validate API behavior, and document findings. The workflow covers **endpoint review → request setup → execution → response checks → defect notes → re-testing**.

---

## 📌 Project Overview

This project is for practicing manual testing of REST APIs. Requests are sent from Postman, then the response status, headers, body, and behavior are checked against the API contract.

The primary practice API is **Swagger Petstore**. The repository also includes a small FreeAPI Postman collection for registration and public-data requests.

## 🎯 Objectives

- Understand HTTP methods, URLs, path parameters, query parameters, headers, and JSON request bodies.
- Check success and error responses, status codes, response structure, and data types.
- Practice API authentication concepts and reusable request data.
- Record defects clearly and re-test fixes.
- Learn how an OpenAPI specification describes endpoints and data models.

## 🧰 Tools and APIs

| Tool / API | Purpose |
|---|---|
| [Postman](https://www.postman.com/) | Create and send API requests manually; inspect responses. |
| [Swagger Petstore](https://petstore.swagger.io/) | Practice pet and store API operations. The API base URL is `https://petstore.swagger.io/v2`. |
| [FreeAPI](https://freeapi.app/) | Practice registration and public API requests from the included collection. |
| OpenAPI 3 | Describe Petstore endpoints, request/response schemas, and authentication. |

## 📁 Project Files

| File | Description |
|---|---|
| [`petstore-api-openapi.json`](petstore-api-openapi.json) | Petstore API description in JSON format. |
| [`petstore-api-openapi.yaml`](petstore-api-openapi.yaml) | The same Petstore API description in YAML format. |
| [`Postman-API-Testing.postman_collection.json`](Postman-API-Testing.postman_collection.json) | Postman collection with Auth and Public FreeAPI requests. |

## 🧪 Petstore Scenarios to Practice

| Feature | Method and endpoint | Example check |
|---|---|---|
| Add a pet | `POST /pet` | Send a valid pet JSON body; check the response and returned pet data. |
| Update a pet | `PUT /pet` | Update an existing pet and verify the returned values. |
| Find pets by status | `GET /pet/findByStatus` | Pass `status=available`; check that the response is a list of pets. |
| Find a pet | `GET /pet/{petId}` | Use a valid ID and check the pet fields; try an invalid ID as a negative case. |
| Delete a pet | `DELETE /pet/{petId}` | Delete a test pet and inspect the status and response. |
| Check inventory | `GET /store/inventory` | Check that the response contains status-to-count values. |
| Place an order | `POST /store/order` | Submit an order body and verify the returned order. |
| Find or delete an order | `GET` or `DELETE /store/order/{orderId}` | Use a valid order ID; also check invalid and missing IDs. |

> ⚠️ Swagger Petstore is a shared sample API. Use test data only; requests that add, update, or delete pets and orders modify server data.

## 🚀 Getting Started in Postman

1. Download or clone this repository.
2. Open Postman and select **Import**.
3. To view the included FreeAPI requests, import `Postman-API-Testing.postman_collection.json`.
4. To import the Petstore contract, import `petstore-api-openapi.json` or `petstore-api-openapi.yaml` as an API definition. Alternatively, create requests manually using the scenarios above.
5. Set the base URL to `https://petstore.swagger.io/v2` for Petstore requests.
6. Configure required path values, query parameters, headers, authentication, and JSON bodies before sending each request.
7. Compare the response with the expected behavior and record any failures.

## ✅ Manual Test Workflow

1. **Review** the endpoint and its expected behavior in the OpenAPI file.
2. **Design** positive, negative, and boundary test cases.
3. **Prepare** the method, URL, parameters, headers, authentication, and body in Postman.
4. **Execute** the request and capture the response status, headers, and body.
5. **Validate** required fields, data types, values, and error handling.
6. **Document** failures with request details, actual result, expected result, and evidence.
7. **Re-test** fixes and run related regression checks.

## 🐞 Defect Report Template

When an API response does not match the expected behavior, record:

- **Title:** Short description of the issue
- **Endpoint:** HTTP method and URL
- **Preconditions:** Required IDs, data, or authentication
- **Steps:** Exact request setup and action
- **Expected result:** Expected status and response
- **Actual result:** Received status and response
- **Evidence:** Sanitized request/response details or screenshots
- **Severity / Priority:** Impact and urgency

## 🔐 Safe Testing Notes

- Never commit real passwords, access tokens, API keys, or private user data.
- Use test records and avoid sending sensitive information to public sample APIs.
- Do not treat sample API behavior as a production service guarantee.

## 📚 References

- [Swagger Petstore UI](https://petstore.swagger.io/)
- [Swagger Petstore v2 API definition](https://petstore.swagger.io/v2/swagger.json)
- [FreeAPI](https://freeapi.app/)
- [OpenAPI Specification](https://spec.openapis.org/oas/v3.0.3)

👤 Author  

Anvesha    
Project: Postman-Petstore-Manual    
Role: QA / Manual Testing    
Testing Approach: API Testing
