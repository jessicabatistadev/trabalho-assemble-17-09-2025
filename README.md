; Programa: Soma de dois números digitados
; Autor: Você :)
; Data: hoje

        ORG 0

; Ler o primeiro número
LEIA1:  IN 1        ; espera o usuário apertar Entrar
        AND #1      ; testa se o botão Entrar foi pressionado
        JZ LEIA1    ; se não, continua esperando
        IN 0        ; lê o número digitado nas chaves
        STA NUM1    ; guarda esse número na memória (NUM1)

; Ler o segundo número
LEIA2:  IN 1        ; espera Entrar de novo
        AND #1
        JZ LEIA2
        IN 0        ; lê o segundo número
        ADD NUM1    ; soma com o primeiro
        OUT 0       ; mostra no visor
        HLT         ; para o programa

; Área de memória
        ORG 100
NUM1:   DS 1        ; espaço reservado para guardar o 1º número
        END 0
