---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azprivateendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateEndpoint.md
ms.openlocfilehash: afb61df71ce0cf0833f82868a7f3f345cf31b023
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93772794"
---
# <span data-ttu-id="960c3-101">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="960c3-101">Set-AzPrivateEndpoint</span></span>

## <span data-ttu-id="960c3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="960c3-102">SYNOPSIS</span></span>
<span data-ttu-id="960c3-103">Atualiza um ponto de extremidade privado.</span><span class="sxs-lookup"><span data-stu-id="960c3-103">Updates a private endpoint.</span></span>

## <span data-ttu-id="960c3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="960c3-104">SYNTAX</span></span>

```
Set-AzPrivateEndpoint -PrivateEndpoint <PSPrivateEndpoint> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="960c3-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="960c3-105">DESCRIPTION</span></span>
<span data-ttu-id="960c3-106">O cmdlet **set-AzPrivateEndpoint** atualiza um ponto de extremidade particular.</span><span class="sxs-lookup"><span data-stu-id="960c3-106">The **Set-AzPrivateEndpoint** cmdlet updates a private endpoint.</span></span>

## <span data-ttu-id="960c3-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="960c3-107">EXAMPLES</span></span>

### <span data-ttu-id="960c3-108">1: cria um ponto de extremidade privado e substitui uma de suas sub-redes em outro</span><span class="sxs-lookup"><span data-stu-id="960c3-108">1: Creates a private endpoint and replace one of its subnets to another</span></span>
```
$virtualNetwork = Get-AzVirtualNetwork -ResourceName MyVirtualNetwork -ResourceGroupName TestResourceGroup
$plsConnection= New-AzPrivateLinkServiceConnection -Name MyPLSConnections -PrivateLinkServiceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Network/privateLinkServices/privateLinkService" -RequestMessage "Please Approve my request"
$privateEndpoint = New-AzPrivateEndpoint -Name MyPrivateEndpoint -ResourceGroup TestResourceGroup -Location centralus -PirvateLinkServiceConnection $plsConnection -Subnet $virtualNetwork.Subnets[0]

$privateEndpoint.Subnet = $virtualNetwork.Subnet[1]

$privateEndpoint | Set-AzPrivateEndpoint
```

<span data-ttu-id="960c3-109">Este exemplo cria um ponto de extremidade privado com uma sub-rede e depois substitui a outra sub-rede da representação na memória da rede virtual.</span><span class="sxs-lookup"><span data-stu-id="960c3-109">This example creates a private endpoint with one subnet, then it replace to another subnet from the in-memory representation of the virtual network.</span></span> <span data-ttu-id="960c3-110">O cmdlet Set-PrivateEndpoint é usado para gravar o estado de ponto de extremidade particular modificado no lado do serviço.</span><span class="sxs-lookup"><span data-stu-id="960c3-110">The Set-PrivateEndpoint cmdlet is then used to write the modified private endpoint state on the service side.</span></span> 

## <span data-ttu-id="960c3-111">OS</span><span class="sxs-lookup"><span data-stu-id="960c3-111">PARAMETERS</span></span>

### <span data-ttu-id="960c3-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="960c3-112">-AsJob</span></span>
<span data-ttu-id="960c3-113">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="960c3-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="960c3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="960c3-114">-DefaultProfile</span></span>
<span data-ttu-id="960c3-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="960c3-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="960c3-116">-PrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="960c3-116">-PrivateEndpoint</span></span>
<span data-ttu-id="960c3-117">Especifica um objeto de ponto de extremidade privado que representa o estado para o qual o ponto de extremidade particular deve ser definido.</span><span class="sxs-lookup"><span data-stu-id="960c3-117">Specifies a private endpoint object representing the state to which the private endpoint should be set.</span></span>

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

### <span data-ttu-id="960c3-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="960c3-118">CommonParameters</span></span>
<span data-ttu-id="960c3-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="960c3-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="960c3-120">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="960c3-120">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="960c3-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="960c3-121">INPUTS</span></span>

### <span data-ttu-id="960c3-122">Microsoft. Azure. Commands. Network. Models. PSPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="960c3-122">Microsoft.Azure.Commands.Network.Models.PSPrivateEndpoint</span></span>

## <span data-ttu-id="960c3-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="960c3-123">OUTPUTS</span></span>

### <span data-ttu-id="960c3-124">Microsoft. Azure. Commands. Network. Models. PSPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="960c3-124">Microsoft.Azure.Commands.Network.Models.PSPrivateEndpoint</span></span>

## <span data-ttu-id="960c3-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="960c3-125">NOTES</span></span>

## <span data-ttu-id="960c3-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="960c3-126">RELATED LINKS</span></span>

[<span data-ttu-id="960c3-127">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="960c3-127">Get-AzPrivateEndpoint</span></span>](./Get-AzPrivateEndpoint.md)

[<span data-ttu-id="960c3-128">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="960c3-128">New-AzPrivateEndpoint</span></span>](./New-AzPrivateEndpoint.md)

[<span data-ttu-id="960c3-129">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="960c3-129">Remove-AzPrivateEndpoint</span></span>](./Remove-AzPrivateEndpoint.md)

