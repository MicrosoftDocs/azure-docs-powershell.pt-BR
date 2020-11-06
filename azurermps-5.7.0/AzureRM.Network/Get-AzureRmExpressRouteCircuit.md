---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C9954E3D-8645-473E-A6D4-86278C2F6BC1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuit.md
ms.openlocfilehash: 380a5f52a520f487e625663f7d84cbbc55564db5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93603015"
---
# <span data-ttu-id="1ff24-101">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="1ff24-101">Get-AzureRmExpressRouteCircuit</span></span>

## <span data-ttu-id="1ff24-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1ff24-102">SYNOPSIS</span></span>
<span data-ttu-id="1ff24-103">Obtém um circuito do Azure ExpressRoute do Azure.</span><span class="sxs-lookup"><span data-stu-id="1ff24-103">Gets an Azure ExpressRoute circuit from Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1ff24-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1ff24-104">SYNTAX</span></span>

```
Get-AzureRmExpressRouteCircuit [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1ff24-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1ff24-105">DESCRIPTION</span></span>
<span data-ttu-id="1ff24-106">O cmdlet **Get-AzureRmExpressRouteCircuit** é usado para recuperar um objeto de circuito do ExpressRoute da sua assinatura.</span><span class="sxs-lookup"><span data-stu-id="1ff24-106">The **Get-AzureRmExpressRouteCircuit** cmdlet is used to retrieve an ExpressRoute circuit object from your subscription.</span></span> <span data-ttu-id="1ff24-107">O objeto de circuito retornado pode ser usado como entrada para outros cmdlets que operam em circuitos do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="1ff24-107">The circuit object returned can be used as input to other cmdlets that operate on ExpressRoute circuits.</span></span>

## <span data-ttu-id="1ff24-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1ff24-108">EXAMPLES</span></span>

### <span data-ttu-id="1ff24-109">Exemplo 1: baixar o circuito do ExpressRoute para ser excluído</span><span class="sxs-lookup"><span data-stu-id="1ff24-109">Example 1: Get the ExpressRoute circuit to be deleted</span></span>
```
Get-AzureRmExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg | Remove-AzureRmExpressRouteCircuit
```

## <span data-ttu-id="1ff24-110">OS</span><span class="sxs-lookup"><span data-stu-id="1ff24-110">PARAMETERS</span></span>

### <span data-ttu-id="1ff24-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ff24-111">-DefaultProfile</span></span>
<span data-ttu-id="1ff24-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1ff24-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ff24-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="1ff24-113">-Name</span></span>
<span data-ttu-id="1ff24-114">O nome do circuito do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="1ff24-114">The name of the ExpressRoute circuit.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ff24-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ff24-115">-ResourceGroupName</span></span>
<span data-ttu-id="1ff24-116">O nome do grupo de recursos que contém o circuito do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="1ff24-116">The name of the resource group that contains the ExpressRoute circuit.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ff24-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ff24-117">CommonParameters</span></span>
<span data-ttu-id="1ff24-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ff24-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ff24-119">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ff24-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ff24-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1ff24-120">INPUTS</span></span>

### <span data-ttu-id="1ff24-121">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="1ff24-121">None</span></span>
<span data-ttu-id="1ff24-122">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="1ff24-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1ff24-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1ff24-123">OUTPUTS</span></span>

### <span data-ttu-id="1ff24-124">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="1ff24-124">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="1ff24-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1ff24-125">NOTES</span></span>

## <span data-ttu-id="1ff24-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1ff24-126">RELATED LINKS</span></span>

[<span data-ttu-id="1ff24-127">Mover-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="1ff24-127">Move-AzureRmExpressRouteCircuit</span></span>](Move-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="1ff24-128">New-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="1ff24-128">New-AzureRmExpressRouteCircuit</span></span>](New-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="1ff24-129">Remove-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="1ff24-129">Remove-AzureRmExpressRouteCircuit</span></span>](Remove-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="1ff24-130">Set-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="1ff24-130">Set-AzureRmExpressRouteCircuit</span></span>](Set-AzureRmExpressRouteCircuit.md)
