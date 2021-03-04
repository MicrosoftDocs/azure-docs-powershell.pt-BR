---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/powershell/module/az.CloudService/new-AzCloudServiceLoadBalancerConfigurationObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceLoadBalancerConfigurationObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceLoadBalancerConfigurationObject.md
ms.openlocfilehash: 5d3acb8c03ceae44024ed8c6c52a8ee962c9861c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889691"
---
# <span data-ttu-id="d504a-101">New-AzCloudServiceLoadBalancerConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="d504a-101">New-AzCloudServiceLoadBalancerConfigurationObject</span></span>

## <span data-ttu-id="d504a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d504a-102">SYNOPSIS</span></span>
<span data-ttu-id="d504a-103">Criar um objeto na memória para LoadBalancerConfiguration</span><span class="sxs-lookup"><span data-stu-id="d504a-103">Create a in-memory object for LoadBalancerConfiguration</span></span>

## <span data-ttu-id="d504a-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="d504a-104">SYNTAX</span></span>

```
New-AzCloudServiceLoadBalancerConfigurationObject
 [-FrontendIPConfiguration <ILoadBalancerFrontendIPConfiguration[]>] [-Name <String>] [<CommonParameters>]
```

## <span data-ttu-id="d504a-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="d504a-105">DESCRIPTION</span></span>
<span data-ttu-id="d504a-106">Criar um objeto na memória para LoadBalancerConfiguration</span><span class="sxs-lookup"><span data-stu-id="d504a-106">Create a in-memory object for LoadBalancerConfiguration</span></span>

## <span data-ttu-id="d504a-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d504a-107">EXAMPLES</span></span>

### <span data-ttu-id="d504a-108">Exemplo 1: Criar objeto de configuração do balanceador de carga</span><span class="sxs-lookup"><span data-stu-id="d504a-108">Example 1: Create load balancer configuration object</span></span>
```powershell
PS C:\> $publicIP = Get-AzPublicIpAddress -ResourceGroupName 'ContosoOrg' -Name 'ContosoPublicIP'
PS C:\> $feIpConfig = New-AzCloudServiceLoadBalancerFrontendIPConfigurationObject -Name 'ContosoFe' -PublicIPAddressId $publicIP.Id
PS C:\> $loadBalancerConfig = New-AzCloudServiceLoadBalancerConfigurationObject -Name 'ContosoLB' -FrontendIPConfiguration $feIpConfig
```

<span data-ttu-id="d504a-109">Este comando cria um objeto de configuração do balanceador de carga que é usado para criar ou atualizar um serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="d504a-109">This command creates load balancer configuration object which is used for creating or updating a cloud service.</span></span>
<span data-ttu-id="d504a-110">Para obter mais detalhes, consulte New-AzCloudService.</span><span class="sxs-lookup"><span data-stu-id="d504a-110">For more details see New-AzCloudService.</span></span>

## <span data-ttu-id="d504a-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="d504a-111">PARAMETERS</span></span>

### <span data-ttu-id="d504a-112">-FrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="d504a-112">-FrontendIPConfiguration</span></span>
<span data-ttu-id="d504a-113">FrontendIPConfiguration.</span><span class="sxs-lookup"><span data-stu-id="d504a-113">FrontendIPConfiguration.</span></span>
<span data-ttu-id="d504a-114">Para construir, consulte a seção NOTES para propriedades FRONTENDIPCONFIGURATION e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="d504a-114">To construct, see NOTES section for FRONTENDIPCONFIGURATION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.ILoadBalancerFrontendIPConfiguration[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d504a-115">-Name</span><span class="sxs-lookup"><span data-stu-id="d504a-115">-Name</span></span>
<span data-ttu-id="d504a-116">Nome de LoadBalancerConfiguration.</span><span class="sxs-lookup"><span data-stu-id="d504a-116">Name of LoadBalancerConfiguration.</span></span>

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

### <span data-ttu-id="d504a-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d504a-117">CommonParameters</span></span>
<span data-ttu-id="d504a-118">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d504a-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d504a-119">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d504a-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d504a-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d504a-120">INPUTS</span></span>

## <span data-ttu-id="d504a-121">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="d504a-121">OUTPUTS</span></span>

### <span data-ttu-id="d504a-122">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.LoadBalancerConfiguration</span><span class="sxs-lookup"><span data-stu-id="d504a-122">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.LoadBalancerConfiguration</span></span>

## <span data-ttu-id="d504a-123">NOTES</span><span class="sxs-lookup"><span data-stu-id="d504a-123">NOTES</span></span>

<span data-ttu-id="d504a-124">ALIASES</span><span class="sxs-lookup"><span data-stu-id="d504a-124">ALIASES</span></span>

<span data-ttu-id="d504a-125">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="d504a-125">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d504a-126">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="d504a-126">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d504a-127">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d504a-127">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d504a-128">FRONTENDIPCONFIGURATION <ILoadBalancerFrontendIPConfiguration[]>: FrontendIPConfiguration.</span><span class="sxs-lookup"><span data-stu-id="d504a-128">FRONTENDIPCONFIGURATION <ILoadBalancerFrontendIPConfiguration[]>: FrontendIPConfiguration.</span></span>
  - <span data-ttu-id="d504a-129">`[Name <String>]`:</span><span class="sxs-lookup"><span data-stu-id="d504a-129">`[Name <String>]`:</span></span> 
  - <span data-ttu-id="d504a-130">`[PrivateIPAddress <String>]`: O endereço IP privado referenciado pelo serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="d504a-130">`[PrivateIPAddress <String>]`: The private IP address referenced by the cloud service.</span></span>
  - <span data-ttu-id="d504a-131">`[PublicIPAddressId <String>]`: ID de recurso</span><span class="sxs-lookup"><span data-stu-id="d504a-131">`[PublicIPAddressId <String>]`: Resource Id</span></span>
  - <span data-ttu-id="d504a-132">`[SubnetId <String>]`: ID de recurso</span><span class="sxs-lookup"><span data-stu-id="d504a-132">`[SubnetId <String>]`: Resource Id</span></span>

## <span data-ttu-id="d504a-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d504a-133">RELATED LINKS</span></span>

