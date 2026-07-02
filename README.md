# -rvore-FHS-raiz-com-tree--L-1-no-KillerCoda-
O terminal que apresento na imagem arvore FHS.png mostra a execução do comando tree -L 1 / dentro de um sistema Linux (Ubuntu), operando como utilizador root.

Esse comando serve para listar de forma visual e hierárquica, limitando-se apenas ao primeiro nível de profundidade (-L 1), todas as pastas principais presentes na raiz (/) do sistema.



## Estrutura de Diretórios do Sistema (FHS)

O ecossistema Linux segue o padrão **FHS (Filesystem Hierarchy Standard)** para organizar os seus ficheiros e pastas. Abaixo está o mapeamento visual do primeiro nível da raiz do sistema (`/`), obtido através do comando `tree`:

```bash
root@ubuntu:~$ tree -L 1 /
/
├── bin -> usr/bin          # Executáveis essenciais do sistema (links simbólicos)
├── bin.usr-is-merged
├── boot                    # Ficheiros de inicialização (arquivos do Kernel e GRUB)
├── dev                     # Arquivos de dispositivos de hardware (devices)
├── etc                     # Ficheiros de configuração globais do sistema
├── home                    # Pastas pessoais dos utilizadores comuns
├── lib -> usr/lib          # Bibliotecas essenciais partilhadas pelo sistema
├── lib.usr-is-merged
├── lib64 -> usr/lib64      # Bibliotecas de 64 bits essenciais
├── lost+found              # Ficheiros recuperados por falhas no sistema de arquivos
├── media                   # Ponto de montagem para mídias removíveis (ex: Pen drives)
├── mnt                     # Ponto de montagem temporário de sistemas de arquivos
├── opt                     # Pacotes de software adicionais/opcionais (add-on)
├── proc                    # Sistema de arquivos virtual com informações de processos
├── root                    # Diretório home do superutilizador (administrador)
├── run                     # Dados de processos em execução desde a inicialização
├── sbin -> usr/sbin        # Executáveis de administração do sistema (root)
├── sbin.usr-is-merged
├── snap                    # Pacotes e aplicativos instalados via Snap
├── srv                     # Dados de serviços fornecidos pelo sistema (ex: servidores web)
├── swapfile                # Ficheiro de memória virtual (Swap)
├── sys                     # Informações e configurações do Kernel e hardware
└── tmp                     # Ficheiros temporários criados por programas
Nota: Como demonstrado pelas setas (->), este sistema utiliza uma estrutura moderna de Merged /usr, onde diretórios antigos como /bin e /lib apontam diretamente para os seus equivalentes dentro de /u
