---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: C1F6BBF9-0DB5-46FD-B8A8-9029B0AB6166
online version: https://docs.microsoft.com/powershell/module/az.logicapp/get-azlogicapptriggerhistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppTriggerHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppTriggerHistory.md
ms.openlocfilehash: 7c0d34ad56021e2fb4f74aef1bed41ca38c918c1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892762"
---
# Get-AzLogicAppTriggerHistory

## SYNOPSIS

Obtém o histórico de gatilhos em um aplicativo lógico.

## SINTAXE

```powershell
Get-AzLogicAppTriggerHistory -ResourceGroupName <String> -Name <String> -TriggerName <String>
 [-HistoryName <String>] [-FollowNextPageLink] [-MaximumFollowNextPageLink <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRIPTION

O cmdlet **Get-AzLogicAppTriggerHistory** obtém o histórico de gatilhos em um aplicativo lógico no recurso Aplicativos Lógicos.
Este cmdlet retorna um **objeto WorkflowTriggerHistory.**
Especifique o aplicativo lógico, o grupo de recursos e o gatilho.
Este módulo dá suporte a parâmetros dinâmicos.
Para usar um parâmetro dinâmico, digite-o no comando.
Para descobrir os nomes dos parâmetros dinâmicos, digite um hífen (-) após o nome do cmdlet e pressione a tecla Tab repetidamente para passar pelos parâmetros disponíveis.
Se você omitir um parâmetro de modelo necessário, o cmdlet solicitará o valor.

## EXEMPLOS

### Exemplo 1: obter um histórico de gatilho de um aplicativo lógico

```powershell
PS C:\>Get-AzLogicAppTriggerHistory -ResourceGroupName "Resourcegroup11" -Name "LogicApp03" -TriggerName "Trigger01" -HistoryName "08587489107387695768"
Code        : BadRequest
EndTime     : 1/13/2016 2:42:26 PM
Error       : {code, message}
Fired       : False
InputsLink  : https://flowprodcu02by01.blob.core.windows.net/flow3ea9ffd11c684c9f9f258b1a6ea5cb6020160113t000000zcontent/A7392_d1e831de68ac4ef89d19a40f05e663
              cb_httpTrigger:5Finputs:2Ejson?sv=2014-02-14&sr=b&sig=&se=2016-01-14T16%3A15%3A16Z&sp=r
Name        : 08587489107387695768
OutputsLink : 
Run         : 
StartTime   : 1/13/2016 2:42:26 PM
Status      : Failed
TrackingId  : f88a499b-f80f-4a28-9bbf-c4cc0d129700
Type        : Microsoft.Logic/workflows/triggers/histories
```

Este comando obtém um histórico de disparo de aplicativo lógico específico para um gatilho no aplicativo lógico chamado LogicApp03.

### Exemplo 2: Obter históricos de gatilho de um aplicativo lógico

```powershell
PS C:\>Get-AzLogicAppTriggerHistory -ResourceGroupName "ResourceGroup11" -Name "LogicApp07" -TriggerName "Trigger01"
Code        : BadRequest
EndTime     : 1/13/2016 2:43:33 PM
Error       : {code, message}
Fired       : False
InputsLink  : https://flowprodcu02by01.blob.core.windows.net/flow3ea9ffd11c684c9f9f258b1a6ea5cb6020160113t000000zcontent/CAB46_60e2ad0f0e1947e8b5798716914c5d
              b6_httpTrigger:5Finputs:2Ejson?sv=2014-02-14&sr=b&sig=&se=2016-01-14T16%3A18%3A27Z&sp=r
Name        : 08587489106716457817
OutputsLink : 
Run         : 
StartTime   : 1/13/2016 2:43:33 PM
Status      : Failed
TrackingId  : c91a63f1-48b4-4eae-91eb-8f6dbfa9fe06
Type        : Microsoft.Logic/workflows/triggers/histories

Code        : BadRequest
EndTime     : 1/13/2016 2:42:26 PM
Error       : {code, message}
Fired       : False
InputsLink  : https://flowprodcu02by01.blob.core.windows.net/flow3ea9ffd11c684c9f9f258b1a6ea5cb6020160113t000000zcontent/A7392_d1e831de68ac4ef89d19a40f05e663
              cb_httpTrigger:5Finputs:2Ejson?sv=2014-02-14&sr=b&sig=&se=2016-01-14T16%3A18%3A27Z&sp=r
Name        : 08587489107387695768
OutputsLink : 
Run         : 
StartTime   : 1/13/2016 2:42:26 PM
Status      : Failed
TrackingId  : f88a499b-f80f-4a28-9bbf-c4cc0d129700
Type        : Microsoft.Logic/workflows/triggers/histories
```

Este comando obtém os históricos de gatilho de fluxo de trabalho para um gatilho no aplicativo lógico chamado LogicApp07.

### Exemplo 3: obter todo o histórico de gatilho de um aplicativo lógico

```powershell
PS C:\>Get-AzLogicAppTriggerHistory -ResourceGroupName "ResourceGroup11" -Name "LogicApp08" -TriggerName "Trigger01" -FollowNextPageLink
```

Esse comando obtém todo o histórico de gatilho de fluxo de trabalho para um gatilho no aplicativo lógico chamado LogicApp08 seguindo o NextPageLink.

### Exemplo 4

```powershell
PS C:\>Get-AzLogicAppTriggerHistory -ResourceGroupName "ResourceGroup11" -Name "LogicApp08" -TriggerName "Trigger01" -FollowNextPageLink -MaximumFollowNextPageLink 1
```

Este comando obtém as duas primeiras páginas do histórico de gatilhos de fluxo de trabalho para um gatilho no aplicativo lógico chamado LogicApp09 seguindo o NextPageLink e limitando o tamanho do resultado a duas páginas.
Cada página contém trinta resultados.

## PARÂMETROS

### -DefaultProfile

As credenciais, conta, locatário e assinatura usadas para comunicação com o azure

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FollowNextPageLink

Indica que o cmdlet deve seguir os links da próxima página.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: FL

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -HistoryName

Especifica o nome do histórico que esse cmdlet obtém.

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

### -MaximumFollowNextPageLink

Especifica quantas vezes seguir os links da próxima página se FollowNextPageLink for usado.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: ML

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name

Especifica o nome do aplicativo lógico para o qual esse cmdlet obtém o histórico do gatilho.

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

Especifica o nome do grupo de recursos no qual este cmdlet obtém histórico.

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

### -TriggerName

Especifica o nome do gatilho para o qual este cmdlet obtém histórico.

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

### CommonParameters

Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### System.String

## SAÍDAS

### Microsoft.Azure.Management.Logic.Models.WorkflowTriggerHistory

## NOTES

## LINKS RELACIONADOS

[Get-AzLogicAppRunHistory](./Get-AzLogicAppRunHistory.md)

[Get-AzLogicAppTrigger](./Get-AzLogicAppTrigger.md)

[Start-AzLogicApp](./Start-AzLogicApp.md)
