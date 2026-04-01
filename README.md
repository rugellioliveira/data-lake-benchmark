# 📊 Data Lake File Format Benchmark

Projeto de **engenharia de dados** que compara os formatos **CSV, JSONL e Parquet**, analisando:

- ⏱️ Tempo de leitura e escrita  
- 💾 Tamanho dos arquivos  
- ⚙️ Eficiência para cenários de Data Lake  

---

## 🚀 Objetivo

Demonstrar, de forma prática, como diferentes formatos de dados impactam:

- performance de I/O  
- custo de armazenamento  
- eficiência em pipelines de dados  

---

## 📁 Formatos analisados

### 🔹 CSV (Comma-Separated Values)

- Formato **texto simples**
- Amplamente utilizado
- Fácil de abrir (Excel, etc.)

**Vantagens:**
- Simples
- Alta compatibilidade

**Desvantagens:**
- Arquivos grandes
- Leitura lenta
- Não mantém tipos de dados (schema)

**👉 Quando usar:**
- Integrações simples
- Troca de dados entre sistemas
- Pequenos volumes

---

### 🔹 JSONL (JSON Lines)

- Cada linha é um JSON independente  
- Muito usado em **APIs e streaming**

**Vantagens:**
- Flexível
- Ideal para dados semi-estruturados
- Fácil ingestão incremental

**Desvantagens:**
- Verboso (repete chaves)
- Arquivos maiores
- Mais lento para análise

**👉 Quando usar:**
- Logs
- APIs
- Streaming de dados

---

### 🔹 Parquet

- Formato **colunar otimizado**
- Padrão em Big Data (Spark, Data Lakes)

**Vantagens:**
- Alta compressão
- Leitura muito rápida
- Mantém schema
- Leitura seletiva por coluna

**Desvantagens:**
- Menos legível (binário)
- Precisa de ferramentas específicas

**👉 Quando usar:**
- Data Lakes
- Analytics
- Grandes volumes de dados

---

## 🧪 O que o projeto faz

1. Gera um dataset simulado  
2. Salva em CSV, JSONL e Parquet  
3. Mede:
   - tempo de escrita  
   - tempo de leitura  
   - tamanho dos arquivos  

---

## 📊 Resultados

Exemplo de execução do benchmark:

<p align="center">
  <img width="800" src="https://github.com/user-attachments/assets/cab389f5-8afb-4ab8-8935-522d216ea0f6" />
</p>

### 🧾 Resumo

- Parquet apresentou melhor desempenho em leitura
- CSV gerou arquivos maiores
- JSONL foi o mais lento e mais verboso

> Os resultados podem variar conforme máquina e volume de dados

---

## ⚙️ Tecnologias

- Python  
- Pandas  
- PyArrow  

---

## ▶️ Como executar

```bash
pip install pandas pyarrow
```
```bash
python main.py
```

📌 Conclusão (esperada)

Parquet → melhor performance e menor tamanho
CSV → mais simples, porém ineficiente
JSONL → útil para ingestão, não para análise
