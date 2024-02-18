# Curso FullCycle - Desafio Commit Assinado
Projeto com assinatura de commits utilizando GPG.

## Objetivo
Criar um repositório `GIT` no `Github` e fazer um push de um `commit assinado`.

### Pré-Requisito
Ter instalado no seu ambiente:
- gpg - ( [link para instalação](https://gnupg.org/download/) )

## GPG
O GPG (Gnu Privacy Guard) é uma ferramenta de criptografia que pode ser usada para assinar commits no Git. Assinar commits com GPG oferece diversos benefícios, como:

1. Autenticidade: A assinatura garante que o commit foi criado por quem você diz ser, protegendo contra falsificações e atribuições errôneas.
2. Integridade: A assinatura garante que o conteúdo do commit não foi modificado desde que foi assinado, protegendo contra adulterações e corrupção de dados.
3. Não repúdio: A assinatura fornece uma prova irrefutável de que você criou o commit, impedindo que você negue sua autoria posteriormente.
4. Verificação: As assinaturas GPG podem ser facilmente verificadas por qualquer pessoa com a chave pública do signatário, permitindo que outros desenvolvedores validem a origem e a integridade dos commits.

## Como usar o GPG para assinar commits:
1. Gerar uma chave GPG:
    - Utilize o comando `gpg --full-generate-key` para gerar um par de chaves GPG (pública e privada).
    - Escolha um tamanho de chave adequado (geralmente 2048 bits ou mais) e configure uma frase-senha forte para proteger sua chave privada.
2. Informar o Git sobre a chave de assinatura:
    - Execute o comando `git config --global commit.gpgsign true` para configurar o Git para assinar todos os commits por padrão com GPG.
    - Se você tiver várias chaves GPG, especifique a chave que deseja usar com o comando `git config --global user.signingkey <ID da chave>`.
3. Assinar commits:
    - Ao fazer um commit, o Git solicitará sua frase-senha GPG para assinar o commit.
    - O commit assinado terá um status "verificado" no GitHub e em outros serviços que suportam verificação de assinatura GPG.

## Recursos adicionais:
- Documentação do GitHub sobre assinatura de commits: https://docs.github.com/pt/authentication/managing-commit-signature-verification/signing-commits