---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualhubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualHubRoute.md
ms.openlocfilehash: 8a9184eddaf5b614b4338a95e1d895d645e0832e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93600270"
---
# <span data-ttu-id="1c3ef-101">New-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="1c3ef-101">New-AzVirtualHubRoute</span></span>

## <span data-ttu-id="1c3ef-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1c3ef-102">SYNOPSIS</span></span>
<span data-ttu-id="1c3ef-103">Cria um objeto de rota de Hub virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="1c3ef-103">Creates an Azure Virtual Hub Route object.</span></span>

## <span data-ttu-id="1c3ef-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1c3ef-104">SYNTAX</span></span>

```
New-AzVirtualHubRoute -AddressPrefix <String[]> -NextHopIpAddress <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1c3ef-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1c3ef-105">DESCRIPTION</span></span>
<span data-ttu-id="1c3ef-106">Cria um objeto de rota de Hub virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="1c3ef-106">Creates an Azure Virtual Hub Route object.</span></span>

## <span data-ttu-id="1c3ef-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1c3ef-107">EXAMPLES</span></span>

### <span data-ttu-id="1c3ef-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="1c3ef-108">Example 1</span></span>

```powershell
PS C:\> $route1 = New-AzVirtualHubRoute -AddressPrefix @("10.0.0.0/16", "11.0.0.0/16") -NextHopIpAddress "12.0.0.5"

AddressPrefixes            NextHopIpAddress
---------------            ----------------
{10.0.0.0/16, 11.0.0.0/16} 12.0.0.5
```

<span data-ttu-id="1c3ef-109">A seguir, você criará um objeto de rota de Hub virtual que pode ser incluído na tabela de rota de Hub virtual.</span><span class="sxs-lookup"><span data-stu-id="1c3ef-109">The above will create a virtual hub route object that can be included in the virtual hub route table.</span></span>

<span data-ttu-id="1c3ef-110">A rota do Hub virtual é um objeto na memória que pode ser usado para criar um objeto VirtualHubRouteTable.</span><span class="sxs-lookup"><span data-stu-id="1c3ef-110">The virtual hub route is an in-memory object that can be used to create a VirtualHubRouteTable object.</span></span>

## <span data-ttu-id="1c3ef-111">OS</span><span class="sxs-lookup"><span data-stu-id="1c3ef-111">PARAMETERS</span></span>

### <span data-ttu-id="1c3ef-112">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="1c3ef-112">-AddressPrefix</span></span>
<span data-ttu-id="1c3ef-113">Lista de prefixos de endereço.</span><span class="sxs-lookup"><span data-stu-id="1c3ef-113">List of Address Prefixes.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c3ef-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c3ef-114">-DefaultProfile</span></span>
<span data-ttu-id="1c3ef-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1c3ef-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1c3ef-116">-NextHopIpAddress</span><span class="sxs-lookup"><span data-stu-id="1c3ef-116">-NextHopIpAddress</span></span>
<span data-ttu-id="1c3ef-117">O endereço IP do próximo salto.</span><span class="sxs-lookup"><span data-stu-id="1c3ef-117">The Next Hop IpAddress.</span></span>

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

### <span data-ttu-id="1c3ef-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c3ef-118">CommonParameters</span></span>
<span data-ttu-id="1c3ef-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c3ef-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c3ef-120">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1c3ef-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c3ef-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1c3ef-121">INPUTS</span></span>

### <span data-ttu-id="1c3ef-122">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="1c3ef-122">None</span></span>

## <span data-ttu-id="1c3ef-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1c3ef-123">OUTPUTS</span></span>

### <span data-ttu-id="1c3ef-124">Microsoft. Azure. Commands. Network. Models. PSVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="1c3ef-124">Microsoft.Azure.Commands.Network.Models.PSVirtualHubRoute</span></span>

## <span data-ttu-id="1c3ef-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1c3ef-125">NOTES</span></span>

## <span data-ttu-id="1c3ef-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1c3ef-126">RELATED LINKS</span></span>

[<span data-ttu-id="1c3ef-127">New-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="1c3ef-127">New-AzVirtualHubRouteTable</span></span>](./New-AzVirtualHubRouteTable.md)
