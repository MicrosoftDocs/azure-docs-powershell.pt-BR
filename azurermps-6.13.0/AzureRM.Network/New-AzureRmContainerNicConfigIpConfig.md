---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-AzureRmNetworkProfileContainerNicconfigipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmContainerNicConfigIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmContainerNicConfigIpConfig.md
ms.openlocfilehash: 0a2157d006277aa491281c51f1c3b7a910b8a5c9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431360"
---
# <span data-ttu-id="6cf88-101">New-AzureRmNetworkProfileContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="6cf88-101">New-AzureRmNetworkProfileContainerNicConfigIpConfig</span></span>

## <span data-ttu-id="6cf88-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6cf88-102">SYNOPSIS</span></span>
<span data-ttu-id="6cf88-103">Cria um objeto de configuração de IP de configuração de NIC de contêiner.</span><span class="sxs-lookup"><span data-stu-id="6cf88-103">Creates a container nic configuration ip configuration object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6cf88-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6cf88-104">SYNTAX</span></span>

```
New-AzureRmNetworkProfileContainerNicConfigIpConfig -Name <String> -Subnet <PSSubnet> [-SubnetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6cf88-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6cf88-105">DESCRIPTION</span></span>
<span data-ttu-id="6cf88-106">O cmdlet **New-AzureRmNetworkProfileContainerNicConfigIpConfig** cria uma nova configuração de IP de configuração de interface de rede de contêiner.</span><span class="sxs-lookup"><span data-stu-id="6cf88-106">The **New-AzureRmNetworkProfileContainerNicConfigIpConfig** cmdlet creates a new container network interface configuration ip configuration.</span></span> 

## <span data-ttu-id="6cf88-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6cf88-107">EXAMPLES</span></span>

### <span data-ttu-id="6cf88-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="6cf88-108">Example 1</span></span>
```powershell
$subnet = New-AzureRmVirtualNetworkSubnetConfig -Name subnet -AddressPrefix 10.0.1.0/24

$vnet = New-AzureRmVirtualNetwork -Name vnet -ResourceGroupName rg1 -Location "West US" -AddressPrefix 10.0.0.0/16 -Subnet $subnet

$containerNicConfigIpConfig = New-AzureRmNetworkProfileContainerNicConfigIpConfig -Name ipconfigprofile1 -Subnet $vnet.Subnets[0]

$containerNicConfig = New-AzureRmNetworkProfileContainerNicConfig -Name cnic -IpConfiguration containerNicConfigIpConfig

$networkProfile = New-AzureRmNetworkProfile -Name np1 -Location "West US" -ResourceGroupName rg1 -ContainerNetworkInterfaceConfiguration $containerNicConfig
```

<span data-ttu-id="6cf88-109">Os dois primeiros comandos criam e inicializam uma rede virtual e uma sub-rede.</span><span class="sxs-lookup"><span data-stu-id="6cf88-109">The first two commands create and initialize a vnet and a subnet.</span></span> <span data-ttu-id="6cf88-110">O terceiro comando cria um perfil de configuração de IP de NIC de contêiner que faz referência à sub-rede criada.</span><span class="sxs-lookup"><span data-stu-id="6cf88-110">The third command creates a container nic ip configuration profile referencing the created subnet.</span></span>  <span data-ttu-id="6cf88-111">O quarto comando cria uma configuração de interface de rede de contêiner que fornece o perfil de configuração de IP criado no comando anterior.</span><span class="sxs-lookup"><span data-stu-id="6cf88-111">The fourth command creates a container network interface configuration supplying the ip configuration profile created in the previous command.</span></span> <span data-ttu-id="6cf88-112">Por fim, o quinto comando cria um perfil de rede inicializado com a configuração de interface de rede de contêiner armazenada em $containerNicConfig.</span><span class="sxs-lookup"><span data-stu-id="6cf88-112">Finally, the fifth command creates a network profile initialized with the container network interface configuration stored in $containerNicConfig.</span></span>

## <span data-ttu-id="6cf88-113">OS</span><span class="sxs-lookup"><span data-stu-id="6cf88-113">PARAMETERS</span></span>

### <span data-ttu-id="6cf88-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6cf88-114">-DefaultProfile</span></span>
<span data-ttu-id="6cf88-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6cf88-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6cf88-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="6cf88-116">-Name</span></span>
<span data-ttu-id="6cf88-117">Nome do perfil de configuração de IP da configuração de interface de rede do contêiner.</span><span class="sxs-lookup"><span data-stu-id="6cf88-117">Name of the container network interface configuration ip configuration profile.</span></span>

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

### <span data-ttu-id="6cf88-118">-Subnet</span><span class="sxs-lookup"><span data-stu-id="6cf88-118">-Subnet</span></span>
<span data-ttu-id="6cf88-119">Redes</span><span class="sxs-lookup"><span data-stu-id="6cf88-119">Subnet</span></span>

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

### <span data-ttu-id="6cf88-120">-Subnetid</span><span class="sxs-lookup"><span data-stu-id="6cf88-120">-SubnetId</span></span>
<span data-ttu-id="6cf88-121">Subnetid</span><span class="sxs-lookup"><span data-stu-id="6cf88-121">SubnetId</span></span>

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

### <span data-ttu-id="6cf88-122">-Confirme</span><span class="sxs-lookup"><span data-stu-id="6cf88-122">-Confirm</span></span>
<span data-ttu-id="6cf88-123">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6cf88-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6cf88-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6cf88-124">-WhatIf</span></span>
<span data-ttu-id="6cf88-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="6cf88-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6cf88-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6cf88-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6cf88-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6cf88-127">CommonParameters</span></span>
<span data-ttu-id="6cf88-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6cf88-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6cf88-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6cf88-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6cf88-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6cf88-130">INPUTS</span></span>

### <span data-ttu-id="6cf88-131">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="6cf88-131">None</span></span>

## <span data-ttu-id="6cf88-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6cf88-132">OUTPUTS</span></span>

### <span data-ttu-id="6cf88-133">Microsoft. Azure. Commands. Network. Models. PSContainerNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="6cf88-133">Microsoft.Azure.Commands.Network.Models.PSContainerNetworkInterfaceConfiguration</span></span>

## <span data-ttu-id="6cf88-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6cf88-134">NOTES</span></span>

## <span data-ttu-id="6cf88-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6cf88-135">RELATED LINKS</span></span>
