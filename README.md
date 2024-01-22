
# IPV4 - Hardware Rede Brasil

## Classes

As classes no endereçamento IPv4 foram introduzidas para gerenciar e alocar de forma eficiente o espaço de endereçamento disponível na internet. Quando o IPv4 foi projetado, na década de 1980, a ideia era criar um sistema que pudesse acomodar a crescente demanda por endereços IP.

### Classe A
Projetada para grandes organizações, com um grande número de hosts. A parte mais significativa do endereço <br>IP é usada para a rede, e o restante é para hosts.

### Classe B
Projetada para organizações de médio porte. A metade mais significativa do endereço IP é usada <br>
para a rede, e a outra metade é para hosts.

### Classe C
Projetada para redes pequenas. Três quartos do endereço IP são usados para a rede, <br>
e apenas um quarto é para hosts.

### Classe D 
Reservada para multicast, onde um pacote é enviado de um emissor para vários receptores simultaneamente.

### Classe E
Reservada para fins experimentais e não é usada para endereçamento público regular.
 
<br>
<br>
 
| Classe | 1º Octeto      | Máscara Padrão | Faixa de Endereços          | Nº. de Redes    | Hosts por Rede           | Finalidade                           |
|:------:|:--------------:|:--------------:|:---------------------------:|:---------------:|:------------------------:|:------------------------------------:|
| `A`    | 0	a	127   | 255.0.0.0      | 1.0.0.0 a 126.0.0.0         | 128             | 16,777,214               | Grandes organizações                 |
| `B`    | 128	a	191   | 255.255.0.0    | 128.0.0.0 a 191.255.0.0     | 16,384          | 65,534                   | Redes de médio porte                 |
| `C`    | 192	a	223   | 255.255.255.0  | 192.0.0.0 a 223.255.255.0   | 2,097,152       | 254                      | Redes pequenas                       |
|  D     | 224	a	239   | Não aplicável  | 224.0.0.0 a 239.255.255.255 | Não aplicável   | Não aplicável            | Multicast                            |
|  E     | 240	a	255   | Não aplicável  | 240.0.0.0 a 255.255.255.255 | Não aplicável   | Não aplicável            | Reservado para fins experimentais    |

<br>

## Comunicação em Redes

1. **Unicast:**
   - Comunicação ponto a ponto, de um remetente para um destinatário.
   - **Uso Comum:** Transferência de dados direta entre dois dispositivos na rede.

2. **Anycast:**
   - Comunicação para o nó mais próximo de um grupo de receptores com o mesmo endereço anycast.
   - **Uso Comum:** Serviços de DNS, onde a consulta é encaminhada para o servidor mais próximo geograficamente.

3. **Multicast:**
   - Comunicação de um remetente para um grupo de receptores.
   - **Uso Comum:** Streaming de vídeo ao vivo, distribuindo dados para múltiplos destinatários simultaneamente.

4. **Broadcast:**
   - Comunicação de um remetente para todos os dispositivos na rede.
   - **Observação:** Menos comum em redes modernas devido à propensão para gerar tráfego desnecessário.

<br>

## IPs Restritos, Privados e Reservados

Além das classes tradicionais de endereçamento IP, é importante considerar categorias especiais de IPs destinadas a cenários específicos. Esses endereços são reservados para propósitos especiais e não são roteados publicamente na internet. Aqui estão algumas categorias notáveis:


### 1. Loopback (127.0.0.0 a 127.255.255.255)
- **Descrição:** Reservado para comunicação interna em um único dispositivo. O endereço mais comum é 127.0.0.1, utilizado para acessar o próprio dispositivo (localhost).

### 2. IPs Reservados para Fins Especiais
- **0.0.0.0 a 0.255.255.255:**
  - **Descrição:** Reservado para diversos fins especiais, incluindo o endereço 0.0.0.0 utilizado como "Gateway Padrão".
- **169.254.0.0 a 169.254.255.255 (Link Local):**
  - **Descrição:** Utilizado para configuração automática de IPs quando nenhum endereço IP está configurado manualmente ou via DHCP. Também conhecido como APIPA (Automatic Private IP Addressing).
- **192.0.2.0 a 192.0.2.255:**
  - **Descrição:** Reservado para documentação e exemplos em documentos técnicos.
- **198.51.100.0 a 198.51.100.255:**
  - **Descrição:** Similar ao bloco anterior, destinado a exemplos e documentação.
- **203.0.113.0 a 203.0.113.255:**
  - **Descrição:** Reservado para fins de teste e exemplos, amplamente utilizado em documentação técnica.

### 3. IPs Reservados para Multicast (224.0.0.0 a 255.255.255.255)
- **Descrição:** Reservado para comunicação multicast, utilizado para enviar dados para um grupo de receptores simultaneamente.

### 4. Broadcast Geral (255.255.255.255)
- **Descrição:** Utilizado para transmitir dados para todos os dispositivos na rede. No entanto, é menos comum em redes modernas devido à propensão para gerar tráfego desnecessário.

Esses IPs reservados desempenham papéis críticos em cenários específicos, como comunicação interna, configuração automática, documentação e multicast.

<br>

## Identificação de Rede e Host

O endereço IP é dividido em duas partes distintas: a identificação da rede e a identificação do host. 
A separação entre essas partes é determinada pelo tipo de classe de endereçamento.


### Classes de Endereçamento e Identificação

1. **Classe A (1.0.0.0 a 126.0.0.0):**
   - **Rede:** O primeiro octeto identifica a rede.
   - **Host:** Os três octetos restantes identificam o host.

2. **Classe B (128.0.0.0 a 191.255.0.0):**
   - **Rede:** Os dois primeiros octetos identificam a rede.
   - **Host:** Os dois octetos restantes identificam o host.

3. **Classe C (192.0.0.0 a 223.255.255.0):**
   - **Rede:** Os três primeiros octetos identificam a rede.
   - **Host:** O último octeto identifica o host.


### Máscaras de Sub-Rede

Máscaras de sub-rede são usadas para dividir ainda mais a identificação de rede e host, permitindo a criação de sub-redes dentro de uma rede maior.

### Exemplo Prático

Considere o endereço **IP** 192.168.1.10 com uma **máscara de sub-rede** 255.255.255.0:
- **Rede:** 192.168.1.0
- **Host:** 10
