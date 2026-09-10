# Curso

[Develop Extensions with CAP Following the SAP BTP Developer's Guide](https://learning.sap.com/courses/develop-extensions-with-cap-following-the-sap-btp-developer-s-guide/exercise-creating-a-cap-based-service_cc9e93f1-9dda-4f67-9d6b-c6bfefcc0b99)

## Passo 1: Inicializar o projeto

No terminal:

```bash
cds init incident-management-teste-rmt
```

## Passo 2: Criar o modelo do banco de dados

Criar o arquivo:

```text
db/schema.cds
```

## Passo 3: Criar o serviço

Criar o arquivo:

```text
srv/services.cds
```

Após esses passos, o servidor CAP já poderá ser iniciado.

## Passo 4: Preparar arquivos de dados

No terminal:

```bash
cds add data
```

## Passo 5: Preencher os dados

Preencher os arquivos `.csv` dentro do diretório:

```text
db/data/
```
