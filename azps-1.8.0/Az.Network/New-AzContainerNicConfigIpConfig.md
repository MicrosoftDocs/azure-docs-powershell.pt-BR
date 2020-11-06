---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-AzContainerNicconfigipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzContainerNicConfigIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzContainerNicConfigIpConfig.md
ms.openlocfilehash: 24cbdaebc21456268d050b5c3a56ec9fc443fedf
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93600363"
---
# <span data-ttu-id="c7dc1-101">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="c7dc1-101">New-AzContainerNicConfigIpConfig</span></span>

## <span data-ttu-id="c7dc1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c7dc1-102">SYNOPSIS</span></span>
<span data-ttu-id="c7dc1-103">Cria um objeto de configuração de IP de configuração de NIC de contêiner.</span><span class="sxs-lookup"><span data-stu-id="c7dc1-103">Creates a container nic configuration ip configuration object.</span></span>

## <span data-ttu-id="c7dc1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c7dc1-104">SYNTAX</span></span>

```
New-AzContainerNicConfigIpConfig -Name <String> -Subnet <PSSubnet> [-SubnetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c7dc1-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c7dc1-105">DESCRIPTION</span></span>
<span data-ttu-id="c7dc1-106">O cmdlet **New-AzContainerNicConfigIpConfig** cria uma nova configuração de IP de configuração de interface de rede de contêiner.</span><span class="sxs-lookup"><span data-stu-id="c7dc1-106">The **New-AzContainerNicConfigIpConfig** cmdlet creates a new container network interface configuration ip configuration.</span></span> 

## <span data-ttu-id="c7dc1-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c7dc1-107">EXAMPLES</span></span>

### <span data-ttu-id="c7dc1-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c7dc1-108">Example 1</span></span>
```powershell
$subnet = New-AzVirtualNetworkSubnetConfig -Name subnet -AddressPrefix 10.0.1.0/24

$vnet = New-AzVirtualNetwork -Name vnet -ResourceGroupName rg1 -Location "West US" -AddressPrefix 10.0.0.0/16 -Subnet $subnet

$containerNicConfigIpConfig = New-AzContainerNicConfigIpConfig -Name ipconfigprofile1 -Subnet $vnet.Subnets[0]

$containerNicConfig = New-AzContainerNicConfig -Name cnic -IpConfiguration containerNicConfigIpConfig

$networkProfile = New-AzNetworkProfile -Name np1 -Location "West US" -ResourceGroupName rg1 -ContainerNetworkInterfaceConfiguration $containerNicConfig
```

<span data-ttu-id="c7dc1-109">Os dois primeiros comandos criam e inicializam uma rede virtual e uma sub-rede.</span><span class="sxs-lookup"><span data-stu-id="c7dc1-109">The first two commands create and initialize a vnet and a subnet.</span></span> <span data-ttu-id="c7dc1-110">O terceiro comando cria um perfil de configuração de IP de NIC de contêiner que faz referência à sub-rede criada.</span><span class="sxs-lookup"><span data-stu-id="c7dc1-110">The third command creates a container nic ip configuration profile referencing the created subnet.</span></span> <span data-ttu-id="c7dc1-111">O quarto comando cria uma configuração de interface de rede de contêiner que fornece o perfil de configuração de IP criado no comando anterior.</span><span class="sxs-lookup"><span data-stu-id="c7dc1-111">The fourth command creates a container network interface configuration supplying the ip configuration profile created in the previous command.</span></span> <span data-ttu-id="c7dc1-112">Por fim, o quinto comando cria um perfil de rede inicializado com a configuração de interface de rede de contêiner armazenada em $containerNicConfig.</span><span class="sxs-lookup"><span data-stu-id="c7dc1-112">Finally, the fifth command creates a network profile initialized with the container network interface configuration stored in $containerNicConfig.</span></span>

## <span data-ttu-id="c7dc1-113">OS</span><span class="sxs-lookup"><span data-stu-id="c7dc1-113">PARAMETERS</span></span>

### <span data-ttu-id="c7dc1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7dc1-114">-DefaultProfile</span></span>
<span data-ttu-id="c7dc1-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c7dc1-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c7dc1-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="c7dc1-116">-Name</span></span>
<span data-ttu-id="c7dc1-117">Nome do perfil de configuração de IP da configuração de interface de rede do contêiner.</span><span class="sxs-lookup"><span data-stu-id="c7dc1-117">Name of the container network interface configuration ip configuration profile.</span></span>

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

### <span data-ttu-id="c7dc1-118">-Subnet</span><span class="sxs-lookup"><span data-stu-id="c7dc1-118">-Subnet</span></span>
<span data-ttu-id="c7dc1-119">Redes</span><span class="sxs-lookup"><span data-stu-id="c7dc1-119">Subnet</span></span>

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

### <span data-ttu-id="c7dc1-120">-Subnetid</span><span class="sxs-lookup"><span data-stu-id="c7dc1-120">-SubnetId</span></span>
<span data-ttu-id="c7dc1-121">Subnetid</span><span class="sxs-lookup"><span data-stu-id="c7dc1-121">SubnetId</span></span>

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

### <span data-ttu-id="c7dc1-122">-Confirme</span><span class="sxs-lookup"><span data-stu-id="c7dc1-122">-Confirm</span></span>
<span data-ttu-id="c7dc1-123">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c7dc1-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c7dc1-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c7dc1-124">-WhatIf</span></span>
<span data-ttu-id="c7dc1-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c7dc1-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c7dc1-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c7dc1-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c7dc1-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7dc1-127">CommonParameters</span></span>
<span data-ttu-id="c7dc1-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c7dc1-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7dc1-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c7dc1-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7dc1-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c7dc1-130">INPUTS</span></span>

### <span data-ttu-id="c7dc1-131">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="c7dc1-131">None</span></span>

## <span data-ttu-id="c7dc1-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c7dc1-132">OUTPUTS</span></span>

### <span data-ttu-id="c7dc1-133">Microsoft. Azure. Commands. Network. Models. PSContainerNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="c7dc1-133">Microsoft.Azure.Commands.Network.Models.PSContainerNetworkInterfaceConfiguration</span></span>

## <span data-ttu-id="c7dc1-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c7dc1-134">NOTES</span></span>

## <span data-ttu-id="c7dc1-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c7dc1-135">RELATED LINKS</span></span>

[<span data-ttu-id="c7dc1-136">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="c7dc1-136">New-AzContainerNicConfig</span></span>](./New-AzContainerNicConfig.md)
