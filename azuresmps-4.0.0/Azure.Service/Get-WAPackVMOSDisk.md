---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: E6E40D1B-A5BC-4B38-9D22-F06A8E4DABDF
online version: ''
schema: 2.0.0
ms.openlocfilehash: f1360f45b751088bd899282cee2e64ce965d11fb
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/08/2020
ms.locfileid: "93947352"
---
# Get-WAPackVMOSDisk

## Sinopse
Obtém objetos de disco do sistema operacional para máquinas virtuais.

## SYNTAX

### Vazio (padrão)
```
Get-WAPackVMOSDisk [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### DEID
```
Get-WAPackVMOSDisk [-ID <Guid>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### FromName
```
Get-WAPackVMOSDisk [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## DESCRITIVO
Esses tópicos são preteridos e serão removidos no futuro.
Este tópico descreve o cmdlet na versão 0.8.1 do módulo do Microsoft Azure PowerShell.
Para descobrir a versão do módulo que você está usando, no console do PowerShell do Azure, digite `(Get-Module -Name Azure).Version` .

O cmdlet **Get-WAPackVMOSDisk** obtém objetos de disco do sistema operacional para máquinas virtuais.

## EXEMPLOS

### Exemplo 1: obter um disco do sistema operacional usando um nome
```
PS C:\> Get-WAPackVMOSDisk -Name "ContosoOSDisk"
```

Esse comando obtém um disco do sistema operacional chamado ContosoOSDisk.

### Exemplo 2: obter um disco do sistema operacional usando uma ID
```
PS C:\> Get-WAPackVMOSDisk -Id 66242D17-189F-480D-87CF-8E1D749998C8
```

Esse comando obtém o disco do sistema operacional que tem a ID especificada.

### Exemplo 3: obter todos os discos do sistema operacional
```
PS C:\> Get-WAPackVMOSDisk
```

Este comando obtém todos os discos do sistema operacional.

## OS

### -ID
Especifica a ID exclusiva de um disco do sistema operacional.

```yaml
Type: Guid
Parameter Sets: FromId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Nome
Especifica o nome de um disco do sistema operacional.

```yaml
Type: String
Parameter Sets: FromName
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

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

## EXIBE

## INFORMA

## LINKS RELACIONADOS

[Get-WAPackVM](./Get-WAPackVM.md)


