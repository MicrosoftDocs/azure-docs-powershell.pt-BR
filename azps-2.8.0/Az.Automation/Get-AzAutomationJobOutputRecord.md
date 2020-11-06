---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 38BB4F4E-B72B-460E-8DF2-2A7A9CACDB41
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationjoboutputrecord
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationJobOutputRecord.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationJobOutputRecord.md
ms.openlocfilehash: f5c6976ca1fa398c38f642cef757f0e7956f40c1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93597843"
---
# Get-AzAutomationJobOutputRecord

## Sinopse
Obtém a saída completa de um registro de saída do trabalho de automação.

## SYNTAX

```
Get-AzAutomationJobOutputRecord [-JobId] <Guid> [-Id] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Get-AzAutomationJobOutputRecord** Obtém a saída completa de um registro de saída do trabalho de automação.
Embora o cmdlet **Get-AzAutomationJobOutput** liste um ou mais registros de saída de trabalho, ele retorna apenas um resumo, como uma cadeia de caracteres, do valor de qualquer registro de saída.
Ele não retorna o valor completo de um valor de saída de um registro de saída em seu tipo original.
Além disso, o resumo tem um comprimento máximo, que o valor total que este cmdlet gera pode exceder.
Ao contrário de **Get-AzAutomationJobOutput** , esse cmdlet retorna o valor completo em seu tipo originalmente reemitida, para qualquer valor de saída de registro de saída.

## EXEMPLOS

### Exemplo 1: obter a saída completa de um trabalho de automação
```
PS C:\>Get-AzAutomationJobOutput -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01" -Stream "Any" | Get-AzAutomationJobOutputRecord
```

Esse comando obtém a saída completa do trabalho que tem a ID do trabalho especificada.

## OS

### -AutomationAccountName
Especifica o nome de uma conta de automação para a qual esse cmdlet obtém um registro de saída de trabalho.

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
Especifica a ID de um registro de saída de trabalho para esse cmdlet ser recuperado.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StreamRecordId

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -JobId
Especifica a ID de um trabalho para o qual esse cmdlet obtém um registro de saída.

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Especifica o nome de um grupo de recursos para o qual esse cmdlet obtém um registro de saída de trabalho.

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
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### System. GUID

### System. String

## EXIBE

### Microsoft. Azure. Commands. Automation. Model. JobStreamRecord

## INFORMA

## LINKS RELACIONADOS

[Get-AzAutomationJobOutput](./Get-AzAutomationJobOutput.md)


