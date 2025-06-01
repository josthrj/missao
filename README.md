# Análise de Sentimentos com spaCy e SpacyTextBlob

Este notebook realiza uma análise de sentimentos em textos usando `spaCy` com a extensão `SpacyTextBlob`.

## Requisitos

Instalação dos seguintes pacotes:

- `pip`, `setuptools`, `wheel` (últimas versões)
- `spaCy`
- `spacytextblob`
- Modelo de linguagem: `en_core_web_sm`

## Fluxo de Trabalho

1. **Instalação das dependências.**
2. **Carregamento do modelo do spaCy.**
3. **Adição do componente `SpacyTextBlob` ao pipeline.**
4. **Análise de textos com extração de:**
   - Polaridade (`polarity`)
   - Subjetividade (`subjectivity`)
   - Avaliações detectadas (`assessments`)

## Correção Aplicada

Foi adicionada uma verificação para evitar erros ao acessar o atributo `polarity`:

```python
if 'spacytextblob' not in nlp.pipe_names:
    nlp.add_pipe('spacytextblob')

---

### 

Este notebook tem como objetivo realizar análise de sentimentos em textos utilizando a biblioteca `spaCy` junto com a extensão `SpacyTextBlob`.

Primeiramente, são instaladas as bibliotecas necessárias e feito o download do modelo de linguagem `en_core_web_sm`. Em seguida, o modelo é carregado e o componente `spacytextblob` é adicionado ao pipeline de processamento de texto. Foi incluída uma verificação para garantir que o componente esteja registrado corretamente antes de utilizar atributos como `.polarity`, evitando erros de execução.

O fluxo geral do notebook é:

1. Instalação dos pacotes (`spaCy`, `spacytextblob`);
2. Carregamento do modelo de linguagem;
3. Integração do componente de análise de sentimentos;
4. Processamento de textos com extração de polaridade, subjetividade e avaliações/opiniões embutidas.

Essa análise permite entender o tom emocional dos textos e pode ser aplicada em contextos como:

- Avaliação de produtos ou serviços;
- Monitoramento de redes sociais;
- Classificação de textos com base no sentimento (positivo, negativo, neutro).

---


