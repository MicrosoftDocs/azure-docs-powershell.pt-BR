---
external help file: Microsoft.Azure.Commands.AnalysisServices.Dataplane.dll-Help.xml
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.analysisservices/export-azureanalysisservicesinstancelog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices.Dataplane/help/Export-AzureAnalysisServicesInstanceLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices.Dataplane/help/Export-AzureAnalysisServicesInstanceLog.md
ms.openlocfilehash: e93e38ef2914635cab61bf225c0d905d011ae643
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428225"
---
# Export-AzureAnalysisServicesInstance

## Sinopse
Exporta um log de uma instância do servidor do Analysis Services no ambiente atualmente conectado, conforme especificado no comando Add-AzureAnalysisServicesAccount

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

```
Export-AzureAnalysisServicesInstanceLog [-Instance] <String> [-OutputPath] <String> [-WhatIf] [-Force]
```

## DESCRITIVO
O cmdlet Export-AzureAnalysisServicesInstance exporta o log de uma instância do servidor do Azure Analysis Services para o arquivo

## EXEMPLOS

### Exemplo 1
```
PS C:\>Export-AzureAnalysisServicesInstanceLog -Instance testserver -OuptutPath C:\path\to\log\testserver.log
```

Esse comando irá exportar o log do servidor ' TestServer ' no ambiente especificado no comando Add-AzureAnalysisServicesAccount e salvá-lo no arquivo especificado no OutputPath ' C:\path\to\log\testserver.log '

## OS

### -Instance
Nome da instância do servidor do Analysis Services

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OutputPath
Caminho de saída do log de arquivo para exportação

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
Substituir arquivo se existir sem perguntar

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## SENSORES

### Nenhuma
Esse cmdlet não aceita nenhuma entrada.

## EXIBE

## INFORMA
Alias: Export-AzureAsInstanceLog

## LINKS RELACIONADOS

