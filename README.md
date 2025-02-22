# HomeMatch AI: Your Intelligent Real Estate Assistant 🏠

[![Python 3.8+](https://img.shields.io/badge/python-3.8+-blue.svg)](https://www.python.org/downloads/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

HomeMatch AI is a cutting-edge real estate recommendation system that leverages advanced Natural Language Processing (NLP) and the power of GPT-3.5 to create personalized property matches. By combining semantic search capabilities with intelligent property analysis, HomeMatch AI transforms the way people find their dream homes.

## 🌟 Key Features

### Intelligent Property Matching
- **Natural Language Understanding**: Simply describe your dream home in plain English
- **Semantic Search Engine**: Powered by ChromaDB for intelligent property matching
- **Personalized Recommendations**: Tailored suggestions based on your unique preferences
- **Dynamic Property Descriptions**: AI-generated, engaging property descriptions that highlight relevant features

### Advanced Technology Stack
- **LangChain Integration**: Seamless combination of language models and document retrieval
- **Vector Database**: ChromaDB for efficient similarity search and property matching
- **GPT-3.5 Language Model**: State-of-the-art natural language processing
- **Interactive UI**: Built with Gradio for a user-friendly experience

### Data Management
- **Synthetic Dataset Generation**: Custom-built dataset using LLM technology
- **Structured Property Information**: Comprehensive property details including:
  - Property specifications (size, bedrooms, bathrooms)
  - Neighborhood information
  - Price points
  - Property descriptions
  - Image URLs

## 🚀 Getting Started

### Prerequisites
- Python 3.8 or higher
- OpenAI API key

### Installation

1. Clone the repository:
```bash
git clone https://github.com/amirhnazerii/Real-Estate-AI-Agent.git
cd Real-Estate-AI-Agent
```

2. Install dependencies:
```bash
pip install -r requirements.txt
```

3. Configure your OpenAI API key:
```python
export OPENAI_API_KEY='your-api-key-here'
# or
os.environ['OPENAI_API_KEY'] = 'your-api-key-here'
```

### Running the Application

1. Generate the dataset (optional):
```bash
jupyter notebook generate_dataset.ipynb
```

2. Launch the application:
```bash
jupyter notebook app.ipynb
```

## 📦 Project Structure
```
Real-Estate-AI-Agent/
├── dataset/
│   ├── RealEstateListingsDatasetv2.csv
│   └── RealEstateListingsDatasetv3.json
├── app.ipynb                 # Main application notebook
├── generate_dataset.ipynb    # Dataset generation script
├── requirements.txt          # Project dependencies
└── README.md                # Project documentation
```

## 💻 Technical Details

### Dependencies
```
langchain==0.0.305
openai==0.28.1
pydantic>=1.10.12
pytest>=7.4.0
sentence-transformers>=2.2.0
transformers>=4.31.0
chromadb==0.4.12
jupyter==1.0.0
tiktoken==0.4.0
```

### Data Model
The system uses Pydantic models for structured data handling:
```python
class RealEstateListing(BaseModel):
    home_type: str
    price: int
    bedrooms: int
    bathrooms: float
    house_size: int
    description: str
    neighborhood: str
    neighborhood_description: Optional[str]
```

## 🎯 Example Usage

1. Start the application and access the Gradio interface
2. Enter your preferences in natural language:
   - "I'm looking for a 3-bedroom house with a pool near downtown"
   - "Show me modern apartments with city views under $500,000"
3. View personalized recommendations with property descriptions and images



## App interaction:

![alt text](image.png)

![alt text](image-1.png)



## 🤝 Contributing

Contributions are welcome! Feel free to submit a Pull Request. For major changes, please open an issue first to discuss what you would like to change.

## 📄 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 🙏 Acknowledgments

- OpenAI for providing the GPT-3.5 API
- LangChain for the framework
- Gradio team for the UI components

## 📧 Contact

Amir H Nazeri - [@amirhnazerii](https://github.com/amirhnazerii)

Project Link: [https://github.com/amirhnazerii/Real-Estate-AI-Agent](https://github.com/amirhnazerii/Real-Estate-AI-Agent)