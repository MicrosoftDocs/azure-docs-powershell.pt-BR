---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 2EA28B90-4BAE-45DF-BD2E-60C74F53FB7B
online version: https://docs.microsoft.com/powershell/module/az.logicapp/get-azlogicapprunaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppRunAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppRunAction.md
ms.openlocfilehash: 6835fb2ce58e834e9270af293fdc4f0d07fc01aa
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892773"
---
# Get-AzLogicAppRunAction

## SYNOPSIS

Obtém uma ação de um aplicativo lógico executado.

## SINTAXE

```powershell
Get-AzLogicAppRunAction -ResourceGroupName <String> -Name <String> -RunName <String> [-ActionName <String>]
 [-FollowNextPageLink] [-MaximumFollowNextPageLink <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## DESCRIPTION

O cmdlet **Get-AzLogicAppRunAction** obtém uma ação de um aplicativo lógico executado.
Este cmdlet retorna um **objeto WorkflowRunAction.**
Especifique o aplicativo lógico, o grupo de recursos e execute.
Este módulo dá suporte a parâmetros dinâmicos.
Para usar um parâmetro dinâmico, digite-o no comando.
Para descobrir os nomes dos parâmetros dinâmicos, digite um hífen (-) após o nome do cmdlet e pressione a tecla Tab repetidamente para passar pelos parâmetros disponíveis.
Se você omitir um parâmetro de modelo necessário, o cmdlet solicitará o valor.

## EXEMPLOS

### Exemplo 1: Obter uma ação de um Aplicativo Lógico executado

```powershell
PS C:\>Get-AzLogicAppRunAction -ResourceGroupName "ResourceGroup11" -Name "LogicApp05" -RunName "08585925184423369718380498702CU26" -ActionName "LogicAppAction01"
Code        : NotFound
EndTime     : 1/13/2016 2:42:56 PM
Error       : 
InputsLink  : Microsoft.Azure.Management.Logic.Models.ContentLink
Name        : LogicAppAction01
OutputsLink : Microsoft.Azure.Management.Logic.Models.ContentLink
StartTime   : 1/13/2016 2:42:55 PM
Status      : Failed
TrackingId  : 
Type        :
```

Este comando obtém uma ação específica do Aplicativo Lógico do aplicativo lógico chamado LogicApp05 para a executar com o identificador 08585925184423369718380498702CU26.

### Exemplo 2: Executar todas as ações de um Aplicativo Lógico

```powershell
PS C:\>Get-AzLogicAppRunAction -ResourceGroupName "ResourceGroup11" -Name "LogicApp05" -RunName "08585925184423369718380498702CU26" -FollowNextPageLink
```

Este comando obtém todas as ações do Aplicativo Lógico de uma executar com o identificador 0858592518442369718380498702CU26 de um aplicativo lógico chamado LogicApp05.

## PARÂMETROS

### -ActionName

Especifica o nome de uma ação em um aplicativo lógico executado.
Este cmdlet obtém a ação especificada por esse parâmetro.

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

Especifica o nome de um aplicativo lógico para o qual este cmdlet obtém uma ação.

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

Especifica o nome de um grupo de recursos no qual este cmdlet obtém uma ação.

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

### -RunName

Especifica o nome de uma executar um aplicativo lógico.
Este cmdlet obtém uma ação para a executar que este parâmetro especifica.

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

### Microsoft.Azure.Management.Logic.Models.WorkflowRunAction

## NOTES

## LINKS RELACIONADOS

[Get-AzLogicAppRunHistory](./Get-AzLogicAppRunHistory.md)

[Stop-AzLogicAppRun](./Stop-AzLogicAppRun.md)
