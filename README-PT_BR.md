# AMWin-RP 
![GitHub release (latest by date including pre-releases)](https://img.shields.io/github/downloads-pre/PKBeam/AMWin-RP/total) ![GitHub release (latest by date including pre-releases)](https://img.shields.io/github/downloads-pre/PKBeam/AMWin-RP/latest/total) &nbsp; ([English](README.md) | [한국어](README-KO.md) | [日本語](README-JA.md) | [Russian](README-RU.md) | [Español de Hispanoamérica](README-ES_419.md) | [Deutsch](README-DE.md) | [Português (Brasil)](README-PT_BR.md))

Um cliente de Discord Rich Presence para o aplicativo nativo do Apple Music no Windows.
Também inclui scrobbling para Last.FM e ListenBrainz.

<image width=450 src="https://github.com/user-attachments/assets/7a8e738a-d7af-4a67-9cf4-f4cf9c3c31d1" />
&nbsp; &nbsp; 
<image src=https://github.com/user-attachments/assets/f5464285-77de-4f98-ac8c-38dca5991c7f width=300 />

## Instalação
O AMWin-RP requer Windows 11 24H2 ou superior.

As builds podem ser encontradas [aqui](https://github.com/PKBeam/AMWin-RP/releases).  

### Qual versão devo usar?
Escolha x64 ou ARM64 de acordo com o processador do seu PC.
Depois, há dois arquivos entre os quais escolher: o normal e o marcado como `NoRuntime`.

Em caso de dúvida, use o *"release"* sem marcação (o que não contém `NoRuntime`).
Esta versão funciona universalmente, mas é maior porque traz empacotados os componentes do .NET necessários para executar o aplicativo.

A versão `NoRuntime` tem um tamanho consideravelmente menor, mas requer que o [.NET 10 desktop runtime](https://dotnet.microsoft.com/en-us/download/dotnet/10.0) esteja instalado.
Se você não tiver o *runtime* instalado, o programa notificará você para instalá-lo quando for aberto.

## Uso
Você precisa da versão do Apple Music da [Microsoft Store](https://apps.microsoft.com/detail/9PFHDD62MXS1) para poder usar o AMWin-RP.

- Execute o .exe para iniciar o aplicativo.
- O AMWin-RP é executado em segundo plano, minimizado na bandeja do sistema.
- Clicar duas vezes no ícone da bandeja abrirá a janela de configurações.
  - Aqui você poderá configurar as diversas opções, como executar ao iniciar o computador, scrobbling e detecção de músicas.
- O aplicativo pode ser encerrado clicando com o botão direito no ícone da bandeja e selecionando "Sair".
- Por padrão, o aplicativo do Apple Music deve estar aberto e reproduzindo música (não pausada) para que o Rich Presence seja exibido.

**Nota**: Se você usar áreas de trabalho virtuais, o AMWin-RP e o Apple Music deverão estar na mesma área de trabalho.
Esta é uma limitação técnica da biblioteca UI Automation usada para extrair dados do cliente do Apple Music.

## Scrobbling
A implementação do scrobbler não suporta Scrobbles offline, o que implica que qualquer música ouvida sem estar conectado à internet não será registrada.

### Last.FM
Você precisará da sua própria Chave de API e API Secret do Last.FM.
Para gerar uma, acesse https://www.last.fm/api e selecione "Get an API Account".
Insira-as no menu de configurações junto com seu nome de usuário do Last.FM e sua senha.

A senha do Last.FM é armazenada no [Gerenciador de Credenciais do Windows](https://support.microsoft.com/pt-br/windows/gerenciador-de-credenciais-no-windows-1b5c916a-6a16-889f-8581-fc16e8165ac0) sob sua conta local do Windows. 

### ListenBrainz 
Você pode fazer scrobble no ListenBrainz adicionando seu token de usuário nas configurações.

## Reportar Erros
Antes de criar um novo issue, certifique-se de que o problema não está incluído em um issue já existente.
Se você estiver reportando um problema, por favor anexe qualquer arquivo `.log.` relevante (localizados em `%localappdata%\AMWin-RichPresence`). 

Antes de publicar, verifique o seguinte:
- O problema não foi coberto em nenhum issue, seja aberto ou fechado.
- Você tem ativado mostrar RP no Discord (Configurações > Configurações de Atividade > Privacidade da atividade > Compartilhar minha Atividade).