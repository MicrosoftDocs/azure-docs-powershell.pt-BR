---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azvirtualhubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualHubRoute.md
ms.openlocfilehash: 42553004f8d084496a1f4809bca408e0b4c62cef
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890240"
---
# <span data-ttu-id="a241b-101">New-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="a241b-101">New-AzVirtualHubRoute</span></span>

## <span data-ttu-id="a241b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a241b-102">SYNOPSIS</span></span>
<span data-ttu-id="a241b-103">Cria um objeto Route do Azure Virtual Hub.</span><span class="sxs-lookup"><span data-stu-id="a241b-103">Creates an Azure Virtual Hub Route object.</span></span>

## <span data-ttu-id="a241b-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="a241b-104">SYNTAX</span></span>

```
New-AzVirtualHubRoute -AddressPrefix <String[]> -NextHopIpAddress <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a241b-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="a241b-105">DESCRIPTION</span></span>
<span data-ttu-id="a241b-106">Cria um objeto Route do Azure Virtual Hub.</span><span class="sxs-lookup"><span data-stu-id="a241b-106">Creates an Azure Virtual Hub Route object.</span></span>

## <span data-ttu-id="a241b-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a241b-107">EXAMPLES</span></span>

### <span data-ttu-id="a241b-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a241b-108">Example 1</span></span>

```powershell
PS C:\> $route1 = New-AzVirtualHubRoute -AddressPrefix @("10.0.0.0/16", "11.0.0.0/16") -NextHopIpAddress "12.0.0.5"

AddressPrefixes            NextHopIpAddress
---------------            ----------------
{10.0.0.0/16, 11.0.0.0/16} 12.0.0.5
```

<span data-ttu-id="a241b-109">O acima criará um objeto de rota de hub virtual que pode ser incluído na tabela de rota do hub virtual.</span><span class="sxs-lookup"><span data-stu-id="a241b-109">The above will create a virtual hub route object that can be included in the virtual hub route table.</span></span>

<span data-ttu-id="a241b-110">A rota do hub virtual é um objeto na memória que pode ser usado para criar um objeto VirtualHubRouteTable.</span><span class="sxs-lookup"><span data-stu-id="a241b-110">The virtual hub route is an in-memory object that can be used to create a VirtualHubRouteTable object.</span></span>

## <span data-ttu-id="a241b-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="a241b-111">PARAMETERS</span></span>

### <span data-ttu-id="a241b-112">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="a241b-112">-AddressPrefix</span></span>
<span data-ttu-id="a241b-113">Lista de Prefixos de Endereço.</span><span class="sxs-lookup"><span data-stu-id="a241b-113">List of Address Prefixes.</span></span>

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

### <span data-ttu-id="a241b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a241b-114">-DefaultProfile</span></span>
<span data-ttu-id="a241b-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a241b-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a241b-116">-NextHopIpAddress</span><span class="sxs-lookup"><span data-stu-id="a241b-116">-NextHopIpAddress</span></span>
<span data-ttu-id="a241b-117">O IpAddress de Próximo Salto.</span><span class="sxs-lookup"><span data-stu-id="a241b-117">The Next Hop IpAddress.</span></span>

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

### <span data-ttu-id="a241b-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a241b-118">CommonParameters</span></span>
<span data-ttu-id="a241b-119">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a241b-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a241b-120">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a241b-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a241b-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a241b-121">INPUTS</span></span>

### <span data-ttu-id="a241b-122">Nenhum</span><span class="sxs-lookup"><span data-stu-id="a241b-122">None</span></span>

## <span data-ttu-id="a241b-123">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="a241b-123">OUTPUTS</span></span>

### <span data-ttu-id="a241b-124">Microsoft.Azure.Commands.Network.Models.PSVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="a241b-124">Microsoft.Azure.Commands.Network.Models.PSVirtualHubRoute</span></span>

## <span data-ttu-id="a241b-125">NOTES</span><span class="sxs-lookup"><span data-stu-id="a241b-125">NOTES</span></span>

## <span data-ttu-id="a241b-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a241b-126">RELATED LINKS</span></span>

[<span data-ttu-id="a241b-127">New-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="a241b-127">New-AzVirtualHubRouteTable</span></span>](./New-AzVirtualHubRouteTable.md)
