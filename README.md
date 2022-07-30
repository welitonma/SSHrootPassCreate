# SSHrootPassCreate 
#### Credito não incluso, salvei o codigo e não lembro onde achei :/


### ENTRAR E DEFINIR ACESSO ROOT:

#### Acesse por SSH e se torne root
```md
sudo -i
```
#### Execute o codigo abaixo e insira uma senha para o root
```md
bash <(wget -qO- https://raw.githubusercontent.com/welitonma/SSHrootPassCreate/main/rootpass.sh)
```

### ABRIR PORTAS SERVER ORACLE:
```md
sudo apt-get update
```
```md
sudo apt install firewalld 
```
#### Substitua a 'PORTA' EX: 8080/tcp - que necessite, repita quantas vezes for necessario. Porta udp substituir texto tcp>udp
```md
sudo firewall-cmd --zone=public --permanent --add-port=PORTA/tcp 
```
```md
sudo firewall-cmd --reload 
```
```md
sudo firewall-cmd --zone=public --list-ports
```
