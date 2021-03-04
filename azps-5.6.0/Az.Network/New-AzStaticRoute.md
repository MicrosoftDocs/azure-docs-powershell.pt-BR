---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azstaticroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzStaticRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzStaticRoute.md
ms.openlocfilehash: 2cf661ab2bcc531c0a88ae86934a53b212bb91d9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885608"
---
# <span data-ttu-id="275f7-101">New-AzStaticRoute</span><span class="sxs-lookup"><span data-stu-id="275f7-101">New-AzStaticRoute</span></span>

## <span data-ttu-id="275f7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="275f7-102">SYNOPSIS</span></span>
<span data-ttu-id="275f7-103">Cria um objeto StaticRoute que pode ser adicionado a um objeto RoutingConfiguration.</span><span class="sxs-lookup"><span data-stu-id="275f7-103">Creates a StaticRoute object which can then be added to a RoutingConfiguration object.</span></span>

## <span data-ttu-id="275f7-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="275f7-104">SYNTAX</span></span>

```powershell
New-AzStaticRoute -Name <String> -AddressPrefix <String[]> -NextHopIpAddress <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="275f7-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="275f7-105">DESCRIPTION</span></span>
<span data-ttu-id="275f7-106">Cria um objeto StaticRoute.</span><span class="sxs-lookup"><span data-stu-id="275f7-106">Creates a StaticRoute object.</span></span>

## <span data-ttu-id="275f7-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="275f7-107">EXAMPLES</span></span>

### <span data-ttu-id="275f7-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="275f7-108">Example 1</span></span>
```powershell
PS C:\> New-AzStaticRoute -Name "route1" -AddressPrefix @("10.20.0.0/16", "10.30.0.0/16") -NextHopIpAddress "10.90.0.5"

Name   AddressPrefixes              NextHopIpAddress
----   ---------------              ----------------
route1 {10.20.0.0/16, 10.30.0.0/16} 10.90.0.5
```

<span data-ttu-id="275f7-109">O comando acima criará um objeto StaticRoute que pode ser adicionado a um objeto RoutingConfiguration.</span><span class="sxs-lookup"><span data-stu-id="275f7-109">The above command will create a StaticRoute object which can then be added to a RoutingConfiguration object.</span></span>

## <span data-ttu-id="275f7-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="275f7-110">PARAMETERS</span></span>

### <span data-ttu-id="275f7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="275f7-111">-DefaultProfile</span></span>
<span data-ttu-id="275f7-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="275f7-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="275f7-113">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="275f7-113">-AddressPrefix</span></span>
<span data-ttu-id="275f7-114">Lista de prefixos de endereço.</span><span class="sxs-lookup"><span data-stu-id="275f7-114">List of address prefixes.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="275f7-115">-Name</span><span class="sxs-lookup"><span data-stu-id="275f7-115">-Name</span></span>
<span data-ttu-id="275f7-116">O nome da rota.</span><span class="sxs-lookup"><span data-stu-id="275f7-116">The route name.</span></span>

```yaml
Type: String
Parameter Sets: (all)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="275f7-117">-NextHopIpAddress</span><span class="sxs-lookup"><span data-stu-id="275f7-117">-NextHopIpAddress</span></span>
<span data-ttu-id="275f7-118">O endereço ip do próximo salto.</span><span class="sxs-lookup"><span data-stu-id="275f7-118">The next hop ip address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="275f7-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="275f7-119">CommonParameters</span></span>
<span data-ttu-id="275f7-120">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="275f7-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="275f7-121">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="275f7-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="275f7-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="275f7-122">INPUTS</span></span>

### <span data-ttu-id="275f7-123">System.String</span><span class="sxs-lookup"><span data-stu-id="275f7-123">System.String</span></span>

## <span data-ttu-id="275f7-124">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="275f7-124">OUTPUTS</span></span>

### <span data-ttu-id="275f7-125">Microsoft.Azure.Commands.Network.Models.PSStaticRoute</span><span class="sxs-lookup"><span data-stu-id="275f7-125">Microsoft.Azure.Commands.Network.Models.PSStaticRoute</span></span>

## <span data-ttu-id="275f7-126">NOTES</span><span class="sxs-lookup"><span data-stu-id="275f7-126">NOTES</span></span>

## <span data-ttu-id="275f7-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="275f7-127">RELATED LINKS</span></span>

[<span data-ttu-id="275f7-128">New-AzRoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="275f7-128">New-AzRoutingConfiguration</span></span>](./New-AzRoutingConfiguration.md)
