---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/powershell/module/az.eventhub/get-azeventhubclustersavailableregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubClustersAvailableRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubClustersAvailableRegion.md
ms.openlocfilehash: 633881b298059c35a54591bb1ff93d4e93a267d5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885725"
---
# <span data-ttu-id="f45cf-101">Get-AzEventHubClustersAvailableRegion</span><span class="sxs-lookup"><span data-stu-id="f45cf-101">Get-AzEventHubClustersAvailableRegion</span></span>

## <span data-ttu-id="f45cf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f45cf-102">SYNOPSIS</span></span>
<span data-ttu-id="f45cf-103">Obtém os detalhes do cluster Eventhub único ou a lista de clusters no determinado Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="f45cf-103">Gets the details of single Eventhub cluster or the list of clusters in the given Resource Group</span></span>

## <span data-ttu-id="f45cf-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="f45cf-104">SYNTAX</span></span>

```
Get-AzEventHubClustersAvailableRegion [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f45cf-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="f45cf-105">DESCRIPTION</span></span>
<span data-ttu-id="f45cf-106">A Get-AzEventHubClustersAvailableRegion de cmdlets de regiões onde dedicados estão disponíveis para criar.</span><span class="sxs-lookup"><span data-stu-id="f45cf-106">The Get-AzEventHubClustersAvailableRegion cmdlet list of regions where dedicated are available to create.</span></span>

## <span data-ttu-id="f45cf-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f45cf-107">EXAMPLES</span></span>

### <span data-ttu-id="f45cf-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f45cf-108">Example 1</span></span>
```powershell
PS C:\> Get-AzEventHubClustersAvailableRegion

Location
--------
northcentralus
westeurope
uksouth
westcentralus
australiasoutheast
ukwest
brazilsouth
centralus
australiaeast
eastus
southcentralus
japaneast
northeurope
eastus2
southeastasia
eastasia
westus
westus2
```

<span data-ttu-id="f45cf-109">Lista de regiões é retornada onde</span><span class="sxs-lookup"><span data-stu-id="f45cf-109">List of regions is returned where</span></span>

## <span data-ttu-id="f45cf-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="f45cf-110">PARAMETERS</span></span>

### <span data-ttu-id="f45cf-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f45cf-111">-DefaultProfile</span></span>
<span data-ttu-id="f45cf-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f45cf-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f45cf-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f45cf-113">CommonParameters</span></span>
<span data-ttu-id="f45cf-114">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f45cf-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f45cf-115">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f45cf-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f45cf-116">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f45cf-116">INPUTS</span></span>

### <span data-ttu-id="f45cf-117">Nenhum</span><span class="sxs-lookup"><span data-stu-id="f45cf-117">None</span></span>

## <span data-ttu-id="f45cf-118">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="f45cf-118">OUTPUTS</span></span>

### <span data-ttu-id="f45cf-119">System.Collections.Generic.IEnumerable'1[[Microsoft.Azure.Commands.EventHub.Models.PSEventHubsAvailableCluster, Microsoft.Azure.PowerShell.Cmdlets.EventHub, Version=1.5.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="f45cf-119">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.EventHub.Models.PSEventHubsAvailableCluster, Microsoft.Azure.PowerShell.Cmdlets.EventHub, Version=1.5.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="f45cf-120">NOTES</span><span class="sxs-lookup"><span data-stu-id="f45cf-120">NOTES</span></span>

## <span data-ttu-id="f45cf-121">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f45cf-121">RELATED LINKS</span></span>
