# AMWin-RP
![GitHub release (latest by date including pre-releases)](https://img.shields.io/github/downloads-pre/PKBeam/AMWin-RP/total) ![GitHub release (latest by date including pre-releases)](https://img.shields.io/github/downloads-pre/PKBeam/AMWin-RP/latest/total) &nbsp; ([English](README.md) | [Korean](README-KO.md) | [Japanese](README-JA.md) | [Español de Latinoamérica](README-ES_419.md) | [Español de España](README-ES.md) | [Deutsch](README-DE.md))

Um cliente de Discord Rich Presence para o aplicativo nativo do Apple Music no Windows.
Também inclui scrobbling para Last.FM e ListenBrainz.

<image width=450 src="https://github.com/user-attachments/assets/7a8e738a-d7af-4a67-9cf4-f4cf9c3c31d1" />
&nbsp; &nbsp; 
<image src=https://github.com/user-attachments/assets/f5464285-77de-4f98-ac8c-38dca5991c7f width=300 />

## Instalação
O AMWin-RP requer Windows 11 24H2 ou superior.

As builds estão disponíveis [aqui](https://github.com/PKBeam/AMWin-RP/releases).

### Qual versão devo usar?
Escolha `x64` ou `ARM64` de acordo com o processador do seu PC.
Depois, escolha um dos dois arquivos: o normal ou o marcado como `NoRuntime`.

Se estiver em dúvida, use o release sem marcação (ou seja, sem `NoRuntime`).
Esta versão funciona universalmente, mas ocupa mais espaço, pois inclui os componentes do .NET necessários para executar o aplicativo.

A versão `NoRuntime` é bem menor, mas requer o [.NET 10 desktop runtime](https://dotnet.microsoft.com/en-us/download/dotnet/10.0) instalado.
Se o runtime não estiver instalado, o programa solicitará que você o instale ao abrir.

## Uso
Você precisa da [versão do Apple Music da Microsoft Store](https://apps.microsoft.com/detail/9PFHDD62MXS1) para usar o AMWin-RP.

- Execute o `.exe` para iniciar o aplicativo.
- O AMWin-RP roda em segundo plano, minimizado na bandeja do sistema.
- Um clique duplo no ícone da bandeja abre a janela de configurações.
  - Aqui você pode configurar opções como executar ao iniciar o Windows, scrobbling e detecção de músicas.
- O aplicativo pode ser fechado clicando com o botão direito no ícone da bandeja e selecionando "Sair".
- Por padrão, para que o Rich Presence seja exibido, o aplicativo do Apple Music deve estar aberto e reproduzindo música (não pausado).

**Nota**: se você usar áreas de trabalho virtuais, o AMWin-RP e o Apple Music precisam estar na mesma área de trabalho.
Esta é uma limitação técnica da biblioteca UI Automation usada para extrair dados do cliente do Apple Music.

## Scrobbling
A implementação atual do scrobbler não suporta scrobbles offline. Isso significa que músicas ouvidas sem conexão com a internet serão perdidas.

### Last.FM
Você precisará da sua própria Chave de API e API Secret do Last.FM.
Para obter uma, acesse https://www.last.fm/api e selecione "Get an API Account."
Insira esses dados nas configurações junto com seu nome de usuário e senha do Last.FM.

A senha do Last.FM é armazenada no [Gerenciador de Credenciais do Windows](https://support.microsoft.com/pt-br/windows/gerenciador-de-credenciais-no-windows-1b5c916a-6a16-889f-8581-fc16e8165ac0) sob sua conta local do Windows.

### ListenBrainz
Você pode fazer scrobble no ListenBrainz adicionando seu token de usuário nas configurações.

## Reportar Erros
Antes de criar um novo issue, certifique-se de que seu problema não duplica um já existente.
Se você estiver reportando um problema, anexe os arquivos `.log` relevantes (eles ficam em `%localappdata%\AMWin-RichPresence`).

Antes de publicar, verifique o seguinte:
- O problema ainda não foi descrito em nenhum issue aberto ou fechado.
- A exibição de atividade está ativada no Discord (Configurações > Configurações de Atividade > Privacidade da Atividade > Status de Atividade).
