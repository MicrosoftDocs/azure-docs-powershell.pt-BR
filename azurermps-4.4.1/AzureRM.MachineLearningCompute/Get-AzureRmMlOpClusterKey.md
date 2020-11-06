---
external help file: Microsoft.Azure.Commands.MachineLearningCompute.dll-Help.xml
Module Name: AzureRM.MachineLearningCompute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Get-AzureRmMlOpClusterKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Get-AzureRmMlOpClusterKey.md
ms.openlocfilehash: 4dfa855bba7318e85eb855e35227070a55d4ed73
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93433088"
---
# Get-AzureRmMlOpClusterKey

## Sinopse
Obtém as teclas de acesso associadas a um cluster de operação.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

### Obter chaves do cluster de operação de parâmetros de entrada de cmdlet.
```
Get-AzureRmMlOpClusterKey -ResourceGroupName <String> -Name <String>
```

### Obter as chaves do cluster de operação de uma definição de instância do OperationalizationCluster.
```
Get-AzureRmMlOpClusterKey -Cluster <PSOperationalizationCluster>
```

### Obter chaves do cluster de operação de um ID de recurso do Azure.
```
Get-AzureRmMlOpClusterKey -ResourceId <String>
```

## DESCRITIVO
As chaves para a conta de armazenamento, o registro de contêiner e outros serviços associados ao cluster de operação de funcionamento não são retornadas ao obter as propriedades do cluster. Uma chamada específica para recuperar as chaves deve ser feita, já que elas são informações confidenciais.

## EXEMPLOS

### Exemplo 1
```
PS C:\> Get-AzureRmMlOpClusterKey -ResourceGroupName my-group -Name my-cluster
```

Retorna as chaves secretas dos serviços associados ao cluster de operação.

## OS

### -InputObject
O objeto de cluster operacional.

```yaml
Type: PSOperationalizationCluster
Parameter Sets: Get operationalization cluster's keys from an OperationalizationCluster instance definition.
Aliases: Cluster

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Nome
O nome do cluster de operação.

```yaml
Type: String
Parameter Sets: Get operationalization cluster's keys from cmdlet input parameters.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
O nome do grupo de recursos para o cluster de operação.

```yaml
Type: String
Parameter Sets: Get operationalization cluster's keys from cmdlet input parameters.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
A ID de recurso do Azure para o cluster de operação.

```yaml
Type: String
Parameter Sets: Get operationalization cluster's keys from an Azure resouce id.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## SENSORES

### Microsoft. Azure. Commands. MachineLearningCompute. Models. PSOperationalizationCluster
System. String


## EXIBE

### Microsoft. Azure. Commands. MachineLearningCompute. Models. PSOperationalizationClusterCredentials


## INFORMA

## LINKS RELACIONADOS

