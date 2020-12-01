# command_parser_ping

Ele emite o comando Cisco IOS ** 'ping' ** e analisa a saída.

O arquivo **ping.yml** é um manual que usa o analisador.
Pode ser usado como exemplo e deve ser autoexplicativo.


## Example

```
$ ansible-playbook ping.yml --limit switch.example.com --extra-vars dst="192.168.0.1 vrf=1150"
```
Aqui está um exemplo de como a saída pode ser:

```
{
    "destination_address": "192.168.0.1",
    "dst": "192.168.0.1",
    "success_rate": "100",
    "vrf": "1150"
}
```

Especificar **dst** é obrigatório, pois esse é o endereço de destino do ping.

A variável **vrf** não é obrigatória. O domínio de roteamento padrão será usado se não for especificado.

