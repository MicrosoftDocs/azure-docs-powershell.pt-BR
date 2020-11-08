---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkvirtualappliancesku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkVirtualApplianceSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkVirtualApplianceSku.md
ms.openlocfilehash: e38e489207267faf53bb790aaab65ad60c74c8b5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94111089"
---
# <span data-ttu-id="07098-101">Get-AzNetworkVirtualApplianceSku</span><span class="sxs-lookup"><span data-stu-id="07098-101">Get-AzNetworkVirtualApplianceSku</span></span>

## <span data-ttu-id="07098-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="07098-102">SYNOPSIS</span></span>
<span data-ttu-id="07098-103">Obtenha ou liste as SKUs do aplicativo virtual de rede disponível no inventário.</span><span class="sxs-lookup"><span data-stu-id="07098-103">Get or List available Network Virtual Appliance Skus in the inventory.</span></span>

## <span data-ttu-id="07098-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="07098-104">SYNTAX</span></span>

```
Get-AzNetworkVirtualApplianceSku [-SkuName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="07098-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="07098-105">DESCRIPTION</span></span>
<span data-ttu-id="07098-106">O Get-AzNetworkVirtualApplianceSku Obtém ou lista as SKUs do aplicativo virtual de rede disponível no inventário do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="07098-106">The Get-AzNetworkVirtualApplianceSku gets or lists available Network Virtual Appliance Skus in the Microsoft Azure inventory.</span></span>

## <span data-ttu-id="07098-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="07098-107">EXAMPLES</span></span>

### <span data-ttu-id="07098-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="07098-108">Example 1</span></span>
```powershell
PS C:\> Get-AzNetworkVirtualApplianceSku -SkuName barracudasdwanrelease                                                                                                                        

Vendor              : barracudasdwanrelease
AvailableVersions   : {8.1.0038301, latest}
AvailableScaleUnits : {Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualApplianceSkuInstances, Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualApplianceSkuInstances}
Name                : barracudasdwanrelease
Etag                : 00000000-0000-0000-0000-000000000000
Id                  :
```

<span data-ttu-id="07098-109">Obter uma SKU por nome.</span><span class="sxs-lookup"><span data-stu-id="07098-109">Get a sku by name.</span></span>

### <span data-ttu-id="07098-110">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="07098-110">Example 2</span></span>
```powershell
PS C:\> Get-AzNetworkVirtualApplianceSku                                                                                                                                                       

Vendor              : barracuda sdwan nightly
AvailableVersions   : {latest}
AvailableScaleUnits : {Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualApplianceSkuInstances}
Name                : barracuda sdwan nightly
Etag                : 00000000-0000-0000-0000-000000000000
Id                  :

Vendor              : barracuda sdwan
AvailableVersions   : {latest}
AvailableScaleUnits : {Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualApplianceSkuInstances}
Name                : barracuda sdwan
Etag                : 00000000-0000-0000-0000-000000000000
Id                  :

Vendor              : barracudasdwanrelease
AvailableVersions   : {8.1.0038301, latest}
AvailableScaleUnits : {Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualApplianceSkuInstances, Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualApplianceSkuInstances}
Name                : barracudasdwanrelease
Etag                : 00000000-0000-0000-0000-000000000000
Id                  :
```

<span data-ttu-id="07098-111">Listar todas as SKUs disponíveis do aplicativo virtual de rede.</span><span class="sxs-lookup"><span data-stu-id="07098-111">List all available Skus of Network Virtual Appliance.</span></span>

## <span data-ttu-id="07098-112">OS</span><span class="sxs-lookup"><span data-stu-id="07098-112">PARAMETERS</span></span>

### <span data-ttu-id="07098-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07098-113">-DefaultProfile</span></span>
<span data-ttu-id="07098-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="07098-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="07098-115">-SkuName</span><span class="sxs-lookup"><span data-stu-id="07098-115">-SkuName</span></span>
<span data-ttu-id="07098-116">O nome do SKU.</span><span class="sxs-lookup"><span data-stu-id="07098-116">The Sku name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07098-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07098-117">CommonParameters</span></span>
<span data-ttu-id="07098-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07098-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07098-119">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="07098-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07098-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="07098-120">INPUTS</span></span>

### <span data-ttu-id="07098-121">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="07098-121">None</span></span>

## <span data-ttu-id="07098-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="07098-122">OUTPUTS</span></span>

### <span data-ttu-id="07098-123">Microsoft. Azure. Commands. Network. Models. PSNetworkVirtualApplianceSku</span><span class="sxs-lookup"><span data-stu-id="07098-123">Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualApplianceSku</span></span>

## <span data-ttu-id="07098-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="07098-124">NOTES</span></span>

## <span data-ttu-id="07098-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="07098-125">RELATED LINKS</span></span>
