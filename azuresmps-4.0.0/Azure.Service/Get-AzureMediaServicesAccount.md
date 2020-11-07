---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: A1327796-0CDC-43E0-97A6-FD1BF570066F
online version: ''
schema: 2.0.0
ms.openlocfilehash: c8676fbf957ebe96f0e849eedd3f64aca19a7741
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946335"
---
# Get-AzureMediaServicesAccount

## Sinopse
Obtém as contas dos serviços de mídia do Azure disponíveis.

**Observação:** Esta versão foi preterida, confira a [versão mais recente](https://docs.microsoft.com/powershell/module/azurerm.media/?view=azurermps-5.4.0#media_services).

## SYNTAX

```
Get-AzureMediaServicesAccount [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## DESCRITIVO
Este tópico descreve o cmdlet na versão 0.8.10 do módulo do Microsoft Azure PowerShell.
Para obter a versão do módulo que você está usando, no console do PowerShell do Azure, digite `(Get-Module -Name Azure).Version` .

Para listar todas as contas, use o `Get-AzureMediaServicesAccount` cmdlet.
Para obter informações mais detalhadas sobre uma conta específica, use o `Get-AzureMediaServicesAccount -Name YourAccountName` cmdlet.

## EXEMPLOS

### Exemplo 1: listar todas as contas de serviços de mídia
```
PS C:\> Get-AzureMediaServicesAccount
```

Esse comando lista todas as contas de serviços de mídia disponíveis.

### Exemplo 2: obter informações detalhadas sobre uma conta de serviços de mídia
```
PS C:\> Get-AzureMediaServicesAccount -Name accountname
```

Esse comando exibe as propriedades de uma conta de serviços de mídia.

## OS

### -Nome
O nome da conta dos serviços de mídia.

```yaml
Type: String
Parameter Sets: (All)
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

[Como usar o Azure PowerShell para serviços de mídia](https://go.microsoft.com/fwlink/?LinkId=324179)


