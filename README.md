### Máscaras de Rede IPv4 em Detalhes

Em redes IPv4, uma máscara de rede é uma ferramenta crucial para dividir endereços IP em duas partes distintas: a parte da rede e a parte do host. A máscara de rede é representada por uma sequência de bits contínuos, onde os bits '1' indicam a parte da rede, e os bits '0' indicam a parte do host.
Existem máscaras de rede padrão e máscaras de rede de comprimento variável (CIDR), representadas por uma notação de barra (/) seguida pelo número de bits dedicados à identificação da rede.

#### Classes IPv4:

1. **Classe A (1.0.0.0 a 126.255.255.255):**
   - Máscara padrão: 255.0.0.0 ou /8.
   - Exemplo: Endereço IP 10.0.0.1 com máscara 255.0.0.0.

2. **Classe B (128.0.0.0 a 191.255.255.255):**
   - Máscara padrão: 255.255.0.0 ou /16.
   - Exemplo: Endereço IP 172.16.0.1 com máscara 255.255.0.0.

3. **Classe C (192.0.0.0 a 223.255.255.255):**
   - Máscara padrão: 255.255.255.0 ou /24.
   - Exemplo: Endereço IP 192.168.1.1 com máscara 255.255.255.0.

4. **Classe D (224.0.0.0 a 239.255.255.255):**
   - Reservada para multicast.

5. **Classe E (240.0.0.0 a 255.255.255.255):**
   - Reservada para usos experimentais.

#### Elementos Importantes:

- **Endereço de Rede:** É o endereço que identifica a própria rede. No exemplo do endereço IP 192.168.1.10 com máscara 255.255.255.0, o endereço de rede é 192.168.1.0.

- **Broadcast:** É um endereço especial usado para enviar dados para todos os dispositivos na rede. No mesmo exemplo, o broadcast seria 192.168.1.255.

#### Exemplo de Máscara de Rede:

Suponha um endereço IP da classe C: 192.168.1.10 com máscara padrão 255.255.255.0 ou /24. Vamos representar isso em formato Markdown:

```
Endereço IP: 192.168.1.10
Máscara de Rede: 255.255.255.0 ou /24
```

Na máscara, os primeiros 24 bits são dedicados à identificação da rede (255.255.255), enquanto os últimos 
8 bits são para os dispositivos na rede (0). Isso permite até 254 dispositivos 
(2^8 - 2, descontando o endereço de rede e o de broadcast).
