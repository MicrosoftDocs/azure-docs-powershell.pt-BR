---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azprivatelinkservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateLinkService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateLinkService.md
ms.openlocfilehash: 4401ae153fc237d1f1bc9ccfa870e5cecc1e2c33
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93772756"
---
# <span data-ttu-id="6494a-101">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="6494a-101">Set-AzPrivateLinkService</span></span>

## <span data-ttu-id="6494a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6494a-102">SYNOPSIS</span></span>
<span data-ttu-id="6494a-103">Atualiza um serviço de link particular.</span><span class="sxs-lookup"><span data-stu-id="6494a-103">Updates a private link service.</span></span>

## <span data-ttu-id="6494a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6494a-104">SYNTAX</span></span>

```
Set-AzPrivateLinkService -PrivateLinkService <PSPrivateLinkService> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6494a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6494a-105">DESCRIPTION</span></span>
<span data-ttu-id="6494a-106">O cmdlet **set-AzPrivateLinkService** atualiza um serviço de link particular.</span><span class="sxs-lookup"><span data-stu-id="6494a-106">The **Set-AzPrivateLinkService** cmdlet updates a private link service.</span></span>

## <span data-ttu-id="6494a-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6494a-107">EXAMPLES</span></span>

### <span data-ttu-id="6494a-108">1: cria um serviço de vínculo particular e atualiza seu</span><span class="sxs-lookup"><span data-stu-id="6494a-108">1: Creates a private link service and update its</span></span>
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

<span data-ttu-id="6494a-109">Este exemplo cria um serviço de link privado chamado mypls.</span><span class="sxs-lookup"><span data-stu-id="6494a-109">This example creates a private link service called mypls.</span></span> <span data-ttu-id="6494a-110">Em seguida, substitua suas ipConfigurations do objeto ipConfiguratiuon na memória.</span><span class="sxs-lookup"><span data-stu-id="6494a-110">Then it replace its ipConfigurations from the in-memory ipConfiguratiuon object.</span></span> <span data-ttu-id="6494a-111">O cmdlet Set-AzPrivateLinkService é usado para gravar o estado do serviço de link particular modificado no lado do serviço.</span><span class="sxs-lookup"><span data-stu-id="6494a-111">The Set-AzPrivateLinkService cmdlet is then used to write the modified private link service state on the service side.</span></span> 

## <span data-ttu-id="6494a-112">OS</span><span class="sxs-lookup"><span data-stu-id="6494a-112">PARAMETERS</span></span>

### <span data-ttu-id="6494a-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6494a-113">-AsJob</span></span>
<span data-ttu-id="6494a-114">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="6494a-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6494a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6494a-115">-DefaultProfile</span></span>
<span data-ttu-id="6494a-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6494a-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6494a-117">-PrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="6494a-117">-PrivateLinkService</span></span>
<span data-ttu-id="6494a-118">Especifica um objeto de serviço de link privado que representa o estado para o qual o serviço de link privado deve ser definido.</span><span class="sxs-lookup"><span data-stu-id="6494a-118">Specifies a private link service object representing the state to which the private link service should be set.</span></span>

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

### <span data-ttu-id="6494a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6494a-119">CommonParameters</span></span>
<span data-ttu-id="6494a-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6494a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6494a-121">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6494a-121">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6494a-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6494a-122">INPUTS</span></span>

### <span data-ttu-id="6494a-123">Microsoft. Azure. Commands. Network. Models. PSPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="6494a-123">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="6494a-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6494a-124">OUTPUTS</span></span>

### <span data-ttu-id="6494a-125">Microsoft. Azure. Commands. Network. Models. PSPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="6494a-125">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="6494a-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6494a-126">NOTES</span></span>

## <span data-ttu-id="6494a-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6494a-127">RELATED LINKS</span></span>

[<span data-ttu-id="6494a-128">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="6494a-128">Get-AzPrivateLinkService</span></span>](./Get-AzPrivateLinkService.md)

[<span data-ttu-id="6494a-129">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="6494a-129">New-AzPrivateLinkService</span></span>](./New-AzPrivateLinkService.md)

[<span data-ttu-id="6494a-130">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="6494a-130">Remove-AzPrivateLinkService</span></span>](./Remove-AzPrivateLinkService.md)

