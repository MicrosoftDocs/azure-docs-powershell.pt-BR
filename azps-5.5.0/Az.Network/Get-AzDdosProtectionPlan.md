---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azddosprotectionplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzDdosProtectionPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzDdosProtectionPlan.md
ms.openlocfilehash: a94ed627d50b8523157d52d3a9c2bf1f8ab29229
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114167"
---
# <span data-ttu-id="ed0be-101">Get-AzDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="ed0be-101">Get-AzDdosProtectionPlan</span></span>

## <span data-ttu-id="ed0be-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ed0be-102">SYNOPSIS</span></span>
<span data-ttu-id="ed0be-103">Obtém um plano de proteção DDoS.</span><span class="sxs-lookup"><span data-stu-id="ed0be-103">Gets a DDoS protection plan.</span></span>

## <span data-ttu-id="ed0be-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ed0be-104">SYNTAX</span></span>

```
Get-AzDdosProtectionPlan [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ed0be-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="ed0be-105">DESCRIPTION</span></span>
<span data-ttu-id="ed0be-106">O Get-AzDdosProtectionPlan cmdlet obtém um plano de proteção DDoS.</span><span class="sxs-lookup"><span data-stu-id="ed0be-106">The Get-AzDdosProtectionPlan cmdlet gets a DDoS protection plan.</span></span>

## <span data-ttu-id="ed0be-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="ed0be-107">EXAMPLES</span></span>

### <span data-ttu-id="ed0be-108">Exemplo 1: Obter um plano de proteção DDoS específico</span><span class="sxs-lookup"><span data-stu-id="ed0be-108">Example 1: Get a specific DDoS protection plan</span></span>
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

<span data-ttu-id="ed0be-109">Nesse caso, precisamos especificar os atributos  **NomedoGrupo** de Recurso, que correspondem ao grupo de recursos e ao nome do plano de proteção DDoS, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="ed0be-109">In this case, we need to specify both **ResourceGroupName** and **Name** attributes, which correspond to the resource group and the name of the DDoS protection plan, respectively.</span></span>

### <span data-ttu-id="ed0be-110">Exemplo 2: Obter todos os planos de proteção DDoS em um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="ed0be-110">Example 2: Get all DDoS protection plans in a resource group</span></span>
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

<span data-ttu-id="ed0be-111">Neste cenário, especificamos apenas o parâmetro **ResourceGroupName** para obter uma lista de planos de proteção DDoS.</span><span class="sxs-lookup"><span data-stu-id="ed0be-111">In this scenario, we only specify the parameter **ResourceGroupName** to get a list of DDoS protection plans.</span></span>

### <span data-ttu-id="ed0be-112">Exemplo 3: Obter todos os planos de proteção DDoS em uma assinatura</span><span class="sxs-lookup"><span data-stu-id="ed0be-112">Example 3: Get all DDoS protection plans in a subscription</span></span>
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

<span data-ttu-id="ed0be-113">Aqui, não especificamos parâmetros para obter uma lista de todos os planos de proteção DDoS em uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="ed0be-113">Here, we do not specify any parameters to get a list of all DDoS protection plans in a subscription.</span></span>

### <span data-ttu-id="ed0be-114">Exemplo 4: Obter todos os planos de proteção DDoS em uma assinatura</span><span class="sxs-lookup"><span data-stu-id="ed0be-114">Example 4: Get all DDoS protection plans in a subscription</span></span>
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

<span data-ttu-id="ed0be-115">Este cmdlet retorna todos os DdosProtectionPlans que começam com "teste".</span><span class="sxs-lookup"><span data-stu-id="ed0be-115">This cmdlet returns all DdosProtectionPlans that start with "test".</span></span>

## <span data-ttu-id="ed0be-116">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ed0be-116">PARAMETERS</span></span>

### <span data-ttu-id="ed0be-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed0be-117">-DefaultProfile</span></span>
<span data-ttu-id="ed0be-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ed0be-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ed0be-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="ed0be-119">-Name</span></span>
<span data-ttu-id="ed0be-120">Especifica o nome do plano de proteção DDoS.</span><span class="sxs-lookup"><span data-stu-id="ed0be-120">Specifies the name of the DDoS protection plan.</span></span>

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

### <span data-ttu-id="ed0be-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed0be-121">-ResourceGroupName</span></span>
<span data-ttu-id="ed0be-122">Especifica o nome do grupo de recursos do plano de proteção DDoS.</span><span class="sxs-lookup"><span data-stu-id="ed0be-122">Specifies the name of the DDoS protection plan resource group.</span></span>

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

### <span data-ttu-id="ed0be-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed0be-123">CommonParameters</span></span>
<span data-ttu-id="ed0be-124">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed0be-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed0be-125">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ed0be-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed0be-126">Entradas</span><span class="sxs-lookup"><span data-stu-id="ed0be-126">INPUTS</span></span>

### <span data-ttu-id="ed0be-127">System.String</span><span class="sxs-lookup"><span data-stu-id="ed0be-127">System.String</span></span>

## <span data-ttu-id="ed0be-128">Saídas</span><span class="sxs-lookup"><span data-stu-id="ed0be-128">OUTPUTS</span></span>

### <span data-ttu-id="ed0be-129">Microsoft.Azure.Commands.Network.Models.PSDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="ed0be-129">Microsoft.Azure.Commands.Network.Models.PSDdosProtectionPlan</span></span>

## <span data-ttu-id="ed0be-130">Notas</span><span class="sxs-lookup"><span data-stu-id="ed0be-130">NOTES</span></span>

## <span data-ttu-id="ed0be-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ed0be-131">RELATED LINKS</span></span>

[<span data-ttu-id="ed0be-132">New-AzDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="ed0be-132">New-AzDdosProtectionPlan</span></span>](./New-AzDdosProtectionPlan.md)

[<span data-ttu-id="ed0be-133">Remove-AzDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="ed0be-133">Remove-AzDdosProtectionPlan</span></span>](./Remove-AzDdosProtectionPlan.md)

[<span data-ttu-id="ed0be-134">New-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="ed0be-134">New-AzVirtualNetwork</span></span>](./New-AzVirtualNetwork.md)

[<span data-ttu-id="ed0be-135">Set-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="ed0be-135">Set-AzVirtualNetwork</span></span>](./Set-AzVirtualNetwork.md)

[<span data-ttu-id="ed0be-136">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="ed0be-136">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)