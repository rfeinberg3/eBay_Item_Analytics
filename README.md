# eBay Auto Seller

<div style="text-align: center;">
    <img src="./Images/logo.jpg" alt="logo" height=200/>
</div>

## Project Overview

eBay Auto Seller is a tool designed to generate descriptions for items that users would like to sell or resell on eBay by simply inputing the items name. Leveraging eBay's extensive API support, and ColBERT for Retrieval-Augmented Generation (RAG), this project aims to streamline the listing process by providing high-quality, autogenerated item pricing and descriptions using aggregated data. This not only saves time for sellers but also ensures that listings are detailed, price appropriate, and appealing to potential buyers.

### Key Aspects
- **Retrieval-Augmented Generation (RAG)**: Fast and size efficient document retrieval.
- **Microservice Architecture**: Using Docker-compose to orchestrate containerization.
- **REST APIs**: Scalable and efficient API calls for knowledge base development.

### User Stories
- As an e-commerce user looking to sell used items, I would like to list my item at a reasonable price, as to attract potiental buyers quickly.
- As an AI developer I would like a tool that allows me to easily scrape useful data about items from e-commerece websites.
- As a developer (especially one new to this programs code) I would like to be able to easily integrate this program with another e-commerce API, another RAG model, or a different database service.

## Micro-service Graph
![Project Graph](Images/project_graph.png)

## Why Microservices?

1.	**Scalability**: Microservices architecture allows different parts of the application to scale independently. For example, if the demand for image processing increases, only the image processing microservice needs to be scaled up, without affecting other parts of the application. This ensures efficient resource utilization and cost management.
2.	**Flexibility**: Each microservice can be developed, deployed, and maintained independently. This modular approach means that different teams can work on different microservices simultaneously, leading to faster development cycles and easier integration of new features or updates.
3.	**Resilience**: Microservices improve the resilience of the application. If one microservice fails, it does not bring down the entire system. Other microservices can continue to function, ensuring that the application remains available and operational, which is critical for maintaining user trust and satisfaction.


## Why eBay?

With numerous e-commerce websites available, why choose eBay? While it may not be everyone's favorite e-commerce platform, I believe eBay is the best choice for this application for several important reasons.

1. **Open-Source API Support:** eBay is the most well-known e-commerce website that supports open-source RESTful API calls. Although more popular services like Facebook Marketplace and OfferUp exist, they don’t offer public APIs.

2. **Extensive Developer Support:** eBay has extensive developer support, evident through consistent updates, maintenance, and community engagement events. This robust support ensures a reliable and up-to-date API service.

3. **Vast and High-Quality Data:** eBay provides a vast quantity and quality of data, superior to other e-commerce sites like Etsy or Shopify. High-quality data is crucial for training a model to generate descriptions of everyday items people may wish to resell. Unlike Shopify and Etsy, which cater more to entrepreneurial startups, eBay's data is well-suited for this purpose.

## Why RAG?
1.	**Minimizes Hallucinations**: Retrieval-Augmented Generation (RAG) significantly reduces the problem of hallucinations in generated text. By leveraging a retrieval mechanism to pull in relevant documents or information before generating a response, RAG ensures that the generated descriptions are grounded in actual data. This is crucial for maintaining accuracy and trustworthiness in item descriptions.

2.	**Enhanced Data Communication**: RAG allows models to essentially communicate with data repositories. This means that users can input queries or item images, and the model can fetch the most relevant information from a knowledge base or vector database before generating a coherent and contextually accurate description. This approach enhances the quality and relevance of the generated content.


## Resources
- [eBay Developer Program](https://developer.ebay.com/develop/get-started)
- [Deploying Microservices with Docker](https://www.linode.com/docs/guides/deploying-microservices-with-docker/)
- [2023 Nvidia, "What is Retrieval-Augmented Generation, aka RAG?"](https://blogs.nvidia.com/blog/what-is-retrieval-augmented-generation/)
- [ColBERT on GitHub](https://github.com/stanford-futuredata/ColBERT?tab=readme-ov-file)



