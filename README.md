# 📌 Document Streaming Project

## 📝 Project Overview
This project is a **real-time document streaming pipeline** that processes structured data from CSV files, transforms it into JSON, and streams it through a series of technologies, including **FastAPI, Kafka, Apache Spark, MongoDB, and Streamlit**. The objective is to facilitate real-time data ingestion, processing, storage, and visualization for business insights.

## 📷 Architecture Diagram
![Architecture Diagram](docs/architecture_diagram-.png)

## ⚙️ Services & Technologies Used
- **FastAPI** – Acts as an ingestion API to receive and process incoming JSON data.
- **Kafka** – Message broker to buffer and stream real-time data.
- **Apache Spark** – Consumes messages from Kafka, processes them, and writes to MongoDB.
- **MongoDB** – Stores the processed data for querying and visualization.
- **Streamlit** – Provides a UI dashboard to visualize customer invoices.
- **Docker & Docker Compose** – Containerizes the entire application for easy deployment.

## 🔄 Project Execution Flow
1. **Data Ingestion**: A CSV file is converted into JSON and sent via a Python client to FastAPI.
2. **Message Streaming**: FastAPI pushes the data to a Kafka topic.
3. **Processing with Spark**: Spark listens to Kafka, processes the streamed data, and writes it to MongoDB.
4. **Data Storage**: MongoDB stores the transformed data for retrieval.
5. **Visualization**: A Streamlit app fetches and displays customer invoices with date-based filters.

## 🚀 Deployment & Future Enhancements
- 🛠 **Deploy the Streamlit app as a Docker container** (Dockerfile setup).
- ☁️ **Deploy the entire platform to a cloud provider** (AWS, Azure, or GCP).
- 🔗 **Create an API between Streamlit and MongoDB** to enhance security by avoiding direct database connections.

## ⚡ Challenges Faced
- Ensuring **real-time data consistency** between Kafka and MongoDB.
- Handling **schema evolution** in streamed messages.
- Optimizing **performance** in a local Docker environment.

## 📚 References & Helpful Links
- [Deploying Streamlit with Docker](https://maelfabien.github.io/project/Streamlit/#the-application)
- [Deploying a Streamlit App on AWS](https://towardsdatascience.com/how-to-deploy-a-semantic-search-engine-with-streamlit-and-docker-on-aws-elastic-beanstalk-42ddce0422f3)

---
### 📢 How to Contribute
If you'd like to improve this project, feel free to fork the repository, submit pull requests, or open issues. 🚀
