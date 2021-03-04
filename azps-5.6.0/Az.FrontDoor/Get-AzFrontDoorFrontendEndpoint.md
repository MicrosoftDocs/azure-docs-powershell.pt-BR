---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/powershell/module/az.frontdoor/get-azfrontdoorfrontendendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorFrontendEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorFrontendEndpoint.md
ms.openlocfilehash: 2887c343c9498eb2b8bde51b51226bffc5795ff3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885724"
---
# <span data-ttu-id="88ae4-101">Get-AzFrontDoorFrontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="88ae4-101">Get-AzFrontDoorFrontendEndpoint</span></span>

## <span data-ttu-id="88ae4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="88ae4-102">SYNOPSIS</span></span>
<span data-ttu-id="88ae4-103">Obter um ponto de extremidade front-end da porta frontal.</span><span class="sxs-lookup"><span data-stu-id="88ae4-103">Get a front door frontend endpoint.</span></span>

## <span data-ttu-id="88ae4-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="88ae4-104">SYNTAX</span></span>

### <span data-ttu-id="88ae4-105">ByFieldsParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="88ae4-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzFrontDoorFrontendEndpoint -ResourceGroupName <String> -FrontDoorName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="88ae4-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="88ae4-106">ByObjectParameterSet</span></span>
```
Get-AzFrontDoorFrontendEndpoint [-Name <String>] -FrontDoorObject <PSFrontDoor>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="88ae4-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="88ae4-107">ByResourceIdParameterSet</span></span>
```
Get-AzFrontDoorFrontendEndpoint -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="88ae4-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="88ae4-108">DESCRIPTION</span></span>
<span data-ttu-id="88ae4-109">O cmdlet **Get-AzFrontDoorFrontendEndpoint** obtém todos os pontos de extremidade front-end existentes no recurso atual da Porta da Frente que corresponde às informações fornecidas.</span><span class="sxs-lookup"><span data-stu-id="88ae4-109">The **Get-AzFrontDoorFrontendEndpoint** cmdlet gets all existing frontend endpoints in the current Front Door resource that matches provided information.</span></span>

## <span data-ttu-id="88ae4-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="88ae4-110">EXAMPLES</span></span>

### <span data-ttu-id="88ae4-111">Exemplo 1: Obter todos os pontos de extremidade front-end no Front Door "frontdoor1" que faz parte do grupo de recursos "rg1".</span><span class="sxs-lookup"><span data-stu-id="88ae4-111">Example 1: Get all frontend endpoints in Front Door "frontdoor1" which is part of resource group "rg1".</span></span>
```powershell
PS C:\> Get-AzFrontDoorFrontendEndpoint -ResourceGroupName "rg1" -FrontDoorName "frontdoor1"


HostName                         : frontdoor1.azurefd.net
SessionAffinityEnabledState      : Disabled
SessionAffinityTtlSeconds        : 0
WebApplicationFirewallPolicyLink :
Backends                         :
CustomHttpsProvisioningState     : Disabled
CustomHttpsProvisioningSubstate  : None
CertificateSource                :
ProtocolType                     :
Vault                            :
SecretName                       :
SecretVersion                    :
CertificateType                  :
ResourceState                    : Enabled
Id                               : /subscriptions/{guid}/resourcegroups/resourcegroup1
                                   /providers/Microsoft.Network/frontdoors/frontdoor1/frontendendpoints/frontdoor1-azurefd-net
Name                             : frontdoor1-azurefd-net
Type                             : Microsoft.Network/frontdoors/frontendendpoints

HostName                         : frontendpointname1.custom.xyz
SessionAffinityEnabledState      : Disabled
SessionAffinityTtlSeconds        : 0
WebApplicationFirewallPolicyLink :
Backends                         :
CustomHttpsProvisioningState     : Disabled
CustomHttpsProvisioningSubstate  : None
CertificateSource                :
ProtocolType                     :
Vault                            :
SecretName                       :
SecretVersion                    :
CertificateType                  :
ResourceState                    : Enabled
Id                               : /subscriptions/{guid}/resourcegroups/resourcegroup1
                                   /providers/Microsoft.Network/frontdoors/frontdoor1/frontendendpoints/frontendpointname1-custom-xyz
Name                             : frontendpointname1-custom-xyz
Type                             : Microsoft.Network/frontdoors/frontendendpoints
```

<span data-ttu-id="88ae4-112">Obter todos os pontos de extremidade front-end no Front Door "frontdoor1" que faz parte do grupo de recursos "rg1".</span><span class="sxs-lookup"><span data-stu-id="88ae4-112">Get all frontend endpoints in Front Door "frontdoor1" which is part of resource group "rg1".</span></span>

### <span data-ttu-id="88ae4-113">Exemplo 2: Obter ponto de extremidade front-end com o nome "frontdoor1-azurefd-net" na Porta da Frente "frontdoor1" que faz parte do grupo de recursos "rg1"</span><span class="sxs-lookup"><span data-stu-id="88ae4-113">Example 2: Get frontend endpoint with name "frontdoor1-azurefd-net" in Front Door "frontdoor1" which is part of resource group "rg1"</span></span>
```powershell
PS C:\> Get-AzFrontDoorFrontendEndpoint -ResourceGroupName "rg1" -FrontDoorName "frontdoor1" -Name "frontdoor1-azurefd-net"


HostName                         : frontdoor1.azurefd.net
SessionAffinityEnabledState      : Disabled
SessionAffinityTtlSeconds        : 0
WebApplicationFirewallPolicyLink :
Backends                         :
CustomHttpsProvisioningState     : Disabled
CustomHttpsProvisioningSubstate  : None
CertificateSource                :
ProtocolType                     :
Vault                            :
SecretName                       :
SecretVersion                    :
CertificateType                  :
ResourceState                    : Enabled
Id                               : /subscriptions/{guid}/resourcegroups/resourcegroup1
                                   /providers/Microsoft.Network/frontdoors/frontdoor1/frontendendpoints/frontdoor1-azurefd-net
Name                             : frontdoor1-azurefd-net
Type                             : Microsoft.Network/frontdoors/frontendendpoints
```

<span data-ttu-id="88ae4-114">Obter ponto de extremidade front-end com o nome "frontdoor1-azurefd-net" no Front Door "frontdoor1" que faz parte do grupo de recursos "rg1"</span><span class="sxs-lookup"><span data-stu-id="88ae4-114">Get frontend endpoint with name "frontdoor1-azurefd-net" in Front Door "frontdoor1" which is part of resource group "rg1"</span></span>

## <span data-ttu-id="88ae4-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="88ae4-115">PARAMETERS</span></span>

### <span data-ttu-id="88ae4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88ae4-116">-DefaultProfile</span></span>
<span data-ttu-id="88ae4-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="88ae4-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="88ae4-118">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="88ae4-118">-FrontDoorName</span></span>
<span data-ttu-id="88ae4-119">Nome da porta frontal.</span><span class="sxs-lookup"><span data-stu-id="88ae4-119">Front Door name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88ae4-120">-FrontDoorObject</span><span class="sxs-lookup"><span data-stu-id="88ae4-120">-FrontDoorObject</span></span>
<span data-ttu-id="88ae4-121">O objeto FrontDoor.</span><span class="sxs-lookup"><span data-stu-id="88ae4-121">The FrontDoor object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="88ae4-122">-Name</span><span class="sxs-lookup"><span data-stu-id="88ae4-122">-Name</span></span>
<span data-ttu-id="88ae4-123">Nome do ponto de extremidade front-end.</span><span class="sxs-lookup"><span data-stu-id="88ae4-123">Frontend endpoint name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88ae4-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88ae4-124">-ResourceGroupName</span></span>
<span data-ttu-id="88ae4-125">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="88ae4-125">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88ae4-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="88ae4-126">-ResourceId</span></span>
<span data-ttu-id="88ae4-127">ID de recurso da Porta da Frente</span><span class="sxs-lookup"><span data-stu-id="88ae4-127">Resource Id of the Front Door</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88ae4-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88ae4-128">CommonParameters</span></span>
<span data-ttu-id="88ae4-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="88ae4-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88ae4-130">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="88ae4-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88ae4-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="88ae4-131">INPUTS</span></span>

### <span data-ttu-id="88ae4-132">Nenhum</span><span class="sxs-lookup"><span data-stu-id="88ae4-132">None</span></span>

## <span data-ttu-id="88ae4-133">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="88ae4-133">OUTPUTS</span></span>

### <span data-ttu-id="88ae4-134">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="88ae4-134">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontendEndpoint</span></span>

## <span data-ttu-id="88ae4-135">NOTES</span><span class="sxs-lookup"><span data-stu-id="88ae4-135">NOTES</span></span>

## <span data-ttu-id="88ae4-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="88ae4-136">RELATED LINKS</span></span>
