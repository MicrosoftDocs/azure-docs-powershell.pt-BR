---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 53BD6ED4-EA66-448B-8B18-F078C0738AF5
online version: ''
schema: 2.0.0
ms.openlocfilehash: 90f02a261dc804f46a7ef503879a8ce9f43fad35
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/08/2020
ms.locfileid: "93947400"
---
# New-WAPackQuickVM

## Sinopse
Cria uma máquina virtual com base em um modelo.

## SYNTAX

```
New-WAPackQuickVM -Name <String> -Template <VMTemplate> -VMCredential <PSCredential>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## DESCRITIVO
Esses tópicos são preteridos e serão removidos no futuro.
Este tópico descreve o cmdlet na versão 0.8.1 do módulo do Microsoft Azure PowerShell.
Para descobrir a versão do módulo que você está usando, no console do PowerShell do Azure, digite `(Get-Module -Name Azure).Version` .

O cmdlet **New-WAPackQuickVM** cria uma máquina virtual com base em um modelo.

## EXEMPLOS

### Exemplo 1: criar uma máquina virtual com base em um modelo
```
PS C:\> $Credentials = Get-Credential
PS C:\> $TemplateId = Get-WAPackVMTemplate -Id 66242D17-189F-480D-87CF-8E1D749998C8
PS C:\> New-WAPackQuickVM -Name "VirtualMachine023" -Template $TemplateId -VMCredential $Credentials
```

O primeiro comando cria um objeto **PSCredential** e, em seguida, armazena-o na variável $Credentials.
O cmdlet solicita uma conta e uma senha.
Para obter mais informações, digite `Get-Help Get-Credential` .

O segundo comando obtém um modelo usando o cmdlet **Get-WAPackVMTemplate** .
O comando especifica a ID de um modelo.
O comando armazena o objeto de modelo na variável $TemplateID.

O comando final cria uma máquina virtual chamada VirtualMachine023.
O comando baseia a máquina virtual no modelo armazenado em $TemplateId.

## OS

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
Para obter um objeto de modelo, use o cmdlet **Get-WAPackVMTemplate** .

```yaml
Type: VMTemplate
Parameter Sets: (All)
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
Parameter Sets: (All)
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

[New-WAPackVM](./New-WAPackVM.md)

[Get-WAPackVMTemplate](./Get-WAPackVMTemplate.md)


