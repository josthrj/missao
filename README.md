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
