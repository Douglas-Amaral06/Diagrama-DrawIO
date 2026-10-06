# Desafio de Arquitetura AWS com EC2, EBS, S3 e Lambda

## Sobre o projeto

Este projeto foi desenvolvido como parte de um laboratório prático de Amazon Web Services (AWS), com foco nos conceitos fundamentais de infraestrutura em nuvem e gerenciamento de recursos.

O objetivo do desafio foi criar uma arquitetura utilizando serviços da AWS, representando visualmente como diferentes componentes podem se comunicar dentro de uma solução em nuvem.

A arquitetura foi construída utilizando o **Draw.io**, com os pacotes de shapes **Amazon 3D** e **Cloud & Enterprise**, buscando deixar o desenho mais organizado, visualmente profissional e próximo de uma arquitetura utilizada em ambientes reais.

---

## Objetivo do laboratório

O laboratório tem como objetivo praticar conceitos relacionados ao gerenciamento de instâncias **Amazon EC2**, utilização de **Amazon EBS**, armazenamento com **Amazon S3** e processamento de eventos utilizando **AWS Lambda**.

Entre os principais conceitos trabalhados estão:

- Criação e utilização de instâncias Amazon EC2;
- Utilização de volumes Amazon EBS;
- Armazenamento de arquivos utilizando Amazon S3;
- Processamento orientado a eventos utilizando AWS Lambda;
- Organização de recursos dentro de uma Amazon VPC;
- Separação entre subnets públicas e privadas;
- Controle de acesso utilizando AWS IAM;
- Monitoramento utilizando Amazon CloudWatch.

---

# Arquitetura proposta

A arquitetura desenvolvida apresenta dois fluxos principais.

## 1. Processamento de arquivos com Amazon S3 e AWS Lambda

O primeiro fluxo utiliza uma arquitetura orientada a eventos.

```text
Usuário
   |
   v
Amazon S3
Bucket de Entrada
   |
   | Evento de criação de arquivo
   v
AWS Lambda
   |
   | Processamento
   v
Amazon S3
Bucket de Saída