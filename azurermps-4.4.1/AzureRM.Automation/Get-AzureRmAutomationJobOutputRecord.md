---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 38BB4F4E-B72B-460E-8DF2-2A7A9CACDB41
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationJobOutputRecord.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationJobOutputRecord.md
ms.openlocfilehash: d9ef76273d89f243f5a8d13543442aba16f7a9d9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431197"
---
# Get-AzureRmAutomationJobOutputRecord

## Sinopse
Obtém a saída completa de um registro de saída do trabalho de automação.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

```
Get-AzureRmAutomationJobOutputRecord [-JobId] <Guid> [-Id] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Get-AzureRmAutomationJobOutputRecord** Obtém a saída completa de um registro de saída do trabalho de automação.

Embora o cmdlet **Get-AzureRmAutomationJobOutput** liste um ou mais registros de saída de trabalho, ele retorna apenas um resumo, como uma cadeia de caracteres, do valor de qualquer registro de saída.
Ele não retorna o valor completo de um valor de saída de um registro de saída em seu tipo original.
Além disso, o resumo tem um comprimento máximo, que o valor total que este cmdlet gera pode exceder.
Ao contrário de **Get-AzureRmAutomationJobOutput** , esse cmdlet retorna o valor completo em seu tipo originalmente reemitida, para qualquer valor de saída de registro de saída.

## EXEMPLOS

### Exemplo 1: obter a saída completa de um trabalho de automação
```
PS C:\>Get-AzureRmAutomationJobOutput -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01" -Stream "Any" | Get-AzureRmAutomationJobOutputRecord
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

### Microsoft. Azure. Commands. Automation. Model. JobStreamRecord

## INFORMA

## LINKS RELACIONADOS

[Get-AzureRmAutomationJobOutput](./Get-AzureRMAutomationJobOutput.md)


