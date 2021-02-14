---
external help file: ''
Module Name: Az.ADDomainServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.ADDomainServices/new-AzADDomainServiceReplicaSet
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ADDomainServices/help/New-AzADDomainServiceReplicaSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ADDomainServices/help/New-AzADDomainServiceReplicaSet.md
ms.openlocfilehash: f95c4148afa3f317914dabe968376e0e86913dcb
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100110865"
---
# <span data-ttu-id="a2cae-101">New-AzADDomainServiceReplicaSet</span><span class="sxs-lookup"><span data-stu-id="a2cae-101">New-AzADDomainServiceReplicaSet</span></span>

## <span data-ttu-id="a2cae-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a2cae-102">SYNOPSIS</span></span>
<span data-ttu-id="a2cae-103">Criar um objeto na memória para o ReplicaSet</span><span class="sxs-lookup"><span data-stu-id="a2cae-103">Create a in-memory object for ReplicaSet</span></span>

## <span data-ttu-id="a2cae-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a2cae-104">SYNTAX</span></span>

```
New-AzADDomainServiceReplicaSet [-Location <String>] [-SubnetId <String>] [<CommonParameters>]
```

## <span data-ttu-id="a2cae-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="a2cae-105">DESCRIPTION</span></span>
<span data-ttu-id="a2cae-106">Criar um objeto na memória para o ReplicaSet</span><span class="sxs-lookup"><span data-stu-id="a2cae-106">Create a in-memory object for ReplicaSet</span></span>

## <span data-ttu-id="a2cae-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="a2cae-107">EXAMPLES</span></span>

### <span data-ttu-id="a2cae-108">Exemplo 1: Criar ReplicaSet para AdDomain</span><span class="sxs-lookup"><span data-stu-id="a2cae-108">Example 1: Create ReplicaSet for AdDomain</span></span>
```powershell
PS C:\> New-AzADDomainServiceReplicaSet -Location eastus -SubnetId /subscriptions/**********-****-****-****-****-**********/resourceGroups/youriADDomain-rg-test/providers/Microsoft.Network/virtualNetworks/yourinttest/subnets/default

DomainControllerIPAddress ExternalAccessIPAddress HealthLastEvaluated Location ServiceStatus SubnetId
------------------------- ----------------------- ------------------- -------- ------------- --------
                                                                      eastus                 /subscriptions/****
                                                                      ****-****-****-****-**********/resourceGroups/youriADDomain-rg-test/providers/M…
```

<span data-ttu-id="a2cae-109">Criar ReplicaSet para AdDomain</span><span class="sxs-lookup"><span data-stu-id="a2cae-109">Create ReplicaSet for AdDomain</span></span>

## <span data-ttu-id="a2cae-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a2cae-110">PARAMETERS</span></span>

### <span data-ttu-id="a2cae-111">-Local</span><span class="sxs-lookup"><span data-stu-id="a2cae-111">-Location</span></span>
<span data-ttu-id="a2cae-112">Local de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="a2cae-112">Virtual network location.</span></span>

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

### <span data-ttu-id="a2cae-113">-Sub-RedeId</span><span class="sxs-lookup"><span data-stu-id="a2cae-113">-SubnetId</span></span>
<span data-ttu-id="a2cae-114">O nome da rede virtual na quais os Serviços de Domínio serão implantados.</span><span class="sxs-lookup"><span data-stu-id="a2cae-114">The name of the virtual network that Domain Services will be deployed on.</span></span>
<span data-ttu-id="a2cae-115">A id da sub-rede na quais os Serviços de Domínio serão implantados.</span><span class="sxs-lookup"><span data-stu-id="a2cae-115">The id of the subnet that Domain Services will be deployed on.</span></span>
<span data-ttu-id="a2cae-116">/virtualNetwork/vnetName/subnets/subnetName.</span><span class="sxs-lookup"><span data-stu-id="a2cae-116">/virtualNetwork/vnetName/subnets/subnetName.</span></span>

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

### <span data-ttu-id="a2cae-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2cae-117">CommonParameters</span></span>
<span data-ttu-id="a2cae-118">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a2cae-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2cae-119">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a2cae-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2cae-120">Entradas</span><span class="sxs-lookup"><span data-stu-id="a2cae-120">INPUTS</span></span>

## <span data-ttu-id="a2cae-121">Saídas</span><span class="sxs-lookup"><span data-stu-id="a2cae-121">OUTPUTS</span></span>

### <span data-ttu-id="a2cae-122">Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.Api202001.ReplicaSet</span><span class="sxs-lookup"><span data-stu-id="a2cae-122">Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.Api202001.ReplicaSet</span></span>

## <span data-ttu-id="a2cae-123">Notas</span><span class="sxs-lookup"><span data-stu-id="a2cae-123">NOTES</span></span>

<span data-ttu-id="a2cae-124">Aliases</span><span class="sxs-lookup"><span data-stu-id="a2cae-124">ALIASES</span></span>

## <span data-ttu-id="a2cae-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a2cae-125">RELATED LINKS</span></span>

