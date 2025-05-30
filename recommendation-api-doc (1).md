# Book Recommendations API Documentation

Base URL: https://recommendationservice-3oal.onrender.com


## Endpoints

### 1. Get All Recommendations
- **Method:** GET
- **Endpoint:** https://recommendationservice-3oal.onrender.com/api/v1/bookrecommendations
- **Description:** Retrieves all book recommendations
- **Response:** List of recommendations

 {
        "recommendationId": 1,
        "productId": 10,
        "bookAuthor": "Ngozi Adichie",
        "rate": 5,
        "content": "I am a huge fan of the author"
    },
    {
        "recommendationId": 2,
        "productId": 11,
        "bookAuthor": "Chimamanda",
        "rate": 5,
        "content": "I am a huge fan of the author"
    },

### 2. Get Recommendations by Product ID
- **Method:** GET
- **Endpoint:** `https://recommendationservice-3oal.onrender.com/api/v1/bookrecommendations/{productId}`
- **Parameters:**
  - `productId`
- **Description:** Retrieves all recommendations for a specific product
- **Response:** List of recommendations for the specified product
[
    {
        "recommendationId": 5,
        "productId": 10,
        "bookAuthor": "Jane Austen",
        "rate": 5,
        "content": "I am a huge fan of the author"
    },
    {
        "recommendationId": 6,
        "productId": 10,
        "bookAuthor": "Jane Austen",
        "rate": 3,
        "content": "The writer was so meticulous"
    }
]
### 3. Add New Recommendation
- **Method:** POST
- **Endpoint:** `https://recommendationservice-3oal.onrender.com/api/v1/bookrecommendation`
- **Description:** Creates a new recommendation
- **Request Body:** - JSON
- **Response:** Returns the created recommendation object

### 4. Update Recommendation
- **Method:** PUT
- **Endpoint:** `https://recommendationservice-3oal.onrender.com/api/v1/bookrecommendation/{recommendationid}`
- **Parameters:**
  - `id` (path parameter, long): The unique identifier of the recommendation
- **Description:** Updates an existing recommendation
- **Request Body:**
- **Response:** Returns the updated recommendation object

### 5. Delete Recommendation
- **Method:** DELETE
- **Endpoint:** `/{productId}`
- **Parameters:**
  - `productId` (path parameter, integer): The product ID of the recommendation to delete
- **Description:** Deletes a recommendation by product ID
- **Response:** Returns the deleted recommendation object



## Notes
1. All endpoints are prefixed with `/api/v1/bookrecommendations`
2. The service accepts and returns JSON data
3. Make sure to include appropriate headers:
   - `Content-Type: application/json`
4. CORS is enabled only for https://recommendationservice-3oal.onrender.com 