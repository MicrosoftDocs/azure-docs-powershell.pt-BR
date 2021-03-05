---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-azprivateendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateEndpoint.md
ms.openlocfilehash: 5bacd7c1b98bf7996ee8e6a8f7b188d67cf32073
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901597"
---
# <span data-ttu-id="55b3e-101">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="55b3e-101">Set-AzPrivateEndpoint</span></span>

## <span data-ttu-id="55b3e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="55b3e-102">SYNOPSIS</span></span>
<span data-ttu-id="55b3e-103">Atualiza um ponto de extremidade privado.</span><span class="sxs-lookup"><span data-stu-id="55b3e-103">Updates a private endpoint.</span></span>

## <span data-ttu-id="55b3e-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="55b3e-104">SYNTAX</span></span>

```
Set-AzPrivateEndpoint -PrivateEndpoint <PSPrivateEndpoint> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="55b3e-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="55b3e-105">DESCRIPTION</span></span>
<span data-ttu-id="55b3e-106">O cmdlet **Set-AzPrivateEndpoint** atualiza um ponto de extremidade privado.</span><span class="sxs-lookup"><span data-stu-id="55b3e-106">The **Set-AzPrivateEndpoint** cmdlet updates a private endpoint.</span></span>

## <span data-ttu-id="55b3e-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="55b3e-107">EXAMPLES</span></span>

### <span data-ttu-id="55b3e-108">1: cria um ponto de extremidade privado e substitui uma de suas sub-redes para outro</span><span class="sxs-lookup"><span data-stu-id="55b3e-108">1: Creates a private endpoint and replace one of its subnets to another</span></span>
```
$virtualNetwork = Get-AzVirtualNetwork -ResourceName MyVirtualNetwork -ResourceGroupName TestResourceGroup
$plsConnection= New-AzPrivateLinkServiceConnection -Name MyPLSConnections -PrivateLinkServiceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Network/privateLinkServices/privateLinkService" -RequestMessage "Please Approve my request"
$privateEndpoint = New-AzPrivateEndpoint -Name MyPrivateEndpoint -ResourceGroup TestResourceGroup -Location centralus -PirvateLinkServiceConnection $plsConnection -Subnet $virtualNetwork.Subnets[0]

$privateEndpoint.Subnet = $virtualNetwork.Subnet[1]

$privateEndpoint | Set-AzPrivateEndpoint
```

<span data-ttu-id="55b3e-109">Este exemplo cria um ponto de extremidade privado com uma sub-rede e, em seguida, ele é substituído por outra sub-rede da representação na memória da rede virtual.</span><span class="sxs-lookup"><span data-stu-id="55b3e-109">This example creates a private endpoint with one subnet, then it replace to another subnet from the in-memory representation of the virtual network.</span></span> <span data-ttu-id="55b3e-110">O Set-PrivateEndpoint cmdlet é usado para gravar o estado de ponto de extremidade privado modificado no lado do serviço.</span><span class="sxs-lookup"><span data-stu-id="55b3e-110">The Set-PrivateEndpoint cmdlet is then used to write the modified private endpoint state on the service side.</span></span> 

## <span data-ttu-id="55b3e-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="55b3e-111">PARAMETERS</span></span>

### <span data-ttu-id="55b3e-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="55b3e-112">-AsJob</span></span>
<span data-ttu-id="55b3e-113">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="55b3e-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="55b3e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55b3e-114">-DefaultProfile</span></span>
<span data-ttu-id="55b3e-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="55b3e-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="55b3e-116">-PrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="55b3e-116">-PrivateEndpoint</span></span>
<span data-ttu-id="55b3e-117">Especifica um objeto de ponto de extremidade privado que representa o estado ao qual o ponto de extremidade privado deve ser definido.</span><span class="sxs-lookup"><span data-stu-id="55b3e-117">Specifies a private endpoint object representing the state to which the private endpoint should be set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPrivateEndpoint
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="55b3e-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55b3e-118">CommonParameters</span></span>
<span data-ttu-id="55b3e-119">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="55b3e-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55b3e-120">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="55b3e-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55b3e-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="55b3e-121">INPUTS</span></span>

### <span data-ttu-id="55b3e-122">Microsoft.Azure.Commands.Network.Models.PSPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="55b3e-122">Microsoft.Azure.Commands.Network.Models.PSPrivateEndpoint</span></span>

## <span data-ttu-id="55b3e-123">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="55b3e-123">OUTPUTS</span></span>

### <span data-ttu-id="55b3e-124">Microsoft.Azure.Commands.Network.Models.PSPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="55b3e-124">Microsoft.Azure.Commands.Network.Models.PSPrivateEndpoint</span></span>

## <span data-ttu-id="55b3e-125">NOTES</span><span class="sxs-lookup"><span data-stu-id="55b3e-125">NOTES</span></span>

## <span data-ttu-id="55b3e-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="55b3e-126">RELATED LINKS</span></span>

[<span data-ttu-id="55b3e-127">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="55b3e-127">Get-AzPrivateEndpoint</span></span>](./Get-AzPrivateEndpoint.md)

[<span data-ttu-id="55b3e-128">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="55b3e-128">New-AzPrivateEndpoint</span></span>](./New-AzPrivateEndpoint.md)

[<span data-ttu-id="55b3e-129">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="55b3e-129">Remove-AzPrivateEndpoint</span></span>](./Remove-AzPrivateEndpoint.md)


