---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 453AEA42-E29C-4FF2-9210-0DD88B77DC07
online version: ''
schema: 2.0.0
ms.openlocfilehash: 29c7f8bc814ddf5295064d89eeaf34c8e7274916
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946508"
---
# Get-WAPackCloudVMRoleSizeProfile

## Sinopse
Obtém objetos de perfil do tamanho da função MV da nuvem.

## SYNTAX

### Vazio (padrão)
```
Get-WAPackCloudVMRoleSizeProfile [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### FromName
```
Get-WAPackCloudVMRoleSizeProfile [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Get-WAPackCloudVMRoleSizeProfile** obtém objetos de perfil do tamanho da função MV da nuvem para máquinas virtuais.

## EXEMPLOS

### Exemplo 1: obter um perfil de tamanho de função VM de nuvem usando um nome
```
PS C:\> Get-WAPackCloudVMRoleSizeProfile -Name "Small"
```

Esse comando obtém o perfil de tamanho chamado Small.

### Exemplo 2: obter todos os perfis de tamanho de função MV da nuvem
```
PS C:\> Get-WAPackCloudVMRoleSizeProfile
```

Esse comando obtém todos os perfis de tamanho.

## OS

### -Nome
Especifica o nome de um perfil de tamanho de função de VM na nuvem.

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


