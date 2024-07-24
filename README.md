## This project involves building a question-answering system using hierarchical indexing of textbooks. The system leverages the Retrieval-Augmented Generation (RAG) approach with a pre-trained question-answering model to provide accurate responses to user queries based on the selected textbook.

## Hierarchical Index and Trees
### The hierarchical index is created using the create_hierarchical_index function. This function reads the content of a textbook and structures it into a hierarchical JSON format. The hierarchical structure includes:

**1.Root Node: Represents the entire textbook.**

**2.Chapter Nodes: Each chapter is a child of the root node, containing its content and further divided into sections.**

**3.Section Nodes: Each section within a chapter is a child node of the chapter node.**

## *The hierarchical structure allows for efficient retrieval of content based on the structure of the textbook.*

## How the Hierarchical Index is Created?
**1.Reading the Textbook: The entire content of the textbook is read into a string.**

**2.Splitting Content: The content is split into chapters and sections based on patterns like "Chapter" and section numbering.**

**3.Combining Sections: Sections are combined with their respective content to ensure correct grouping.**

**4.Building the Tree: A nested dictionary structure is created where each chapter contains sections, and each section contains its text.** 

# Example Hierarchical Tree Structure
For a textbook with chapters and sections, the hierarchical tree structure in JSON might look like this:

![gitjson](https://github.com/user-attachments/assets/7f6d03fa-ca88-4df0-bf0d-c9938f8afb30)


# Retrieval-Augmented Generation (RAG)
### *The RAG approach integrates retrieval-based techniques with generative models to enhance the quality of answers. Here's how it works in this project:*

**1️⃣Retrieval: The hierarchical index allows efficient retrieval of relevant content based on the user's query.**

**2️⃣Generation: A pre-trained question-answering model (deepset/roberta-base-squad2) generates answers based on the retrieved context.**

## **Setup Instructions**

**1️⃣Download the Notebook: Download the Colab Notebook.**

**2️⃣Run the Notebook:**

**3️⃣Upload your textbooks to the specified paths.**

### *Execute all cells in the notebook to create hierarchical indices, save them, and set up the Gradio interface.*

## **Interact with Gradio:**

**1️⃣Select a book from the dropdown menu.**

**2️⃣Enter your question in the text box.**

**3️⃣Click "Submit" to get an answer.**

# **Example Questions**
### **Book 1:**

**What is thesis?**

**What is Criteria for Examination?**

### **Book 2:**

**What is the Secret of Healthy Weight Loss?**

**Why the Nutrient-Rich World’s Healthiest Foods Promote Healthy Weight Loss?**

### **Book 3:**

**What is Ecology and environmentalism?**
**Formation and structure of the Earth?**
