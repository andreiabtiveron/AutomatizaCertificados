# Gerador de Certificados em Lote

Este projeto permite gerar certificados em PDF para múltiplos participantes de um workshop/evento, com layout personalizado, uso de fontes customizadas e quebras automáticas de linha, usando Python com as bibliotecas ReportLab e PyPDF2.

## Funcionalidades

- Geração em lote: lê todos os nomes de um arquivo `.txt`, um por linha.  
- Layout configurável: tamanho e posição do nome do participante, workshop em negrito, datas, carga horária.  
- Quebra automática de texto com base na largura util da página — evita que o texto ultrapasse as bordas laterais.  
- Uso de fonte “caligráfica” para o nome do participante (ex: *Great Vibes*) e fonte “Montserrat” para o texto do certificado.  
- Integração de um modelo base de certificado em PDF (`CertificadoModelo.pdf`) sobre o qual o texto é “mesclado”.  
- Salva cada certificado no diretório atual (ou em pasta específica, se configurado).

## Créditos

Este script foi desenvolvido com base no código inicial fornecido por @massarrahelenna (link original: *https://github.com/massarrahelenna/GeradorDeCertificado*).  
A versão atualiza inclui quebra automática de texto, fonte em negrito para o nome do workshop, verificação de existência de fontes, e organização para uso em lote.

## Como usar

1. Clone ou baixe este repositório.  
2. Certifique-se da estrutura de pastas e arquivos:  
   ```text
   /seu-projeto/
   ├── CertificadoModelo.pdf
   ├── n_gerador.py
   ├── nome_participantes.txt   ← um nome por linha
   ├── Great_Vibes/
   │   └── GreatVibes-Regular.ttf
   └── Montserrat/
       ├── Montserrat-VariableFont_wght.ttf
       └── static/
           └── Montserrat-Bold.ttf

3. No terminal, instale dependências:

```bash
pip install reportlab PyPDF2
```


4. Execute o script:

```bash
python3 n_gerador.py
```

Ele vai solicitar:

Arquivo .txt com nomes

Nome do workshop

Data do evento

Data da assinatura

Carga horária


Após a execução, os certificados serão gerados no mesmo diretório do script (ou pasta de saída configurada) com nomes como certificado_Nome_Do_Participante.pdf.
