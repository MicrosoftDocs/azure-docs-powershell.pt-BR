---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azprivatelinkservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateLinkService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateLinkService.md
ms.openlocfilehash: a594e23505b9db1004a086ff4e0c168353c6bc28
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112759"
---
# <span data-ttu-id="76cc1-101">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="76cc1-101">Set-AzPrivateLinkService</span></span>

## <span data-ttu-id="76cc1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="76cc1-102">SYNOPSIS</span></span>
<span data-ttu-id="76cc1-103">Atualiza um serviço de link particular.</span><span class="sxs-lookup"><span data-stu-id="76cc1-103">Updates a private link service.</span></span>

## <span data-ttu-id="76cc1-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="76cc1-104">SYNTAX</span></span>

```
Set-AzPrivateLinkService -PrivateLinkService <PSPrivateLinkService> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="76cc1-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="76cc1-105">DESCRIPTION</span></span>
<span data-ttu-id="76cc1-106">O **cmdlet Set-AzPrivateLinkService** atualiza um serviço de link particular.</span><span class="sxs-lookup"><span data-stu-id="76cc1-106">The **Set-AzPrivateLinkService** cmdlet updates a private link service.</span></span>

## <span data-ttu-id="76cc1-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="76cc1-107">EXAMPLES</span></span>

### <span data-ttu-id="76cc1-108">1: Cria um serviço de link particular e atualiza seu</span><span class="sxs-lookup"><span data-stu-id="76cc1-108">1: Creates a private link service and update its</span></span>
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

<span data-ttu-id="76cc1-109">Este exemplo cria um serviço de link particular chamado mypls.</span><span class="sxs-lookup"><span data-stu-id="76cc1-109">This example creates a private link service called mypls.</span></span> <span data-ttu-id="76cc1-110">Em seguida, ele substitui suas ipConfigurações do objeto ipConfiguratiuon na memória.</span><span class="sxs-lookup"><span data-stu-id="76cc1-110">Then it replace its ipConfigurations from the in-memory ipConfiguratiuon object.</span></span> <span data-ttu-id="76cc1-111">O Set-AzPrivateLinkService cmdlet é usado para gravar o estado de serviço de link particular modificado no lado do serviço.</span><span class="sxs-lookup"><span data-stu-id="76cc1-111">The Set-AzPrivateLinkService cmdlet is then used to write the modified private link service state on the service side.</span></span> 

## <span data-ttu-id="76cc1-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="76cc1-112">PARAMETERS</span></span>

### <span data-ttu-id="76cc1-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="76cc1-113">-AsJob</span></span>
<span data-ttu-id="76cc1-114">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="76cc1-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="76cc1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76cc1-115">-DefaultProfile</span></span>
<span data-ttu-id="76cc1-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="76cc1-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="76cc1-117">-PrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="76cc1-117">-PrivateLinkService</span></span>
<span data-ttu-id="76cc1-118">Especifica um objeto de serviço de link privado que representa o estado ao qual o serviço de vinculação particular deve ser definido.</span><span class="sxs-lookup"><span data-stu-id="76cc1-118">Specifies a private link service object representing the state to which the private link service should be set.</span></span>

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

### <span data-ttu-id="76cc1-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76cc1-119">CommonParameters</span></span>
<span data-ttu-id="76cc1-120">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76cc1-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76cc1-121">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="76cc1-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76cc1-122">Entradas</span><span class="sxs-lookup"><span data-stu-id="76cc1-122">INPUTS</span></span>

### <span data-ttu-id="76cc1-123">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="76cc1-123">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="76cc1-124">Saídas</span><span class="sxs-lookup"><span data-stu-id="76cc1-124">OUTPUTS</span></span>

### <span data-ttu-id="76cc1-125">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="76cc1-125">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="76cc1-126">Notas</span><span class="sxs-lookup"><span data-stu-id="76cc1-126">NOTES</span></span>

## <span data-ttu-id="76cc1-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="76cc1-127">RELATED LINKS</span></span>

[<span data-ttu-id="76cc1-128">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="76cc1-128">Get-AzPrivateLinkService</span></span>](./Get-AzPrivateLinkService.md)

[<span data-ttu-id="76cc1-129">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="76cc1-129">New-AzPrivateLinkService</span></span>](./New-AzPrivateLinkService.md)

[<span data-ttu-id="76cc1-130">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="76cc1-130">Remove-AzPrivateLinkService</span></span>](./Remove-AzPrivateLinkService.md)


