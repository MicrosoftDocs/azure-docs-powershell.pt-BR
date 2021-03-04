---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-AzContainerNicconfigipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzContainerNicConfigIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzContainerNicConfigIpConfig.md
ms.openlocfilehash: 6ed82377de2a87b3bc40d3d4e8dff6af751ed1f4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886210"
---
# <span data-ttu-id="f3a07-101">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="f3a07-101">New-AzContainerNicConfigIpConfig</span></span>

## <span data-ttu-id="f3a07-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f3a07-102">SYNOPSIS</span></span>
<span data-ttu-id="f3a07-103">Cria um objeto de configuração ip de configuração de contêiner.</span><span class="sxs-lookup"><span data-stu-id="f3a07-103">Creates a container nic configuration ip configuration object.</span></span>

## <span data-ttu-id="f3a07-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="f3a07-104">SYNTAX</span></span>

```
New-AzContainerNicConfigIpConfig -Name <String> -Subnet <PSSubnet> [-SubnetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f3a07-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="f3a07-105">DESCRIPTION</span></span>
<span data-ttu-id="f3a07-106">O cmdlet **New-AzContainerNicConfigIpConfig** cria uma nova configuração ip de configuração de interface de rede de contêiner.</span><span class="sxs-lookup"><span data-stu-id="f3a07-106">The **New-AzContainerNicConfigIpConfig** cmdlet creates a new container network interface configuration ip configuration.</span></span> 

## <span data-ttu-id="f3a07-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f3a07-107">EXAMPLES</span></span>

### <span data-ttu-id="f3a07-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f3a07-108">Example 1</span></span>
```powershell
$subnet = New-AzVirtualNetworkSubnetConfig -Name subnet -AddressPrefix 10.0.1.0/24

$vnet = New-AzVirtualNetwork -Name vnet -ResourceGroupName rg1 -Location "West US" -AddressPrefix 10.0.0.0/16 -Subnet $subnet

$containerNicConfigIpConfig = New-AzContainerNicConfigIpConfig -Name ipconfigprofile1 -Subnet $vnet.Subnets[0]

$containerNicConfig = New-AzContainerNicConfig -Name cnic -IpConfiguration containerNicConfigIpConfig

$networkProfile = New-AzNetworkProfile -Name np1 -Location "West US" -ResourceGroupName rg1 -ContainerNetworkInterfaceConfiguration $containerNicConfig
```

<span data-ttu-id="f3a07-109">Os dois primeiros comandos criam e inicializam uma vnet e uma sub-rede.</span><span class="sxs-lookup"><span data-stu-id="f3a07-109">The first two commands create and initialize a vnet and a subnet.</span></span> <span data-ttu-id="f3a07-110">O terceiro comando cria um perfil de configuração de ip de contêiner referenciando a sub-rede criada.</span><span class="sxs-lookup"><span data-stu-id="f3a07-110">The third command creates a container nic ip configuration profile referencing the created subnet.</span></span> <span data-ttu-id="f3a07-111">O quarto comando cria uma configuração de interface de rede de contêiner que fornece o perfil de configuração ip criado no comando anterior.</span><span class="sxs-lookup"><span data-stu-id="f3a07-111">The fourth command creates a container network interface configuration supplying the ip configuration profile created in the previous command.</span></span> <span data-ttu-id="f3a07-112">Por fim, o quinto comando cria um perfil de rede inicializado com a configuração da interface de rede do contêiner armazenada $containerNicConfig.</span><span class="sxs-lookup"><span data-stu-id="f3a07-112">Finally, the fifth command creates a network profile initialized with the container network interface configuration stored in $containerNicConfig.</span></span>

## <span data-ttu-id="f3a07-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="f3a07-113">PARAMETERS</span></span>

### <span data-ttu-id="f3a07-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3a07-114">-DefaultProfile</span></span>
<span data-ttu-id="f3a07-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f3a07-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f3a07-116">-Name</span><span class="sxs-lookup"><span data-stu-id="f3a07-116">-Name</span></span>
<span data-ttu-id="f3a07-117">Nome do perfil de configuração ip da interface de rede do contêiner.</span><span class="sxs-lookup"><span data-stu-id="f3a07-117">Name of the container network interface configuration ip configuration profile.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3a07-118">-Sub-rede</span><span class="sxs-lookup"><span data-stu-id="f3a07-118">-Subnet</span></span>
<span data-ttu-id="f3a07-119">Sub-rede</span><span class="sxs-lookup"><span data-stu-id="f3a07-119">Subnet</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSubnet
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3a07-120">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="f3a07-120">-SubnetId</span></span>
<span data-ttu-id="f3a07-121">SubnetId</span><span class="sxs-lookup"><span data-stu-id="f3a07-121">SubnetId</span></span>

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

### <span data-ttu-id="f3a07-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f3a07-122">-Confirm</span></span>
<span data-ttu-id="f3a07-123">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f3a07-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3a07-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f3a07-124">-WhatIf</span></span>
<span data-ttu-id="f3a07-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f3a07-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f3a07-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f3a07-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3a07-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3a07-127">CommonParameters</span></span>
<span data-ttu-id="f3a07-128">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3a07-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3a07-129">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3a07-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3a07-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f3a07-130">INPUTS</span></span>

### <span data-ttu-id="f3a07-131">Nenhum</span><span class="sxs-lookup"><span data-stu-id="f3a07-131">None</span></span>

## <span data-ttu-id="f3a07-132">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="f3a07-132">OUTPUTS</span></span>

### <span data-ttu-id="f3a07-133">Microsoft.Azure.Commands.Network.Models.PSContainerNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="f3a07-133">Microsoft.Azure.Commands.Network.Models.PSContainerNetworkInterfaceConfiguration</span></span>

## <span data-ttu-id="f3a07-134">NOTES</span><span class="sxs-lookup"><span data-stu-id="f3a07-134">NOTES</span></span>

## <span data-ttu-id="f3a07-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f3a07-135">RELATED LINKS</span></span>

[<span data-ttu-id="f3a07-136">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="f3a07-136">New-AzContainerNicConfig</span></span>](./New-AzContainerNicConfig.md)
