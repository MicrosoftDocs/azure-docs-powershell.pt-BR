---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: CBDF4BCB-7EB3-4D64-B19C-1314D4AB84E4
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetwork.md
ms.openlocfilehash: ff2e1a820a2a1cc664969c1872aebe6b88fc415b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94118126"
---
# <span data-ttu-id="202d2-101">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="202d2-101">Get-AzVirtualNetwork</span></span>

## <span data-ttu-id="202d2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="202d2-102">SYNOPSIS</span></span>
<span data-ttu-id="202d2-103">Obtém uma rede virtual em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="202d2-103">Gets a virtual network in a resource group.</span></span>

## <span data-ttu-id="202d2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="202d2-104">SYNTAX</span></span>

### <span data-ttu-id="202d2-105">NOEXPAND</span><span class="sxs-lookup"><span data-stu-id="202d2-105">NoExpand</span></span>
```
Get-AzVirtualNetwork [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="202d2-106">Amplie</span><span class="sxs-lookup"><span data-stu-id="202d2-106">Expand</span></span>
```
Get-AzVirtualNetwork -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="202d2-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="202d2-107">DESCRIPTION</span></span>
<span data-ttu-id="202d2-108">O cmdlet **Get-AzVirtualNetwork** Obtém uma ou mais redes virtuais n um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="202d2-108">The **Get-AzVirtualNetwork** cmdlet gets one or more virtual networks n a resource group.</span></span>

## <span data-ttu-id="202d2-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="202d2-109">EXAMPLES</span></span>

### <span data-ttu-id="202d2-110">1: recuperar uma rede virtual</span><span class="sxs-lookup"><span data-stu-id="202d2-110">1: Retrieve a virtual network</span></span>
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

<span data-ttu-id="202d2-111">Esse comando obtém a rede virtual chamada MyVirtualNetwork na TestResourceGroup do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="202d2-111">This command gets the virtual network named MyVirtualNetwork in the resource group TestResourceGroup</span></span>

### <span data-ttu-id="202d2-112">2: listar redes virtuais usando filtro</span><span class="sxs-lookup"><span data-stu-id="202d2-112">2: List virtual networks using filter</span></span>
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

<span data-ttu-id="202d2-113">Esse comando obtém todas as redes virtuais que começam com "MyVirtualNetwork".</span><span class="sxs-lookup"><span data-stu-id="202d2-113">This command gets all virtual networks that start with "MyVirtualNetwork".</span></span>

## <span data-ttu-id="202d2-114">OS</span><span class="sxs-lookup"><span data-stu-id="202d2-114">PARAMETERS</span></span>

### <span data-ttu-id="202d2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="202d2-115">-DefaultProfile</span></span>
<span data-ttu-id="202d2-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="202d2-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="202d2-117">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="202d2-117">-ExpandResource</span></span>
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

### <span data-ttu-id="202d2-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="202d2-118">-Name</span></span>
<span data-ttu-id="202d2-119">Especifica o nome da rede virtual obtida por esse cmdlet.</span><span class="sxs-lookup"><span data-stu-id="202d2-119">Specifies the name of the virtual network that this cmdlet gets.</span></span>

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

### <span data-ttu-id="202d2-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="202d2-120">-ResourceGroupName</span></span>
<span data-ttu-id="202d2-121">Especifica o nome do grupo de recursos ao qual a rede virtual pertence.</span><span class="sxs-lookup"><span data-stu-id="202d2-121">Specifies the name of the resource group that virtual network belongs to.</span></span>

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

### <span data-ttu-id="202d2-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="202d2-122">CommonParameters</span></span>
<span data-ttu-id="202d2-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="202d2-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="202d2-124">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="202d2-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="202d2-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="202d2-125">INPUTS</span></span>

### <span data-ttu-id="202d2-126">System. String</span><span class="sxs-lookup"><span data-stu-id="202d2-126">System.String</span></span>

## <span data-ttu-id="202d2-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="202d2-127">OUTPUTS</span></span>

### <span data-ttu-id="202d2-128">Microsoft. Azure. Commands. Network. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="202d2-128">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="202d2-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="202d2-129">NOTES</span></span>

## <span data-ttu-id="202d2-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="202d2-130">RELATED LINKS</span></span>

[<span data-ttu-id="202d2-131">New-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="202d2-131">New-AzVirtualNetwork</span></span>](./New-AzVirtualNetwork.md)

[<span data-ttu-id="202d2-132">Remove-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="202d2-132">Remove-AzVirtualNetwork</span></span>](./Remove-AzVirtualNetwork.md)

[<span data-ttu-id="202d2-133">Set-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="202d2-133">Set-AzVirtualNetwork</span></span>](./Set-AzVirtualNetwork.md)


