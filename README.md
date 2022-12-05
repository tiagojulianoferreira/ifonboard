# ifonboard
Aplicativo multiplataforma para automatizar o provisionamento do acesso sem fio baseado em WPA2 e de impressoras em dispositivos de usuários.

# Problema
Ao utilizar o protocolo de autentição WPA2 Enterprise na rede de acesso Wifi surgem desafios relacionados a complexidade e diversidade de configurações de rede sem fio presentes nas diversas plataformas de sistemas operacionais.

No Windows, por exemplo, são cerca 10 passos diferentes para adicionar uma nova rede sem fio, o que do ponto de vista de um usuário não especialista pode gerar grande dificuldade, demandando o apoio da TI.

# Funcionalidades e notas sobre arquitetura


- Criar nova rede sem fio nas diversas versão do Windows (7, 8.1,10,11) a partir do arquivo template em XML
- Salvar as credenciais de usuário e rede e habilitar conexão automática
- Caixa de Seleção do perfil de rede (ADM, ALUNO, etc) ou se usarmos SSID único, escolher o campus 
- Desacoplar ao máximo aspectos referentes aos SOs, ou seja, permitir aplicação de configurações específicas de acordo com versão do SO (Win 7, 8, 10)
- Permitir atualizações e hotfix pontuais. Ex: poder atualizar uma correção pro Win 10 sem afetar outras versões funcionais do SO
- Recurso de validação da conexão
- Com conexão/navegação validada, exibir status no APP para o usuário (Conexão OK)
- Com conexão, baixar e instalar drivers de impressoras de acordo com o perfil LDAP (ADM, Professor)
- O backend deve ter os endpoint de autenticação, verificação de plataforma e download de configurações via HTTP
