---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: D704BAC0-D89E-4F15-ACF8-FA2C1F0D1B8F
online version: https://docs.microsoft.com/powershell/module/az.automation/get-azautomationdsccompilationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscCompilationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscCompilationJob.md
ms.openlocfilehash: 5157b4d4e1a291193f10fef22308002de210e748
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890672"
---
# Get-AzAutomationDscCompilationJob

## SYNOPSIS
Obtém trabalhos de compilação DSC em Automação.

## SINTAXE

### ByAll (Padrão)
```
Get-AzAutomationDscCompilationJob [-Status <String>] [-StartTime <DateTimeOffset>] [-EndTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ByJobId
```
Get-AzAutomationDscCompilationJob -Id <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByConfigurationName
```
Get-AzAutomationDscCompilationJob -ConfigurationName <String> [-Status <String>] [-StartTime <DateTimeOffset>]
 [-EndTime <DateTimeOffset>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRIPTION
O cmdlet **Get-AzAutomationDscCompilationJob** obtém trabalhos de compilação de Configuração de Estado Desejado (DSC) do APS no Azure Automation.

## EXEMPLOS

### Exemplo 1: Obter todos os trabalhos de compilação DSC
```
PS C:\>Get-AzAutomationDscCompilationJob -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17"
```

Este comando obtém todos os trabalhos de compilação na conta de automação chamada Contoso17.

### Exemplo 2: Obter trabalhos de compilação DSC para uma configuração
```
PS C:\>Get-AzAutomationDscCompilationJob -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -ConfigurationName "ContosoConfiguration"
```

Este comando obtém todos os trabalhos de compilação para a configuração DSC chamada ContosoConfiguration na conta de automação chamada Contoso17.

### Exemplo 3: Obter um trabalho de compilação DSC específico
```
PS C:\>Get-AzAutomationDscCompilationJob -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Id c0a1718e-d8be-4fa3-91b6-82e1d3a36298
```

Este comando obtém o trabalho de compilação com a ID especificada na conta de automação chamada Contoso17.

## PARÂMETROS

### -AutomationAccountName
Especifica o nome da conta de automação que contém trabalhos de compilação DSC que este cmdlet obtém.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ConfigurationName
Especifica o nome da configuração DSC para a qual este cmdlet obtém trabalhos de compilação.

```yaml
Type: System.String
Parameter Sets: ByConfigurationName
Aliases: Name

Required: True
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

### -EndTime
Especifica uma hora de término.
Este cmdlet obtém trabalhos de compilação iniciados até o momento especificado por esse parâmetro.

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: ByAll, ByConfigurationName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Id
Especifica a ID exclusiva do trabalho de compilação DSC que este cmdlet obtém.

```yaml
Type: System.Guid
Parameter Sets: ByJobId
Aliases: JobId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Especifica o nome de um grupo de recursos no qual este cmdlet obtém trabalhos de compilação de DSC.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StartTime
Especifica uma hora de início.
Este cmdlet obtém trabalhos que começam em ou após o tempo especificado por esse parâmetro.

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: ByAll, ByConfigurationName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Status
Especifica o status dos trabalhos que esse cmdlet obtém.
Os valores válidos são: 
- Concluído 
- Falha 
- En fila 
- Iniciando 
- Resumindo 
- Executando 
- Parado 
- Parando 
- Suspenso 
- Suspensão 
- Ativando
- Novo

```yaml
Type: System.String
Parameter Sets: ByAll, ByConfigurationName
Aliases:
Accepted values: Completed, Failed, Queued, Starting, Resuming, Running, Stopped, Stopping, Suspended, Suspending, Activating, New

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### System.Guid

### System.String

## SAÍDAS

### Microsoft.Azure.Commands.Automation.Model.CompilationJob

## NOTES

## LINKS RELACIONADOS

[Get-AzAutomationDscCompilationJobOutput](./Get-AzAutomationDscCompilationJobOutput.md)

[Start-AzAutomationDscCompilationJob](./Start-AzAutomationDscCompilationJob.md)


