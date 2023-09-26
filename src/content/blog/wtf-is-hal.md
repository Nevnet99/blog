---
title: 'WTF is HAL (Hypertext Application Language)?'
description: 'A quick overview of HAL and how to use it'
pubDate: 'Sep 26 2023'
heroImage: '/codecult-placeholder.png'
---


So you've found yourself making decisions about an API, and are interested in Hypertext Application Language.

So I'm writing this specific blog post to learn as we go along, so come along for the journey. I hope you enjoy it!

### Table of Contents
1. <a href="#background">The Background</a>
2. <a href="#how">How do I use HAL</a>


<b>TL;DR: Hypertext Application Language (HAL)</b> is a convention for defining hypermedia links within JSON or XML code. It simplifies API development by making APIs more discoverable and allowing easy interaction using JSON or XML. HAL uses a special media type (application/hal+json or application/xml+json) to indicate its usage. It facilitates linking resources, such as books and authors, by including _links objects. These links can be used to navigate between resources and perform actions. HAL offers a minimal impact approach and enables the creation of general-purpose libraries for APIs.

You can customize the table of contents based on the headings and sections in your document. Simply replace the example headings and section links with your own.

<h2 id="background">The Background</h2>

Let's start off with Wikipedia's definition of what Hypertext Application Language is:

Hypertext Application Language (HAL) is a convention for defining hypermedia such as links to external resources within JSON or XML code. It is documented in an Internet Draft (a "work in progress"), however, the latest version of HAL Internet-Draft expired on November 12, 2016. The standard was initially proposed in June 2012 specifically for use with JSON[1] and has since become available in two variations, JSON and XML. The two associated MIME types are media type: application/hal+xml and media type: application/hal+json.

HAL was created to be simple to use and easily applicable across different domains by avoiding the need to impose any requirements on how the project be structured. Maintaining this minimal impact approach, HAL has enabled developers to create general-purpose libraries which can be easily incorporated on any API that uses HAL.

APIs that adopt HAL simplify the use of open source libraries and make it possible to interact with the API using JSON or XML. The alternative would be having to develop a proprietary format which in turn forces developers to learn how to use yet another foreign format.

From this point on, Hypertext Application Language will be referred to as HAL.

So, to unpack that and to make it easier to read, here is my interpretation of this:

HAL is used to handle links across your API and make your API more discoverable.
HAL can be used for both internal routes as well as routes external to your application, despite being only mentioned here as external.
HAL has a special media type application/hal+json or application/xml+json. This should be used to let clients of your API know that you are using HAL.

<h2 id="how">How do I use HAL?</h2>

Let's start with an example of a bookstore.

Endpoint: GET /books/{bookId}

Response:

```json
{
  "id": "1",
  "title": "The Hobbit",
  "genre": "Fantasy",
  "author": {
    "id": "1",
    "name": "J.R.R. Tolkien",
    "_links": {
      "self": {
        "href": "/authors/1"
      }
    }
  },
  "_links": {
    "self": {
      "href": "/books/1"
      }
  }
}
```

When you send a GET request to retrieve information about a specific book with the ID 1, the API responds with the book's details, including its title, genre, and the author associated with it. The response follows the HAL format. The book resource includes a link to the author's resource using the _links object, where the self link points to the URL for the author resource.

Endpoint: GET /authors/{authorId}

Response:
```json
{
  "id": "1",
  "name": "J.R.R. Tolkien",
  "books": [
    {
      "id": "1",
      "title": "The Hobbit",
      "_links": {
        "self": {
          "href": "/books/1"
        }
      }
    },
    {
      "id": "2",
      "title": "The Lord of the Rings",
      "_links": {
        "self": {
          "href": "/books/2"
        }
      }
    }


  ],
  "_links": {
    "self": {
      "href": "/authors/1"
    }
  }
}
```

When you send a GET request to retrieve information about a specific author with the ID 1, the API responds with the author's details, including their name and the books they have written. The response follows the HAL format. The author resource includes a list of books, each represented as a separate object with its own _links object. These links point to the URLs for the respective book resources.

_links
The _links key can include a wide array of keys. In the book example, we could add a "next" key to show the next book in the series or even a "prev" to show the previous book in the series.

It's also a great place to link together actions. For example, editing a book would now include:
```json
{
  "id": "1",
  "title": "The Hobbit",
  "_links": {
    "self": {
      "href": "/books/1"
    },
    "next": {
      "href": "/books/2"
    },
    "edit": {
      "href": "/books/2/edit"
    }
  }
}
```
