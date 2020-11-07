---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 0B3EF123-8424-4CCA-95E8-01301B70CBDC
online version: ''
schema: 2.0.0
ms.openlocfilehash: f84db81f51a4f8d0da605917f99e14c1721cd89d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946382"
---
# Add-AzureProvisioningConfig

## Sinopse
Adiciona a configuração de provisionamento para uma máquina virtual do Azure.

## SYNTAX

### Windows (padrão)
```
Add-AzureProvisioningConfig -VM <IPersistentVM> [-DisableGuestAgent] [-CustomDataFile <String>] [-Windows]
 [-AdminUsername <String>] [-Password <String>] [-ResetPasswordOnFirstLogon] [-DisableAutomaticUpdates]
 [-NoRDPEndpoint] [-TimeZone <String>] [-Certificates <CertificateSettingList>] [-EnableWinRMHttp]
 [-DisableWinRMHttps] [-WinRMCertificate <X509Certificate2>] [-X509Certificates <X509Certificate2[]>]
 [-NoExportPrivateKey] [-NoWinRMEndpoint] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### Linux
```
Add-AzureProvisioningConfig -VM <IPersistentVM> [-DisableGuestAgent] [-Linux] [-LinuxUser <String>]
 [-DisableSSH] [-NoSSHEndpoint] [-NoSSHPassword] [-SSHPublicKeys <SSHPublicKeyList>]
 [-SSHKeyPairs <SSHKeyPairList>] [-CustomDataFile <String>] [-Password <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### WindowsDomain
```
Add-AzureProvisioningConfig -VM <IPersistentVM> [-DisableGuestAgent] [-CustomDataFile <String>]
 -AdminUsername <String> [-WindowsDomain] [-Password <String>] [-ResetPasswordOnFirstLogon]
 [-DisableAutomaticUpdates] [-NoRDPEndpoint] [-TimeZone <String>] [-Certificates <CertificateSettingList>]
 -JoinDomain <String> -Domain <String> -DomainUserName <String> -DomainPassword <String>
 [-MachineObjectOU <String>] [-EnableWinRMHttp] [-DisableWinRMHttps] [-WinRMCertificate <X509Certificate2>]
 [-X509Certificates <X509Certificate2[]>] [-NoExportPrivateKey] [-NoWinRMEndpoint] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Add-AzureProvisioningConfig** adiciona informações de configuração de provisionamento a uma configuração de máquina virtual do Azure.
Você pode usar o objeto de configuração para criar uma máquina virtual.

Esse cmdlet dá suporte a diferentes configurações de provisionamento, incluindo servidores autônomos do Windows, Windows Servers associados a um domínio do Active Directory e servidores baseados em Linux.

Para criar um servidor associado a um domínio do Active Directory, especifique o nome de domínio totalmente qualificado do domínio do Active Directory e as credenciais de domínio de um usuário que tenha permissão para ingressar na máquina virtual no domínio.

## EXEMPLOS

### Exemplo 1: criar uma máquina virtual autônoma
```
PS C:\> New-AzureVMConfig -Name "NonDomainVM" -InstanceSize Small -ImageName "Image07" | Add-AzureProvisioningConfig -Windows -Password "password" -AdminUsername "AdminMain" | New-AzureVM -ServiceName "ContosoService"
```

Esse comando cria um objeto de configuração de máquina virtual usando o cmdlet **New-AzureVMConfig** .
O comando passa o objeto para o cmdlet atual usando o operador pipeline.
O cmdlet atual adiciona a configuração de provisionamento para uma máquina virtual que executa o sistema operacional Windows.
A configuração inclui o nome de usuário e a senha de administrador.
O comando passa a configuração para o cmdlet **New-AzureVM** , que cria a máquina virtual.

### Exemplo 2: criar uma máquina virtual unida ao domínio
```
PS C:\> New-AzureVMConfig -Name "DomainVM" -InstanceSize Small -ImageName "Image09" | Add-AzureProvisioningConfig -WindowsDomain -Password "password" -AdminUsername "AdminMain" -ResetPasswordOnFirstLogon -JoinDomain "contoso.com" -Domain "contoso" -DomainUserName "DomainAdminUser" -DomainPassword "DomainPassword" -MachineObjectOU 'OU=AzureVMs,DC=contoso,DC=com' | New-AzureVM -ServiceName "ContosoService"
```

Esse comando cria um objeto de configuração de máquina virtual e, em seguida, passa-o para o cmdlet atual.
O cmdlet atual adiciona a configuração de provisionamento de uma máquina virtual para ingressar no domínio contoso.
O comando inclui o nome de usuário e a senha necessários para ingressar na máquina virtual no domínio.
A configuração exige que o usuário altere a senha do usuário no primeiro logon.
O comando cria a máquina virtual com base no objeto de configuração.

### Exemplo 3: criar uma máquina virtual baseada em Linux
```
PS C:\> New-AzureVMConfig -Name "LinuxVM" -InstanceSize Small -ImageName "LinuxImage03" | Add-AzureProvisioningConfig -Linux -LinuxUser "LinuxRoot" -Password "password" | New-AzureVM -ServiceName "ContosoService"
```

Esse comando cria um objeto de configuração de máquina virtual e, em seguida, passa-o para o cmdlet atual.
O cmdlet atual adiciona a configuração de provisionamento para uma máquina virtual que executa o sistema operacional Linux.
A configuração inclui o nome de usuário e a senha raiz.
O comando cria a máquina virtual com base no objeto de configuração.

### Exemplo 4: criar uma máquina virtual que inclua certificados para WinRM
```
PS C:\> $certs = Get-ChildItem Cert:\CurrentUser\My
New-AzureVMConfig -Name "NonDomainVM" -InstanceSize Small -ImageName "Image11" | Add-AzureProvisioningConfig -Windows -Password "password" -AdminUsername "AdminMain" -WinRMCertificate $certs[0] -X509Certificates $certs[1], $certs[2] | New-AzureVM -ServiceName "ContosoService" -WaitForBoot
```

O primeiro comando obtém certificados de um repositório de certificados e, em seguida, os armazena na variável de matriz de $certs.

O segundo comando cria um objeto de configuração de máquina virtual e, em seguida, passa-o para o cmdlet atual.
O cmdlet atual adiciona configuração de provisionamento que inclui certificados para WinRM.
O comando cria a máquina virtual com base no objeto de configuração.

### Exemplo 5: criar uma máquina virtual com o WinRM habilitado em HTTP
```
PS C:\> New-AzureVMConfig -Name "NonDomainVM" -InstanceSize Small -ImageName "Image14" | Add-AzureProvisioningConfig -Windows -Password "password" -AdminUsername "AdminMain" -EnableWinRMHttp | New-AzureVM -ServiceName "ContosoService" -WaitForBoot
```

Esse comando cria um objeto de configuração de máquina virtual e, em seguida, passa-o para o cmdlet atual.
O cmdlet atual adiciona configuração de provisionamento que tem o WinRM habilitado em HTTP.
O comando cria a máquina virtual com base no objeto de configuração.

### Exemplo 6: criar uma máquina virtual que tenha o WinRM desabilitado em HTTPS
```
PS C:\> New-AzureVMConfig -Name "NonDomainVM" -InstanceSize Small -ImageName "Image07" | Add-AzureProvisioningConfig -Windows -Password "password" -AdminUsername "AdminMain" -DisableWinRMHttps | New-AzureVM -ServiceName "ContosoService" -WaitForBoot
```

Esse comando cria um objeto de configuração de máquina virtual e, em seguida, passa-o para o cmdlet atual.
O cmdlet atual adiciona uma configuração de provisionamento que desabilita o WinRM em HTTPS.
O comando cria a máquina virtual com base no objeto de configuração.

### Exemplo 7: criar uma máquina virtual sem exportação de chave
```
PS C:\> $certs = Get-ChildItem Cert:\CurrentUser\My
New-AzureVMConfig -Name "NonDomainVM" -InstanceSize Small -ImageName "Image07" | Add-AzureProvisioningConfig -Windows -Password "password" -AdminUsername "AdminMain" -X509Certificates $certs[0], $certs[1] -NoExportPrivateKey | New-AzureVM -ServiceName "ContosoService" -WaitForBoot
```

O primeiro comando obtém certificados de um repositório de certificados e, em seguida, os armazena na variável de matriz de $certs.

O segundo comando cria um objeto de configuração de máquina virtual e, em seguida, passa-o para o cmdlet atual.
O cmdlet atual adiciona a configuração de provisionamento para uma máquina virtual que inclui certificados e não exporta chaves privadas.
O comando cria a máquina virtual com base no objeto de configuração.

## OS

### -AdminUsername
Especifica o nome de usuário da conta de administrador que essa configuração cria na máquina virtual.

```yaml
Type: String
Parameter Sets: Windows
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: WindowsDomain
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Certificados
Especifica um conjunto de certificados que essa configuração instala na máquina virtual.

```yaml
Type: CertificateSettingList
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CustomDatafile
Especifica um arquivo de dados para a máquina virtual.
Esse cmdlet codifica o conteúdo do arquivo como Base64.
O arquivo deve ter menos de 64 kilobytes de comprimento.

Se o sistema operacional convidado for o sistema operacional do Windows, essa configuração salvará esses dados como um arquivo binário denominado%SYSTEMDRIVE%\AzureData\CustomData.bin.

Se o sistema operacional convidado for Linux, essa configuração passará os dados usando o arquivo ovf-env.xml.
A configuração copia o arquivo para o diretório/var/lib/waagent.
O agente também armazena os dados codificados em base64 no/var/lib/waagent/CustomData.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisableAutomaticUpdates
Indica que essa configuração desabilita as atualizações automáticas.

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisableGuestAgent
Indica que essa configuração desabilita o agente convidado de infraestrutura como serviço (IaaS).

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisableSSH
Indica que essa configuração desabilita o SSH.

```yaml
Type: SwitchParameter
Parameter Sets: Linux
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisableWinRMHttps
Indica que essa configuração desabilita o gerenciamento remoto do Windows (WinRM) em HTTPS.
Por padrão, o WinRM está habilitado no HTTPS.

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Domain
Especifica o nome do domínio da conta que tem permissão para adicionar o computador a um domínio.

```yaml
Type: String
Parameter Sets: WindowsDomain
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DomainPassword
Especifica a senha da conta de usuário que tem permissão para adicionar o computador a um domínio.

```yaml
Type: String
Parameter Sets: WindowsDomain
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DomainUserName
Especifica o nome da conta de usuário que tem permissão para adicionar o computador a um domínio.

```yaml
Type: String
Parameter Sets: WindowsDomain
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableWinRMHttp
Indica que essa configuração habilita o WinRM sobre HTTP.

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Informationaction
Especifica como esse cmdlet responde a um evento de informações.

Os valores aceitáveis para esse parâmetro são:

- Contínuo
- Ignorar
- Inquire
- SilentlyContinue
- Finaliza
- Suspensão

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InformationVariable
Especifica uma variável de informações.

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -JoinDomain
Especifica o nome de domínio totalmente qualificado (FQDN) do domínio para ingressar.

```yaml
Type: String
Parameter Sets: WindowsDomain
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Linux
Indica que essa configuração cria uma configuração Linux.

```yaml
Type: SwitchParameter
Parameter Sets: Linux
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LinuxUser
Especifica o nome de usuário da conta administrativa do Linux que essa configuração cria na máquina virtual.

```yaml
Type: String
Parameter Sets: Linux
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MachineObjectOU
Especifica o nome totalmente qualificado da unidade organizacional (UO) na qual a configuração cria a conta do computador.

```yaml
Type: String
Parameter Sets: WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NoExportPrivateKey
Indica que essa configuração não carrega a chave privada.

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NoRDPEndpoint
Indica que essa configuração cria uma máquina virtual sem um ponto de extremidade da área de trabalho remota.

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NoSSHEndpoint
Indica que essa configuração cria uma máquina virtual sem um ponto de extremidade SSH.

```yaml
Type: SwitchParameter
Parameter Sets: Linux
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NoSSHPassword
Indica que essa configuração cria uma máquina virtual sem uma senha SSH.

```yaml
Type: SwitchParameter
Parameter Sets: Linux
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NoWinRMEndpoint
Indica que essa configuração não adiciona um ponto de extremidade WinRM para a máquina virtual.

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Senha
Especifica a senha da conta de administrador.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Perfil
Especifica o perfil do Azure do qual este cmdlet lê.
Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResetPasswordOnFirstLogon
Indica que a máquina virtual exige que o usuário altere a senha no primeiro logon.

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SSHKeyPairs
Especifica os pares de chaves SSH.

```yaml
Type: SSHKeyPairList
Parameter Sets: Linux
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SSHPublicKeys
Especifica as chaves públicas SSH.

```yaml
Type: SSHPublicKeyList
Parameter Sets: Linux
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Fuso horário
Especifica o fuso horário da máquina virtual, por exemplo, hora padrão do Pacífico ou horário padrão central do Canadá.

```yaml
Type: String
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VM
Especifica um objeto de máquina virtual.

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Windows
Indica que essa configuração cria uma máquina virtual autônoma que executa o sistema operacional Windows.

```yaml
Type: SwitchParameter
Parameter Sets: Windows
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WindowsDomain
Indica que essa configuração cria o Windows Server que ingressou em um domínio do Active Directory.

```yaml
Type: SwitchParameter
Parameter Sets: WindowsDomain
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WinRMCertificate
Especifica um certificado que essa configuração associa a um ponto de extremidade WinRM.

```yaml
Type: X509Certificate2
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -X509Certificates
Especifica uma matriz de certificados X509 que são implantados em um serviço hospedado.

```yaml
Type: X509Certificate2[]
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

## EXIBE

## INFORMA

## LINKS RELACIONADOS

[New-AzureVM](./New-AzureVM.md)

[New-AzureVMConfig](./New-AzureVMConfig.md)


