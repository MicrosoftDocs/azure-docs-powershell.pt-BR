---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermvirtualhubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualHubRoute.md
ms.openlocfilehash: 7197c90e5d5cb0c8a0e15b5e16d1a3c05aaeebf2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432295"
---
# <span data-ttu-id="8000e-101">New-AzureRmVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="8000e-101">New-AzureRmVirtualHubRoute</span></span>

## <span data-ttu-id="8000e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8000e-102">SYNOPSIS</span></span>
<span data-ttu-id="8000e-103">Cria um objeto de rota de Hub virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="8000e-103">Creates an Azure Virtual Hub Route object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8000e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8000e-104">SYNTAX</span></span>

```
New-AzureRmVirtualHubRoute -AddressPrefix <String[]> -NextHopIpAddress <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8000e-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8000e-105">DESCRIPTION</span></span>
<span data-ttu-id="8000e-106">Cria um objeto de rota de Hub virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="8000e-106">Creates an Azure Virtual Hub Route object.</span></span>

## <span data-ttu-id="8000e-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8000e-107">EXAMPLES</span></span>

### <span data-ttu-id="8000e-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="8000e-108">Example 1</span></span>

```powershell
PS C:\> $route1 = 

AddressPrefixes            NextHopIpAddress
---------------            ----------------
{10.0.0.0/16, 11.0.0.0/16} 12.0.0.5
```

<span data-ttu-id="8000e-109">A seguir, você criará um objeto de rota de Hub virtual que pode ser incluído na tabela de rota de Hub virtual.</span><span class="sxs-lookup"><span data-stu-id="8000e-109">The above will create a virtual hub route object that can be included in the virtual hub route table.</span></span>

<span data-ttu-id="8000e-110">A rota do Hub virtual é um objeto na memória que pode ser usado para criar um objeto VirtualHubRouteTable.</span><span class="sxs-lookup"><span data-stu-id="8000e-110">The virtual hub route is an in-memory object that can be used to create a VirtualHubRouteTable object.</span></span>

## <span data-ttu-id="8000e-111">OS</span><span class="sxs-lookup"><span data-stu-id="8000e-111">PARAMETERS</span></span>

### <span data-ttu-id="8000e-112">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="8000e-112">-AddressPrefix</span></span>
<span data-ttu-id="8000e-113">Lista de prefixos de endereço.</span><span class="sxs-lookup"><span data-stu-id="8000e-113">List of Address Prefixes.</span></span>

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

### <span data-ttu-id="8000e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8000e-114">-DefaultProfile</span></span>
<span data-ttu-id="8000e-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8000e-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8000e-116">-NextHopIpAddress</span><span class="sxs-lookup"><span data-stu-id="8000e-116">-NextHopIpAddress</span></span>
<span data-ttu-id="8000e-117">O endereço IP do próximo salto.</span><span class="sxs-lookup"><span data-stu-id="8000e-117">The Next Hop IpAddress.</span></span>

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

### <span data-ttu-id="8000e-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8000e-118">CommonParameters</span></span>
<span data-ttu-id="8000e-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8000e-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8000e-120">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8000e-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8000e-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8000e-121">INPUTS</span></span>

### <span data-ttu-id="8000e-122">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="8000e-122">None</span></span>

## <span data-ttu-id="8000e-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8000e-123">OUTPUTS</span></span>

### <span data-ttu-id="8000e-124">Microsoft. Azure. Commands. Network. Models. PSVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="8000e-124">Microsoft.Azure.Commands.Network.Models.PSVirtualHubRoute</span></span>

## <span data-ttu-id="8000e-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8000e-125">NOTES</span></span>

## <span data-ttu-id="8000e-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8000e-126">RELATED LINKS</span></span>
