---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: DBD40431-DD7A-42CB-83AA-568B1065A468
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermrouteconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmRouteConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmRouteConfig.md
ms.openlocfilehash: f00a1d0c67d7bb395a328e01915f5bb0334d3d83
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428180"
---
# <span data-ttu-id="a5141-101">Get-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="a5141-101">Get-AzureRmRouteConfig</span></span>

## <span data-ttu-id="a5141-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a5141-102">SYNOPSIS</span></span>
<span data-ttu-id="a5141-103">Obtém rotas de uma tabela de rota.</span><span class="sxs-lookup"><span data-stu-id="a5141-103">Gets routes from a route table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a5141-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a5141-104">SYNTAX</span></span>

```
Get-AzureRmRouteConfig -RouteTable <PSRouteTable> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a5141-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a5141-105">DESCRIPTION</span></span>
<span data-ttu-id="a5141-106">O cmdlet **Get-AzureRmRouteConfig** Obtém rotas de uma tabela de rota do Azure.</span><span class="sxs-lookup"><span data-stu-id="a5141-106">The **Get-AzureRmRouteConfig** cmdlet gets routes from an Azure route table.</span></span>
<span data-ttu-id="a5141-107">Você pode especificar uma rota por nome.</span><span class="sxs-lookup"><span data-stu-id="a5141-107">You can specify a route by name.</span></span>

## <span data-ttu-id="a5141-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a5141-108">EXAMPLES</span></span>

### <span data-ttu-id="a5141-109">Exemplo 1: obter uma tabela de rota</span><span class="sxs-lookup"><span data-stu-id="a5141-109">Example 1: Get a route table</span></span>
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

<span data-ttu-id="a5141-110">Esse comando obtém a tabela de rota chamada RouteTable01 usando o cmdlet **Get-AzureRmRouteTable** .</span><span class="sxs-lookup"><span data-stu-id="a5141-110">This command gets the route table named RouteTable01 by using the **Get-AzureRmRouteTable** cmdlet.</span></span>
<span data-ttu-id="a5141-111">O comando transmite essa tabela para o cmdlet atual usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="a5141-111">The command passes that table to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="a5141-112">O cmdlet atual Obtém a rota chamada Route07 na tabela de rota chamada RouteTable01.</span><span class="sxs-lookup"><span data-stu-id="a5141-112">The current cmdlet gets the route named Route07 in the route table named RouteTable01.</span></span>

## <span data-ttu-id="a5141-113">OS</span><span class="sxs-lookup"><span data-stu-id="a5141-113">PARAMETERS</span></span>

### <span data-ttu-id="a5141-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5141-114">-DefaultProfile</span></span>
<span data-ttu-id="a5141-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a5141-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a5141-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="a5141-116">-Name</span></span>
<span data-ttu-id="a5141-117">Especifica o nome da rota obtida por esse cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a5141-117">Specifies the name of the route that this cmdlet gets.</span></span>

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

### <span data-ttu-id="a5141-118">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="a5141-118">-RouteTable</span></span>
<span data-ttu-id="a5141-119">Especifica a tabela de rotas da qual esse cmdlet obtém rotas.</span><span class="sxs-lookup"><span data-stu-id="a5141-119">Specifies the route table from which this cmdlet gets routes.</span></span>

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

### <span data-ttu-id="a5141-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5141-120">CommonParameters</span></span>
<span data-ttu-id="a5141-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5141-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5141-122">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5141-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5141-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a5141-123">INPUTS</span></span>

### <span data-ttu-id="a5141-124">PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="a5141-124">PSRouteTable</span></span>
<span data-ttu-id="a5141-125">O parâmetro ' RouteTable ' aceita o valor do tipo ' PSRouteTable ' da pipeline</span><span class="sxs-lookup"><span data-stu-id="a5141-125">Parameter 'RouteTable' accepts value of type 'PSRouteTable' from the pipeline</span></span>

## <span data-ttu-id="a5141-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a5141-126">OUTPUTS</span></span>

### <span data-ttu-id="a5141-127">Microsoft. Azure. Commands. Network. Models. PSRoute</span><span class="sxs-lookup"><span data-stu-id="a5141-127">Microsoft.Azure.Commands.Network.Models.PSRoute</span></span>

## <span data-ttu-id="a5141-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a5141-128">NOTES</span></span>

## <span data-ttu-id="a5141-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a5141-129">RELATED LINKS</span></span>

[<span data-ttu-id="a5141-130">Add-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="a5141-130">Add-AzureRmRouteConfig</span></span>](./Add-AzureRmRouteConfig.md)

[<span data-ttu-id="a5141-131">Get-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="a5141-131">Get-AzureRmRouteTable</span></span>](./Get-AzureRmRouteTable.md)

[<span data-ttu-id="a5141-132">New-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="a5141-132">New-AzureRmRouteConfig</span></span>](./New-AzureRmRouteConfig.md)

[<span data-ttu-id="a5141-133">Remove-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="a5141-133">Remove-AzureRmRouteConfig</span></span>](./Remove-AzureRmRouteConfig.md)

[<span data-ttu-id="a5141-134">Set-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="a5141-134">Set-AzureRmRouteConfig</span></span>](./Set-AzureRmRouteConfig.md)


