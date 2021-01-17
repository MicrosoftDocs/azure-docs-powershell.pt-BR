---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 35CE5C5F-F8D4-426F-A33A-4F9EA50E9B83
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/new-azstreamanalyticsinput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsInput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsInput.md
ms.openlocfilehash: 74145a6d65fdaa9634d7681133e10b2496b5f903
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98432915"
---
# New-AzStreamAnalyticsInput

## Sinopse
Cria ou atualiza uma entrada de trabalho.

## SYNTAX

```
New-AzStreamAnalyticsInput [-JobName] <String> [[-Name] <String>] [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **New-AzStreamAnalyticsInput** cria uma entrada em um trabalho do Stream Analytics ou atualiza uma entrada existente.
O nome da entrada pode ser especificado no arquivo JSON ou na linha de comando.
Se ambos forem especificados, o nome na linha de comando deve coincidir com o nome no arquivo.
Se você especificar uma entrada que já existe e não especificar o parâmetro *Force* , o cmdlet perguntará se deseja ou não substituir a entrada existente.
Se você especificar o parâmetro *Force* e especificar um nome de entrada existente, a entrada será substituída sem confirmação.

## EXEMPLOS

### Exemplo 1: criar uma entrada de trabalho com uma definição de um arquivo
```powershell
PS C:\>New-AzStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -File "C:\Input.json"
```

Esse comando cria uma entrada do arquivo Input.jsem.
Se uma entrada existente com o nome especificado no arquivo de definição de entrada já estiver definida, o cmdlet perguntará se deseja ou não substituí-la.

### Exemplo 2: criar uma entrada de trabalho
```powershell
PS C:\>New-AzStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -File "C:\Input.json" -Name "EntryStream"
```

Esse comando cria uma nova entrada no trabalho chamada EntryStream.
Se uma entrada existente com esse nome já estiver definida, o cmdlet perguntará se deseja ou não substituí-la.

### Exemplo 3: substituir uma entrada de trabalho por uma definição de um arquivo
```powershell
PS C:\>New-AzStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -File "C:\Input.json" -Name "EntryStream" -Force
```

Esse comando substitui a definição da fonte de entrada existente chamada EntryStream com a definição do arquivo sem confirmação.

## OS

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.

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

### -Arquivo
Especifica o caminho para um arquivo JSON que contém a representação JSON da entrada do Azure Stream Analytics a ser criada.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
Força o comando a ser executado sem pedir confirmação do usuário.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -JobName
Especifica o nome do trabalho do Azure Stream Analytics em que a entrada do Azure Stream Analytics deve ser criada.

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

### -Nome
Especifica o nome da entrada do Azure Stream Analytics a ser criada.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Especifica o nome do grupo de recursos sob o qual criar a entrada de fluxo do Azure.

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

### -Confirme
Solicita confirmação antes de executar o cmdlet.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Mostra o que aconteceria se o cmdlet fosse executado.
O cmdlet não é executado.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### System. String

## EXIBE

### Microsoft. Azure. Commands. StreamAnalytics. Models. PSInput

## INFORMA

## LINKS RELACIONADOS

[Get-AzStreamAnalyticsInput](./Get-AzStreamAnalyticsInput.md)

[Remove-AzStreamAnalyticsInput](./Remove-AzStreamAnalyticsInput.md)

[Test-AzStreamAnalyticsInput](./Test-AzStreamAnalyticsInput.md)


