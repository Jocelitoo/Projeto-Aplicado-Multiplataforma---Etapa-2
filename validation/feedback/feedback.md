- Feedback: O público alvo achou o sistema muito interessante pois em um só lugar era possível ter acesso à informações de várias ongs de maneira fácil e intuitiva

- Sugestões de melhorias recebidas: Por conta da lógica do código, ao criar uma ONG, o usuário precisava sair da conta e entrar novamente para o sistema trazer a ONG vinculada a ele. O público alvo não gostou disso e reportou

- Ajustes implementados baseados no feedback: Os dados da ONG estavam sendo puxados através do nextauth que retornava a ONG do usuário que havia feito o login, porém em caso de edição ou criação o processo de login não era feito, a consequência disso era que o sistema não retornava a ONG criada/atualizada. Então, foi alterado a lógica do código para pegar a ONG vinculada ao usuário diretamente através do prisma quando a página fosse carragada, e não quando o usuário fazia login
