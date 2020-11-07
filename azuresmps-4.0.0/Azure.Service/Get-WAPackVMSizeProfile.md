---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 48211644-1B92-443D-A992-BDF517D89341
online version: ''
schema: 2.0.0
ms.openlocfilehash: 49b4039e07cf9f393a85c9592598ad870586fd06
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/08/2020
ms.locfileid: "93947430"
---
# Get-WAPackVMSizeProfile

## Sinopse
Obtém objetos de perfil de tamanho.

## SYNTAX

### Vazio (padrão)
```
Get-WAPackVMSizeProfile [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### DEID
```
Get-WAPackVMSizeProfile [-ID <Guid>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### FromName
```
Get-WAPackVMSizeProfile [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## DESCRITIVO
Esses tópicos são preteridos e serão removidos no futuro.
Este tópico descreve o cmdlet na versão 0.8.1 do módulo do Microsoft Azure PowerShell.
Para descobrir a versão do módulo que você está usando, no console do PowerShell do Azure, digite `(Get-Module -Name Azure).Version` .

O cmdlet **Get-WAPackVMSizeProfile** tem o tamanho dos objetos de perfil para máquinas virtuais.

## EXEMPLOS

### Exemplo 1: obter um perfil de tamanho usando um nome
```
PS C:\> Get-WAPackVMSizeProfile -Name "ContosoSizeProfile07"
```

Esse comando obtém o perfil de tamanho chamado ContosoSizeProfile07.

### Exemplo 2: obter um perfil de tamanho usando uma ID
```
PS C:\> Get-WAPackVMSizeProfile -ID 66242D17-189F-480D-87CF-8E1D749998C8
```

Esse comando obtém o perfil de tamanho que tem a ID especificada.

### Exemplo 3: obter todos os perfis de tamanho
```
PS C:\> Get-WAPackVMSizeProfile
```

Esse comando obtém todos os perfis de tamanho.

## OS

### -ID
Especifica a ID exclusiva de um perfil de tamanho.

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
Especifica o nome de um perfil de tamanho.

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


