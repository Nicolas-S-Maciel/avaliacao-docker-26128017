# Respostas · Avaliação Prática de Docker · Cooperativa AgroVale (Turma A)

Nome: Nícolas Silva Maciel
Matrícula: 26128017
Usuário do GitHub: Nicolas-S-Maciel
Usuário do Docker Hub: nikottrw

Responda com as suas palavras e com o que aconteceu na SUA máquina. Resposta curta e certa vale mais
do que texto longo copiado. Resposta que contradiz o seu próprio Dockerfile ou compose vale zero.

## Parte 1 · Dockerfile do portal

1. Qual imagem base você usou e qual o tamanho final da imagem do portal (saída de `docker images`)?
R: Foi utilizada a imagem base oficial do Nginx com a tag fixa alpine (nginx:alpine).


2. Em qual pasta do container o Nginx procura os arquivos do site? Mostre o comando que você usou para conferir que o `index.html` está lá dentro.
R: Foi utilizada a instrução COPY ./html/ /usr/share/nginx/html/ para copiar o conteúdo do diretório portal/html/ para o diretório padrão onde o Nginx serve os arquivos estáticos na imagem.


## Parte 2 · Docker Hub

3. Nome completo da imagem publicada e link público do repositório no Docker Hub.
R: * **Nome completo da imagem:** `ghcr.io/nicolas-s-maciel/agrovale-portal:1.0-26128017` ou `nikottrw/agrovale-portal:1.0-26128017` no Docker Hub
* **Link público do repositório:** `https://github.com/Nicolas-S-Maciel/agrovale-portal/pkgs/container/agrovale-portal` ou `https://hub.docker.com/r/nikottrw/agrovale-portal` no Docker hub

4. Por que o `docker login` foi feito com um token de acesso e não com a senha da conta?
R: Foi feito assim por questão de segurança, e para oferecer suporte a 2FA que sria a autenticação

## Parte 3 · Página de manutenção

5. Preencha uma linha por defeito encontrado. Defeito inexistente listado aqui desconta pontos.
R: Nenhum defeito foi encontrado

6. Qual a diferença entre `-p 7042:80` e `-p 80:7042` no `docker run`? Qual dos dois números é a porta do container?
R: -p 7042:80: Mapeia a porta 7042 do computador (host) para a porta 80 do container.
-p 80:7042: Mapeia a porta 80 do computador (host) para a porta 7042 do container.
O segundo número é a porta interna do container.

## Parte 4 · docker-compose.yml

7. No serviço `blog`, por que `WORDPRESS_DB_HOST` recebe `db` e não `localhost`?

8. Por que o serviço `db` não publica a porta 3306? Se precisar consultar o banco, como faz sem publicar
   a porta? Mostre o comando.

## Parte 5 · Persistência

9. Quais comandos você usou para derrubar e subir a stack? Qual comando teria apagado o post que você criou,
   e por quê?

10. Código de conclusão impresso pelo verificador:

```
(cole aqui)
```
