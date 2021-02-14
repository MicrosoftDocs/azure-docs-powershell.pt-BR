---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/en-us/powershell/module/az.CloudService/new-AzCloudServiceLoadBalancerConfigurationObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceLoadBalancerConfigurationObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceLoadBalancerConfigurationObject.md
ms.openlocfilehash: 6afabb94ae006cec122d7e89997be17c20e85b05
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116574"
---
# <span data-ttu-id="d1250-101">New-AzCloudServiceLoadBalancerConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="d1250-101">New-AzCloudServiceLoadBalancerConfigurationObject</span></span>

## <span data-ttu-id="d1250-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d1250-102">SYNOPSIS</span></span>
<span data-ttu-id="d1250-103">Criar um objeto na memória para LoadBalancerConfiguration</span><span class="sxs-lookup"><span data-stu-id="d1250-103">Create a in-memory object for LoadBalancerConfiguration</span></span>

## <span data-ttu-id="d1250-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d1250-104">SYNTAX</span></span>

```
New-AzCloudServiceLoadBalancerConfigurationObject
 [-FrontendIPConfiguration <ILoadBalancerFrontendIPConfiguration[]>] [-Name <String>] [<CommonParameters>]
```

## <span data-ttu-id="d1250-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="d1250-105">DESCRIPTION</span></span>
<span data-ttu-id="d1250-106">Criar um objeto na memória para LoadBalancerConfiguration</span><span class="sxs-lookup"><span data-stu-id="d1250-106">Create a in-memory object for LoadBalancerConfiguration</span></span>

## <span data-ttu-id="d1250-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="d1250-107">EXAMPLES</span></span>

### <span data-ttu-id="d1250-108">Exemplo 1: Criar objeto de configuração do balanceador de carga</span><span class="sxs-lookup"><span data-stu-id="d1250-108">Example 1: Create load balancer configuration object</span></span>
```powershell
PS C:\> $publicIP = Get-AzPublicIpAddress -ResourceGroupName 'ContosoOrg' -Name 'ContosoPublicIP'
PS C:\> $feIpConfig = New-AzCloudServiceLoadBalancerFrontendIPConfigurationObject -Name 'ContosoFe' -PublicIPAddressId $publicIP.Id
PS C:\> $loadBalancerConfig = New-AzCloudServiceLoadBalancerConfigurationObject -Name 'ContosoLB' -FrontendIPConfiguration $feIpConfig
```

<span data-ttu-id="d1250-109">Esse comando cria um objeto de configuração de balanceador de carga que é usado para criar ou atualizar um serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="d1250-109">This command creates load balancer configuration object which is used for creating or updating a cloud service.</span></span>
<span data-ttu-id="d1250-110">Para obter mais detalhes, consulte New-AzCloudService.</span><span class="sxs-lookup"><span data-stu-id="d1250-110">For more details see New-AzCloudService.</span></span>

## <span data-ttu-id="d1250-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d1250-111">PARAMETERS</span></span>

### <span data-ttu-id="d1250-112">-FrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="d1250-112">-FrontendIPConfiguration</span></span>
<span data-ttu-id="d1250-113">FrontendIPConfiguration.</span><span class="sxs-lookup"><span data-stu-id="d1250-113">FrontendIPConfiguration.</span></span>
<span data-ttu-id="d1250-114">Para construir, confira a seção ANOTAÇÕES para propriedades FRONTENDIPCONFIGURATION e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="d1250-114">To construct, see NOTES section for FRONTENDIPCONFIGURATION properties and create a hash table.</span></span>

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

### <span data-ttu-id="d1250-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="d1250-115">-Name</span></span>
<span data-ttu-id="d1250-116">Nome do LoadBalancerConfiguration.</span><span class="sxs-lookup"><span data-stu-id="d1250-116">Name of LoadBalancerConfiguration.</span></span>

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

### <span data-ttu-id="d1250-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1250-117">CommonParameters</span></span>
<span data-ttu-id="d1250-118">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d1250-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1250-119">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d1250-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1250-120">Entradas</span><span class="sxs-lookup"><span data-stu-id="d1250-120">INPUTS</span></span>

## <span data-ttu-id="d1250-121">Saídas</span><span class="sxs-lookup"><span data-stu-id="d1250-121">OUTPUTS</span></span>

### <span data-ttu-id="d1250-122">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.LoadBalancerConfiguration</span><span class="sxs-lookup"><span data-stu-id="d1250-122">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.LoadBalancerConfiguration</span></span>

## <span data-ttu-id="d1250-123">Notas</span><span class="sxs-lookup"><span data-stu-id="d1250-123">NOTES</span></span>

<span data-ttu-id="d1250-124">Aliases</span><span class="sxs-lookup"><span data-stu-id="d1250-124">ALIASES</span></span>

<span data-ttu-id="d1250-125">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="d1250-125">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d1250-126">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="d1250-126">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d1250-127">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d1250-127">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d1250-128">FRONTENDIPCONFIGURATION <ILoadBalancerFrontendIPConfiguration[]>: FrontendIPConfiguration.</span><span class="sxs-lookup"><span data-stu-id="d1250-128">FRONTENDIPCONFIGURATION <ILoadBalancerFrontendIPConfiguration[]>: FrontendIPConfiguration.</span></span>
  - <span data-ttu-id="d1250-129">`[Name <String>]`:</span><span class="sxs-lookup"><span data-stu-id="d1250-129">`[Name <String>]`:</span></span> 
  - <span data-ttu-id="d1250-130">`[PrivateIPAddress <String>]`: O endereço IP particular referenciado pelo serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="d1250-130">`[PrivateIPAddress <String>]`: The private IP address referenced by the cloud service.</span></span>
  - <span data-ttu-id="d1250-131">`[PublicIPAddressId <String>]`: ID do Recurso</span><span class="sxs-lookup"><span data-stu-id="d1250-131">`[PublicIPAddressId <String>]`: Resource Id</span></span>
  - <span data-ttu-id="d1250-132">`[SubnetId <String>]`: ID do Recurso</span><span class="sxs-lookup"><span data-stu-id="d1250-132">`[SubnetId <String>]`: Resource Id</span></span>

## <span data-ttu-id="d1250-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d1250-133">RELATED LINKS</span></span>

