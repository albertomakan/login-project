# login-project
# English
Project to log in with Github + Google.

# Project file configuration:
Create the application-local.properties file in the path: src\main\resources\application-local.properties
add the following content to the created file:

#Github Login
spring.security.oauth2.client.registration.github.client-id=ChangeToYourGithubClientID
spring.security.oauth2.client.registration.github.client-secret=ChangeToYourGithubClientSecret

#Google Login
spring.security.oauth2.client.registration.google.client-id=ChangeToYourGoogleClientId
spring.security.oauth2.client.registration.google.client-secret=ChangeToYourGoogleClientSecret
spring.security.oauth2.client.registration.google.scope=openid,profile,email
spring.security.oauth2.client.registration.google.redirect-uri=http://localhost:8080/login/oauth2/code/google
spring.security.oauth2.client.registration.google.authorization-uri=https://accounts.google.com/o/oauth2/auth
spring.security.oauth2.client.registration.google.token-uri=https://oauth2.googleapis.com/token
spring.security.oauth2.client.registration.google.user-info-uri=https://www.googleapis.com/oauth2/v3/userinfo

Add to the end of the mvnw file (if it does not exist): spring-boot:run -Dspring.profiles.active=local

Note: after creating the project in Google Cloud Console, and entering the ClientId and ClientSecret in their respective areas, you must also create a user for testing, otherwise the login will fail.
To create the user in Google Cloud Console, with your project open, click on 'Target Audience' and you will have the option to add test users, add the email that will be used for testing and confirm.

# redirect-uri for local tests
Google: http://localhost:8080/login/oauth2/code/google
Github: http://localhost:8080/login/oauth2/code/github

# ------------------------------------------------------------------------------------------------

# Portuguese
Projeto para realização de login com Github + Google.

# Configuração de arquivos do projeto:
Criar o arquivo application-local.properties no caminho: src\main\resources\application-local.properties
adicionar o seguinte conteúdo ao arquivo criado:

#Github Login
spring.security.oauth2.client.registration.github.client-id=ChangeToYourGithubClientID
spring.security.oauth2.client.registration.github.client-secret=ChangeToYourGithubClientSecret

#Google Login
spring.security.oauth2.client.registration.google.client-id=ChangeToYourGoogleClientId
spring.security.oauth2.client.registration.google.client-secret=ChangeToYourGoogleClientSecret
spring.security.oauth2.client.registration.google.scope=openid,profile,email
spring.security.oauth2.client.registration.google.redirect-uri=http://localhost:8080/login/oauth2/code/google
spring.security.oauth2.client.registration.google.authorization-uri=https://accounts.google.com/o/oauth2/auth
spring.security.oauth2.client.registration.google.token-uri=https://oauth2.googleapis.com/token
spring.security.oauth2.client.registration.google.user-info-uri=https://www.googleapis.com/oauth2/v3/userinfo

Adicionar ao final do arquivo mvnw (caso não exista): spring-boot:run -Dspring.profiles.active=local

Obs.: após criar o projeto no Google Cloud Console, e inserir o ClientId e o ClientSecret em suas respectivas áreas, tem que criar também um usuário para teste senão o login irá falhar.
Para criar o usuário no Google Cloud Console, com seu projeto aberto clique em 'Público-Alvo'e terá a opção de adicionar usuários de teste, adicione o e-mail que sera utilizado para os testes e confirme.

# uri de redirecionamento para testes locais
Google: http://localhost:8080/login/oauth2/code/google
Github: http://localhost:8080/login/oauth2/code/github
