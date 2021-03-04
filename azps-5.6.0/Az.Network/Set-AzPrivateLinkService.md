---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-azprivatelinkservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateLinkService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateLinkService.md
ms.openlocfilehash: fc0e3ad0bcc86a0ad49450393a79c6c60540ba23
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891784"
---
# <span data-ttu-id="85c9d-101">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="85c9d-101">Set-AzPrivateLinkService</span></span>

## <span data-ttu-id="85c9d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="85c9d-102">SYNOPSIS</span></span>
<span data-ttu-id="85c9d-103">Atualiza um serviço de link privado.</span><span class="sxs-lookup"><span data-stu-id="85c9d-103">Updates a private link service.</span></span>

## <span data-ttu-id="85c9d-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="85c9d-104">SYNTAX</span></span>

```
Set-AzPrivateLinkService -PrivateLinkService <PSPrivateLinkService> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="85c9d-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="85c9d-105">DESCRIPTION</span></span>
<span data-ttu-id="85c9d-106">O cmdlet **Set-AzPrivateLinkService** atualiza um serviço de link privado.</span><span class="sxs-lookup"><span data-stu-id="85c9d-106">The **Set-AzPrivateLinkService** cmdlet updates a private link service.</span></span>

## <span data-ttu-id="85c9d-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="85c9d-107">EXAMPLES</span></span>

### <span data-ttu-id="85c9d-108">1: cria um serviço de link privado e atualiza seu</span><span class="sxs-lookup"><span data-stu-id="85c9d-108">1: Creates a private link service and update its</span></span>
```
$vnet = Get-AzVirtualNetwork -ResourceName "myvnet" -ResourceGroupName "myresourcegroup"
$IPConfig = New-AzPrivateLinkServiceIpConfig -Name "IP-Config" -Subnet $vnet.subnets[1] -PrivateIpAddress "10.0.0.5"
$publicip = Get-AzPublicIpAddress -ResourceGroupName "myresourcegroup"
$frontend = New-AzLoadBalancerFrontendIpConfig -Name "FrontendIpConfig01" -PublicIpAddress $publicip
$lb = New-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "myresourcegroup" -Location "West US" -FrontendIpConfiguration $frontend  
$privateLinkService = New-AzPrivateLinkService -ServiceName "mypls" -ResourceGroupName myresourcegroup -Location "West US" -LoadBalancerFrontendIpConfiguration $frontend -IpConfiguration $IPConfig

$newIPConfig = New-AzPrivateLinkServiceIpConfig -Name "New-IP-Config" -Subnet $vnet.subnets[0] 
$privateLinkService.IpConfigurations[0] = $newIPConfig
$privateLinkService | Set-AzPrivateLinkService
```

<span data-ttu-id="85c9d-109">Este exemplo cria um serviço de link privado chamado mypls.</span><span class="sxs-lookup"><span data-stu-id="85c9d-109">This example creates a private link service called mypls.</span></span> <span data-ttu-id="85c9d-110">Em seguida, ele substitui seus ipConfigurations do objeto ipConfiguratiuon na memória.</span><span class="sxs-lookup"><span data-stu-id="85c9d-110">Then it replace its ipConfigurations from the in-memory ipConfiguratiuon object.</span></span> <span data-ttu-id="85c9d-111">O Set-AzPrivateLinkService cmdlet é usado para gravar o estado do serviço de link privado modificado no lado do serviço.</span><span class="sxs-lookup"><span data-stu-id="85c9d-111">The Set-AzPrivateLinkService cmdlet is then used to write the modified private link service state on the service side.</span></span> 

## <span data-ttu-id="85c9d-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="85c9d-112">PARAMETERS</span></span>

### <span data-ttu-id="85c9d-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="85c9d-113">-AsJob</span></span>
<span data-ttu-id="85c9d-114">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="85c9d-114">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85c9d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85c9d-115">-DefaultProfile</span></span>
<span data-ttu-id="85c9d-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="85c9d-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="85c9d-117">-PrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="85c9d-117">-PrivateLinkService</span></span>
<span data-ttu-id="85c9d-118">Especifica um objeto de serviço de link privado que representa o estado ao qual o serviço de link privado deve ser definido.</span><span class="sxs-lookup"><span data-stu-id="85c9d-118">Specifies a private link service object representing the state to which the private link service should be set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="85c9d-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85c9d-119">CommonParameters</span></span>
<span data-ttu-id="85c9d-120">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85c9d-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85c9d-121">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="85c9d-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85c9d-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="85c9d-122">INPUTS</span></span>

### <span data-ttu-id="85c9d-123">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="85c9d-123">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="85c9d-124">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="85c9d-124">OUTPUTS</span></span>

### <span data-ttu-id="85c9d-125">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="85c9d-125">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="85c9d-126">NOTES</span><span class="sxs-lookup"><span data-stu-id="85c9d-126">NOTES</span></span>

## <span data-ttu-id="85c9d-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="85c9d-127">RELATED LINKS</span></span>

[<span data-ttu-id="85c9d-128">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="85c9d-128">Get-AzPrivateLinkService</span></span>](./Get-AzPrivateLinkService.md)

[<span data-ttu-id="85c9d-129">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="85c9d-129">New-AzPrivateLinkService</span></span>](./New-AzPrivateLinkService.md)

[<span data-ttu-id="85c9d-130">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="85c9d-130">Remove-AzPrivateLinkService</span></span>](./Remove-AzPrivateLinkService.md)


