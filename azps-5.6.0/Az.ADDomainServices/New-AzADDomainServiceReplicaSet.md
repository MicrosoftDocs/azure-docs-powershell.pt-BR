---
external help file: ''
Module Name: Az.ADDomainServices
online version: https://docs.microsoft.com/powershell/module/az.ADDomainServices/new-AzADDomainServiceReplicaSet
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ADDomainServices/help/New-AzADDomainServiceReplicaSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ADDomainServices/help/New-AzADDomainServiceReplicaSet.md
ms.openlocfilehash: ad11cbe364cd4d9cd8a667fd40a6a1d438f1aed4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889709"
---
# <span data-ttu-id="737a8-101">New-AzADDomainServiceReplicaSet</span><span class="sxs-lookup"><span data-stu-id="737a8-101">New-AzADDomainServiceReplicaSet</span></span>

## <span data-ttu-id="737a8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="737a8-102">SYNOPSIS</span></span>
<span data-ttu-id="737a8-103">Criar um objeto na memória para ReplicaSet</span><span class="sxs-lookup"><span data-stu-id="737a8-103">Create a in-memory object for ReplicaSet</span></span>

## <span data-ttu-id="737a8-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="737a8-104">SYNTAX</span></span>

```
New-AzADDomainServiceReplicaSet [-Location <String>] [-SubnetId <String>] [<CommonParameters>]
```

## <span data-ttu-id="737a8-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="737a8-105">DESCRIPTION</span></span>
<span data-ttu-id="737a8-106">Criar um objeto na memória para ReplicaSet</span><span class="sxs-lookup"><span data-stu-id="737a8-106">Create a in-memory object for ReplicaSet</span></span>

## <span data-ttu-id="737a8-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="737a8-107">EXAMPLES</span></span>

### <span data-ttu-id="737a8-108">Exemplo 1: Criar ReplicaSet para AdDomain</span><span class="sxs-lookup"><span data-stu-id="737a8-108">Example 1: Create ReplicaSet for AdDomain</span></span>
```powershell
PS C:\> New-AzADDomainServiceReplicaSet -Location eastus -SubnetId /subscriptions/**********-****-****-****-****-**********/resourceGroups/youriADDomain-rg-test/providers/Microsoft.Network/virtualNetworks/yourinttest/subnets/default

DomainControllerIPAddress ExternalAccessIPAddress HealthLastEvaluated Location ServiceStatus SubnetId
------------------------- ----------------------- ------------------- -------- ------------- --------
                                                                      eastus                 /subscriptions/****
                                                                      ****-****-****-****-**********/resourceGroups/youriADDomain-rg-test/providers/M…
```

<span data-ttu-id="737a8-109">Criar ReplicaSet para AdDomain</span><span class="sxs-lookup"><span data-stu-id="737a8-109">Create ReplicaSet for AdDomain</span></span>

## <span data-ttu-id="737a8-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="737a8-110">PARAMETERS</span></span>

### <span data-ttu-id="737a8-111">-Location</span><span class="sxs-lookup"><span data-stu-id="737a8-111">-Location</span></span>
<span data-ttu-id="737a8-112">Local da rede virtual.</span><span class="sxs-lookup"><span data-stu-id="737a8-112">Virtual network location.</span></span>

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

### <span data-ttu-id="737a8-113">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="737a8-113">-SubnetId</span></span>
<span data-ttu-id="737a8-114">O nome da rede virtual na quais os Serviços de Domínio serão implantados.</span><span class="sxs-lookup"><span data-stu-id="737a8-114">The name of the virtual network that Domain Services will be deployed on.</span></span>
<span data-ttu-id="737a8-115">A id da sub-rede em que os Serviços de Domínio serão implantados.</span><span class="sxs-lookup"><span data-stu-id="737a8-115">The id of the subnet that Domain Services will be deployed on.</span></span>
<span data-ttu-id="737a8-116">/virtualNetwork/vnetName/subnets/subnetName.</span><span class="sxs-lookup"><span data-stu-id="737a8-116">/virtualNetwork/vnetName/subnets/subnetName.</span></span>

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

### <span data-ttu-id="737a8-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="737a8-117">CommonParameters</span></span>
<span data-ttu-id="737a8-118">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="737a8-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="737a8-119">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="737a8-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="737a8-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="737a8-120">INPUTS</span></span>

## <span data-ttu-id="737a8-121">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="737a8-121">OUTPUTS</span></span>

### <span data-ttu-id="737a8-122">Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.Api202001.ReplicaSet</span><span class="sxs-lookup"><span data-stu-id="737a8-122">Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.Api202001.ReplicaSet</span></span>

## <span data-ttu-id="737a8-123">NOTES</span><span class="sxs-lookup"><span data-stu-id="737a8-123">NOTES</span></span>

<span data-ttu-id="737a8-124">ALIASES</span><span class="sxs-lookup"><span data-stu-id="737a8-124">ALIASES</span></span>

## <span data-ttu-id="737a8-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="737a8-125">RELATED LINKS</span></span>

