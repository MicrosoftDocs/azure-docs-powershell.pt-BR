---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: DBD40431-DD7A-42CB-83AA-568B1065A468
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermrouteconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmRouteConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmRouteConfig.md
ms.openlocfilehash: dd23891bc56ac2eb8fce30708d9a72055a567bf3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429499"
---
# <span data-ttu-id="334e5-101">Get-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="334e5-101">Get-AzureRmRouteConfig</span></span>

## <span data-ttu-id="334e5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="334e5-102">SYNOPSIS</span></span>
<span data-ttu-id="334e5-103">Obtém rotas de uma tabela de rota.</span><span class="sxs-lookup"><span data-stu-id="334e5-103">Gets routes from a route table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="334e5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="334e5-104">SYNTAX</span></span>

```
Get-AzureRmRouteConfig -RouteTable <PSRouteTable> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="334e5-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="334e5-105">DESCRIPTION</span></span>
<span data-ttu-id="334e5-106">O cmdlet **Get-AzureRmRouteConfig** Obtém rotas de uma tabela de rota do Azure.</span><span class="sxs-lookup"><span data-stu-id="334e5-106">The **Get-AzureRmRouteConfig** cmdlet gets routes from an Azure route table.</span></span>
<span data-ttu-id="334e5-107">Você pode especificar uma rota por nome.</span><span class="sxs-lookup"><span data-stu-id="334e5-107">You can specify a route by name.</span></span>

## <span data-ttu-id="334e5-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="334e5-108">EXAMPLES</span></span>

### <span data-ttu-id="334e5-109">Exemplo 1: obter uma tabela de rota</span><span class="sxs-lookup"><span data-stu-id="334e5-109">Example 1: Get a route table</span></span>
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

<span data-ttu-id="334e5-110">Esse comando obtém a tabela de rota chamada RouteTable01 usando o cmdlet **Get-AzureRmRouteTable** .</span><span class="sxs-lookup"><span data-stu-id="334e5-110">This command gets the route table named RouteTable01 by using the **Get-AzureRmRouteTable** cmdlet.</span></span>
<span data-ttu-id="334e5-111">O comando transmite essa tabela para o cmdlet atual usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="334e5-111">The command passes that table to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="334e5-112">O cmdlet atual Obtém a rota chamada Route07 na tabela de rota chamada RouteTable01.</span><span class="sxs-lookup"><span data-stu-id="334e5-112">The current cmdlet gets the route named Route07 in the route table named RouteTable01.</span></span>

## <span data-ttu-id="334e5-113">OS</span><span class="sxs-lookup"><span data-stu-id="334e5-113">PARAMETERS</span></span>

### <span data-ttu-id="334e5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="334e5-114">-DefaultProfile</span></span>
<span data-ttu-id="334e5-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="334e5-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="334e5-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="334e5-116">-Name</span></span>
<span data-ttu-id="334e5-117">Especifica o nome da rota obtida por esse cmdlet.</span><span class="sxs-lookup"><span data-stu-id="334e5-117">Specifies the name of the route that this cmdlet gets.</span></span>

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

### <span data-ttu-id="334e5-118">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="334e5-118">-RouteTable</span></span>
<span data-ttu-id="334e5-119">Especifica a tabela de rotas da qual esse cmdlet obtém rotas.</span><span class="sxs-lookup"><span data-stu-id="334e5-119">Specifies the route table from which this cmdlet gets routes.</span></span>

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

### <span data-ttu-id="334e5-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="334e5-120">CommonParameters</span></span>
<span data-ttu-id="334e5-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="334e5-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="334e5-122">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="334e5-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="334e5-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="334e5-123">INPUTS</span></span>

### <span data-ttu-id="334e5-124">Microsoft. Azure. Commands. Network. Models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="334e5-124">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="334e5-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="334e5-125">OUTPUTS</span></span>

### <span data-ttu-id="334e5-126">Microsoft. Azure. Commands. Network. Models. PSRoute</span><span class="sxs-lookup"><span data-stu-id="334e5-126">Microsoft.Azure.Commands.Network.Models.PSRoute</span></span>

## <span data-ttu-id="334e5-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="334e5-127">NOTES</span></span>

## <span data-ttu-id="334e5-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="334e5-128">RELATED LINKS</span></span>

[<span data-ttu-id="334e5-129">Add-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="334e5-129">Add-AzureRmRouteConfig</span></span>](./Add-AzureRmRouteConfig.md)

[<span data-ttu-id="334e5-130">Get-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="334e5-130">Get-AzureRmRouteTable</span></span>](./Get-AzureRmRouteTable.md)

[<span data-ttu-id="334e5-131">New-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="334e5-131">New-AzureRmRouteConfig</span></span>](./New-AzureRmRouteConfig.md)

[<span data-ttu-id="334e5-132">Remove-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="334e5-132">Remove-AzureRmRouteConfig</span></span>](./Remove-AzureRmRouteConfig.md)

[<span data-ttu-id="334e5-133">Set-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="334e5-133">Set-AzureRmRouteConfig</span></span>](./Set-AzureRmRouteConfig.md)


