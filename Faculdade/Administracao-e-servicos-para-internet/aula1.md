# Endereçamento IP, Máscaras de rede e sub-rede

## Endereçamento IP

O IP (Internet Protocol) permite que os dispositivos/hosts sejam conectadas à Internet.

Formato do IP: X.Y.Z.A
    
> Octeto de Bits EX: 10001011 -> 8bits = 1byte

Quantidade de IP's: 0.0.0.0 até 255.255.255.255

> 00000000.00000000.00000000.00000000 até 11111111.11111111.11111111.11111111

Cerca de 4 bilhões de IP's disponíveis.
	
## Máscara de rede e sub-rede

O endereço da Máscara de rede/sub-rede é dividido em duas partes: Uma para identificação da rede/sub-rede e outra para identificação dos hosts.

* Switch:

<table>
    <tr>
        <td>PC1</td>
        <td>PC2</td>
        <td>...</td>
        <td>...</td>
        <td>...</td>
        <td>...</td>
        <td>...</td>
        <td>...</td>
        <td>...</td>
        <td>...</td>
    </tr>
     <tr>
        <td>...</td>
        <td>...</td>
        <td>...</td>
        <td>...</td>
        <td>...</td>
        <td>...</td>
        <td>...</td>
        <td>...</td>
        <td>...</td>
        <td>PC20</td>
    </tr>
</table>


Ex1: Imagine a máscara -> 255.255.255.0

Neste caso, os 3 primeiros octetos são para rede e o último octeto para identificação dos hosts.

255.255.255.0 = 
11111111.11111111.11111111.00000000
8bits	  8bits	   8bits	8bits
↳ Octeto

Para o endereço de máscara de rede/sub-rede 255.255.255.0:

Nº máximo de hosts: 2⁸
_________________↳ Nº de bits destinados a identificação dos hosts.

Nº máximo de hosts: 256

Endereços que não podem ser usados: 0	e	255
_______________________________↳ Rede	 ↳ Broadcast

Nº total de dispositivos endereçáveis: 254

Ex: Imagine o endereço de rede: 23.43.0.0.
_______________________________↳ 23.43.0.1 até 23.43.0.254

O último IP é destinado ao broadcast. Dessa forma, o IP 23.43.0.255 é o endereço de broadcast da rede 23.43.0.0.

##Classes de Endereços IP

Para permitir uma maior gama de Endereços IPs, as mesmas são divididas em 5 (cinco) diferentes classes:

Classe A → Máscara: 255.0.0.0

Classe B → Máscara: 255.255.0.0

Classe C → Máscara: 255.255.255.0

Classe D → Máscara: Endereços de Multicast.

Classe E → Não são utilizados/definidas para futuras utilizações e testes.

## Classes A

range (Alcance): 1.0.0.0 até 126.0.0.0
máscara de rede: 255.0.0.0
notação CIDR: /8
nº de bites para rede: 8
nº de bites para hosts: 24
Exemplo de rede: 10.0.0.1/8
			 
Classe A →	

<table>
    <tr>
        <td>Rede</td>
        <td>Host</td>
        <td>Host</td>
        <td>Host</td>
    </tr>
</table>

nº de redes: 2⁸ = 256 - 2 = 254
nº de hosts: 2⁸ * 2⁸ * 2⁸ = 16.777.216 hosts

## Classes B

range (Alcance): 128.0.0.0 até 191.255.0.0
máscara de rede: 255.255.0.0
notação CIDR: /16
nº de bites para rede: 16
nº de bites para hosts: 16
Exemplo de rede: 190.168.0.1/16
			 
		    
Classe B →	

<table>
    <tr>
        <td>Rede</td>
        <td>Rede</td>
        <td>Host</td>
        <td>Host</td>
    </tr>
</table>

nº de redes: 2⁸ * 2⁸ = 65536
nº de hosts: 2⁸ * 2⁸ = 65536 hosts

## Classes C

range (Alcance): 192.0.0.0 até 223.255.255.0
máscara de rede: 255.255.255.0
notação CIDR: /24
nº de bites para rede: 24
nº de bites para hosts: 8
Exemplo de rede: 192.168.0.1/16
		    
Classe C →	
			
<table>
    <tr>
        <td>Rede</td>
        <td>Rede</td>
        <td>Rede</td>
        <td>Host</td>
    </tr>
</table>

nº de redes: 2⁸ * 2⁸ * 2⁸ = 16.777.216 - 2 = 16.777.214
nº de hosts: 2⁸ = 256 - 2 = 254

## Endereços Inválidos/Reservados

1. 0.xxx.xxx.xxx

2. 127.xxx.xxx.xxx → Testes Internos e Loopback (127.0.0.1)

3. 10.0.0.0 até 10.255.255.255 / 172.16.0.0 até 172.31.255.255 e 192.168.0.0 até 192.168.255.255 → Redes privadas.

## Como calcular e criar Sub-redes

Para criar uma quantidade (x) de Sub-redes, pega-se emprestado (x) bits da ponte identificadora dos hosts.

Para criar 2 sub-redes: 255.255.255.0 → 255.255.255.10000000
_________________________________________⇓
_________________________________________2¹ = 2 sub-redes
_________________________________________Máscara: 255.255.255.128

Nº de hosts: 2⁷ - 2 → 126 hosts.

Para criar 4 sub-redes: 255.255.255.0 → 255.255.255.11000000
_________________________________________⇓
_________________________________________2² = 4 sub-redes
_________________________________________Máscara: 255.255.255.192

Nº de hosts: 2⁶ - 2 → 62 hosts.

CONCLUSÃO: Quanto mais bits pega-se emprestados da máscara, maior é a quantidade de Sub-redes e menor é a quantidade de hosts endereçáveis em cada sub-rede.

Estudo de Caso:

200.100.10.x 	200.100.11.x 	200.100.12.x 	200.100.13.x
Empresa A 		Empresa B 		Empresa C 		Empresa D
60pc			55pcs			59pcs			45pcs

Ao invés de criar uma rede para cada empresa, vamos evitar o desperdício de Endereços IPs com a criação de Sub-redes.

Sub-rede que será criada: 200.100.10.x
_________________________________________↱ 2² = 4 Sub-redes
Máscara de Sub-rede: 11111111.11111111.11111111.11000000
					  255	.	255	 .	255   .	 192

Quantidade de hosts disponíveis em cada uma: 2⁶ = 64 -2 = 62 hosts disponíveis.

<table>
    <tr>
        <th></th>
        <th>End. Rede</th>
        <th>1º Host</th>
        <th>Último Host</th>
        <th>End. Broadcast</th>
    </tr>
    <tr>
        <td>1ª Sub-rede</td>
        <td>000000</td>
        <td>000001</td>
        <td>111110</td>
        <td>000000</td>
    </tr>
    <tr>
        <td>2ª Sub-rede</td>
        <td>000001</td>
        <td>000001 </td>
        <td>111110</td>
        <td>000000</td>
    </tr>
    <tr>
        <td>3ª Sub-rede</td>
        <td>000010</td>
        <td>000001</td>
        <td>111110</td>
        <td>000000</td>
    </tr>
    <tr>
        <td>4ª Sub-rede</td>
        <td>000011</td>
        <td>000001</td>
        <td>111110</td>
        <td>000000</td>
    </tr>
</table>

Sub-rede: 200.100.10.x

1ª Sub-rede:

End. Rede: 200.100.10.0
End. 1º Host: 200.100.10.1
End. Último Host: 200.100.10.62
End. Broadcast: 200.100.10.63

2ª Sub-rede?
3ª Sub-rede?
4ª Sub-rede?

É necessário calcular os endereços para cada sub-rede.