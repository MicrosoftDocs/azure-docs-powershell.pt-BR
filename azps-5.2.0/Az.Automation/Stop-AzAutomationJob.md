---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: BE1A9247-9F8E-45EA-9590-684A5A5662AC
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/stop-azautomationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Stop-AzAutomationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Stop-AzAutomationJob.md
ms.openlocfilehash: 451457cf4483d9af6d8a7aca8731b95dc5c95859
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98260209"
---
# Stop-AzAutomationJob

## Sinopse
Interrompe um trabalho de automação.

## SYNTAX

```
Stop-AzAutomationJob [-Id] <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Stop-AzAutomationJob** interrompe um trabalho de automação do Azure.
Especifique um trabalho de automação em execução.

## EXEMPLOS

### Exemplo 1: parar um trabalho
```
PS C:\>Stop-AzAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01"
```

Esse comando para o trabalho que tem a ID especificada.

## OS

### -AutomationAccountName
Especifica o nome de uma conta de automação na qual esse cmdlet interrompe um trabalho.

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

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure

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

### -ID
Especifica a ID de um trabalho que este cmdlet interrompe.

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases: JobId

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Especifica o nome de um grupo de recursos.

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

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### System. GUID

### System. String

## EXIBE

### System. void

## INFORMA

## LINKS RELACIONADOS

[Get-AzAutomationJob](./Get-AzAutomationJob.md)

[Get-AzAutomationJobOutput](./Get-AzAutomationJobOutput.md)

[Currículo-AzAutomationJob](./Resume-AzAutomationJob.md)

[Suspender-AzAutomationJob](./Suspend-AzAutomationJob.md)


