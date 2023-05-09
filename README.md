# Subnetting4

## Obbiettivo:
### Creare il piano di indirizzamento per una rete così composta:
- la rete principale è la 172.130.20.0/24
- si vuole fare subnetting in modo da ottenere 4 sottoreti della stessa dimensione

- 1 router con 4 porte
- 8 PC
- 4 switch
- Ciascuna sottorete ha 1 switch e 2 PC, il router permette la comunicazione tra le 4 sottoreti

## Risoluzione:
### Inizialmente abbiamo assegnato alle 4 porte del router un ip e una subnetmask
### ### ![router config](/subnetting4/sub4_1.png)

### Dopo aver eseguito ciò abbiamo assegnato a ogni dispositivo per entrambe le sottoreti un ip(rispettando il range a disposizione) con un gateway che ci permette di collegarci al router 
### ![config disp](/subnetting4/subn4_2.png)

### Ci rimane quindi da assegnare anche la subnet a ogni dispositivo cosi che possano comunicare anche con le rete, quindi dato che la nostra rete e suddivisa in 4 la nostra subnet sarà 255.255.255.192 e ogni sottorete potra contenere  254/4 dispositivi togliendo però primo e ultimo indirizzo disponibile per rete 
### ![Assegnazione netmask](/subnetting4/sub4_3.png)

### Infine non ci resta che verificare che i dispostivi di una delle 4 sottoreti riescano a comunicare coi dispositivi delle altre sottoreti, quindi effetuiamo un ping e verifichiamo che arrivino i pacchetti
### ![verifica](/subnetting4/sub4_4.png)
### Quindi come possiamo notare i pacchetti sono arrivati e quindi i dispositivi riescono a comunincare 
