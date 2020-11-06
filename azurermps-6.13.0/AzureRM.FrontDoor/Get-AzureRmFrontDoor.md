---
external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml
Module Name: AzureRM.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/get-azurermfrontdoor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/Get-AzureRmFrontDoor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/Get-AzureRmFrontDoor.md
ms.openlocfilehash: ca54e2cc86daca89a9872366dea32b375080c63d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602934"
---
# <span data-ttu-id="a3ded-101">Get-AzureRmFrontDoor</span><span class="sxs-lookup"><span data-stu-id="a3ded-101">Get-AzureRmFrontDoor</span></span>

## <span data-ttu-id="a3ded-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a3ded-102">SYNOPSIS</span></span>
<span data-ttu-id="a3ded-103">Obter balanceador de carga de porta frontal</span><span class="sxs-lookup"><span data-stu-id="a3ded-103">Get Front Door load balancer</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a3ded-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a3ded-104">SYNTAX</span></span>

```
Get-AzureRmFrontDoor [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a3ded-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a3ded-105">DESCRIPTION</span></span>
<span data-ttu-id="a3ded-106">O cmdletGet **Get-AzureRmFrontDoor** obtém todas as portas frontais existentes na assinatura atual que corresponde às informações fornecidas.</span><span class="sxs-lookup"><span data-stu-id="a3ded-106">The **Get-AzureRmFrontDoor** cmdletGet gets all existing Front Doors in the current subscription that matches provided information.</span></span>

## <span data-ttu-id="a3ded-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a3ded-107">EXAMPLES</span></span>

### <span data-ttu-id="a3ded-108">Exemplo 1: obter todos os FrontDoors na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="a3ded-108">Example 1: Get all FrontDoors in the current subscription.</span></span>
```powershell
PS C:\> Get-AzureRmFrontDoor

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

<span data-ttu-id="a3ded-109">Obtenha todos os FrontDoors na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="a3ded-109">Get all FrontDoors in the current subscription.</span></span>

### <span data-ttu-id="a3ded-110">Exemplo 2: obter todos os FrontDoors no grupo de recursos "Rg1" na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="a3ded-110">Example 2: Get all FrontDoors in resource group "rg1" in the current subscription.</span></span>
```powershell
PS C:\> Get-AzureRmFrontDoor -ResourceGroupName "rg1"

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

<span data-ttu-id="a3ded-111">Obtenha todos os FrontDoors no grupo de recursos "Rg1" na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="a3ded-111">Get all FrontDoors in resource group "rg1" in the current subscription.</span></span>

### <span data-ttu-id="a3ded-112">Exemplo 3: obter o FrontDoors no grupo de recursos "Rg1" com nome "frontDoor1" na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="a3ded-112">Example 3: Get the FrontDoors in resource group "rg1" with name "frontDoor1" in the current subscription.</span></span>
```powershell
PS C:\> Get-AzureRmFrontDoor -ResourceGroupName "rg1" -Name "frontDoor1"

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

<span data-ttu-id="a3ded-113">Obtenha o FrontDoors no grupo de recursos "Rg1" com o nome "frontDoor1" na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="a3ded-113">Get the FrontDoors in resource group "rg1" with name "frontDoor1" in the current subscription.</span></span>

## <span data-ttu-id="a3ded-114">OS</span><span class="sxs-lookup"><span data-stu-id="a3ded-114">PARAMETERS</span></span>

### <span data-ttu-id="a3ded-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3ded-115">-DefaultProfile</span></span>
<span data-ttu-id="a3ded-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a3ded-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3ded-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="a3ded-117">-Name</span></span>
<span data-ttu-id="a3ded-118">Nome da porta frontal.</span><span class="sxs-lookup"><span data-stu-id="a3ded-118">Front Door name.</span></span>

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

### <span data-ttu-id="a3ded-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3ded-119">-ResourceGroupName</span></span>
<span data-ttu-id="a3ded-120">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a3ded-120">The resource group name.</span></span>

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

### <span data-ttu-id="a3ded-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3ded-121">CommonParameters</span></span>
<span data-ttu-id="a3ded-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3ded-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3ded-123">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a3ded-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3ded-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a3ded-124">INPUTS</span></span>

### <span data-ttu-id="a3ded-125">System. String</span><span class="sxs-lookup"><span data-stu-id="a3ded-125">System.String</span></span>

## <span data-ttu-id="a3ded-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a3ded-126">OUTPUTS</span></span>

### <span data-ttu-id="a3ded-127">Microsoft. Azure. Commands. FrontDoor. Models. PSFrontDoor</span><span class="sxs-lookup"><span data-stu-id="a3ded-127">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span></span>

## <span data-ttu-id="a3ded-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a3ded-128">NOTES</span></span>

## <span data-ttu-id="a3ded-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a3ded-129">RELATED LINKS</span></span>

<span data-ttu-id="a3ded-130">[New-AzureRmFrontDoor](./New-AzureRmFrontDoor.md) 
 [Set-AzureRmFrontDoor](./Set-AzureRmFrontDoor.md) 
 [Remove-AzureRmFrontDoor](./Remove-AzureRmFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="a3ded-130">[New-AzureRmFrontDoor](./New-AzureRmFrontDoor.md)
[Set-AzureRmFrontDoor](./Set-AzureRmFrontDoor.md)
[Remove-AzureRmFrontDoor](./Remove-AzureRmFrontDoor.md)</span></span>
