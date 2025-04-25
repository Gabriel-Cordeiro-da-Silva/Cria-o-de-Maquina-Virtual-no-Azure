## 📖 Dicionário de Termos do Azure – Máquinas Virtuais

| Termo | Definição |
|------|-----------|
| **VM (Virtual Machine)** | Computador virtual hospedado na nuvem, com sistema operacional, memória, armazenamento e recursos configuráveis. |
| **Azure** | Plataforma de computação em nuvem da Microsoft que fornece serviços como máquinas virtuais, bancos de dados, redes e mais. |
| **Região** | Localização geográfica onde os recursos do Azure são hospedados. Ex: Brazil South, East US. |
| **Zona de disponibilidade** | Subdivisão de uma região que oferece redundância física para alta disponibilidade. |
| **Grupo de Recursos** | Container lógico usado para agrupar recursos relacionados no Azure para gerenciamento e organização. |
| **Imagem** | Sistema operacional pré-configurado que será usado para criar a VM. Ex: Ubuntu 22.04, Windows 11. |
| **Geração da VM (Gen2)** | Versão mais recente da arquitetura de VMs no Azure, com suporte a recursos modernos de segurança e desempenho. |
| **Arquitetura x64 / ARM64** | Define o tipo de processador que a VM irá utilizar. x64 é a mais comum para desktops e servidores. ARM64 é mais eficiente em energia, usado em dispositivos móveis e novas gerações. |
| **SSH (Secure Shell)** | Protocolo usado para acessar a máquina remotamente com segurança. |
| **Chave pública/privada (SSH)** | Par de chaves usado para autenticação em conexões SSH. A chave pública vai na VM e a privada fica com o usuário. |
| **RSA / Ed25519** | Algoritmos usados para gerar chaves SSH. RSA é mais compatível, Ed25519 é mais rápido e seguro para alguns casos. |
| **IP Público** | Endereço acessível pela internet para se conectar à VM. |
| **Sub-rede** | Faixa de endereços IP dentro da rede virtual, usada para organizar e isolar recursos. |
| **Rede virtual (VNet)** | Rede definida pelo usuário dentro do Azure, onde recursos como VMs e bancos de dados podem se comunicar. |
| **Disco Gerenciado** | Disco virtual gerenciado pela Microsoft. Mais fácil de usar e mais seguro. |
| **SSD Premium / HDD Standard / SSD Standard** | Tipos de discos com diferentes níveis de desempenho e custo. SSD Premium oferece o melhor desempenho. |
| **Hibernação** | Recurso que permite pausar a VM mantendo seu estado atual, para retomada posterior sem perder dados. |
| **Azure Spot** | Instâncias de VM com desconto, sujeitas a interrupção pela Microsoft quando os recursos forem necessários por outros clientes. |
| **NSG (Network Security Group)** | Grupo de regras que controla o tráfego de rede que entra e sai dos recursos do Azure. |
| **Azure Bastion** | Serviço que permite conexão RDP ou SSH ao Azure sem expor IP público. |
| **LRS (Locally Redundant Storage)** | Armazenamento redundante localmente, com três cópias de seus dados na mesma região. |
| **Diagnóstico de Inicialização** | Permite visualizar logs e capturas de tela da VM durante o boot, útil para identificar erros. |
| **vTPM (Virtual Trusted Platform Module)** | Módulo de segurança virtual usado para criptografia e inicialização segura. |
| **Identidade Gerenciada** | Permite que a VM acesse outros serviços do Azure com uma identidade própria, sem precisar armazenar senhas. |
| **Microsoft Defender para Nuvem** | Solução de segurança que protege recursos em nuvem contra ameaças. |
| **Cloud-init / User Data** | Scripts de automação que podem ser executados durante a criação da VM para configuração inicial. |
| **Extensões de VM** | Ferramentas que podem ser instaladas automaticamente para tarefas como backup, monitoramento, ou antivírus. |

