# loops-shell
#Além de servir como exercício, este repositório ajuda a entender como fazer loops em shell-scrip
#!/bin/bash
#Tipos de loops
#By Jw = José wesley
#2/12/2017

echo -e "\nBem vindo aos loops For e while"

forcao() { 

for ((i=1 ; i < 20 ; i++)) #aqui eu falei para o interpretador assim: i é igual a um, enquanto i for menor que vinte some ele mais um, com intuito de realizar o "do", portanto ele fará o "do" até que a variável for menor que um.

do #fazer

  echo -e ".\c"

  sleep 1 #dorme por um segundo, para poder fazer outro ponto

 done #feito
 
}

#loop agora com while

whicao() {

while true #foi dito meio que assim:  enquanto for verdade, faça o date, corte a quinta coluna e depois de imprimir isso, durma por um segundo, assim adiante...

do #fazer

data=`date | cut -d\  -f5`

echo -e "$data"

sleep 1 #dorme por um segundo para poder apagar e atualizar o date

clear

done

}

echo  "Escolha:"
 
 menu="
1) Exemplo com for
2) Exemplo com While
3) Sair"

echo "$menu"

read opc
  
case $opc in

1) forcao ;;
2) whicao ;;
3) exit ;;
*) echo "Um numero porra" ;;

esac

echo "Aperte enter para voltar ao menu."

read enter
