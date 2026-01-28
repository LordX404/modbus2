Modbus Tool é uma ferramenta de automação e gerenciamento de dispositivos Modbus, com recursos avançados para controle a leitura de bobinas e registradores, escaneamento de rede, e acesso remoto via SSH para interação com dispositivos.
A ferramente é baseada em Python e utiliza bibliotecas como pymodbus para comunicação Modbus e paramiko para acesso SSH.

Funcionalidades:
Escaneamento de rede: detecta dispositivos Modbus na rede, buscando por dispositivos conectados no intervalo de IPs especificado.
Leitura e escrita de bobinas e registradores: Permite ler e escrever valores em bobinas e registradores Modbus.
Controle de dispositivos: Ligar/desligar dispositivos ou bobinas usando comandos Modbus.
Acesso SSH remoto: Conecta-se ao terminal de dispositivo via SSH, com suporte a login com ou sem autenticação.
Histórico e macros: Armazena um histórico de comandos executados e permite criar macros para execução de sequências de comandos.

Comandos Disponíveis:
exit, quit: Encerra o programa
ping: Verifica se o dispositivo está online.
read_coils <addr> <cnt>: Lê bobinas a partir do endereço especificado.
read_regs <addr> <cnt>: Lê registradores a partir do endereço especificado.
write_coil <addr> <val>: Escreve valor em uma bobina.
write_regs <addr> <val>: Escreve valores em registradores.
send_payload <addr> <payload>: Envia um payload (sequência de dados) para um endereço.
device_id_basic: Lê informações básicas do dispositivo Modbus.
device_id_extended:Lê informações avançadas do dispositivo Modbus.
system_info: Lê informações do sistema do dispositivo especificado.
turn_on <addr>: Liga o dispositivo ou bobina no endereço especificado.
turn_off <addr>: Desliga o dispositivo ou bobina no endereço especificado.
modify_register <addr> <value>: Modifica o valor de um registrador.
history: Exibe o histórico de comandos executados.
macro <name>: Cria um macro (sequência de comandos).
run <macro_name>: Executa uma macro.
sleep <seconds>: Aguarda por um determinado número de segundos.
clear: Limpa a tela do terminal.
scan_network: Escaneia a rede local em busca de dispositivos Modbus.
terminal: Conecta ao dispositivo via SSH.
help: Exibe este menu de ajuda.

Como Executar:
1- Clone esse repositório:
(git clone https://github.com/LordX404/modbus2.git)

2- Instale as dependências:
(pip install -r requirement.txt)

3- Execute o script principal:
(python modbus2.py)

4- Siga as instruções no Terminal para interagir com os dispositivos Modbus.

Acesso SSH:
Quando você usar o comando (terminal), a ferramenta ira perguntar o IP do dispositivo e, caso necessário, solicitará a autenticação para realizar a conexão via SSH.
Você pode optar por fornecer um nome de usuario e senha ou se conectar sem autenticação, caso o dispositivo permita.

Requisitos:
Python 3x
Bibliotecas: 
pymodbus
paramiko

Exemplo de execução:
Escaneando a Rede para dispositivos Modbus:
Para escanear a rede em busca de dispositivos Modbus, use o comando:
scan_network 192.168.1.0/24

Lendo e Escrevendo em Registradores:
Para ler um registrador a partir de um dispositivo:
read_regs 0 10

Para escrever em um registrador:
write_regs 0 100

Acesso SSH:
Para acessar um dispositivo via SSH:
terminal
Digite o IP do dispositivo, escolha se deseja fornecer um nome de usuário e senha, e inicie a conexão.




