# Processamento Digital de Imagens

## 1. Exercícios práticos -  Aula 17/09/25
### **Exercício 1 — NumPy básico**
- Crie uma matriz 5x5 com valores aleatórios entre 0 e 100.
- Encontre o maior e menor valor.
- Substitua todos os valores maiores que a média por 255.
---
### **Exercício 2 — Vizinhança e adjacência**
- Crie uma matriz binária 6x6.
- Escolha um pixel e mostre seus vizinhos-4 e vizinhos-8.
- Verifique se dois pixels fazem parte da mesma região.
---
### **Exercício 3 — Operações com imagens**
- Gere duas matrizes aleatórias representando imagens.
- Realize soma, subtração e multiplicação pixel a pixel.
- Visualize os resultados com `matplotlib`.

---
#  Transformada de Intensidade de Imagem

A transformada de intensidade é uma técnica fundamental no processamento digital de imagens. Seu objetivo principal é modificar os níveis de cinza ou intensidade de uma imagem para melhorar sua visualização, destacar informações importantes ou prepará-la para etapas posteriores de análise.

---

##  Conceito Básico

Uma imagem digital pode ser representada como uma função:

```
g(x, y) = T[f(x, y)]
```

- `f(x, y)`: imagem original  
- `T`: transformação de intensidade  
- `g(x, y)`: imagem resultante transformada

A função `T` define como cada valor de intensidade original é **mapeado para um novo valor**.

---

##  Principais Tipos de Transformações

### 1. Transformações Lineares
- **Ajuste de brilho e contraste**  

```
g(x, y) = a * f(x, y) + b
```
- `a` → ganho (contraste)  
- `b` → deslocamento (brilho)

- Normalização: ajusta os valores para um intervalo desejado (ex.: 0–255).

---

### 2. Transformações Logarítmicas

```
g(x, y) = c * log(1 + f(x, y))
```

- Realça detalhes em regiões escuras.  
- Útil em imagens com grande faixa dinâmica.

---

### 3. Transformações de Potência (Gamma)
```
g(x, y) = c * f(x, y)^γ
```

- `γ < 1`: realça tons escuros.  
- `γ > 1`: realça tons claros.  
- Muito usada em **correção gama**.

---

### 4. Transformações em Escada / Segmentadas
- Mapas definidos por trechos (piecewise).  
- Usadas para realçar regiões específicas da intensidade.

---

## Aplicações Práticas

- 🌟 Melhoria de contraste de imagens médicas e astronômicas.  
- 🖼️ Correção de iluminação em fotografias.  
- 🔍 Realce de bordas e detalhes sutis.  
- 📈 Pré-processamento para segmentação e reconhecimento de padrões.

---

##  Observações Importantes

- Transformações de intensidade não alteram a geometria da imagem, apenas seus níveis de brilho/cor.  
- A função de transformação precisa ser monótona para preservar a ordem dos tons.  
- Normalmente aplicadas pixel a pixel.


---
##  Implementação

Na pasta **`Equalização`**, há um notebook **Jupyter** que contém a implementação prática de **transformações de intensidade** e **equalização de histograma** em uma imagem.  
