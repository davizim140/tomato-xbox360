# Roadmap técnico

## Fase 1 — validar o SDK
- Compilar o toolchain xsdk em GitHub Actions.
- Compilar a amostra oficial e verificar que o arquivo XEX existe.
- Guardar o XEX como artefato de CI, sem substituir arquivos do console.

## Fase 2 — aplicação nativa mínima
- Criar o projeto C/C++ próprio com CMake e `xsdk_add_xex()`.
- Implementar desenho de tela, navegação D-pad/A/B/Back e mensagens de erro.
- Validar leitura de arquivos locais e conexão de rede separadamente.

## Fase 3 — funções do app
Possíveis módulos a investigar e implementar, conforme fontes e serviços acessíveis:
- catálogo e pesquisa;
- detalhes e lista de episódios;
- favoritos e histórico local;
- configurações e estado da conexão;
- catálogo de mangás/recomendações, se confirmado como função do app original.

Esta lista é uma hipótese de escopo, não uma confirmação do conteúdo do APK.

## Fase 4 — mídia online
Antes de prometer streaming, testar protocolos HTTPS/TLS, formatos de playlist e codecs que o console realmente consiga decodificar. Se o serviço depender de DRM, APIs privadas, autenticação incompatível ou codecs não suportados, essa função pode não ser reproduzível diretamente no Xbox 360.

## Critérios para considerar funcional
- código-fonte no repositório;
- build XEX bem-sucedido no Actions;
- controles e telas testados;
- resultados de testes documentados;
- validação no Xenia e/ou console físico;
- nenhuma alegação de paridade total sem evidência.
