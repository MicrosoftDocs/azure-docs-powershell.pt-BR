---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-AzContainerNicconfigipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzContainerNicConfigIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzContainerNicConfigIpConfig.md
ms.openlocfilehash: 2e15819fe8b6b21b0f0c0751dc39736408606a7c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98263954"
---
# <span data-ttu-id="a3827-101">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="a3827-101">New-AzContainerNicConfigIpConfig</span></span>

## <span data-ttu-id="a3827-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a3827-102">SYNOPSIS</span></span>
<span data-ttu-id="a3827-103">Cria um objeto de configuração de IP de configuração de NIC de contêiner.</span><span class="sxs-lookup"><span data-stu-id="a3827-103">Creates a container nic configuration ip configuration object.</span></span>

## <span data-ttu-id="a3827-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a3827-104">SYNTAX</span></span>

```
New-AzContainerNicConfigIpConfig -Name <String> -Subnet <PSSubnet> [-SubnetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a3827-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a3827-105">DESCRIPTION</span></span>
<span data-ttu-id="a3827-106">O cmdlet **New-AzContainerNicConfigIpConfig** cria uma nova configuração de IP de configuração de interface de rede de contêiner.</span><span class="sxs-lookup"><span data-stu-id="a3827-106">The **New-AzContainerNicConfigIpConfig** cmdlet creates a new container network interface configuration ip configuration.</span></span> 

## <span data-ttu-id="a3827-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a3827-107">EXAMPLES</span></span>

### <span data-ttu-id="a3827-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a3827-108">Example 1</span></span>
```powershell
$subnet = New-AzVirtualNetworkSubnetConfig -Name subnet -AddressPrefix 10.0.1.0/24

$vnet = New-AzVirtualNetwork -Name vnet -ResourceGroupName rg1 -Location "West US" -AddressPrefix 10.0.0.0/16 -Subnet $subnet

$containerNicConfigIpConfig = New-AzContainerNicConfigIpConfig -Name ipconfigprofile1 -Subnet $vnet.Subnets[0]

$containerNicConfig = New-AzContainerNicConfig -Name cnic -IpConfiguration containerNicConfigIpConfig

$networkProfile = New-AzNetworkProfile -Name np1 -Location "West US" -ResourceGroupName rg1 -ContainerNetworkInterfaceConfiguration $containerNicConfig
```

<span data-ttu-id="a3827-109">Os dois primeiros comandos criam e inicializam uma rede virtual e uma sub-rede.</span><span class="sxs-lookup"><span data-stu-id="a3827-109">The first two commands create and initialize a vnet and a subnet.</span></span> <span data-ttu-id="a3827-110">O terceiro comando cria um perfil de configuração de IP de NIC de contêiner que faz referência à sub-rede criada.</span><span class="sxs-lookup"><span data-stu-id="a3827-110">The third command creates a container nic ip configuration profile referencing the created subnet.</span></span> <span data-ttu-id="a3827-111">O quarto comando cria uma configuração de interface de rede de contêiner que fornece o perfil de configuração de IP criado no comando anterior.</span><span class="sxs-lookup"><span data-stu-id="a3827-111">The fourth command creates a container network interface configuration supplying the ip configuration profile created in the previous command.</span></span> <span data-ttu-id="a3827-112">Por fim, o quinto comando cria um perfil de rede inicializado com a configuração de interface de rede de contêiner armazenada em $containerNicConfig.</span><span class="sxs-lookup"><span data-stu-id="a3827-112">Finally, the fifth command creates a network profile initialized with the container network interface configuration stored in $containerNicConfig.</span></span>

## <span data-ttu-id="a3827-113">OS</span><span class="sxs-lookup"><span data-stu-id="a3827-113">PARAMETERS</span></span>

### <span data-ttu-id="a3827-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3827-114">-DefaultProfile</span></span>
<span data-ttu-id="a3827-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a3827-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a3827-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="a3827-116">-Name</span></span>
<span data-ttu-id="a3827-117">Nome do perfil de configuração de IP da configuração de interface de rede do contêiner.</span><span class="sxs-lookup"><span data-stu-id="a3827-117">Name of the container network interface configuration ip configuration profile.</span></span>

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

### <span data-ttu-id="a3827-118">-Subnet</span><span class="sxs-lookup"><span data-stu-id="a3827-118">-Subnet</span></span>
<span data-ttu-id="a3827-119">Redes</span><span class="sxs-lookup"><span data-stu-id="a3827-119">Subnet</span></span>

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

### <span data-ttu-id="a3827-120">-Subnetid</span><span class="sxs-lookup"><span data-stu-id="a3827-120">-SubnetId</span></span>
<span data-ttu-id="a3827-121">Subnetid</span><span class="sxs-lookup"><span data-stu-id="a3827-121">SubnetId</span></span>

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

### <span data-ttu-id="a3827-122">-Confirme</span><span class="sxs-lookup"><span data-stu-id="a3827-122">-Confirm</span></span>
<span data-ttu-id="a3827-123">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a3827-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a3827-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a3827-124">-WhatIf</span></span>
<span data-ttu-id="a3827-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a3827-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a3827-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a3827-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a3827-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3827-127">CommonParameters</span></span>
<span data-ttu-id="a3827-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3827-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3827-129">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a3827-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3827-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a3827-130">INPUTS</span></span>

### <span data-ttu-id="a3827-131">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="a3827-131">None</span></span>

## <span data-ttu-id="a3827-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a3827-132">OUTPUTS</span></span>

### <span data-ttu-id="a3827-133">Microsoft. Azure. Commands. Network. Models. PSContainerNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="a3827-133">Microsoft.Azure.Commands.Network.Models.PSContainerNetworkInterfaceConfiguration</span></span>

## <span data-ttu-id="a3827-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a3827-134">NOTES</span></span>

## <span data-ttu-id="a3827-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a3827-135">RELATED LINKS</span></span>

[<span data-ttu-id="a3827-136">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="a3827-136">New-AzContainerNicConfig</span></span>](./New-AzContainerNicConfig.md)
