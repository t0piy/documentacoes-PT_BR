youtube-dl - baixe vídeos do youtube.com ou outras plataformas de vídeo

- [INSTALAÇÃO](#instalação)
- [DESCRIÇÃO](#descrição)
- [OPÇÕES](#opções)

# INSTALAÇÃO

Para instalá-lo para todos os usuários UNIX (Linux, macOS, etc.), digite:

    sudo curl -L https://yt-dl.org/downloads/latest/youtube-dl -o /usr/local/bin/youtube-dl
    sudo chmod a+rx /usr/local/bin/youtube-dl

Se você não tiver curl, você pode alternativamente usar um wget recente:

    sudo wget https://yt-dl.org/downloads/latest/youtube-dl -O /usr/local/bin/youtube-dl
    sudo chmod a+rx /usr/local/bin/youtube-dl

Usuários do Windows podem [baixar um arquivo .exe](https://yt-dl.org/latest/youtube-dl.exe) e colocá-lo em qualquer local em seu [PATH](https://en.wikipedia.org/wiki/PATH_%28variable%29) exceto em `%SYSTEMROOT%\System32` (i.e. **não** coloque em `C:\Windows\System32`).

Você também pode usar pip:

    sudo -H pip install --upgrade youtube-dl
    
Este comando atualizará o youtube-dl se você já o instalou. Veja a [página pypi](https://pypi.python.org/pypi/youtube_dl) para mais informações.

Usuários do macOS podem instalar o youtube-dl com [Homebrew](https://brew.sh/):

    brew install youtube-dl

Ou com [MacPorts](https://www.macports.org/):

    sudo port install youtube-dl

Como alternativa, consulte as instruções do desenvolvedor para saber como verificar e trabalhar com o repositório git. Para mais opções, incluindo assinaturas PGP, consulte a [Página de Download do youtube-dl](https://ytdl-org.github.io/youtube-dl/download.html).

# DESCRIÇÃO
**youtube-dl** é um programa de linha de comando para baixar vídeos do YouTube.com e de alguns outros sites. Requer o interpretador Python, versão 2.6, 2.7 ou 3.2+, e não é específico da plataforma. Ele deve funcionar em seu Unix, no Windows ou no macOS. Ele foi lançado para o domínio público, o que significa que você pode modificá-lo, redistribuí-lo ou usá-lo como quiser.

    youtube-dl [OPTIONS] URL [URL...]

# OPÇÕES
    -h, --help                           Exibe este texto de ajuda e sai
    --version                            Exibe a versão do programa e sai
    -U, --update                         Atualiza este programa para a versão mais
                                         recente. Certifique-se de que você tem
                                         permissões suficientes (execute com sudo
                                         se necessário)
    -i, --ignore-errors                  Continuar ao receber erros de download, 
                                         por exemplo, para pular vídeos
                                         indisponíveis em uma playlist
    --abort-on-error                     Abortar o download dos vídeos restantes (na
                                         playlist ou na linha de comando) caso
                                         ocorra um erro
    --dump-user-agent                    Mostra a identificação do navegador atual
    --list-extractors                    Lista todos os extratores suportados
    --extractor-descriptions             Descrições de saída de todos os extratores
                                         suportados
    --force-generic-extractor            Força a extração para usar o extrator
                                         genérico
    --default-search PREFIX              Use este prefixo para URLs não qualificados.
                                         ////////////////////////////////////
                                         ////PRECISA DE AJUDA NA TRADUÇÃO////
                                         /////////////. Use o valor "auto"
                                         para deixar que o youtube-dl adivinhe
                                         ("auto_warning" "auto_warning" para emitir
                                         um aviso ao adivinhar). "error" apenas
                                         envia um erro. O valor padrão "fixup_error"
                                         repara URLs quebrados, porém emite
                                         um erro se isso não for possível, em
                                         vez de pesquisar.
    --ignore-config                      Não lê os arquivos de configuração. Quando
                                         fornecido no arquivo de configuração global
                                         /etc/youtube-dl.conf: Não lê a configuração
                                         do usuário em ~/.config/youtube-dl/config
                                         (%APPDATA%/youtube-dl/config.txt no
                                         Windows)
    --config-location PATH               Localização do arquivo de configuração;
                                         o caminho para a configuração ou 
                                         o diretório onde está localizado.
    --flat-playlist                      Não extrai os vídeos de uma playlist,
                                         apenas lista-os. 
    --mark-watched                       Marcar vídeos como assistido (Apenas YouTube)
    --no-mark-watched                    Não marcar vídeos como assistido (Apenas
                                         YouTube)
    --no-color                           Não emitir códigos de core na saída

## Opções de rede:
    --proxy URL                          Use o proxy HTTP/HTTPS/SOCKS especificado.
                                         proxy. Para habilitar o proxy SOCKS,
                                         especifique um esquema apropriado.
                                         Por exemplo socks5://127.0.0.1:1080/.
                                         Passe uma string vazia (--proxy "")
                                         para conexão direta
    --socket-timeout SECONDS             Tempo de espera antes de desistir, em
                                         segundos
    --source-address IP                  Endereço IP do cliente para vincular
    -4, --force-ipv4                     Faça todas as conexões via IPv4
    -6, --force-ipv6                     Faça todas as conexões via IPv6
