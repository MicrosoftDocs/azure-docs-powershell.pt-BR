---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azuredosprotectionplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmDdosProtectionPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmDdosProtectionPlan.md
ms.openlocfilehash: 2d1942dd5c069660d062922a069cc88b505748fa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93609385"
---
# <span data-ttu-id="9fd4e-101">Get-AzureRmDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="9fd4e-101">Get-AzureRmDdosProtectionPlan</span></span>

## <span data-ttu-id="9fd4e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9fd4e-102">SYNOPSIS</span></span>
<span data-ttu-id="9fd4e-103">Obtém um plano de proteção contra DDoS.</span><span class="sxs-lookup"><span data-stu-id="9fd4e-103">Gets a DDoS protection plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9fd4e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9fd4e-104">SYNTAX</span></span>

### <span data-ttu-id="9fd4e-105">GetByNameAndGroup</span><span class="sxs-lookup"><span data-stu-id="9fd4e-105">GetByNameAndGroup</span></span>
```
Get-AzureRmDdosProtectionPlan -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9fd4e-106">Programação</span><span class="sxs-lookup"><span data-stu-id="9fd4e-106">List</span></span>
```
Get-AzureRmDdosProtectionPlan [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9fd4e-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9fd4e-107">DESCRIPTION</span></span>
<span data-ttu-id="9fd4e-108">O cmdlet Get-AzureRmDdosProtectionPlan Obtém um plano de proteção contra DDoS.</span><span class="sxs-lookup"><span data-stu-id="9fd4e-108">The Get-AzureRmDdosProtectionPlan cmdlet gets a DDoS protection plan.</span></span>

## <span data-ttu-id="9fd4e-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9fd4e-109">EXAMPLES</span></span>

### <span data-ttu-id="9fd4e-110">Exemplo 1: obter um plano de proteção contra DDoS específico</span><span class="sxs-lookup"><span data-stu-id="9fd4e-110">Example 1: Get a specific DDoS protection plan</span></span>
```
D:\> Get-AzureRmDdosProtectionPlan -ResourceGroupName ResourceGroupName -Name DdosProtectionPlanName


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

<span data-ttu-id="9fd4e-111">Nesse caso, precisamos especificar ambos os atributos **ResourceGroupName** e **Name** , que correspondem ao grupo de recursos e ao nome do plano de proteção contra DDoS, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="9fd4e-111">In this case, we need to specify both **ResourceGroupName** and **Name** attributes, which correspond to the resource group and the name of the DDoS protection plan, respectively.</span></span>

### <span data-ttu-id="9fd4e-112">Exemplo 2: obter todos os planos de proteção contra DDoS em um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="9fd4e-112">Example 2: Get all DDoS protection plans in a resource group</span></span>
```
D:\> Get-AzureRmDdosProtectionPlan -ResourceGroupName ResourceGroupName


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

<span data-ttu-id="9fd4e-113">Nesse cenário, especificamos somente o parâmetro **ResourceGroupName** para obter uma lista de planos de proteção contra DDoS.</span><span class="sxs-lookup"><span data-stu-id="9fd4e-113">In this scenario, we only specify the parameter **ResourceGroupName** to get a list of DDoS protection plans.</span></span>

### <span data-ttu-id="9fd4e-114">Exemplo 2: obter todos os planos de proteção DDoS em uma assinatura</span><span class="sxs-lookup"><span data-stu-id="9fd4e-114">Example 2: Get all DDoS protection plans in a subscription</span></span>
```
D:\> Get-AzureRmDdosProtectionPlan


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

<span data-ttu-id="9fd4e-115">Aqui, não especificamos parâmetros para obter uma lista de todos os planos de proteção contra DDoS em uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="9fd4e-115">Here, we do not specify any parameters to get a list of all DDoS protection plans in a subscription.</span></span>

## <span data-ttu-id="9fd4e-116">OS</span><span class="sxs-lookup"><span data-stu-id="9fd4e-116">PARAMETERS</span></span>

### <span data-ttu-id="9fd4e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9fd4e-117">-DefaultProfile</span></span>
<span data-ttu-id="9fd4e-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9fd4e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9fd4e-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="9fd4e-119">-Name</span></span>
<span data-ttu-id="9fd4e-120">Especifica o nome do plano de proteção contra DDoS.</span><span class="sxs-lookup"><span data-stu-id="9fd4e-120">Specifies the name of the DDoS protection plan.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameAndGroup
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9fd4e-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9fd4e-121">-ResourceGroupName</span></span>
<span data-ttu-id="9fd4e-122">Especifica o nome do grupo de recursos plano de proteção contra DDoS.</span><span class="sxs-lookup"><span data-stu-id="9fd4e-122">Specifies the name of the DDoS protection plan resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameAndGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9fd4e-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9fd4e-123">CommonParameters</span></span>
<span data-ttu-id="9fd4e-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9fd4e-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9fd4e-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9fd4e-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9fd4e-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9fd4e-126">INPUTS</span></span>

### <span data-ttu-id="9fd4e-127">System. String</span><span class="sxs-lookup"><span data-stu-id="9fd4e-127">System.String</span></span>

## <span data-ttu-id="9fd4e-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9fd4e-128">OUTPUTS</span></span>

### <span data-ttu-id="9fd4e-129">Microsoft.Azure.Commands.Network.Models.PSDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="9fd4e-129">Microsoft.Azure.Commands.Network.Models.PSDdosProtectionPlan</span></span>

## <span data-ttu-id="9fd4e-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9fd4e-130">NOTES</span></span>

## <span data-ttu-id="9fd4e-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9fd4e-131">RELATED LINKS</span></span>

[<span data-ttu-id="9fd4e-132">New-AzureRmDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="9fd4e-132">New-AzureRmDdosProtectionPlan</span></span>](./New-AzureRmDdosProtectionPlan.md)

[<span data-ttu-id="9fd4e-133">Remove-AzureRmDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="9fd4e-133">Remove-AzureRmDdosProtectionPlan</span></span>](./Remove-AzureRmDdosProtectionPlan.md)

[<span data-ttu-id="9fd4e-134">New-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="9fd4e-134">New-AzureRmVirtualNetwork</span></span>](./New-AzureRmVirtualNetwork.md)

[<span data-ttu-id="9fd4e-135">Set-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="9fd4e-135">Set-AzureRmVirtualNetwork</span></span>](./Set-AzureRmVirtualNetwork.md)

[<span data-ttu-id="9fd4e-136">Get-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="9fd4e-136">Get-AzureRmVirtualNetwork</span></span>](./Get-AzureRmVirtualNetwork.md)
