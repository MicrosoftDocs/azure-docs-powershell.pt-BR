---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: D40BA2E2-50DF-4D51-A4D2-2D02AECBF20F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationdsccompilationjoboutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscCompilationJobOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscCompilationJobOutput.md
ms.openlocfilehash: a7ddc25fa7c6bc52acbe9369c569db060cf63a06
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426469"
---
# Get-AzureRmAutomationDscCompilationJobOutput

## Sinopse
Obtém os fluxos de log de um trabalho de compilação DSC de automação.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

```
Get-AzureRmAutomationDscCompilationJobOutput [-Id] <Guid> [-Stream <CompilationJobStreamType>]
 [-StartTime <DateTimeOffset>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Get-AzureRmAutomationDscCompilationJobOutput** Obtém os registros de fluxo de um trabalho de compilação DSC (configuração de estado desejado APS) na automação do Azure.

## EXEMPLOS

### Exemplo 1: obter os logs para um trabalho de compilação DSC
```
PS C:\>$Jobs = Get-AzureRmAutomationDscCompilationJob -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17"
PS C:\> $Jobs[0] | Get-AzureRmAutomationDscCompilationJobOutput -Stream "Any"
```

O primeiro comando obtém os trabalhos de compilação na conta de automação chamada Contoso17 usando o cmdlet Get-AzureRmAutomationDscCompilationJob.
O comando armazena esses objetos na variável $Jobs.
O segundo comando obtém a saída do trabalho de compilação para qualquer fluxo para o primeiro membro da matriz de $Jobs.

## OS

### -AutomationAccountName
Especifica o nome da conta de automação que contém o trabalho de compilação DSC.

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
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ID
Especifica a ID exclusiva do trabalho de compilação DSC para o qual esse cmdlet é apresentado.

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
Especifica o nome do grupo de recursos que contém o trabalho de compilação DSC para o qual esse cmdlet obtém registros de fluxo.

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
Esse cmdlet obtém registros de fluxo que o trabalho de compilação DSC gera após esse tempo.

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Stream
Especifica o tipo de fluxo para a saída obtida por esse cmdlet.
Os valores válidos são: 
- Qualquer 
- Avisa 
- Erros 
- Detalha

```yaml
Type: Microsoft.Azure.Commands.Automation.Common.CompilationJobStreamType
Parameter Sets: (All)
Aliases:
Accepted values: Warning, Error, Verbose, Any

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### System. GUID

### Microsoft. Azure. Commands. Automation. Common. CompilationJobStreamType

### System. Nullable ' 1 [[System. DateTimeOffset, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]

### System. String

## EXIBE

### Microsoft. Azure. Commands. Automation. Model. JobStream

## INFORMA

## LINKS RELACIONADOS

[Get-AzureRmAutomationDscCompilationJob](./Get-AzureRmAutomationDscCompilationJob.md)

[Start-AzureRmAutomationDscCompilationJob](./Start-AzureRmAutomationDscCompilationJob.md)


