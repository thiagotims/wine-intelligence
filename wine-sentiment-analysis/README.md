
# 🧠 Análise de Sentimentos com BERTimbau em Comentários de Vinho

![Python](https://img.shields.io/badge/Python-3.9%2B-blue.svg)
![PyTorch](https://img.shields.io/badge/PyTorch-1.13+-ee4c2c.svg)
![Transformers](https://img.shields.io/badge/Transformers-HuggingFace-yellow.svg)
![Status](https://img.shields.io/badge/status-concluído-brightgreen)
![Idioma](https://img.shields.io/badge/Idioma-Português-red)

## 🔍 Descrição

Este projeto explora a aplicação de **modelos de linguagem pré-treinados** em português para **classificação de sentimentos**. Utilizando o **BERTimbau**, analisamos comentários sobre vinhos, categorizando-os como **positivos**, **neutros** ou **negativos**. A solução cobre desde a preparação dos dados até a exportação do modelo treinado e previsão em novos textos.

---

## 🛠️ Ficha Técnica

| Item                         | Detalhes                                                                 |
|-----------------------------|--------------------------------------------------------------------------|
| **🎯 Objetivo**             | Classificação de sentimentos em comentários de vinho                     |
| **📚 Modelo**              | `neuralmind/bert-base-portuguese-cased` (BERTimbau)                      |
| **🧪 Frameworks**           | PyTorch, Transformers (HuggingFace), Scikit-learn                        |
| **🧼 Pré-processamento**     | Limpeza textual, tokenização com BERT                                    |
| **📊 Dataset**              | 350 comentários (200 rotulados, 150 não rotulados)                       |
| **📈 Métricas**             | Acurácia, relatório de classificação (Precision, Recall, F1)             |
| **💻 Dispositivo**          | Suporte a GPU e CPU (torch.device)                                       |
| **💾 Saídas**               | Modelo salvo `.pt`, resultados `.csv`                                    |
| **🔎 Sentimentos**         | Negativo (0), Neutro (1), Positivo (2)                                   |

---

## 📦 Instalação

```bash
pip install transformers pandas numpy scikit-learn torch
```

### Versões de pacotes utilizadas (Google Colab)
- 📄 requirements.txt


```bash
pip install -r requirements.txt
```

---

## 🚀 Funcionalidades

- ✅ Geração ou carregamento de dataset com comentários.
- ✅ Pré-processamento textual automatizado.
- ✅ Treinamento e validação de um classificador BERT.
- ✅ Exportação do modelo e resultados.
- ✅ Previsão de sentimento em novos comentários.

---

## 💡 Exemplos de Entrada

```text
"Este vinho tem um sabor maravilhoso, com notas de frutas vermelhas e um final suave."
→ Sentimento: Positivo
```

```text
"Não gostei muito deste vinho, achei o sabor fraco e sem personalidade."
→ Sentimento: Negativo
```

---

## 📁 Arquivos Importantes

- `modelo_bertimbau_sentimento.pt` — Modelo treinado salvo.
- `resultados_sentimento.csv` — Comentários com sentimentos previstos.
- `requirements.txt`   — arquivo contendo os pacotes utilizados nos testes via Google Colab.

---

## 📌 Observações

- O dataset utilizado é parcialmente sintético para fins de demonstração.
- Este projeto pode ser adaptado facilmente para outros domínios de texto em português.

---

## 🧑‍💻 Autor

**[Seu Nome Aqui]**  
[🔗 LinkedIn](https://www.linkedin.com/in/devtim/) • [📂 Portfólio](https://seuportfolio.com) • [📫 Contato](mailto:thiagotimdev@gmail.com)

---

## 📃 Licença

Este projeto está sob a licença [MIT](LICENSE).
