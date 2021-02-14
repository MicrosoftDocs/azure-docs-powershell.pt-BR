---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/en-us/powershell/module/az.CloudService/new-AzCloudServiceLoadBalancerFrontendIPConfigurationObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceLoadBalancerFrontendIPConfigurationObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceLoadBalancerFrontendIPConfigurationObject.md
ms.openlocfilehash: cdd983e2ede5cd06c3b9b00805b337eac5b73a9b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115498"
---
# <span data-ttu-id="07977-101">New-AzCloudServiceLoadBalancerFrontendIPConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="07977-101">New-AzCloudServiceLoadBalancerFrontendIPConfigurationObject</span></span>

## <span data-ttu-id="07977-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="07977-102">SYNOPSIS</span></span>
<span data-ttu-id="07977-103">Criar um objeto na memória para LoadBalancerFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="07977-103">Create a in-memory object for LoadBalancerFrontendIPConfiguration</span></span>

## <span data-ttu-id="07977-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="07977-104">SYNTAX</span></span>

```
New-AzCloudServiceLoadBalancerFrontendIPConfigurationObject [-Name <String>] [-PublicIPAddressId <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="07977-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="07977-105">DESCRIPTION</span></span>
<span data-ttu-id="07977-106">Criar um objeto na memória para LoadBalancerFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="07977-106">Create a in-memory object for LoadBalancerFrontendIPConfiguration</span></span>

## <span data-ttu-id="07977-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="07977-107">EXAMPLES</span></span>

### <span data-ttu-id="07977-108">Exemplo 1: Criar objeto de configuração IP frontend do balanceador de carga</span><span class="sxs-lookup"><span data-stu-id="07977-108">Example 1: Create load balancer frontend IP configuration object</span></span>
```powershell
PS C:\> $publicIP = Get-AzPublicIpAddress -ResourceGroupName 'ContosoOrg' -Name 'ContosoPublicIP'
PS C:\> $feIpConfig = New-AzCloudServiceLoadBalancerFrontendIPConfigurationObject -Name 'ContosoFe' -PublicIPAddressId $publicIp.Id
PS C:\> $loadBalancerConfig = New-AzCloudServiceLoadBalancerConfigurationObject -Name 'ContosoLB' -FrontendIPConfiguration $feIpConfig
```

<span data-ttu-id="07977-109">Esse comando cria um objeto de configuração IP frontend do balanceador de carga que é usado para criar ou atualizar um serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="07977-109">This command creates load balancer frontend IP configuration object which is used for creating or updating a cloud service.</span></span>
<span data-ttu-id="07977-110">Para obter mais detalhes, consulte New-AzCloudService.</span><span class="sxs-lookup"><span data-stu-id="07977-110">For more details see New-AzCloudService.</span></span>

## <span data-ttu-id="07977-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="07977-111">PARAMETERS</span></span>

### <span data-ttu-id="07977-112">-Nome</span><span class="sxs-lookup"><span data-stu-id="07977-112">-Name</span></span>
<span data-ttu-id="07977-113">Nome de FrontendIpConfigration.</span><span class="sxs-lookup"><span data-stu-id="07977-113">Name of FrontendIpConfigration.</span></span>

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

### <span data-ttu-id="07977-114">-PublicIPAddressId</span><span class="sxs-lookup"><span data-stu-id="07977-114">-PublicIPAddressId</span></span>
<span data-ttu-id="07977-115">ID do Recurso.</span><span class="sxs-lookup"><span data-stu-id="07977-115">Resource Id.</span></span>

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

### <span data-ttu-id="07977-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07977-116">CommonParameters</span></span>
<span data-ttu-id="07977-117">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07977-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07977-118">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="07977-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07977-119">Entradas</span><span class="sxs-lookup"><span data-stu-id="07977-119">INPUTS</span></span>

## <span data-ttu-id="07977-120">Saídas</span><span class="sxs-lookup"><span data-stu-id="07977-120">OUTPUTS</span></span>

### <span data-ttu-id="07977-121">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.LoadBalancerFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="07977-121">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.LoadBalancerFrontendIPConfiguration</span></span>

## <span data-ttu-id="07977-122">Notas</span><span class="sxs-lookup"><span data-stu-id="07977-122">NOTES</span></span>

<span data-ttu-id="07977-123">Aliases</span><span class="sxs-lookup"><span data-stu-id="07977-123">ALIASES</span></span>

## <span data-ttu-id="07977-124">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="07977-124">RELATED LINKS</span></span>

