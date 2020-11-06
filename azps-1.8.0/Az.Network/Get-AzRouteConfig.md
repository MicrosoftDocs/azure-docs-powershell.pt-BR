---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: DBD40431-DD7A-42CB-83AA-568B1065A468
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azrouteconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteConfig.md
ms.openlocfilehash: 195ff0f8da8af5408f9b7ad2bffdd35507b10d1b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93600503"
---
# <span data-ttu-id="ccda3-101">Get-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="ccda3-101">Get-AzRouteConfig</span></span>

## <span data-ttu-id="ccda3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ccda3-102">SYNOPSIS</span></span>
<span data-ttu-id="ccda3-103">Obtém rotas de uma tabela de rota.</span><span class="sxs-lookup"><span data-stu-id="ccda3-103">Gets routes from a route table.</span></span>

## <span data-ttu-id="ccda3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ccda3-104">SYNTAX</span></span>

```
Get-AzRouteConfig -RouteTable <PSRouteTable> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ccda3-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ccda3-105">DESCRIPTION</span></span>
<span data-ttu-id="ccda3-106">O cmdlet **Get-AzRouteConfig** Obtém rotas de uma tabela de rota do Azure.</span><span class="sxs-lookup"><span data-stu-id="ccda3-106">The **Get-AzRouteConfig** cmdlet gets routes from an Azure route table.</span></span>
<span data-ttu-id="ccda3-107">Você pode especificar uma rota por nome.</span><span class="sxs-lookup"><span data-stu-id="ccda3-107">You can specify a route by name.</span></span>

## <span data-ttu-id="ccda3-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ccda3-108">EXAMPLES</span></span>

### <span data-ttu-id="ccda3-109">Exemplo 1: obter uma tabela de rota</span><span class="sxs-lookup"><span data-stu-id="ccda3-109">Example 1: Get a route table</span></span>
```
PS C:\>Get-AzRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01" | Get-AzRouteConfig -Name "Route07"
Name              : route07
Id                : 
Etag              : 
ProvisioningState : 
AddressPrefix     : 10.1.0.0/16
NextHopType       : VnetLocal
NextHopIpAddress  :
```

<span data-ttu-id="ccda3-110">Esse comando obtém a tabela de rota chamada RouteTable01 usando o cmdlet **Get-AzRouteTable** .</span><span class="sxs-lookup"><span data-stu-id="ccda3-110">This command gets the route table named RouteTable01 by using the **Get-AzRouteTable** cmdlet.</span></span>
<span data-ttu-id="ccda3-111">O comando transmite essa tabela para o cmdlet atual usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="ccda3-111">The command passes that table to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="ccda3-112">O cmdlet atual Obtém a rota chamada Route07 na tabela de rota chamada RouteTable01.</span><span class="sxs-lookup"><span data-stu-id="ccda3-112">The current cmdlet gets the route named Route07 in the route table named RouteTable01.</span></span>

## <span data-ttu-id="ccda3-113">OS</span><span class="sxs-lookup"><span data-stu-id="ccda3-113">PARAMETERS</span></span>

### <span data-ttu-id="ccda3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ccda3-114">-DefaultProfile</span></span>
<span data-ttu-id="ccda3-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ccda3-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ccda3-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="ccda3-116">-Name</span></span>
<span data-ttu-id="ccda3-117">Especifica o nome da rota obtida por esse cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ccda3-117">Specifies the name of the route that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccda3-118">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="ccda3-118">-RouteTable</span></span>
<span data-ttu-id="ccda3-119">Especifica a tabela de rotas da qual esse cmdlet obtém rotas.</span><span class="sxs-lookup"><span data-stu-id="ccda3-119">Specifies the route table from which this cmdlet gets routes.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRouteTable
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ccda3-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ccda3-120">CommonParameters</span></span>
<span data-ttu-id="ccda3-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ccda3-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ccda3-122">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ccda3-122">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ccda3-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ccda3-123">INPUTS</span></span>

### <span data-ttu-id="ccda3-124">Microsoft. Azure. Commands. Network. Models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="ccda3-124">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="ccda3-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ccda3-125">OUTPUTS</span></span>

### <span data-ttu-id="ccda3-126">Microsoft. Azure. Commands. Network. Models. PSRoute</span><span class="sxs-lookup"><span data-stu-id="ccda3-126">Microsoft.Azure.Commands.Network.Models.PSRoute</span></span>

## <span data-ttu-id="ccda3-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ccda3-127">NOTES</span></span>

## <span data-ttu-id="ccda3-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ccda3-128">RELATED LINKS</span></span>

[<span data-ttu-id="ccda3-129">Add-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="ccda3-129">Add-AzRouteConfig</span></span>](./Add-AzRouteConfig.md)

[<span data-ttu-id="ccda3-130">Get-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="ccda3-130">Get-AzRouteTable</span></span>](./Get-AzRouteTable.md)

[<span data-ttu-id="ccda3-131">New-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="ccda3-131">New-AzRouteConfig</span></span>](./New-AzRouteConfig.md)

[<span data-ttu-id="ccda3-132">Remove-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="ccda3-132">Remove-AzRouteConfig</span></span>](./Remove-AzRouteConfig.md)

[<span data-ttu-id="ccda3-133">Set-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="ccda3-133">Set-AzRouteConfig</span></span>](./Set-AzRouteConfig.md)


