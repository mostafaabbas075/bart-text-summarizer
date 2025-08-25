
# Abstractive Text Summarizer (BART)

This project is a **web-based abstractive text summarizer** powered by the `facebook/bart-large-cnn` model from Hugging Face Transformers. It allows users to input text and get a concise, coherent summary using a pre-trained BART model. The interface is built with **Streamlit**, and the app can be exposed publicly using **Ngrok**.

---

## Features

- **Abstractive summarization**: Generates human-like summaries rather than just extracting sentences.
- **Clean input processing**: Removes unnecessary whitespace and special characters for better results.
- **Configurable summarization**: Adjust maximum input and summary lengths, beam size, and other generation parameters.
- **Web interface**: Easy-to-use text area input with a “Generate Summary” button.
- **Device-aware**: Automatically uses GPU if available, otherwise CPU.

---

## Requirements

- Python 3.10+
- Packages:  
  ```bash
  pip install transformers streamlit
  npm install -g localtunnel
  ```
- GPU recommended for faster summarization (optional).
- Ngrok account (optional, only if you want public URL access).

---

## Usage

1. **Clone the repository**  
```bash
git clone https://github.com/YOUR_USERNAME/YOUR_REPO.git
cd YOUR_REPO
```

2. **Set up Ngrok token (optional)**  
Open `app.py` and set your Ngrok authtoken:  
```python
NGROK_AUTHTOKEN = "YOUR_NGROK_AUTHTOKEN_HERE"
```

3. **Run the Streamlit app**  
```bash
streamlit run app.py
```

4. **Access the app**  
- Locally: `http://localhost:8501`  
- Publicly (via Ngrok): URL will be printed in the console.

5. **Enter your text** in the text area and click **Generate Summary**. The summary will appear below.

---

## Notes

- Ensure your input text is meaningful and not too short for best summarization results.
- Ngrok token is **sensitive**. Do not commit your personal token to public repositories. Replace it with a placeholder before committing.
- For GPU users, the app will automatically utilize CUDA if available. Otherwise, CPU will be used.

---

## Example

**Input:**  
```
Rising global temperatures contribute to melting ice caps, rising sea levels, and more frequent extreme weather events. Wildlife is forced to adapt or face extinction, and crop yields may decline, threatening food security. Addressing climate change requires coordinated global action.
```

**Output:**  
```
Rising global temperatures lead to melting ice caps, higher sea levels, extreme weather events, and threats to wildlife and food security. Global action is needed to address climate change.
```

---

## References

- [Hugging Face BART Model](https://huggingface.co/facebook/bart-large-cnn)
- [Transformers Documentation](https://huggingface.co/docs/transformers)
- [Streamlit Documentation](https://docs.streamlit.io/)

## ✍️ Author  
Mostafa Abbas Saleh  
AI Student | NLP Practitioner

## 🙏 Acknowledgment  
Thanks to **Elevvo** for the valuable internship experience and professional training.


