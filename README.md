# Tomato Animes para Xbox 360 RGH

Port nativo em andamento para Xbox 360 RGH/JTAG usando o SDK aberto [xenosworks/xsdk](https://github.com/xenosworks/xsdk) e GitHub Actions.

## Estado real

- [x] Repositório inicializado.
- [x] Workflow de CI criado.
- [ ] Compilação do toolchain/amostras confirmada.
- [ ] Criar interface nativa e navegação pelo controle.
- [ ] Investigar fontes de catálogo e serviços acessíveis.
- [ ] Implementar e testar as funções confirmadas do app.
- [ ] Validar reprodução de vídeo no hardware real.

**Importante:** não temos o APK nem o código-fonte original. Ainda não é possível afirmar que todas as funções do app original foram identificadas ou reproduzidas. O primeiro XEX produzido pelo workflow será uma amostra de validação do SDK — não será o Tomato Animes funcional.

## Executar a compilação

1. Abra a aba [Actions](https://github.com/davizim140/tomato-xbox360/actions).
2. Selecione **Build xsdk bootstrap (not the app)**.
3. Clique em **Run workflow** e confirme.
4. Quando terminar, abra a execução e confira se ficou verde.
5. Se passar, baixe o artefato `tomato-xbox360-bootstrap-xex`.

A primeira compilação pode demorar bastante por construir o toolchain. Se falhar, envie a captura ou o texto do primeiro erro vermelho.

## Limitações

Um APK Android não é convertido diretamente em XEX: é necessário recriar o aplicativo em C/C++ para Xbox 360. Streaming moderno pode ser limitado por TLS, protocolos, autenticação e codecs não suportados pelo console. Isso precisa ser testado antes de prometer reprodução.

O workflow compila as amostras oficiais do xsdk; não compila ainda uma aplicação Tomato própria. Consulte [o roteiro técnico](docs/ROADMAP.md).

## Segurança

O artefato inicial não precisa modificar a NAND, a dashboard nem os arquivos do jogo. Não substitua arquivos do sistema para testar esta amostra.
