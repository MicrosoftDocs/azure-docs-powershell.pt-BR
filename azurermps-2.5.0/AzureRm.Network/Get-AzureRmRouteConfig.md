---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: DBD40431-DD7A-42CB-83AA-568B1065A468
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermrouteconfig
schema: 2.0.0
ms.openlocfilehash: 907ca017518304a38340e9539aa4e8faf4216d59
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93786449"
---
# <span data-ttu-id="da8ea-101">Get-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="da8ea-101">Get-AzureRmRouteConfig</span></span>

## <span data-ttu-id="da8ea-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="da8ea-102">SYNOPSIS</span></span>
<span data-ttu-id="da8ea-103">Obtém rotas de uma tabela de rota.</span><span class="sxs-lookup"><span data-stu-id="da8ea-103">Gets routes from a route table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="da8ea-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="da8ea-104">SYNTAX</span></span>

```
Get-AzureRmRouteConfig -RouteTable <PSRouteTable> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="da8ea-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="da8ea-105">DESCRIPTION</span></span>
<span data-ttu-id="da8ea-106">O cmdlet **Get-AzureRmRouteConfig** Obtém rotas de uma tabela de rota do Azure.</span><span class="sxs-lookup"><span data-stu-id="da8ea-106">The **Get-AzureRmRouteConfig** cmdlet gets routes from an Azure route table.</span></span>
<span data-ttu-id="da8ea-107">Você pode especificar uma rota por nome.</span><span class="sxs-lookup"><span data-stu-id="da8ea-107">You can specify a route by name.</span></span>

## <span data-ttu-id="da8ea-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="da8ea-108">EXAMPLES</span></span>

### <span data-ttu-id="da8ea-109">Exemplo 1: obter uma tabela de rota</span><span class="sxs-lookup"><span data-stu-id="da8ea-109">Example 1: Get a route table</span></span>
```
PS C:\>Get-AzureRmRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01" | Get-AzureRmRouteConfig -Name "Route07"
Name              : route07
Id                : 
Etag              : 
ProvisioningState : 
AddressPrefix     : 10.1.0.0/16
NextHopType       : VnetLocal
NextHopIpAddress  :
```

<span data-ttu-id="da8ea-110">Esse comando obtém a tabela de rota chamada RouteTable01 usando o cmdlet **Get-AzureRmRouteTable** .</span><span class="sxs-lookup"><span data-stu-id="da8ea-110">This command gets the route table named RouteTable01 by using the **Get-AzureRmRouteTable** cmdlet.</span></span>
<span data-ttu-id="da8ea-111">O comando transmite essa tabela para o cmdlet atual usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="da8ea-111">The command passes that table to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="da8ea-112">O cmdlet atual Obtém a rota chamada Route07 na tabela de rota chamada RouteTable01.</span><span class="sxs-lookup"><span data-stu-id="da8ea-112">The current cmdlet gets the route named Route07 in the route table named RouteTable01.</span></span>

## <span data-ttu-id="da8ea-113">OS</span><span class="sxs-lookup"><span data-stu-id="da8ea-113">PARAMETERS</span></span>

### <span data-ttu-id="da8ea-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da8ea-114">-DefaultProfile</span></span>
<span data-ttu-id="da8ea-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="da8ea-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="da8ea-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="da8ea-116">-Name</span></span>
<span data-ttu-id="da8ea-117">Especifica o nome da rota obtida por esse cmdlet.</span><span class="sxs-lookup"><span data-stu-id="da8ea-117">Specifies the name of the route that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da8ea-118">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="da8ea-118">-RouteTable</span></span>
<span data-ttu-id="da8ea-119">Especifica a tabela de rotas da qual esse cmdlet obtém rotas.</span><span class="sxs-lookup"><span data-stu-id="da8ea-119">Specifies the route table from which this cmdlet gets routes.</span></span>

```yaml
Type: PSRouteTable
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="da8ea-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da8ea-120">CommonParameters</span></span>
<span data-ttu-id="da8ea-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da8ea-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da8ea-122">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="da8ea-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da8ea-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="da8ea-123">INPUTS</span></span>

### <span data-ttu-id="da8ea-124">PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="da8ea-124">PSRouteTable</span></span>
<span data-ttu-id="da8ea-125">O parâmetro ' RouteTable ' aceita o valor do tipo ' PSRouteTable ' da pipeline</span><span class="sxs-lookup"><span data-stu-id="da8ea-125">Parameter 'RouteTable' accepts value of type 'PSRouteTable' from the pipeline</span></span>

## <span data-ttu-id="da8ea-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="da8ea-126">OUTPUTS</span></span>

### <span data-ttu-id="da8ea-127">Microsoft. Azure. Commands. Network. Models. PSRoute</span><span class="sxs-lookup"><span data-stu-id="da8ea-127">Microsoft.Azure.Commands.Network.Models.PSRoute</span></span>

## <span data-ttu-id="da8ea-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="da8ea-128">NOTES</span></span>

## <span data-ttu-id="da8ea-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="da8ea-129">RELATED LINKS</span></span>

[<span data-ttu-id="da8ea-130">Add-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="da8ea-130">Add-AzureRmRouteConfig</span></span>](./Add-AzureRmRouteConfig.md)

[<span data-ttu-id="da8ea-131">Get-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="da8ea-131">Get-AzureRmRouteTable</span></span>](./Get-AzureRmRouteTable.md)

[<span data-ttu-id="da8ea-132">New-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="da8ea-132">New-AzureRmRouteConfig</span></span>](./New-AzureRmRouteConfig.md)

[<span data-ttu-id="da8ea-133">Remove-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="da8ea-133">Remove-AzureRmRouteConfig</span></span>](./Remove-AzureRmRouteConfig.md)

[<span data-ttu-id="da8ea-134">Set-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="da8ea-134">Set-AzureRmRouteConfig</span></span>](./Set-AzureRmRouteConfig.md)


