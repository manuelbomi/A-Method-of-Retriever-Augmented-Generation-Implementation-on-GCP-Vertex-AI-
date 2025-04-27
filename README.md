# A-Method-of-Retriever-Augmented-Generation-Implementation-on-GCP-Vertex-AI-
### **OVERVIEW**
In this discourse, we briefly discuss RAG and grounding methods of reducing hallucination in LLM and generative AI applications. We motivate the discussion by showing a complete example on GCP Vertex AI using publicly available Hertz Global Holdings, Inc data  

Vertex AI Studio is a Google Cloud console tool for rapidly prototyping and testing generative AI 
models.

Vertex AI Search lets you create a custom search engine over your own data, including websites, 
Documents, documents, cloud storage, Google drive, Databases, videos and 3rd party connectors. 
•	Definition:
Grounding refers to the process of connecting language models (LLMs) to real-world referents, ensuring they understand and generate language in a contextually meaningful way. 
•	Purpose:
Grounding aims to enhance the accuracy, reliability, and relevance of AI-generated responses by grounding them in factual data. 
•	Example:
A customer service chatbot using RAG to provide answers based on a company's user manual would be an example of grounding. 
Key Differences:
•	Scope:
Grounding is a broader concept that encompasses RAG and other techniques, while RAG is a specific method for achieving grounding. 
•	Implementation:
RAG involves a retrieval step and integration with the LLM, while other grounding methods might involve fine-tuning or prompt engineering. 
Data Sources:
RAG relies on readily available external data sources, while some grounding methods might require specialized knowledge bases or data products
In essence:
Grounding is the goal of ensuring AI models are accurate and reliable by connecting them to real-world knowledge, while RAG is a specific technique used to achieve that goal by retrieving and incorporating external information into the generation process

---
[![Icons](https://skillicons.dev/icons?i=c,py,anaconda&theme=dark)](https://skillicons.dev)



---

### **Background Discussion**

To solve the All-Pairs Shortest Path (APSP) problem using Dijkstra's algorithm, one can execute $n$ instances of the Single-Source Shortest Path (SSSP) problem for each of the $n$ source vertices. Both in the sequential and parallel versions, this adaptation of the algorithm mentioned earlier is used to solve the APSP. However, the main difference in executions and performance lies in the utilization of a parallelization strategy adopted by the parallel version.

> [!IMPORTANT]
> In the CUDA code, the source is partitioned in such a way that each thread in the kernel is responsible for processing a specific vertex of the graph, thus calculating the shortest path from this vertex to all others. In other words, it executes Dijkstra's algorithm in its variation for SSSP.


---
1 create Vertex AI project and app. Select search App to create a custom search engine
![Image](https://github.com/user-attachments/assets/01525f1b-79c0-4f6a-8320-f9f177851db5)

---
2 Set billing and press continue and activate the API
![Image](https://github.com/user-attachments/assets/5a19bc8a-3748-4037-bbba-68b6bcf9e81a)

---
**3 select search assistant app  **
![Image](https://github.com/user-attachments/assets/661917e7-bfa6-4b4a-a489-e6d7f12cf6f3)

---
4 Select Enterprise and Advanced LLM Features
![Image](https://github.com/user-attachments/assets/43696f18-046c-486a-b6df-ac3785673ceb)
---
5 Hertz clone internal search engine
![Image](https://github.com/user-attachments/assets/ceac2700-38c5-414e-892c-d25e432393ba)
---
6 Click create data store
![Image](https://github.com/user-attachments/assets/cc4af316-7865-4850-a64f-b613738f8ecc)
---
7 Different types of data stores can be selected
![Image](https://github.com/user-attachments/assets/e3d69b61-0d5d-4a16-89fa-5d90296e3795)
![Image](https://github.com/user-attachments/assets/eb3e912a-4f15-4394-a192-c29618af818c)
![Image](https://github.com/user-attachments/assets/94412c6f-0ba8-40e0-b30e-5b9de0d8b080)
---

8 Open another homepage an dsearch for Google CLoud Storage
![Image](https://github.com/user-attachments/assets/abd45a15-9a88-44ff-84b9-905b1d6a641a)

![Image](https://github.com/user-attachments/assets/d766d1e3-4729-496e-8850-42c0cb05877e)
---
9 create bucket
![Image](https://github.com/user-attachments/assets/c439d767-7a93-4efa-a0ca-551e153e5d5d)
---
10 enforce public access prevention
![Image](https://github.com/user-attachments/assets/c366d1dc-4877-4eae-97e9-936d3d8ef818)
---
11 to transfer data into your folder, click on Upload and select files from your PC
![Image](https://github.com/user-attachments/assets/bffc75d4-ee05-4f02-a6bc-c7ed0b9bef41)

---
11 Transfer data into your folder
![Image](https://github.com/user-attachments/assets/0970b9a0-fa3b-4f47-bf37-2301fade2098)

---
12 select all the files and upload them
![Image](https://github.com/user-attachments/assets/063d1809-34bf-48d5-9ff2-e39b2027eff3)

---
13 select to load unstructured files
![Image](https://github.com/user-attachments/assets/766ff951-26f7-4f08-8bdf-f3ea23cd0810)

---
14 browse for the folder that ypu want to upload
![Image](https://github.com/user-attachments/assets/52c37077-430f-4a7e-bb0b-6589562d25e5)

---
15 give the data store a name and note the ID given to you as you will need it later
![Image](https://github.com/user-attachments/assets/542200a2-dbb8-4990-b30e-a17ed470bb46)
---
16 click create and select the created datastore
![Image](https://github.com/user-attachments/assets/978a427e-c44a-4d0f-9ce3-4cb10d1913e1)
![Image](https://github.com/user-attachments/assets/996aa8dd-5ecc-4e41-a75b-f6e643cd9d8f)
![Image](https://github.com/user-attachments/assets/31917658-6606-4445-9047-970121ddd956)
---
17 The Hertz App is created
![Image](https://github.com/user-attachments/assets/c7eaa2ff-da18-4937-8d1f-8593efb88e22)
---
18 Preview of the App
![Image](https://github.com/user-attachments/assets/33140e00-afc5-46a3-b573-668fbb050300)
---
19 test the app
![Image](https://github.com/user-attachments/assets/eeb681c9-4b30-4a99-b7f8-076405112df1)
---
20 the app suggests how I may ask questions
![Image](https://github.com/user-attachments/assets/cc8a33fa-ccb9-4f6f-92d3-f12a4bdb1177)
---
21 I changed my search query
![Image](https://github.com/user-attachments/assets/48e27588-8112-4363-8ff9-b18ec0ff3677)
---
22 It also listed documnets that I can check further
![Image](https://github.com/user-attachments/assets/0fbd24ab-6cfe-4092-b18d-a165a3387344)
---
23 different answer configuartion types
23 You can click on any of the cited documents and read through it
![Image](https://github.com/user-attachments/assets/7f4e17e2-d5c5-42e8-a0a6-5d46c7d16ff0)
---
24 Search with follow ups - conversational AI
![Image](https://github.com/user-attachments/assets/16e3e14a-0e50-4695-8c20-9bb4860b226d)
---
25 Search wt follo ups
![Image](https://github.com/user-attachments/assets/b097bfa4-3742-4649-b256-195832ebb53f)
---
26 Ask follow up questions
![Image](https://github.com/user-attachments/assets/7f2e06d5-d322-441f-a646-2b82df61251a)
---
27 widget calls  can be used to access the website
![Image](https://github.com/user-attachments/assets/afd24eaa-63b3-44cc-aa8e-07a58217c1de)
---
28 API calls are also possible
![Image](https://github.com/user-attachments/assets/62511c18-ad58-4caa-bd6f-d7277dda1675)
---
29 you can get result with a cloud shell
![Image](https://github.com/user-attachments/assets/46523a4c-ebf8-4e41-8df2-d2612c270656)
---

30 You can obatin metrics about your website through a Looker dashboard
![Image](https://github.com/user-attachments/assets/2c226bfd-a7e1-49b1-b86b-fab91600ffe5)

---
31 comparison of per page and per search visit using Looker dashboard

![Image](https://github.com/user-attachments/assets/a84d12d6-ec86-4c0f-8641-995a6ebbbd53)

---

Copy the following code to your web application
Copy the following snippet into your web page to add a "Search here" link. Users click "Search here" to open the widget. By default, the reCAPTCHA badge is displayed. To hide the reCAPTCHA badge, see reCAPTCHA documentation. 
If you want a different language for the widget UI, edit the hl parameter from the script URL. See Languages 


> [!TIP]
> Here, the projects can be intergrated onto a pre-existing webpage in form of a widget. Fro  the widget, it can be used by a customer or staff in form of the company's intranet. Upon a query, it will access the company's intranet and use _grounding_ to fetch the customer a most relevant response to the user's queries. It will access the in It can also be deployed as an API endpoint. Here, we show the code that may be used to deploy it as a widget in a pre-existing webpage:

> WIDGET FOR INTRANET SEARCH 

```ruby
<!-- Widget JavaScript bundle -->
<script src="https://cloud.google.com/ai/gen-app-builder/client?hl=en_US"></script>

<!-- Search widget element is not visible by default -->
<gen-search-widget
  configId="bb717de3-6b83-4ec7-afaa-c126829b5a8f"
  triggerId="searchWidgetTrigger">
</gen-search-widget>

<!-- Element that opens the widget on click. It does not have to be an input -->
<input placeholder="Search here" id="searchWidgetTrigger" />
```
> [!CAUTION]
> To use as a widget in a pre-existing webpage, permissions must be given from the App's Vertex AI page for the pre-existing webpage to access the App whenever a user input queries to the App's prompt. 

```
> [!NOTE]
> The parallel programs were executed and compiled in a Windows environment using CUDA Toolkit 12.3 utilizing the dedicated NVIDIA GeForce MX250 graphics card for executing the algorithms on the GPU.

```
