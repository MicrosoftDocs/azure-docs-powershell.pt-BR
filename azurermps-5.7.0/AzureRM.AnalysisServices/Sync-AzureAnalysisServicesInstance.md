---
external help file: Microsoft.Azure.Commands.AnalysisServices.Dataplane.dll-Help.xml
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.analysisservices/sync-azureanalysisservicesinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices.Dataplane/help/Sync-AzureAnalysisServicesInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices.Dataplane/help/Sync-AzureAnalysisServicesInstance.md
ms.openlocfilehash: f3fb2377fd78db4b330afd39a8691f958597f07a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428221"
---
# Sync-AzureAnalysisServicesInstance

## Sinopse

Sincroniza um banco de dados especificado na instância especificada do servidor do Analysis Services para todas as instâncias de dimensionamento de consulta no ambiente atualmente conectado, conforme especificado no comando Add-AzureAnalysisServicesAccount

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

```
Sync-AzureAnalysisServicesInstance [-Instance] <String> [-Database] <String> [-Passthru]
```

## DESCRITIVO

O cmdlet Sync-AzureAnalysisServicesInstance sincroniza um banco de dados especificado na instância especificada do servidor do Analysis Services para todas as instâncias de dimensionamento de consulta no ambiente atualmente conectado, conforme especificado no comando Add-AzureAnalysisServicesAccount

## EXEMPLOS

### Exemplo 1

```
PS C:\>Sync-AzureAnalysisServicesInstance -Instance asazure://westus.asazure.windows.net/contoso -Database SalesOrders
```

Esse comando sincronizará o banco de dados chamado SalesOrders no servidor chamado ' contoso ' no ambiente westus.asazure.windows.net desde que o usuário tenha se conectado nesse ambiente usando Add-AzureAnalysisServicesAccount comando.

## OS

### -Instance

Nome da instância do servidor do Analysis Services para reiniciar

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

### -Banco de dados

Identidade do banco de dados a ser sincronizado

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

### -PassThru

Se o comando foi concluído, a especificação será retorna true se o comando foi bem-sucedido.

```yaml
Type: Switch
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

### System. Boolean

## INFORMA

Alias: Sync-AzureAsInstance

## LINKS RELACIONADOS
