---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 5307F1F1-E84C-4949-A557-99EF0012C3DF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmLogicAppTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmLogicAppTrigger.md
ms.openlocfilehash: 777c95375900662cd238e6f03f0929bcd645fb18
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427885"
---
# Get-AzureRmLogicAppTrigger

## Sinopse
Obtém os gatilhos de um aplicativo lógico.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

```
Get-AzureRmLogicAppTrigger -ResourceGroupName <String> -Name <String> [-TriggerName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Get-AzureRmLogicAppTrigger** Obtém gatilhos de um aplicativo lógico.
Esse cmdlet retorna um objeto **WorkflowTrigger** .
Especifique o fluxo de trabalho, o grupo de recursos e o gatilho.

Este módulo dá suporte a parâmetros dinâmicos.
Para usar um parâmetro dinâmico, digite-o no comando.
Para descobrir os nomes dos parâmetros dinâmicos, digite um hífen (-) após o nome do cmdlet e, em seguida, pressione a tecla TAB repetidamente para percorrer os parâmetros disponíveis.
Se você omitir um parâmetro de modelo obrigatório, o cmdlet solicitará que você tenha o valor.

## EXEMPLOS

### Exemplo 1: obter um gatilho de um aplicativo lógico
```
PS C:\>Get-AzureRmLogicAppTrigger -ResourceGroupName "ResourceGroup11" -Name "LogicApp05" -TriggerName "Trigger01"
ChangedTime         : 1/14/2016 11:45:07 AM
CreatedTime         : 1/13/2016 2:42:26 PM
LastExecutionTime   : 1/14/2016 11:45:07 AM
Name                : Trigger01
NextExecutionTime   : 1/14/2016 12:45:07 PM
RecurrenceFrequency : Minute
RecurrenceInterval  : 60
Status              : Waiting
Type                : Microsoft.Logic/workflows/triggers
LogicAppName        : LogicApp05
LogicAppVersion     : 08587489107406290826
```

Esse comando obtém o gatilho chamado Trigger01 do aplicativo lógico chamado LogicApp05.

### Exemplo 2: obter todos os gatilhos de um aplicativo lógico
```
PS C:\>Get-AzureRmLogicAppTrigger -ResourceGroupName "ResourceGroup11" -Name "LogicApp07"
ChangedTime         : 1/14/2016 11:45:07 AM
CreatedTime         : 1/13/2016 2:42:26 PM
LastExecutionTime   : 1/14/2016 11:45:07 AM
Name                : Trigger02
NextExecutionTime   : 1/14/2016 12:45:07 PM
RecurrenceFrequency : Minute
RecurrenceInterval  : 60
Status              : Waiting
Type                : Microsoft.Logic/workflows/triggers
LogicAppName        : LogicApp07
LogicAppVersion     : 08587489107406290826
```

Esse comando obtém os gatilhos do aplicativo lógico chamado LogicApp07.

## OS

### -Nome
Especifica o nome do aplicativo lógico do qual esse cmdlet recebe um gatilho.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Especifica o nome de um grupo de recursos em que esse cmdlet recebe um gatilho.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Triggername
Especifica o nome do gatilho que este cmdlet obtém.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

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

### Microsoft. Azure. Management. Logic. Models. WorkflowTrigger

## INFORMA

## LINKS RELACIONADOS

[Get-AzureRmLogicAppTriggerHistory](./Get-AzureRmLogicAppTriggerHistory.md)

[Start-AzureRmLogicApp](./Start-AzureRmLogicApp.md)


