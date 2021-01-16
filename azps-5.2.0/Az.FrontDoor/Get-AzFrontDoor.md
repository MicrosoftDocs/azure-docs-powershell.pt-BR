---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/get-azfrontdoor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoor.md
ms.openlocfilehash: 8c378d7f0b1ac7a753f7f270fd3969eb881c7aec
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98261772"
---
# <span data-ttu-id="97c8c-101">Get-AzFrontDoor</span><span class="sxs-lookup"><span data-stu-id="97c8c-101">Get-AzFrontDoor</span></span>

## <span data-ttu-id="97c8c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="97c8c-102">SYNOPSIS</span></span>
<span data-ttu-id="97c8c-103">Obter balanceador de carga de porta frontal</span><span class="sxs-lookup"><span data-stu-id="97c8c-103">Get Front Door load balancer</span></span>

## <span data-ttu-id="97c8c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="97c8c-104">SYNTAX</span></span>

```
Get-AzFrontDoor [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="97c8c-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="97c8c-105">DESCRIPTION</span></span>
<span data-ttu-id="97c8c-106">O cmdletGet **Get-AzFrontDoor** obtém todas as portas frontais existentes na assinatura atual que corresponde às informações fornecidas.</span><span class="sxs-lookup"><span data-stu-id="97c8c-106">The **Get-AzFrontDoor** cmdletGet gets all existing Front Doors in the current subscription that matches provided information.</span></span>

## <span data-ttu-id="97c8c-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="97c8c-107">EXAMPLES</span></span>

### <span data-ttu-id="97c8c-108">Exemplo 1: obter todos os FrontDoors na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="97c8c-108">Example 1: Get all FrontDoors in the current subscription.</span></span>
```powershell
PS C:\> Get-AzFrontDoor

FriendlyName          : frontdoor1
RoutingRules          : {routingrule1}
BackendPools          : {backendpool1}
HealthProbeSettings   : {healthProbeSetting1}
LoadBalancingSettings : {loadbalancingsetting1}
FrontendEndpoints     : {frontendendpoint1}
EnabledState          : Enabled
ResourceState         : Enabled
ProvisioningState     : Succeeded
Cname                 :
Tags                  : {tag1, tag2}
Id                    : /subscriptions/{guid}/resourcegroups/{guid1}/providers/M
                        icrosoft.Network/frontdoors/frontdoor1
Name                  : frontdoor1
Type                  : Microsoft.Network/frontdoor1

FriendlyName          : frontdoor1
RoutingRules          : {routingrule1}
BackendPools          : {backendpool1}
HealthProbeSettings   : {healthProbeSetting1}
LoadBalancingSettings : {loadbalancingsetting1}
FrontendEndpoints     : {frontendendpoint1}
EnabledState          : Enabled
ResourceState         : Enabled
ProvisioningState     : Succeeded
Cname                 :
Tags                  : {tag1, tag2}
Id                    : /subscriptions/{guid}/resourcegroups/{guid2}/providers/M
                        icrosoft.Network/frontdoors/frontdoor1
Name                  : frontdoor1
Type                  : Microsoft.Network/frontdoor1
```

<span data-ttu-id="97c8c-109">Obtenha todos os FrontDoors na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="97c8c-109">Get all FrontDoors in the current subscription.</span></span>

### <span data-ttu-id="97c8c-110">Exemplo 2: obter todos os FrontDoors no grupo de recursos "Rg1" na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="97c8c-110">Example 2: Get all FrontDoors in resource group "rg1" in the current subscription.</span></span>
```powershell
PS C:\> Get-AzFrontDoor -ResourceGroupName "rg1"

FriendlyName          : frontdoor1
RoutingRules          : {routingrule1}
BackendPools          : {backendpool1}
HealthProbeSettings   : {healthProbeSetting1}
LoadBalancingSettings : {loadbalancingsetting1}
FrontendEndpoints     : {frontendendpoint1}
EnabledState          : Enabled
ResourceState         : Enabled
ProvisioningState     : Succeeded
Cname                 :
Tags                  : {tag1, tag2}
Id                    : /subscriptions/{guid}/resourcegroups/rg1/providers/M
                        icrosoft.Network/frontdoors/frontdoor1
Name                  : frontdoor1
Type                  : Microsoft.Network/frontdoor1

FriendlyName          : frontdoor2
RoutingRules          : {routingrule1}
BackendPools          : {backendpool1}
HealthProbeSettings   : {healthProbeSetting1}
LoadBalancingSettings : {loadbalancingsetting1}
FrontendEndpoints     : {frontendendpoint1}
EnabledState          : Enabled
ResourceState         : Enabled
ProvisioningState     : Succeeded
Cname                 :
Tags                  : {tag1, tag2}
Id                    : /subscriptions/{guid}/resourcegroups/rg1/providers/M
                        icrosoft.Network/frontdoors/frontdoor1
Name                  : frontdoor1
Type                  : Microsoft.Network/frontdoor1
```

<span data-ttu-id="97c8c-111">Obtenha todos os FrontDoors no grupo de recursos "Rg1" na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="97c8c-111">Get all FrontDoors in resource group "rg1" in the current subscription.</span></span>

### <span data-ttu-id="97c8c-112">Exemplo 3: obter o FrontDoors no grupo de recursos "Rg1" com nome "frontDoor1" na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="97c8c-112">Example 3: Get the FrontDoors in resource group "rg1" with name "frontDoor1" in the current subscription.</span></span>
```powershell
PS C:\> Get-AzFrontDoor -ResourceGroupName "rg1" -Name "frontDoor1"

FriendlyName          : frontdoor1
RoutingRules          : {routingrule1}
BackendPools          : {backendpool1}
HealthProbeSettings   : {healthProbeSetting1}
LoadBalancingSettings : {loadbalancingsetting1}
FrontendEndpoints     : {frontendendpoint1}
EnabledState          : Enabled
ResourceState         : Enabled
ProvisioningState     : Succeeded
Cname                 :
Tags                  : {tag1, tag2}
Id                    : /subscriptions/{guid}/resourcegroups/rg1/providers/M
                        icrosoft.Network/frontdoors/frontdoor1
Name                  : frontdoor1
Type                  : Microsoft.Network/frontdoor1
```

<span data-ttu-id="97c8c-113">Obtenha o FrontDoors no grupo de recursos "Rg1" com o nome "frontDoor1" na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="97c8c-113">Get the FrontDoors in resource group "rg1" with name "frontDoor1" in the current subscription.</span></span>

## <span data-ttu-id="97c8c-114">OS</span><span class="sxs-lookup"><span data-stu-id="97c8c-114">PARAMETERS</span></span>

### <span data-ttu-id="97c8c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97c8c-115">-DefaultProfile</span></span>
<span data-ttu-id="97c8c-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="97c8c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="97c8c-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="97c8c-117">-Name</span></span>
<span data-ttu-id="97c8c-118">Nome da porta frontal.</span><span class="sxs-lookup"><span data-stu-id="97c8c-118">Front Door name.</span></span>

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

### <span data-ttu-id="97c8c-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97c8c-119">-ResourceGroupName</span></span>
<span data-ttu-id="97c8c-120">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="97c8c-120">The resource group name.</span></span>

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

### <span data-ttu-id="97c8c-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97c8c-121">CommonParameters</span></span>
<span data-ttu-id="97c8c-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97c8c-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97c8c-123">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="97c8c-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97c8c-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="97c8c-124">INPUTS</span></span>

### <span data-ttu-id="97c8c-125">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="97c8c-125">None</span></span>

## <span data-ttu-id="97c8c-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="97c8c-126">OUTPUTS</span></span>

### <span data-ttu-id="97c8c-127">Microsoft. Azure. Commands. FrontDoor. Models. PSFrontDoor</span><span class="sxs-lookup"><span data-stu-id="97c8c-127">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span></span>

## <span data-ttu-id="97c8c-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="97c8c-128">NOTES</span></span>

## <span data-ttu-id="97c8c-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="97c8c-129">RELATED LINKS</span></span>

<span data-ttu-id="97c8c-130">[New-AzFrontDoor](./New-AzFrontDoor.md) 
 [Set-AzFrontDoor](./Set-AzFrontDoor.md) 
 [Remove-AzFrontDoor](./Remove-AzFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="97c8c-130">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)
[Remove-AzFrontDoor](./Remove-AzFrontDoor.md)</span></span>
