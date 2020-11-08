---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/get-azeventhubclustersavailableregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubClustersAvailableRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubClustersAvailableRegion.md
ms.openlocfilehash: 712e9274eabe27bbe5f4a8acce704926e1e895fe
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94124637"
---
# <span data-ttu-id="5e25a-101">Get-AzEventHubClustersAvailableRegion</span><span class="sxs-lookup"><span data-stu-id="5e25a-101">Get-AzEventHubClustersAvailableRegion</span></span>

## <span data-ttu-id="5e25a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5e25a-102">SYNOPSIS</span></span>
<span data-ttu-id="5e25a-103">Obtém os detalhes do cluster do Eventhub único ou da lista de clusters no grupo de recursos especificado</span><span class="sxs-lookup"><span data-stu-id="5e25a-103">Gets the details of single Eventhub cluster or the list of clusters in the given Resource Group</span></span>

## <span data-ttu-id="5e25a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5e25a-104">SYNTAX</span></span>

```
Get-AzEventHubClustersAvailableRegion [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5e25a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5e25a-105">DESCRIPTION</span></span>
<span data-ttu-id="5e25a-106">A lista cmdlet Get-AzEventHubClustersAvailableRegion de regiões onde o Dedicated está disponível para criação.</span><span class="sxs-lookup"><span data-stu-id="5e25a-106">The Get-AzEventHubClustersAvailableRegion cmdlet list of regions where dedicated are available to create.</span></span>

## <span data-ttu-id="5e25a-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5e25a-107">EXAMPLES</span></span>

### <span data-ttu-id="5e25a-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="5e25a-108">Example 1</span></span>
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

<span data-ttu-id="5e25a-109">A lista de regiões é retornada onde</span><span class="sxs-lookup"><span data-stu-id="5e25a-109">List of regions is returned where</span></span>

## <span data-ttu-id="5e25a-110">OS</span><span class="sxs-lookup"><span data-stu-id="5e25a-110">PARAMETERS</span></span>

### <span data-ttu-id="5e25a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e25a-111">-DefaultProfile</span></span>
<span data-ttu-id="5e25a-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5e25a-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5e25a-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e25a-113">CommonParameters</span></span>
<span data-ttu-id="5e25a-114">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e25a-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e25a-115">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5e25a-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e25a-116">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5e25a-116">INPUTS</span></span>

### <span data-ttu-id="5e25a-117">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="5e25a-117">None</span></span>

## <span data-ttu-id="5e25a-118">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5e25a-118">OUTPUTS</span></span>

### <span data-ttu-id="5e25a-119">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. EventHub. Models. PSEventHubsAvailableCluster, Microsoft. Azure. PowerShell. cmdlets. EventHub, Version = 1.5.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="5e25a-119">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.EventHub.Models.PSEventHubsAvailableCluster, Microsoft.Azure.PowerShell.Cmdlets.EventHub, Version=1.5.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="5e25a-120">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5e25a-120">NOTES</span></span>

## <span data-ttu-id="5e25a-121">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5e25a-121">RELATED LINKS</span></span>
