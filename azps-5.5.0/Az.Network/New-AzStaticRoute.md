---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azstaticroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzStaticRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzStaticRoute.md
ms.openlocfilehash: e4d9b8cd09aa1bf1528de1cd2179a76e7907e82b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113469"
---
# <span data-ttu-id="11a3c-101">New-AzStaticRoute</span><span class="sxs-lookup"><span data-stu-id="11a3c-101">New-AzStaticRoute</span></span>

## <span data-ttu-id="11a3c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="11a3c-102">SYNOPSIS</span></span>
<span data-ttu-id="11a3c-103">Cria um objeto StaticRoute que pode ser adicionado a um objeto RoutingConfiguration.</span><span class="sxs-lookup"><span data-stu-id="11a3c-103">Creates a StaticRoute object which can then be added to a RoutingConfiguration object.</span></span>

## <span data-ttu-id="11a3c-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="11a3c-104">SYNTAX</span></span>

```powershell
New-AzStaticRoute -Name <String> -AddressPrefix <String[]> -NextHopIpAddress <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="11a3c-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="11a3c-105">DESCRIPTION</span></span>
<span data-ttu-id="11a3c-106">Cria um objeto StaticRoute.</span><span class="sxs-lookup"><span data-stu-id="11a3c-106">Creates a StaticRoute object.</span></span>

## <span data-ttu-id="11a3c-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="11a3c-107">EXAMPLES</span></span>

### <span data-ttu-id="11a3c-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="11a3c-108">Example 1</span></span>
```powershell
PS C:\> New-AzStaticRoute -Name "route1" -AddressPrefix @("10.20.0.0/16", "10.30.0.0/16") -NextHopIpAddress "10.90.0.5"

Name   AddressPrefixes              NextHopIpAddress
----   ---------------              ----------------
route1 {10.20.0.0/16, 10.30.0.0/16} 10.90.0.5
```

<span data-ttu-id="11a3c-109">O comando acima criará um objeto StaticRoute que pode ser adicionado a um objeto RoutingConfiguration.</span><span class="sxs-lookup"><span data-stu-id="11a3c-109">The above command will create a StaticRoute object which can then be added to a RoutingConfiguration object.</span></span>

## <span data-ttu-id="11a3c-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="11a3c-110">PARAMETERS</span></span>

### <span data-ttu-id="11a3c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11a3c-111">-DefaultProfile</span></span>
<span data-ttu-id="11a3c-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="11a3c-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="11a3c-113">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="11a3c-113">-AddressPrefix</span></span>
<span data-ttu-id="11a3c-114">Lista de prefixos de endereço.</span><span class="sxs-lookup"><span data-stu-id="11a3c-114">List of address prefixes.</span></span>

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

### <span data-ttu-id="11a3c-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="11a3c-115">-Name</span></span>
<span data-ttu-id="11a3c-116">O nome da rota.</span><span class="sxs-lookup"><span data-stu-id="11a3c-116">The route name.</span></span>

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

### <span data-ttu-id="11a3c-117">-NextHopIpAddress</span><span class="sxs-lookup"><span data-stu-id="11a3c-117">-NextHopIpAddress</span></span>
<span data-ttu-id="11a3c-118">O endereço ip do próximo salto.</span><span class="sxs-lookup"><span data-stu-id="11a3c-118">The next hop ip address.</span></span>

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

### <span data-ttu-id="11a3c-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11a3c-119">CommonParameters</span></span>
<span data-ttu-id="11a3c-120">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11a3c-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11a3c-121">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="11a3c-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11a3c-122">Entradas</span><span class="sxs-lookup"><span data-stu-id="11a3c-122">INPUTS</span></span>

### <span data-ttu-id="11a3c-123">System.String</span><span class="sxs-lookup"><span data-stu-id="11a3c-123">System.String</span></span>

## <span data-ttu-id="11a3c-124">Saídas</span><span class="sxs-lookup"><span data-stu-id="11a3c-124">OUTPUTS</span></span>

### <span data-ttu-id="11a3c-125">Microsoft.Azure.Commands.Network.Models.PSStaticRoute</span><span class="sxs-lookup"><span data-stu-id="11a3c-125">Microsoft.Azure.Commands.Network.Models.PSStaticRoute</span></span>

## <span data-ttu-id="11a3c-126">Notas</span><span class="sxs-lookup"><span data-stu-id="11a3c-126">NOTES</span></span>

## <span data-ttu-id="11a3c-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="11a3c-127">RELATED LINKS</span></span>

[<span data-ttu-id="11a3c-128">New-AzRoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="11a3c-128">New-AzRoutingConfiguration</span></span>](./New-AzRoutingConfiguration.md)
