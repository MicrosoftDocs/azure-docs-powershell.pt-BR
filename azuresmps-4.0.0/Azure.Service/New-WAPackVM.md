---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: AA7BD103-5C91-4E3B-9E46-2CAEDA5BA615
online version: ''
schema: 2.0.0
ms.openlocfilehash: d8f5643756cfad93399664298378e97264dedc2f
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/08/2020
ms.locfileid: "93947398"
---
# New-WAPackVM

## Sinopse
Cria uma máquina virtual.

## SYNTAX

### CreateVMFromTemplate (padrão)
```
New-WAPackVM -Name <String> -Template <VMTemplate> -VMCredential <PSCredential> [-VNet <VMNetwork>]
 [-ProductKey <String>] [-Windows] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### CreateLinuxVMFromTemplate
```
New-WAPackVM -Name <String> -Template <VMTemplate> -VMCredential <PSCredential> [-VNet <VMNetwork>] [-Linux]
 [-AdministratorSSHKey <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### CreateVMFromOSDisk
```
New-WAPackVM -Name <String> [-VNet <VMNetwork>] -OSDisk <VirtualHardDisk> -VMSizeProfile <HardwareProfile>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## DESCRITIVO
Esses tópicos são preteridos e serão removidos no futuro.
Este tópico descreve o cmdlet na versão 0.8.1 do módulo do Microsoft Azure PowerShell.
Para descobrir a versão do módulo que você está usando, no console do PowerShell do Azure, digite `(Get-Module -Name Azure).Version` .

O cmdlet **New-WAPackVM** cria uma máquina virtual.

## EXEMPLOS

### Exemplo 1: criar uma máquina virtual para o sistema operacional Windows usando um modelo
```
PS C:\> $Credentials = Get-Credential PS C:\> $Template = Get-WAPackVMTemplate -Name "ContosoTemplate04"PS C:\> New-WAPackVM -Name "ContosoV023" -Template $Template -VMCredential $Credentials -Windows
```

O primeiro comando cria um objeto **PSCredential** e, em seguida, armazena-o na variável $Credentials.
O cmdlet solicita uma conta e uma senha.
Para obter mais informações, digite `Get-Help Get-Credential` .

O segundo comando obtém o modelo de máquina virtual chamado ContosoTemplate04 usando o cmdlet **Get-WAPackVMTemplate** e, em seguida, armazena-o na variável $template.

O comando final cria uma máquina virtual chamada ContosoV023, com base no modelo armazenado na variável $Template.
O comando especifica o parâmetro *Windows* e, portanto, a máquina virtual deve executar uma versão do sistema operacional Windows.

### Exemplo 2: criar uma máquina virtual para o sistema operacional Linux usando um modelo
```
PS C:\> $Credentials = Get-Credential
PS C:\> $Template = Get-WAPackVMTemplate -Name "ContosoTemplate19"
PS C:\> New-WAPackVM -Linux -Name "ContosoV028" -Template $Template -VMCredential $Credentials
```

O primeiro comando cria um objeto **PSCredential** e, em seguida, armazena-o na variável $Credentials.

O segundo comando obtém o modelo de máquina virtual chamado ContosoTemplate19 usando o cmdlet **Get-WAPackVMTemplate** e, em seguida, armazena-o na variável $template.

O comando final cria uma máquina virtual chamada ContosoV028, com base no modelo armazenado na variável $Template.
O comando especifica o parâmetro *Linux* e, portanto, a máquina virtual deve executar uma versão do sistema operacional Linux.

### Exemplo 3: criar uma máquina virtual a partir de um disco de sistema operacional e dimensionar o perfil
```
PS C:\> $OSDisk = Get-WAPackVMOSDisk -Name "ContosoDiskOS"
PS C:\> $SizeProfile = Get-WAPackVMSizeProfile -Name "MediumSizeVM"
PS C:\> New-WAPackVM -Name "ContosoV073" -OSDisk $OSDisk -VMSizeProfile $SizeProfile
```

O primeiro comando obtém um disco do sistema operacional chamado ContosoDiskOS usando o cmdlet **Get-WAPackVMOSDisk** e, em seguida, armazena-o na variável $OSDisk.

O segundo comando obtém o perfil de tamanho chamado MediumSizeVM usando o cmdlet **Get-WAPackVMSizeProfile** e, em seguida, armazena-o na variável $SizeProfile.

O comando final cria uma máquina virtual nomeada ContosoV073 a partir do disco do sistema operacional armazenado no $OSDisk e o perfil de tamanho armazenado no $SizeProfile.

## OS

### -AdministratorSSHKey
Especifica a chave do Secure Shell (SSH) para a conta de administrador.

```yaml
Type: String
Parameter Sets: CreateLinuxVMFromTemplate
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Linux
Indica que o cmdlet cria uma máquina virtual para executar o sistema operacional Linux.

```yaml
Type: SwitchParameter
Parameter Sets: CreateLinuxVMFromTemplate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Nome
Especifica um nome para a máquina virtual.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -OSDisk
Especifica um disco do sistema operacional como um objeto **VirtualHardDisk** .
Para obter um disco do sistema operacional, use o cmdlet **Get-WAPackVMOSDisk** .

```yaml
Type: VirtualHardDisk
Parameter Sets: CreateVMFromOSDisk
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ProductKey
Especifica uma chave do produto (Product Key).
A chave do produto (Product Key) é um número de 25 dígitos que identifica a licença do produto.
Use uma chave do produto (Product Key) para um sistema operacional que você planeja instalar em uma máquina virtual ou host.

```yaml
Type: String
Parameter Sets: CreateVMFromTemplate
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### -Modelo
Especifica um modelo.
O cmdlet cria uma máquina virtual com base no modelo que você especificar.
Para obter um objeto de modelo, use o cmdlet Get-WAPackVMTemplate.

```yaml
Type: VMTemplate
Parameter Sets: CreateVMFromTemplate, CreateLinuxVMFromTemplate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VMCredential
Especifica a credencial para a conta de administrador local.
Para obter um objeto **PSCredential** , use o cmdlet **Get-Credential** .
Para obter mais informações, digite `Get-Help Get-Credential` .

```yaml
Type: PSCredential
Parameter Sets: CreateVMFromTemplate, CreateLinuxVMFromTemplate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VMSizeProfile
Especifica um perfil de tamanho para uma máquina virtual como um objeto **HardwareProfile** .
Para obter um perfil de tamanho, use o cmdlet **Get-WAPackVMSizeProfile** .

```yaml
Type: HardwareProfile
Parameter Sets: CreateVMFromOSDisk
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VNet
Especifica uma rede virtual.
O cmdlet conecta a máquina virtual à rede virtual que você especificar.
Para obter uma rede virtual, use o cmdlet **Get-WAPackVNet** .

```yaml
Type: VMNetwork
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Windows
Indica que o cmdlet cria uma máquina virtual para executar o sistema operacional do Windows.

```yaml
Type: SwitchParameter
Parameter Sets: CreateVMFromTemplate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

## EXIBE

## INFORMA

## LINKS RELACIONADOS

[Get-WAPackVM](./Get-WAPackVM.md)

[Remove-WAPackVM](./Remove-WAPackVM.md)

[Restart-WAPackVM](./Restart-WAPackVM.md)

[Currículo-WAPackVM](./Resume-WAPackVM.md)

[Set-WAPackVM](./Set-WAPackVM.md)

[Start-WAPackVM](./Start-WAPackVM.md)

[Parar-WAPackVM](./Stop-WAPackVM.md)

[Suspender-WAPackVM](./Suspend-WAPackVM.md)

[Get-WAPackVMSizeProfile](./Get-WAPackVMSizeProfile.md)

[Get-WAPackVMTemplate](./Get-WAPackVMTemplate.md)

[Get-WAPackVMOSDisk](./Get-WAPackVMOSDisk.md)


