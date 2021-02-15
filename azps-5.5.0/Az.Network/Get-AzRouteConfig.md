---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: DBD40431-DD7A-42CB-83AA-568B1065A468
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azrouteconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteConfig.md
ms.openlocfilehash: 0d941289f0798854a3647bcb5fbf4d1e6be1053d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117446"
---
# <span data-ttu-id="fd459-101">Get-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="fd459-101">Get-AzRouteConfig</span></span>

## <span data-ttu-id="fd459-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fd459-102">SYNOPSIS</span></span>
<span data-ttu-id="fd459-103">Obtém rotas de uma tabela de rota.</span><span class="sxs-lookup"><span data-stu-id="fd459-103">Gets routes from a route table.</span></span>

## <span data-ttu-id="fd459-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fd459-104">SYNTAX</span></span>

```
Get-AzRouteConfig -RouteTable <PSRouteTable> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fd459-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="fd459-105">DESCRIPTION</span></span>
<span data-ttu-id="fd459-106">O **cmdlet Get-AzRouteConfig obtém** rotas de uma tabela de rota do Azure.</span><span class="sxs-lookup"><span data-stu-id="fd459-106">The **Get-AzRouteConfig** cmdlet gets routes from an Azure route table.</span></span>
<span data-ttu-id="fd459-107">Você pode especificar uma rota por nome.</span><span class="sxs-lookup"><span data-stu-id="fd459-107">You can specify a route by name.</span></span>

## <span data-ttu-id="fd459-108">Exemplos</span><span class="sxs-lookup"><span data-stu-id="fd459-108">EXAMPLES</span></span>

### <span data-ttu-id="fd459-109">Exemplo 1: Obter uma tabela de rota</span><span class="sxs-lookup"><span data-stu-id="fd459-109">Example 1: Get a route table</span></span>
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

<span data-ttu-id="fd459-110">Esse comando obtém a tabela de rota chamada Roteável01 usando o cmdlet **Get-AzRouteTable.**</span><span class="sxs-lookup"><span data-stu-id="fd459-110">This command gets the route table named RouteTable01 by using the **Get-AzRouteTable** cmdlet.</span></span>
<span data-ttu-id="fd459-111">O comando passa essa tabela para o cmdlet atual usando o operador de pipeline.</span><span class="sxs-lookup"><span data-stu-id="fd459-111">The command passes that table to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="fd459-112">O cmdlet atual obtém a rota chamada Roteada07 na tabela de rota chamada Roteável01.</span><span class="sxs-lookup"><span data-stu-id="fd459-112">The current cmdlet gets the route named Route07 in the route table named RouteTable01.</span></span>

## <span data-ttu-id="fd459-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fd459-113">PARAMETERS</span></span>

### <span data-ttu-id="fd459-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd459-114">-DefaultProfile</span></span>
<span data-ttu-id="fd459-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="fd459-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fd459-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="fd459-116">-Name</span></span>
<span data-ttu-id="fd459-117">Especifica o nome da rota que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="fd459-117">Specifies the name of the route that this cmdlet gets.</span></span>

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

### <span data-ttu-id="fd459-118">-Tabela de Rota</span><span class="sxs-lookup"><span data-stu-id="fd459-118">-RouteTable</span></span>
<span data-ttu-id="fd459-119">Especifica a tabela de rota da qual este cmdlet obtém rotas.</span><span class="sxs-lookup"><span data-stu-id="fd459-119">Specifies the route table from which this cmdlet gets routes.</span></span>

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

### <span data-ttu-id="fd459-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd459-120">CommonParameters</span></span>
<span data-ttu-id="fd459-121">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd459-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd459-122">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fd459-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd459-123">Entradas</span><span class="sxs-lookup"><span data-stu-id="fd459-123">INPUTS</span></span>

### <span data-ttu-id="fd459-124">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="fd459-124">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="fd459-125">Saídas</span><span class="sxs-lookup"><span data-stu-id="fd459-125">OUTPUTS</span></span>

### <span data-ttu-id="fd459-126">Microsoft.Azure.Commands.Network.Models.PSRoute</span><span class="sxs-lookup"><span data-stu-id="fd459-126">Microsoft.Azure.Commands.Network.Models.PSRoute</span></span>

## <span data-ttu-id="fd459-127">Notas</span><span class="sxs-lookup"><span data-stu-id="fd459-127">NOTES</span></span>

## <span data-ttu-id="fd459-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fd459-128">RELATED LINKS</span></span>

[<span data-ttu-id="fd459-129">Add-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="fd459-129">Add-AzRouteConfig</span></span>](./Add-AzRouteConfig.md)

[<span data-ttu-id="fd459-130">Get-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="fd459-130">Get-AzRouteTable</span></span>](./Get-AzRouteTable.md)

[<span data-ttu-id="fd459-131">New-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="fd459-131">New-AzRouteConfig</span></span>](./New-AzRouteConfig.md)

[<span data-ttu-id="fd459-132">Remove-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="fd459-132">Remove-AzRouteConfig</span></span>](./Remove-AzRouteConfig.md)

[<span data-ttu-id="fd459-133">Set-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="fd459-133">Set-AzRouteConfig</span></span>](./Set-AzRouteConfig.md)


