---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/get-azfrontdoorfrontendendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorFrontendEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorFrontendEndpoint.md
ms.openlocfilehash: f685bb7bdad663e84a67397c89568d2263d0ed9a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93770869"
---
# <span data-ttu-id="eabcb-101">Get-AzFrontDoorFrontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="eabcb-101">Get-AzFrontDoorFrontendEndpoint</span></span>

## <span data-ttu-id="eabcb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="eabcb-102">SYNOPSIS</span></span>
<span data-ttu-id="eabcb-103">Obtenha um ponto de extremidade de front-end de front door.</span><span class="sxs-lookup"><span data-stu-id="eabcb-103">Get a front door frontend endpoint.</span></span>

## <span data-ttu-id="eabcb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="eabcb-104">SYNTAX</span></span>

### <span data-ttu-id="eabcb-105">ByFieldsParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="eabcb-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzFrontDoorFrontendEndpoint -ResourceGroupName <String> -FrontDoorName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eabcb-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="eabcb-106">ByObjectParameterSet</span></span>
```
Get-AzFrontDoorFrontendEndpoint [-Name <String>] -FrontDoorObject <PSFrontDoor>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eabcb-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="eabcb-107">ByResourceIdParameterSet</span></span>
```
Get-AzFrontDoorFrontendEndpoint -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="eabcb-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="eabcb-108">DESCRIPTION</span></span>
<span data-ttu-id="eabcb-109">O cmdlet **Get-AzFrontDoorFrontendEndpoint** Obtém todos os pontos de extremidade de frontend existentes no recurso de porta frontal atual que corresponde às informações fornecidas.</span><span class="sxs-lookup"><span data-stu-id="eabcb-109">The **Get-AzFrontDoorFrontendEndpoint** cmdlet gets all existing frontend endpoints in the current Front Door resource that matches provided information.</span></span>

## <span data-ttu-id="eabcb-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="eabcb-110">EXAMPLES</span></span>

### <span data-ttu-id="eabcb-111">Exemplo 1: obter todos os pontos de extremidade de front-end na porta frontal "frontdoor1" que faz parte do grupo de recursos "Rg1".</span><span class="sxs-lookup"><span data-stu-id="eabcb-111">Example 1: Get all frontend endpoints in Front Door "frontdoor1" which is part of resource group "rg1".</span></span>
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

<span data-ttu-id="eabcb-112">Obter todos os pontos de extremidade de front-end na porta frontal "frontdoor1" que faz parte do grupo de recursos "Rg1".</span><span class="sxs-lookup"><span data-stu-id="eabcb-112">Get all frontend endpoints in Front Door "frontdoor1" which is part of resource group "rg1".</span></span>

### <span data-ttu-id="eabcb-113">Exemplo 2: obter ponto de extremidade de front-end com nome "frontdoor1-azurefd-net" na porta frontal "frontdoor1", que faz parte do grupo de recursos "Rg1"</span><span class="sxs-lookup"><span data-stu-id="eabcb-113">Example 2: Get frontend endpoint with name "frontdoor1-azurefd-net" in Front Door "frontdoor1" which is part of resource group "rg1"</span></span>
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

<span data-ttu-id="eabcb-114">Obtenha um ponto de extremidade de front-end com o nome "frontdoor1-azurefd-net" na porta frontal "frontdoor1", que faz parte do grupo de recursos "Rg1"</span><span class="sxs-lookup"><span data-stu-id="eabcb-114">Get frontend endpoint with name "frontdoor1-azurefd-net" in Front Door "frontdoor1" which is part of resource group "rg1"</span></span>

## <span data-ttu-id="eabcb-115">OS</span><span class="sxs-lookup"><span data-stu-id="eabcb-115">PARAMETERS</span></span>

### <span data-ttu-id="eabcb-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eabcb-116">-DefaultProfile</span></span>
<span data-ttu-id="eabcb-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="eabcb-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eabcb-118">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="eabcb-118">-FrontDoorName</span></span>
<span data-ttu-id="eabcb-119">Nome da porta frontal.</span><span class="sxs-lookup"><span data-stu-id="eabcb-119">Front Door name.</span></span>

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

### <span data-ttu-id="eabcb-120">-FrontDoorObject</span><span class="sxs-lookup"><span data-stu-id="eabcb-120">-FrontDoorObject</span></span>
<span data-ttu-id="eabcb-121">O objeto FrontDoor.</span><span class="sxs-lookup"><span data-stu-id="eabcb-121">The FrontDoor object.</span></span>

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

### <span data-ttu-id="eabcb-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="eabcb-122">-Name</span></span>
<span data-ttu-id="eabcb-123">Nome do ponto de extremidade front-end.</span><span class="sxs-lookup"><span data-stu-id="eabcb-123">Frontend endpoint name.</span></span>

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

### <span data-ttu-id="eabcb-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eabcb-124">-ResourceGroupName</span></span>
<span data-ttu-id="eabcb-125">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="eabcb-125">The resource group name.</span></span>

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

### <span data-ttu-id="eabcb-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="eabcb-126">-ResourceId</span></span>
<span data-ttu-id="eabcb-127">ID do recurso da porta frontal</span><span class="sxs-lookup"><span data-stu-id="eabcb-127">Resource Id of the Front Door</span></span>

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

### <span data-ttu-id="eabcb-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eabcb-128">CommonParameters</span></span>
<span data-ttu-id="eabcb-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eabcb-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eabcb-130">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="eabcb-130">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eabcb-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="eabcb-131">INPUTS</span></span>

### <span data-ttu-id="eabcb-132">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="eabcb-132">None</span></span>

## <span data-ttu-id="eabcb-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="eabcb-133">OUTPUTS</span></span>

### <span data-ttu-id="eabcb-134">Microsoft. Azure. Commands. FrontDoor. Models. PSFrontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="eabcb-134">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontendEndpoint</span></span>

## <span data-ttu-id="eabcb-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="eabcb-135">NOTES</span></span>

## <span data-ttu-id="eabcb-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="eabcb-136">RELATED LINKS</span></span>
