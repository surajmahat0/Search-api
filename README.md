# Search-api

Overview:

This project is a Proof of Concept (PoC) for the Makersharks platform, enabling buyers to search for manufacturers based on customized requirements. The API is built using Spring Boot and allows users to query suppliers by location, nature of business, and manufacturing processes.

Features:
Search for suppliers based on location, business nature, and manufacturing capabilities.
Pagination support for handling large datasets.
Input validation and basic security features.
RESTful API design.

Technologies Used:
Java: Programming language
Spring Boot: Framework for building the API
MySQL: Database for storing supplier information
Hibernate: ORM framework for database interactions
Maven: Dependency management
Postman: API testing

API Endpoints
1. Query Suppliers
URL: /api/supplier/query

Method: POST

Description: Retrieve a list of suppliers based on location, nature of business, and manufacturing processes.

Request Body:

json:
{
    "location": "Kolkata",
    "natureOfBusiness": "small_scale",
    "process": "3d_printing",
    "page": 0,
    "size": 10
}
Response:

json:
{
    "content": [
        {
            "supplierId": 1,
            "companyName": "ABC Manufacturing",
            "website": "http://www.abcmfg.com",
            "location": "Kolkata",
            "natureOfBusiness": "small_scale",
            "manufacturingProcesses": ["3d_printing"]
        }
    ],
    "pageable": {
        "pageNumber": 0,
        "pageSize": 10,
        "offset": 0,
        "paged": true,
        "unpaged": false
    },
    "totalPages": 1,
    "totalElements": 1,
    "last": true,
    "first": true,
    "numberOfElements": 1,
    "size": 10,
    "number": 0,
    "sort": {
        "sorted": false,
        "unsorted": true,
        "empty": true
    },
    "empty": false
}
