# Claim Swift REST Server

A simple Swift REST server created to manage Claim entries in a SQLite3 database.

| Property Name | Description                                            | Data Type (Swift) | Data Type (SQLite3) |
|---------------|--------------------------------------------------------|-------------------|---------------------|
| id            | Unique claim id, randomly generated UUID               | UUID              | TEXT                |
| title         | Claim title, brief description about the claim         | String            | TEXT                |
| date          | The date (format "yyyy-MM-dd") when the claim occurred | String            | TEXT                |
| isSolved      | This indicates if the claim is closed                  | Boolean           | INT                 |


| Service Name | Request Method | Request Format | Request Data | Response Format | Response Data |
|-|-|-|-|-|-|
| /ClaimService/add | POST | JSON | Claim object without id and isSolved (encoded string) | Plain Text | Success Message |
| /ClaimService/getAll | GET | N/A | N/A | JSON | List of Claim objects (encoded string) |
