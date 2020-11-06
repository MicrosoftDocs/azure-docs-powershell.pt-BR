---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric/get-azurermservicefabriccluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Get-AzureRmServiceFabricCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Get-AzureRmServiceFabricCluster.md
ms.openlocfilehash: 5f034253326f551c5b1930f6cf90a80c83ed82f5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427437"
---
# Get-AzureRmServiceFabricCluster

## Sinopse
Obter os detalhes do recurso de cluster.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

### BySubscription (padrão)
```
Get-AzureRmServiceFabricCluster [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByResourceGroup
```
Get-AzureRmServiceFabricCluster [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ByName
```
Get-AzureRmServiceFabricCluster [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
O **Add-AzureRmServiceFabricCluster** receberá os detalhes do recurso de cluster.

## EXEMPLOS

### Exemplo 1
```
PS C:\> Get-AzureRmServiceFabricCluster -ResourceGroupName 'Group1' -ClusterName 'Contoso01SFCluster'
```

Esse comando receberá os detalhes do recurso de cluster do cluster ' mycluster '.

## OS

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Nome
Especifique o nome do cluster.

```yaml
Type: String
Parameter Sets: ByName
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Especifica o nome do grupo de recursos.

```yaml
Type: String
Parameter Sets: ByResourceGroup, ByName
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

### System. String

## EXIBE

### System. Collections. Generic. IList ' 1 [[Microsoft. Azure. Commands. createfabric. Models. PsCluster, Microsoft. Azure. Commands. Fabric, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]

## INFORMA

## LINKS RELACIONADOS

