---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: CBDF4BCB-7EB3-4D64-B19C-1314D4AB84E4
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetwork.md
ms.openlocfilehash: ff2e1a820a2a1cc664969c1872aebe6b88fc415b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111682"
---
# <span data-ttu-id="7bca4-101">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="7bca4-101">Get-AzVirtualNetwork</span></span>

## <span data-ttu-id="7bca4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7bca4-102">SYNOPSIS</span></span>
<span data-ttu-id="7bca4-103">Obtém uma rede virtual em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="7bca4-103">Gets a virtual network in a resource group.</span></span>

## <span data-ttu-id="7bca4-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7bca4-104">SYNTAX</span></span>

### <span data-ttu-id="7bca4-105">Noexpand</span><span class="sxs-lookup"><span data-stu-id="7bca4-105">NoExpand</span></span>
```
Get-AzVirtualNetwork [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7bca4-106">Expandir</span><span class="sxs-lookup"><span data-stu-id="7bca4-106">Expand</span></span>
```
Get-AzVirtualNetwork -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7bca4-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="7bca4-107">DESCRIPTION</span></span>
<span data-ttu-id="7bca4-108">O cmdlet **Get-AzVirtualNetwork** obtém uma ou mais redes virtuais em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="7bca4-108">The **Get-AzVirtualNetwork** cmdlet gets one or more virtual networks n a resource group.</span></span>

## <span data-ttu-id="7bca4-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="7bca4-109">EXAMPLES</span></span>

### <span data-ttu-id="7bca4-110">1: Recuperar uma rede virtual</span><span class="sxs-lookup"><span data-stu-id="7bca4-110">1: Retrieve a virtual network</span></span>
```
Get-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup

Name                   : MyVirtualNetwork1
ResourceGroupName      : TestResourceGroup
Location               : eastus
Id                     : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup
                         /providers/Microsoft.Network/virtualNetworks/MyVirtualNetwork1
Etag                   : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid           : 00000000-0000-0000-0000-000000000000
ProvisioningState      : Succeeded
Tags                   :
AddressSpace           : {
                           "AddressPrefixes": [
                             "xx.x.x.x/x"
                           ]
                         }
DhcpOptions            : {}
Subnets                : []
VirtualNetworkPeerings : []
EnableDdosProtection   : false
DdosProtectionPlan     : null
```

<span data-ttu-id="7bca4-111">Esse comando obtém a rede virtual chamada MyVirtualNetwork no grupo de recursos TestResourceGroup</span><span class="sxs-lookup"><span data-stu-id="7bca4-111">This command gets the virtual network named MyVirtualNetwork in the resource group TestResourceGroup</span></span>

### <span data-ttu-id="7bca4-112">2: Listar redes virtuais usando filtro</span><span class="sxs-lookup"><span data-stu-id="7bca4-112">2: List virtual networks using filter</span></span>
```
Get-AzVirtualNetwork -Name MyVirtualNetwork*

Name                   : MyVirtualNetwork1
ResourceGroupName      : TestResourceGroup
Location               : eastus
Id                     : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup
                         /providers/Microsoft.Network/virtualNetworks/MyVirtualNetwork1
Etag                   : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid           : 00000000-0000-0000-0000-000000000000
ProvisioningState      : Succeeded
Tags                   :
AddressSpace           : {
                           "AddressPrefixes": [
                             "xx.x.x.x/x"
                           ]
                         }
DhcpOptions            : {}
Subnets                : []
VirtualNetworkPeerings : []
EnableDdosProtection   : false
DdosProtectionPlan     : null
```

<span data-ttu-id="7bca4-113">Esse comando obtém todas as redes virtuais que começam com "MyVirtualNetwork".</span><span class="sxs-lookup"><span data-stu-id="7bca4-113">This command gets all virtual networks that start with "MyVirtualNetwork".</span></span>

## <span data-ttu-id="7bca4-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7bca4-114">PARAMETERS</span></span>

### <span data-ttu-id="7bca4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7bca4-115">-DefaultProfile</span></span>
<span data-ttu-id="7bca4-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="7bca4-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7bca4-117">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="7bca4-117">-ExpandResource</span></span>
```yaml
Type: System.String
Parameter Sets: Expand
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7bca4-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="7bca4-118">-Name</span></span>
<span data-ttu-id="7bca4-119">Especifica o nome da rede virtual que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="7bca4-119">Specifies the name of the virtual network that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="7bca4-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7bca4-120">-ResourceGroupName</span></span>
<span data-ttu-id="7bca4-121">Especifica o nome do grupo de recursos ao que a rede virtual pertence.</span><span class="sxs-lookup"><span data-stu-id="7bca4-121">Specifies the name of the resource group that virtual network belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="7bca4-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7bca4-122">CommonParameters</span></span>
<span data-ttu-id="7bca4-123">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7bca4-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7bca4-124">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7bca4-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7bca4-125">Entradas</span><span class="sxs-lookup"><span data-stu-id="7bca4-125">INPUTS</span></span>

### <span data-ttu-id="7bca4-126">System.String</span><span class="sxs-lookup"><span data-stu-id="7bca4-126">System.String</span></span>

## <span data-ttu-id="7bca4-127">Saídas</span><span class="sxs-lookup"><span data-stu-id="7bca4-127">OUTPUTS</span></span>

### <span data-ttu-id="7bca4-128">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="7bca4-128">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="7bca4-129">Notas</span><span class="sxs-lookup"><span data-stu-id="7bca4-129">NOTES</span></span>

## <span data-ttu-id="7bca4-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7bca4-130">RELATED LINKS</span></span>

[<span data-ttu-id="7bca4-131">New-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="7bca4-131">New-AzVirtualNetwork</span></span>](./New-AzVirtualNetwork.md)

[<span data-ttu-id="7bca4-132">Remove-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="7bca4-132">Remove-AzVirtualNetwork</span></span>](./Remove-AzVirtualNetwork.md)

[<span data-ttu-id="7bca4-133">Set-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="7bca4-133">Set-AzVirtualNetwork</span></span>](./Set-AzVirtualNetwork.md)


