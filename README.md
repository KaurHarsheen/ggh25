# Enterprise Cortex - Intelligent Process Automation (IPA)

## **Overview**
This project implements **Intelligent Process Automation (IPA)** for enterprise workflows, focusing on automating **document processing, data extraction, and workflow orchestration**. The system utilizes **OCR, document classification, and entity extraction** to process and route documents efficiently.

## **Prerequisites**
Before running the project, ensure you have the following installed:

- **Elixir** (>= 1.14)
- **Phoenix Framework** (>= 1.7)
- **PostgreSQL** (>= 13)

## **Setup Instructions**

### **Step 1: Clone the Repository**
```sh
git clone https://github.com/KaurHarsheen/ggh25.git
cd ggh25/EnterpriseCortex/document_processor
```

### **Step 2: Install Dependencies**
```sh
mix deps.get
```

### **Step 3: Configure the Database**
Modify `config/dev.exs` with your database credentials, then run:
```sh
mix ecto.create
mix ecto.migrate
```

### **Step 5: Run the Application**
```sh
mix phx.server
```
The application should now be available at `http://localhost:4000`.

### **Step 6: Running Tests**
To ensure everything works correctly, run:
```sh
mix test
```

## **Usage**
### **Uploading Documents**
You can upload documents via API:
```sh
curl -X POST "http://localhost:4000/api/documents" \
     -F "file=@path/to/document.pdf"
```

### **Viewing Processed Documents**
Once processed, documents can be accessed at:
```sh
GET http://localhost:4000/api/documents/:id
```
