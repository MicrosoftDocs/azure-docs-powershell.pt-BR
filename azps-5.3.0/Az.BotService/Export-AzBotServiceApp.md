---
external help file: ''
Module Name: Az.BotService
online version: https://docs.microsoft.com/en-us/powershell/module/az.botservice/export-azbotserviceapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Export-AzBotServiceApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Export-AzBotServiceApp.md
ms.openlocfilehash: dd922730f03b715924a69219c0b1f1ccb11534de
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98434460"
---
# Export-AzBotServiceApp

## Sinopse
Retorna um BotService especificado pelos parâmetros.

## SYNTAX

```
Export-AzBotServiceApp [-Name <String>] [-ResourceGroupName <String>] [-SavePath <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## DESCRITIVO
Retorna um BotService especificado pelos parâmetros.

## EXEMPLOS

### Exemplo 1: baixar a pasta de aplicativos BotService
```powershell
PS C:\> Export-AzBotServiceApp -ResourceGroupName youriBotTest -name youriechobottest

Parameter $SavePath not provided, defaulting to current working directory.

    Directory: D:\powershell\BotService\azure-powershell\src\BotService

Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
d----          2020/12/15    13:45                youriechobottest
```

Baixar a pasta de aplicativos BotService

## OS

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Nome
O nome do recurso bot.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: BotName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
O nome do grupo de recursos de bot na assinatura do usuário.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SavePath


```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubscriptionId
ID da assinatura do Azure.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## SENSORES

## EXIBE

### Microsoft. Azure. PowerShell. cmdlets. BotService. Models. Api20180712. IBot

## INFORMA

ALIASES

## LINKS RELACIONADOS

