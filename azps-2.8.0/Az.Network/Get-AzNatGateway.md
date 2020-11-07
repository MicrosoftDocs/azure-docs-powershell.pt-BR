---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznatgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNatGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNatGateway.md
ms.openlocfilehash: f52f6a2872d6f7567a51e1433336ccb8e1629fdb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93772007"
---
# <span data-ttu-id="ee20d-101">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="ee20d-101">Get-AzNatGateway</span></span>

## <span data-ttu-id="ee20d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ee20d-102">SYNOPSIS</span></span>
<span data-ttu-id="ee20d-103">Obtém um recurso de gateway NAT em um grupo de recursos por nome ou ID NatGateway ou todos os recursos do gateway NAT em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ee20d-103">Gets a Nat Gateway resource in a resource group by name or NatGateway Id  or all Nat Gateway resources in a resource group.</span></span>

## <span data-ttu-id="ee20d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ee20d-104">SYNTAX</span></span>

### <span data-ttu-id="ee20d-105">ListParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="ee20d-105">ListParameterSet (Default)</span></span>
```
Get-AzNatGateway [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ee20d-106">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="ee20d-106">GetByNameParameterSet</span></span>
```
Get-AzNatGateway -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ee20d-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ee20d-107">GetByResourceIdParameterSet</span></span>
```
Get-AzNatGateway -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ee20d-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ee20d-108">DESCRIPTION</span></span>
<span data-ttu-id="ee20d-109">Obtém um recurso de gateway NAT em um grupo de recursos por nome ou ID NatGateway ou todos os recursos do gateway NAT em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ee20d-109">Gets a Nat Gateway resource in a resource group by name OR NatGateway Id OR all Nat Gateway resources in a resource group.</span></span>

## <span data-ttu-id="ee20d-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ee20d-110">EXAMPLES</span></span>

### <span data-ttu-id="ee20d-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ee20d-111">Example 1</span></span>
```powershell
PS C:> Get-AzNatGateway -ResourceGroupName "natgateway_test"


IdleTimeoutInMinutes  : 4
ProvisioningState     : Succeeded
Sku                   : Microsoft.Azure.Commands.Network.Models.PSNatGatewaySku
PublicIpAddresses     : {/subscriptions/<subid>/resourceGroups/natgateway_test/providers/Microsoft.Network/publicIPAddresses/Test_Pip}
PublicIpPrefixes      : {}
SkuText               : {
                          "Name": "Standard"
                        }
PublicIpAddressesText : [
                          {
                            "Id": "/subscriptions/<subid>/resourceGroups/natgateway_test/providers/Microsoft.Network/publicIPAddresses/Test_Pip"
                          }
                        ]
PublicIpPrefixesText  : []
ResourceGroupName     : natgateway_test
Location              : eastus2
ResourceGuid          :
Type                  : Microsoft.Network/natGateways
Tag                   :
TagsTable             :
Name                  : nat_gateway
Etag                  : W/"178470d2-7b86-4ddd-b954-e0cd3ab30a90"
Id                    : /subscriptions/<subid>/resourceGroups/natgateway_test/providers/Microsoft.Network/natGateways/nat_gateway

IdleTimeoutInMinutes  : 4
ProvisioningState     : Succeeded
Sku                   : Microsoft.Azure.Commands.Network.Models.PSNatGatewaySku
PublicIpAddresses     : {}
PublicIpPrefixes      : {}
SkuText               : {
                          "Name": "Standard"
                        }
PublicIpAddressesText : []
PublicIpPrefixesText  : []
ResourceGroupName     : natgateway_test
Location              : eastus2
ResourceGuid          :
Type                  : Microsoft.Network/natGateways
Tag                   :
TagsTable             :
Name                  : ng1
Etag                  : W/"bdf98e30-d6c6-4af2-8f62-10d1fdaa6e84"
Id                    : /subscriptions/<subid>/resourceGroups/natgateway_test/providers/Microsoft.Network/natGateways/ng1


PS C:> Get-AzNatGateway -ResourceGroupName "natgateway_test" -Name "nat_gateway"


IdleTimeoutInMinutes  : 4
ProvisioningState     : Succeeded
Sku                   : Microsoft.Azure.Commands.Network.Models.PSNatGatewaySku
PublicIpAddresses     : {/subscriptions/<subid>/resourceGroups/natgateway_test/providers/Microsoft.Network/publicIPAddresses/Test_Pip}
PublicIpPrefixes      : {}
SkuText               : {
                          "Name": "Standard"
                        }
PublicIpAddressesText : [
                          {
                            "Id": "/subscriptions/<subid>/resourceGroups/natgateway_test/providers/Microsoft.Network/publicIPAddresses/Test_Pip"
                          }
                        ]
PublicIpPrefixesText  : []
ResourceGroupName     : natgateway_test
Location              : eastus2
ResourceGuid          :
Type                  : Microsoft.Network/natGateways
Tag                   :
TagsTable             :
Name                  : nat_gateway
Etag                  : W/"178470d2-7b86-4ddd-b954-e0cd3ab30a90"
Id                    : /subscriptions/<subid>/resourceGroups/natgateway_test/providers/Microsoft.Network/natGateways/nat_gateway

PS C:> Get-AzNatGateway -ResourceId "/subscriptions/<subid>/resourceGroups/natgateway_test/providers/Microsoft.Network/natGateways/nat_gateway"


IdleTimeoutInMinutes  : 4
ProvisioningState     : Succeeded
Sku                   : Microsoft.Azure.Commands.Network.Models.PSNatGatewaySku
PublicIpAddresses     : {/subscriptions/<subid>/resourceGroups/natgateway_test/providers/Microsoft.Network/publicIPAddresses/Test_Pip}
PublicIpPrefixes      : {}
SkuText               : {
                          "Name": "Standard"
                        }
PublicIpAddressesText : [
                          {
                            "Id": "/subscriptions/<subid>/resourceGroups/natgateway_test/providers/Microsoft.Network/publicIPAddresses/Test_Pip"
                          }
                        ]
PublicIpPrefixesText  : []
ResourceGroupName     : natgateway_test
Location              : eastus2
ResourceGuid          :
Type                  : Microsoft.Network/natGateways
Tag                   :
TagsTable             :
Name                  : nat_gateway
Etag                  : W/"178470d2-7b86-4ddd-b954-e0cd3ab30a90"
Id                    : /subscriptions/<subid>/resourceGroups/natgateway_test/providers/Microsoft.Network/natGateways/nat_gateway
```

## <span data-ttu-id="ee20d-112">OS</span><span class="sxs-lookup"><span data-stu-id="ee20d-112">PARAMETERS</span></span>

### <span data-ttu-id="ee20d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee20d-113">-DefaultProfile</span></span>
<span data-ttu-id="ee20d-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ee20d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ee20d-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="ee20d-115">-Name</span></span>
<span data-ttu-id="ee20d-116">O nome do gateway NAT.</span><span class="sxs-lookup"><span data-stu-id="ee20d-116">The name of the nat gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee20d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee20d-117">-ResourceGroupName</span></span>
<span data-ttu-id="ee20d-118">O nome do grupo de recursos do gateway NAT.</span><span class="sxs-lookup"><span data-stu-id="ee20d-118">The resource group name of the nat gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee20d-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ee20d-119">-ResourceId</span></span>
<span data-ttu-id="ee20d-120">ID do gateway NAT</span><span class="sxs-lookup"><span data-stu-id="ee20d-120">Nat Gateway Id</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee20d-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee20d-121">CommonParameters</span></span>
<span data-ttu-id="ee20d-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ee20d-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee20d-123">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ee20d-123">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee20d-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ee20d-124">INPUTS</span></span>

### <span data-ttu-id="ee20d-125">System. String</span><span class="sxs-lookup"><span data-stu-id="ee20d-125">System.String</span></span>

## <span data-ttu-id="ee20d-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ee20d-126">OUTPUTS</span></span>

### <span data-ttu-id="ee20d-127">Microsoft. Azure. Commands. Network. Models. PSNatGateway</span><span class="sxs-lookup"><span data-stu-id="ee20d-127">Microsoft.Azure.Commands.Network.Models.PSNatGateway</span></span>

## <span data-ttu-id="ee20d-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ee20d-128">NOTES</span></span>

## <span data-ttu-id="ee20d-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ee20d-129">RELATED LINKS</span></span>
