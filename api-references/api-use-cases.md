# API use cases

Based on the Dastra API documentation specifications, here's a guide for three common use cases, along with Python examples using AIOHTTP to make the requests:

#### Prerequisites

Make sure you have AIOHTTP installed in your environment:

```sh
pip install aiohttp
```

#### 1. Create an Attachment Linked to a Data Subject Request

**Endpoint**: `/datasubjectattachments`

**Method**: POST

**Description**: This endpoint is used to create an attachment linked to a data subject request.

**Example request**:

```python
import aiohttp
import asyncio

async def create_attachment(workspace_id, api_key, attachment_data):
    url = f"https://api.dastra.eu/v1/ws/{workspace_id}/datasubjectattachments"
    
    headers = {
        "Content-Type": "application/json",
        "X-Api-Key": api_key
    }

    async with aiohttp.ClientSession() as session:
        async with session.post(url, json=attachment_data, headers=headers) as response:
            return await response.json()

# Usage example
workspace_id = "your_workspace_id"
api_key = "your_api_key"
attachment_data = {
    # Fill in with your attachment data
    "dataSubjectRequestId": "request_id",
    "fileName": "example.pdf",
    "fileContent": "base64_encoded_content"
}

response = asyncio.run(create_attachment(workspace_id, api_key, attachment_data))
print(response)
```

#### 2. Send a Message with the Attachment in a Data Subject Request

**Endpoint**: `/datasubjectmessages`

**Method**: POST

**Description**: This endpoint is used to send a message with an attachment in a data subject request.

**Example request**:

```python
import aiohttp
import asyncio

async def send_message_with_attachment(workspace_id, api_key, message_data):
    url = f"https://api.dastra.eu/v1/ws/{workspace_id}/datasubjectmessages"
    
    headers = {
        "Content-Type": "application/json",
        "X-Api-Key": api_key
    }

    async with aiohttp.ClientSession() as session:
        async with session.post(url, json=message_data, headers=headers) as response:
            return await response.json()

# Usage example
workspace_id = "your_workspace_id"
api_key = "your_api_key"
message_data = {
    # Fill in with your message data
    "requestId": "request_id",
    "subject": "Message subject",
    "body": "Message content",
    "attachmentId": "attachment_id"  # ID of the previously created attachment
}

response = asyncio.run(send_message_with_attachment(workspace_id, api_key, message_data))
print(response)
```

#### 3. Retrieve New Requests According to Filters

**Endpoint**: `/DataSubjectRequests`

**Method**: GET

**Description**: This endpoint is used to retrieve new data subject rights requests based on specified filters.

**Example request**:

```
import aiohttp
import asyncio

async def get_new_requests(workspace_id, api_key, filters):
    url = f"https://api.dastra.eu/v1/ws/{workspace_id}/DataSubjectRequests"
    
    headers = {
        "Content-Type": "application/json",
        "X-Api-Key": api_key
    }

    params = {
        "filters": filters  # Filters must be a JSON string
    }

    async with aiohttp.ClientSession() as session:
        async with session.get(url, headers=headers, params=params) as response:
            return await response.json()

# Usage example
workspace_id = "your_workspace_id"
api_key = "your_api_key"
filters = '{"field":"status","operator":"equal","value":"new"}'  # Filter example

response = asyncio.run(get_new_requests(workspace_id, api_key, filters))
print(response)
```

#### Conclusion

This guide provides a step-by-step approach to interacting with the Dastra API using Python and AIOHTTP. Replace placeholders like `workspace_id`, `api_key`, and the request data with your actual data.

Feel free to adjust the filtering criteria and request payloads to suit your needs.
