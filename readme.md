# Curso (Intermediário)

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

# Complementos:

## Importar serviço externo
### Instalar dependências para conectividade
No terminal:
```bash
npm add @sap-cloud-sdk/http-client@3.x @sap-cloud-sdk/util@3.x @sap-cloud-sdk/connectivity@3.x @sap-cloud-sdk/resilience@3.x
```
* Se atentar nas versões das bibliotecas.
### Importação
Pegar o arquivo edmx (metadata) do serviço, importar na raiz do projeto e executar no terminal:
```bash
cds import NOME_ARQUIVO.edmx --as cds
```
Isto moverá o arquivo .edmx para srv/external, criando junto dele o equivalente com extensão .cds.

## Adicionar XSUAA
No terminal:
```bash
cds add xsuaa --for production
```

## Adicionar HanaCloud
No terminal:
```bash
cds add xsuaa --for production
```

Além de adicionar a configuração no package, irá criar o arquivo xs-security.json baseado nas roles/scopes declarados nas annotaions dos CDS Models criados.
### Se houver mudança nas annotations:
No terminal:
```bash
cds compile --to xsuaa
```
Isto atualizará o xs-security.json.

## Adicionar configuração de deploy utilizando Multitarget Application (MTA)
No terminal:
```bash
cds add mta
```