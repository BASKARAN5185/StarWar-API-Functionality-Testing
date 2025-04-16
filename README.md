# StarWar-API-Functionality-Testing

This repository contains **API testing** and **exploration** using the **Star Wars API (SWAPI)**. The purpose of this project is to validate the functionality, accuracy, and performance of the various Star Wars API endpoints, including resources like **planets**, **people**, **films**, and **starships**.

The repository contains examples of making requests using tools like **Postman**, **curl**, and **HTTPie** to validate API responses and ensure that the API is functioning correctly.

---

## 🛠️ Features

- **API Exploration**: Learn how to interact with the Star Wars API by exploring resources like planets, people, films, species, vehicles, and starships.
- **Automated Testing**: Includes test cases for validating API responses such as status codes, response times, and data structure validation.
- **Request Examples**: Usage of **Postman**, **curl**, and **HTTPie** to make API requests and test endpoints.
- **Rate Limiting Awareness**: Acknowledges that the Star Wars API has a rate limit of **10,000 requests per day** to avoid abuse.
- **Search Functionality**: Examples of using the search query parameter to filter and retrieve specific resources (e.g., searching for a specific character or planet).
- **JSON and Wookiee Formats**: Demonstrates how to request responses in both standard **JSON** format and **Wookiee** format for Star Wars enthusiasts.

---

## 🚀 Getting Started

Let's make our first API request to the **Star Wars API (SWAPI)**!

Open up your terminal and use **curl** or **HTTPie** to make an API request for a resource. For example, we can retrieve details for the first planet, **Tatooine**, using the following commands.

### Using HTTPie:
```bash
http https://swapi.dev/api/planets/1/
```

### Using cURL:
```bash
curl https://swapi.dev/api/planets/1/
```

#### Sample Response:
```json
{
    "climate": "Arid",
    "diameter": "10465",
    "gravity": "1 standard",
    "name": "Tatooine",
    "orbital_period": "304",
    "population": "200000",
    "residents": [
        "https://swapi.dev/api/people/1/",
        "https://swapi.dev/api/people/2/"
    ],
    "rotation_period": "23",
    "surface_water": "1",
    "terrain": "Desert",
    "url": "https://swapi.dev/api/planets/1/"
}
```

---

## 🌍 Base URL

The **Base URL** for all SWAPI requests is:

```plaintext
https://swapi.dev/api/
```

Make sure to prepend this base URL to all API endpoints when constructing your requests.

---

## ⚠️ Rate Limiting

The **Star Wars API** has a rate limit to prevent abuse and ensure fair use. The current limit is **10,000 requests per day** per IP address. This should be more than sufficient for most use cases, but keep this in mind when making large numbers of requests.

---

## 🔐 Authentication

SWAPI is an **open API** and does **not require authentication**. You can freely access the data with any valid HTTP GET request. However, you are limited to read-only operations (GET) and cannot modify the data.

---

## 🔎 Searching Resources

Each resource (planets, people, films, etc.) supports a **search** parameter. This allows you to filter the dataset by searching for specific keywords.

For example, to search for people related to "Luke," you can make a request like:

```bash
http https://swapi.dev/api/people/?search=luke
```

This will return a list of people whose names match "Luke" (e.g., Luke Skywalker).

---

## 🧬 JSON Schema

The API supports **JSON Schema** for every resource, which allows you to programmatically inspect the attributes and their types for each resource. You can retrieve the schema for any resource by appending `/schema` to the endpoint.

For example:
```bash
http https://swapi.dev/api/planets/schema
```

---

## 🛸 Wookiee Format

In addition to the default **JSON** format, SWAPI also offers a **Wookiee** format, which translates the response into Wookiee language (for Star Wars fans!). To request Wookiee format, append `?format=wookiee` to the URL.

For example:
```bash
http https://swapi.dev/api/planets/1/?format=wookiee
```

---

## 📚 Available Resources

Here are the main resources provided by the API:

- **Films**: `/films/` - List of Star Wars films.
- **People**: `/people/` - List of characters (e.g., Luke Skywalker, Han Solo).
- **Planets**: `/planets/` - List of planets (e.g., Tatooine, Alderaan).
- **Species**: `/species/` - List of species (e.g., Human, Wookiee).
- **Starships**: `/starships/` - List of starships (e.g., X-wing, Millennium Falcon).
- **Vehicles**: `/vehicles/` - List of vehicles (e.g., Speeder bike, AT-AT).

You can explore the available resources by making requests to the **Root** endpoint:

```bash
http https://swapi.dev/api/
```

This will return a list of all available resources.

---

## 🧑‍💻 API Testing with Postman

This repository includes **Postman collections** for testing various SWAPI endpoints. These collections provide ready-to-use requests for testing different resources and verifying that the API is returning the expected responses.

To get started with Postman:

1. Download and install [Postman](https://www.postman.com/downloads/).
2. Import the provided Postman collection from this repository into Postman.
3. Run the requests to verify the API responses.

---

## 🧑‍🏫 Example Test Cases

Here are a few example test cases that are included in the repository:

- **Test 1**: Verify that the `/people/` endpoint returns a **200 OK** response.
- **Test 2**: Ensure that the `Tatooine` planet exists in the `/planets/` endpoint.
- **Test 3**: Validate that the search functionality works for people with the name "Luke."
- **Test 4**: Check if the API handles invalid endpoints (e.g., `/people/9999/`).

---

## 🤝 Contributing

Contributions to this repository are welcome! If you'd like to add more test cases or improve the existing ones, feel free to submit a pull request. Here's how you can contribute:

1. Fork the repository.
2. Create a new branch for your changes.
3. Make your changes and commit them.
4. Push the changes to your forked repository.
5. Submit a pull request for review.

---
