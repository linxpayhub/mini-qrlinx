
# Desafio Back-end QrLinx

Primeiramente, obrigado pelo seu interesse em trabalhar na Linx! Abaixo, você encontrará todas as informações necessárias para iniciar o seu teste.

## 📝 Avisos antes de começar
- Crie um repositório no seu GitHub sem citar nada relacionado à Linx.
- Faça seus commits no seu repositório.
- Envie o link do seu repositório para o email do recrutador responsável.
- Você poderá consultar o Google, StackOverflow ou algum projeto particular na sua máquina.
- Dê uma olhada nos Materiais úteis ao final.
- Fique à vontade para perguntar qualquer dúvida aos recrutadores.
- Fique tranquilo e respire; estamos ansiosos para ver sua solução!

## 📧 Corpo do Email com o link do repositório do desafio
```
Seu Nome

Nome do recrutador

Link do repositório

Link do Linkedin
```

## 🛠️ Sobre o ambiente da aplicação
Você pode escolher qualquer framework com o qual se sinta confortável, mas destacamos que em nossa empresa utilizamos predominantemente o .NET. Portanto, familiaridade com esse framework será um diferencial. Se optar pelo usou de algum framework, tente evitar o uso excessivo de métodos mágicos ou atalhos pré-construídos. Queremos ver sua habilidade em resolver problemas e a lógica que você aplica.

Valorizamos uma boa estrutura e a utilização de padrões de projeto.

## 📅 Para o dia da entrevista técnica
Na data marcada pelo recrutador, tenha sua aplicação rodando na sua máquina local para execução dos testes e para nos mostrar os pontos desenvolvidos e possíveis questionamentos. Faremos um code review juntos, e você poderá explicar suas decisões de projeto e arquitetura.

## 🎯 Objetivo: Mini QrLinx
Temos 2 tipos de usuários: Administradores e Lojistas.

**Requisitos:**
- Lojistas podem criar cobranças, mas não podem cancelá-las.
- Administradores podem cancelar as cobranças que já foram pagas.
- Deve haver um endpoint para os lojistas verificarem o status de suas cobranças (pagas/canceladas), como não existe um webhook para avisar os lojistas sobre alterações das cobranças, esse é um ponto crítico do nosso Mini QrLinx visto que haverá muitas requests para esse endpoint.

### Integrações externas
- No fluxo de criação de cobrança, deve ser feita uma request POST para [https://eoc56jqea5ysq7e.m.pipedream.net](https://eoc56jqea5ysq7e.m.pipedream.net) passando no body o valor da cobrança:
```json
{
    "value": 10.8
}
```
- No fluxo de cancelamento, deve ser feita uma request para [https://eo45xtt0qoks1ru.m.pipedream.net](https://eo45xtt0qoks1ru.m.pipedream.net) passando o id da transação:
```json
{
    "id": "2Vt9yiDUF2h7vxdSD3qUuzCvKwR"
}
```

## 📋 Avaliação
Apresente sua solução utilizando o framework de sua preferência, justificando sua escolha. Durante a entrevista, discutiremos suas decisões e avaliaremos com base nos seguintes critérios:

- Documentação
- Código limpo e organizado
- Conhecimento de padrões (PSRs, design patterns, SOLID, etc.)
- Modelagem de Dados
- Manutenibilidade do Código
- Tratamento de erros
- Cuidado com itens de segurança
- Arquitetura e estruturação do código

## O que NÃO será avaliado
- Fluxo de cadastro de usuários
- Autenticação

## O que será um Diferencial
- Testes de [integração](https://www.atlassian.com/continuous-delivery/software-testing/types-of-software-testing)
- Testes [unitários](https://www.atlassian.com/continuous-delivery/software-testing/types-of-software-testing)
- Uso de Design Patterns
- Documentação
- Proposta de melhoria na arquitetura

## ⭐ Diferenciais
- Uso do framework .NET
- Testes de integração
- Testes unitários
- Uso de Design Patterns
- Documentação detalhada
- Proposta de melhoria na arquitetura

## 📚 Materiais úteis
- [Documentação do .NET](https://docs.microsoft.com/pt-br/dotnet/)
- [Design Patterns em .NET](https://www.dofactory.com/net/design-patterns)
- [Referências de arquitetura](https://docs.microsoft.com/pt-br/dotnet/architecture/)

Boa sorte e estamos ansiosos para ver sua solução!
