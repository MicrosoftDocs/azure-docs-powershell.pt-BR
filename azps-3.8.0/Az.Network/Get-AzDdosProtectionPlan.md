---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azddosprotectionplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzDdosProtectionPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzDdosProtectionPlan.md
ms.openlocfilehash: a94ed627d50b8523157d52d3a9c2bf1f8ab29229
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93944955"
---
# <span data-ttu-id="b8622-101">Get-AzDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="b8622-101">Get-AzDdosProtectionPlan</span></span>

## <span data-ttu-id="b8622-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b8622-102">SYNOPSIS</span></span>
<span data-ttu-id="b8622-103">Obtém um plano de proteção contra DDoS.</span><span class="sxs-lookup"><span data-stu-id="b8622-103">Gets a DDoS protection plan.</span></span>

## <span data-ttu-id="b8622-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b8622-104">SYNTAX</span></span>

```
Get-AzDdosProtectionPlan [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b8622-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b8622-105">DESCRIPTION</span></span>
<span data-ttu-id="b8622-106">O cmdlet Get-AzDdosProtectionPlan Obtém um plano de proteção contra DDoS.</span><span class="sxs-lookup"><span data-stu-id="b8622-106">The Get-AzDdosProtectionPlan cmdlet gets a DDoS protection plan.</span></span>

## <span data-ttu-id="b8622-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b8622-107">EXAMPLES</span></span>

### <span data-ttu-id="b8622-108">Exemplo 1: obter um plano de proteção contra DDoS específico</span><span class="sxs-lookup"><span data-stu-id="b8622-108">Example 1: Get a specific DDoS protection plan</span></span>
```
D:\> Get-AzDdosProtectionPlan -ResourceGroupName ResourceGroupName -Name DdosProtectionPlanName


Name              : DdosProtectionPlanName
Id                : /subscriptions/d1dbd366-9871-45ac-84b7-fb318152a9e0/resourceGroups/ResourceGroupName/providers/Microsoft.Network/ddosProtectionPlans/DdosProtectionPlanName
Etag              : W/"a20e5592-9b51-423b-9758-b00cd322f744"
ProvisioningState : Succeeded
VirtualNetworks   : [
                      {
                        "Id": "/subscriptions/d1dbd366-9871-45ac-84b7-fb318152a9e0/resourceGroups/ResourceGroupName/providers/Microsoft.Network/virtualNetworks/VnetName"
                      }
                    ]
```

<span data-ttu-id="b8622-109">Nesse caso, precisamos especificar ambos os atributos **ResourceGroupName** e **Name** , que correspondem ao grupo de recursos e ao nome do plano de proteção contra DDoS, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="b8622-109">In this case, we need to specify both **ResourceGroupName** and **Name** attributes, which correspond to the resource group and the name of the DDoS protection plan, respectively.</span></span>

### <span data-ttu-id="b8622-110">Exemplo 2: obter todos os planos de proteção contra DDoS em um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="b8622-110">Example 2: Get all DDoS protection plans in a resource group</span></span>
```
D:\> Get-AzDdosProtectionPlan -ResourceGroupName ResourceGroupName


Name              : DdosProtectionPlanName
Id                : /subscriptions/d1dbd366-9871-45ac-84b7-fb318152a9e0/resourceGroups/ResourceGroupName/providers/Microsoft.Network/ddosProtectionPlans/DdosProtectionPlanName
Etag              : W/"a20e5592-9b51-423b-9758-b00cd322f744"
ProvisioningState : Succeeded
VirtualNetworks   : [
                      {
                        "Id": "/subscriptions/d1dbd366-9871-45ac-84b7-fb318152a9e0/resourceGroups/ResourceGroupName/providers/Microsoft.Network/virtualNetworks/VnetName"
                      }
                    ]
```

<span data-ttu-id="b8622-111">Nesse cenário, especificamos somente o parâmetro **ResourceGroupName** para obter uma lista de planos de proteção contra DDoS.</span><span class="sxs-lookup"><span data-stu-id="b8622-111">In this scenario, we only specify the parameter **ResourceGroupName** to get a list of DDoS protection plans.</span></span>

### <span data-ttu-id="b8622-112">Exemplo 3: obter todos os planos de proteção DDoS em uma assinatura</span><span class="sxs-lookup"><span data-stu-id="b8622-112">Example 3: Get all DDoS protection plans in a subscription</span></span>
```
D:\> Get-AzDdosProtectionPlan


Name              : DdosProtectionPlanName
Id                : /subscriptions/d1dbd366-9871-45ac-84b7-fb318152a9e0/resourceGroups/ResourceGroupName/providers/Microsoft.Network/ddosProtectionPlans/DdosProtectionPlanName
Etag              : W/"a20e5592-9b51-423b-9758-b00cd322f744"
ProvisioningState : Succeeded
VirtualNetworks   : [
                      {
                        "Id": "/subscriptions/d1dbd366-9871-45ac-84b7-fb318152a9e0/resourceGroups/ResourceGroupName/providers/Microsoft.Network/virtualNetworks/VnetName"
                      }
                    ]
```

<span data-ttu-id="b8622-113">Aqui, não especificamos parâmetros para obter uma lista de todos os planos de proteção contra DDoS em uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="b8622-113">Here, we do not specify any parameters to get a list of all DDoS protection plans in a subscription.</span></span>

### <span data-ttu-id="b8622-114">Exemplo 4: obter todos os planos de proteção DDoS em uma assinatura</span><span class="sxs-lookup"><span data-stu-id="b8622-114">Example 4: Get all DDoS protection plans in a subscription</span></span>
```
D:\> Get-AzDdosProtectionPlan -Name test*


Name              : test1
Id                : /subscriptions/d1dbd366-9871-45ac-84b7-fb318152a9e0/resourceGroups/ResourceGroupName/providers/Microsoft.Network/ddosProtectionPlans/test1
Etag              : W/"a20e5592-9b51-423b-9758-b00cd322f744"
ProvisioningState : Succeeded
VirtualNetworks   : [
                      {
                        "Id": "/subscriptions/d1dbd366-9871-45ac-84b7-fb318152a9e0/resourceGroups/ResourceGroupName/providers/Microsoft.Network/virtualNetworks/VnetName"
                      }
                    ]

Name              : test2
Id                : /subscriptions/d1dbd366-9871-45ac-84b7-fb318152a9e0/resourceGroups/ResourceGroupName/providers/Microsoft.Network/ddosProtectionPlans/test2
Etag              : W/"a20e5592-9b51-423b-9758-b00cd322f744"
ProvisioningState : Succeeded
VirtualNetworks   : [
                      {
                        "Id": "/subscriptions/d1dbd366-9871-45ac-84b7-fb318152a9e0/resourceGroups/ResourceGroupName/providers/Microsoft.Network/virtualNetworks/VnetName"
                      }
                    ]
```

<span data-ttu-id="b8622-115">Esse cmdlet retorna todos os DdosProtectionPlans que começam com "Test".</span><span class="sxs-lookup"><span data-stu-id="b8622-115">This cmdlet returns all DdosProtectionPlans that start with "test".</span></span>

## <span data-ttu-id="b8622-116">OS</span><span class="sxs-lookup"><span data-stu-id="b8622-116">PARAMETERS</span></span>

### <span data-ttu-id="b8622-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8622-117">-DefaultProfile</span></span>
<span data-ttu-id="b8622-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b8622-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b8622-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="b8622-119">-Name</span></span>
<span data-ttu-id="b8622-120">Especifica o nome do plano de proteção contra DDoS.</span><span class="sxs-lookup"><span data-stu-id="b8622-120">Specifies the name of the DDoS protection plan.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="b8622-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8622-121">-ResourceGroupName</span></span>
<span data-ttu-id="b8622-122">Especifica o nome do grupo de recursos plano de proteção contra DDoS.</span><span class="sxs-lookup"><span data-stu-id="b8622-122">Specifies the name of the DDoS protection plan resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="b8622-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8622-123">CommonParameters</span></span>
<span data-ttu-id="b8622-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b8622-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8622-125">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b8622-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8622-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b8622-126">INPUTS</span></span>

### <span data-ttu-id="b8622-127">System. String</span><span class="sxs-lookup"><span data-stu-id="b8622-127">System.String</span></span>

## <span data-ttu-id="b8622-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b8622-128">OUTPUTS</span></span>

### <span data-ttu-id="b8622-129">Microsoft.Azure.Commands.Network.Models.PSDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="b8622-129">Microsoft.Azure.Commands.Network.Models.PSDdosProtectionPlan</span></span>

## <span data-ttu-id="b8622-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b8622-130">NOTES</span></span>

## <span data-ttu-id="b8622-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b8622-131">RELATED LINKS</span></span>

[<span data-ttu-id="b8622-132">New-AzDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="b8622-132">New-AzDdosProtectionPlan</span></span>](./New-AzDdosProtectionPlan.md)

[<span data-ttu-id="b8622-133">Remove-AzDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="b8622-133">Remove-AzDdosProtectionPlan</span></span>](./Remove-AzDdosProtectionPlan.md)

[<span data-ttu-id="b8622-134">New-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="b8622-134">New-AzVirtualNetwork</span></span>](./New-AzVirtualNetwork.md)

[<span data-ttu-id="b8622-135">Set-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="b8622-135">Set-AzVirtualNetwork</span></span>](./Set-AzVirtualNetwork.md)

[<span data-ttu-id="b8622-136">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="b8622-136">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)