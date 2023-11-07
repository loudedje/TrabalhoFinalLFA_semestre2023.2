
# Gerador de AFD a partir de Relação de Tokens e Gramáticas Regulares

Este repositório contém uma aplicação para construção de um Autômato Finito Determinístico (AFD) livre de estados inalcançáveis e mortos a partir de uma relação de tokens e Gramáticas Regulares (GRs) de uma linguagem. O objetivo é gerar o AFD correspondente a partir de um arquivo fonte que contém as informações sobre os tokens e GRs da linguagem.

## Objetivo

O objetivo principal deste projeto é criar uma aplicação que seja capaz de gerar um AFD a partir de tokens e GRs fornecidos como entrada, sem a necessidade de aplicação de classes de equivalência entre estados. O AFD gerado deve ser determinístico e mínimo.

## Entrada

A entrada para a aplicação é um arquivo de texto que contém a relação de tokens e/ou GRs da linguagem. Os tokens representam palavras reservadas, operadores, símbolos especiais, ou qualquer outro elemento reconhecível na linguagem. As GRs são definidas usando a notação BNF (Backus-Naur Form).

## Saída

A saída da aplicação é um AFD que representa a linguagem definida pelos tokens e GRs. Este AFD é gerado a partir do arquivo de entrada e passa por dois principais processos:

1. Determinização: O AFD inicialmente gerado a partir do arquivo de entrada pode ser não determinístico. Portanto, é aplicado o teorema de determinização para torná-lo determinístico.

2. Minimização: O AFD determinístico é submetido ao processo de minimização. No entanto, a minimização é realizada sem a aplicação de classes de equivalência entre estados.

Após a minimização, um último estado final é adicionado ao AFD para representar um "estado de erro". Todas as células do AFD que não possuem mapeamento devem ser preenchidas com o estado de erro, e todas as transições a partir do estado de erro permanecem no estado de erro.
