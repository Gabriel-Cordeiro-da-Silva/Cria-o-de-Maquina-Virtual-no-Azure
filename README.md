# 🚀 Criação e Configuração de Máquina Virtual no Microsoft Azure

## 📌 Introdução

Este repositório documenta o processo de criação e configuração de uma máquina virtual (VM) no Microsoft Azure, conforme proposto no desafio da DIO. O objetivo é aplicar os conhecimentos adquiridos sobre computação em nuvem, especificamente na plataforma Azure, e compartilhar a experiência por meio de documentação técnica clara e estruturada.

## 🎯 Objetivos do Desafio

- Aplicar conceitos de computação em nuvem em um ambiente prático.
- Documentar processos técnicos de forma clara e estruturada.
- Utilizar o GitHub como ferramenta para compartilhamento de documentação técnica.

## 🛠️ Etapas para Criação da Máquina Virtual

### 1. Acesso ao Portal do Azure

- Acesse o [Portal do Azure](https://portal.azure.com/).
- No menu lateral, clique em **"Máquinas virtuais"**.
- Clique em **"Criar"** e selecione **"Máquina virtual"**.

### 2. Configuração Básica

- **Assinatura**: Azure for Students (caso não tenha convenio estudantil pode utilizar a versão free, onde possui 200 creditos iniciais)
- **Grupo de Recursos**: (novo) MC (de sua escolha)
- **Nome da Máquina Virtual**: MC1 (de sua escolha)
- **Região**: Brazil South
- **Opções de Disponibilidade**: Zona de disponibilidade - Zona 1
- **Tipo de Segurança**: Computadores virtuais de inicialização confiável
  - Habilitar inicialização segura: Sim
  - Habilitar vTPM: Sim
  - Monitoramento de integridade: Não
- **Imagem**: Ubuntu Server 22.04 LTS – Gen2 (utilizei o Unbutu para que a maquina tivesse um menor custo de operação)
- **Arquitetura de VM**: x64
- **Tamanho**: Standard B2as v2 (2 vCPUs, 8 GiB de memória)
- **Habilitar Hibernação**: Não

### 3. Configuração de Autenticação

- **Tipo de Autenticação**: Chave pública de SSH (utilizei uma chave pulblica pois era apenas para fins de apredizado e o VM seria excluido depois)
- **Nome de Usuário**: Gabriel
- **Formato de Chave SSH**: RSA
- **Nome do Par de Chaves**: Gabriel

> **Nota**: Certifique-se de baixar e armazenar a chave privada com segurança, pois ela será necessária para acessar a VM via SSH.

### 4. Configuração de Disco

- **Tamanho do Disco do SO**: Padrão de imagem
- **Tipo de Disco do SO**: LRS do SSD Padrão
- **Usar Discos Gerenciados**: Sim
- **Excluir o Disco do SO com a VM**: Habilitado
- **Disco de SO Efêmero**: Não

### 5. Configuração de Rede

- **Rede Virtual**: (novo) MC1-vnet
- **Sub-rede**: (novo) default (10.0.0.0/24)
- **IP Público**: (novo) MC1-ip
- **Rede Acelerada**: Desativado
- **Colocar esta máquina virtual por trás de uma solução de balanceamento de carga existente?**: Não
- **Excluir o IP público e a NIC quando a VM for excluída**: Habilitado

### 6. Configurações Avançadas

- **Microsoft Defender para Nuvem**: Básico (gratuito)
- **Identidade Gerenciada Atribuída pelo Sistema**: Desativado
- **Fazer Login com o Microsoft Entra ID**: Desativado
- **Desligamento Automático**: Desativado
- **Backup**: Desabilitado
- **Habilitar Avaliação Periódica**: Desativado
- **Habilitar Patch Dinâmico**: Desativado
- **Opções de Orquestração de Patch**: Padrão da Imagem
- **Alertas**: Desativado
- **Diagnóstico de Inicialização**: Ativado
- **Habilitar o Diagnóstico de Convidado do SO**: Desativado
- **Habilitar o Monitoramento de Integridade do Aplicativo**: Desativado
- **Extensões**: Nenhum
- **Aplicativos da VM**: Nenhum
- **Cloud-init**: Não
- **Dados do Usuário**: Não
- **Tipo de Controlador de Disco**: SCSI
- **Grupo de Posicionamento por Proximidade**: Nenhum
- **Grupo de Reserva de Capacidade**: Nenhum

### 7. Configuração de Portas de Entrada

- **Portas de Entrada Públicas**: SSH

> **Alerta de Segurança**: O Azure exibe um aviso ao abrir a porta SSH para a Internet, recomendando essa configuração apenas para testes. Para ambientes de produção, é aconselhável restringir o acesso SSH a endereços IP específicos ou utilizar soluções como o Azure Bastion para conexões seguras.


## 🧠 Dicas e Observações

- **Chave SSH**: Utilize o formato RSA para maior compatibilidade. Certifique-se de armazenar a chave privada em local seguro.
- **Segurança**: Para ambientes de produção, evite expor a porta SSH diretamente à Internet. Utilize grupos de segurança de rede (NSG) para restringir o acesso ou implemente o Azure Bastion.
- **Gerenciamento de Custos**: Monitore o uso da VM para evitar custos inesperados. Considere desligar ou excluir recursos não utilizados.

## 📚 Referências

- [Início Rápido: Criar uma máquina virtual do Windows no portal do Azure](https://learn.microsoft.com/pt-br/azure/virtual-machines/windows/quick-create-portal)
- [Documentação do Azure sobre Máquinas Virtuais](https://learn.microsoft.com/pt-br/azure/virtual-machines/)
- [Guia de Segurança para Máquinas Virtuais no Azure](https://learn.microsoft.com/pt-br/azure/security/fundamentals/virtual-machines-overview)

## ✅ Conclusão

A criação e configuração de uma máquina virtual no Microsoft Azure proporcionam uma compreensão prática dos conceitos de computação em nuvem. permitindo aplicar conhecimentos teóricos em um ambiente real, além de reforçar a importância da documentação técnica e das boas práticas de segurança.
