# 💸 DICAS PARA BARATEAR O CUSTO DA VM NO AZURE

Este documento contém dicas práticas para reduzir os custos ao usar máquinas virtuais (VMs) na plataforma Microsoft Azure, 
com foco especial no uso com a licença *Azure for Students* tendo em vista as limitações da mesma.

---

## 🧠 ESCOLHAS INTELIGENTES NA CRIAÇÃO

### 1. Escolha SKUs mais econômicas
- Prefira VMs da série **B (Burstable)** como `B1s`, `B1ms` ou `B2as_v2`.
- Caso a `B1` não esteja disponível, verifique a disponibilidade em outras **regiões**.

### 2. Use imagens Linux ao invés de Windows
- Sistemas como **Ubuntu Server** ou **Debian** não possuem custo de licenciamento.

### 3. Desative recursos não essenciais
- **Backup automático**
- **Diagnóstico de inicialização e convidado**
- **Microsoft Defender for Cloud** (quando usado apenas para testes)
- **Hibernação** e **Rede acelerada**, se não forem necessárias

### 4. Evite discos SSD Premium
- Prefira o **Standard HDD** ou **Standard SSD** para economizar.

---

## ⏱️ OTIMIZE O USO

### 5. Desligue a VM quando não estiver usando
- Você **só paga enquanto a VM está ligada**.

### 6. Configure desligamento automático
- Habilite o **auto-shutdown** nas configurações de gerenciamento.

---

## 🌍 LOCALIZAÇÃO E REGIÕES

### 7. Altere a região de implantação
- Algumas regiões são mais baratas. Considere:
  - **East US**
  - **North Europe**
  - **West Europe**

---

## 🧪 CONSIDERE USAR AZURE SPOT

### 8. Azure Spot Instances
- Usam capacidade ociosa do Azure com **até 90% de desconto**.
- Podem ser **interrompidas a qualquer momento**, então são ideais para testes ou cargas não críticas.

---

## 🔐 SEGURANÇA E ACESSO

### 9. Desative IP público se não for necessário
- Reduz riscos e pode evitar custos adicionais com segurança.
- Use rede privada e acesse via VPN.

### 10. Evite portas expostas desnecessariamente
- Limite portas abertas à internet (ex: SSH ou RDP) apenas para uso temporário.
- Utilize **regras de NSG (Grupo de Segurança de Rede)** para controle.

---

## 📌 DICA EXTRA

### 11. Use scripts para automatizar
- Crie scripts para **ligar/desligar a VM automaticamente** com base no horário de uso.
- Exemplo: desligar toda noite às 23h.

---

