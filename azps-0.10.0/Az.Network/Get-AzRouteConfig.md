---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: DBD40431-DD7A-42CB-83AA-568B1065A468
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azrouteconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzRouteConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzRouteConfig.md
ms.openlocfilehash: a5b80a15711314d5acc4f0288c1fd0304da772fc
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775489"
---
# <span data-ttu-id="1ee10-101">Get-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="1ee10-101">Get-AzRouteConfig</span></span>

## <span data-ttu-id="1ee10-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1ee10-102">SYNOPSIS</span></span>
<span data-ttu-id="1ee10-103">Obtém rotas de uma tabela de rota.</span><span class="sxs-lookup"><span data-stu-id="1ee10-103">Gets routes from a route table.</span></span>

## <span data-ttu-id="1ee10-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1ee10-104">SYNTAX</span></span>

```
Get-AzRouteConfig -RouteTable <PSRouteTable> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1ee10-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1ee10-105">DESCRIPTION</span></span>
<span data-ttu-id="1ee10-106">O cmdlet **Get-AzRouteConfig** Obtém rotas de uma tabela de rota do Azure.</span><span class="sxs-lookup"><span data-stu-id="1ee10-106">The **Get-AzRouteConfig** cmdlet gets routes from an Azure route table.</span></span>
<span data-ttu-id="1ee10-107">Você pode especificar uma rota por nome.</span><span class="sxs-lookup"><span data-stu-id="1ee10-107">You can specify a route by name.</span></span>

## <span data-ttu-id="1ee10-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1ee10-108">EXAMPLES</span></span>

### <span data-ttu-id="1ee10-109">Exemplo 1: obter uma tabela de rota</span><span class="sxs-lookup"><span data-stu-id="1ee10-109">Example 1: Get a route table</span></span>
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

<span data-ttu-id="1ee10-110">Esse comando obtém a tabela de rota chamada RouteTable01 usando o cmdlet **Get-AzRouteTable** .</span><span class="sxs-lookup"><span data-stu-id="1ee10-110">This command gets the route table named RouteTable01 by using the **Get-AzRouteTable** cmdlet.</span></span>
<span data-ttu-id="1ee10-111">O comando transmite essa tabela para o cmdlet atual usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="1ee10-111">The command passes that table to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="1ee10-112">O cmdlet atual Obtém a rota chamada Route07 na tabela de rota chamada RouteTable01.</span><span class="sxs-lookup"><span data-stu-id="1ee10-112">The current cmdlet gets the route named Route07 in the route table named RouteTable01.</span></span>

## <span data-ttu-id="1ee10-113">OS</span><span class="sxs-lookup"><span data-stu-id="1ee10-113">PARAMETERS</span></span>

### <span data-ttu-id="1ee10-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ee10-114">-DefaultProfile</span></span>
<span data-ttu-id="1ee10-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1ee10-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1ee10-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="1ee10-116">-Name</span></span>
<span data-ttu-id="1ee10-117">Especifica o nome da rota obtida por esse cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1ee10-117">Specifies the name of the route that this cmdlet gets.</span></span>

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

### <span data-ttu-id="1ee10-118">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="1ee10-118">-RouteTable</span></span>
<span data-ttu-id="1ee10-119">Especifica a tabela de rotas da qual esse cmdlet obtém rotas.</span><span class="sxs-lookup"><span data-stu-id="1ee10-119">Specifies the route table from which this cmdlet gets routes.</span></span>

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

### <span data-ttu-id="1ee10-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ee10-120">CommonParameters</span></span>
<span data-ttu-id="1ee10-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ee10-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ee10-122">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ee10-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ee10-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1ee10-123">INPUTS</span></span>

### <span data-ttu-id="1ee10-124">PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="1ee10-124">PSRouteTable</span></span>
<span data-ttu-id="1ee10-125">O parâmetro ' RouteTable ' aceita o valor do tipo ' PSRouteTable ' da pipeline</span><span class="sxs-lookup"><span data-stu-id="1ee10-125">Parameter 'RouteTable' accepts value of type 'PSRouteTable' from the pipeline</span></span>

## <span data-ttu-id="1ee10-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1ee10-126">OUTPUTS</span></span>

### <span data-ttu-id="1ee10-127">Microsoft. Azure. Commands. Network. Models. PSRoute</span><span class="sxs-lookup"><span data-stu-id="1ee10-127">Microsoft.Azure.Commands.Network.Models.PSRoute</span></span>

## <span data-ttu-id="1ee10-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1ee10-128">NOTES</span></span>

## <span data-ttu-id="1ee10-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1ee10-129">RELATED LINKS</span></span>

[<span data-ttu-id="1ee10-130">Add-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="1ee10-130">Add-AzRouteConfig</span></span>](./Add-AzRouteConfig.md)

[<span data-ttu-id="1ee10-131">Get-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="1ee10-131">Get-AzRouteTable</span></span>](./Get-AzRouteTable.md)

[<span data-ttu-id="1ee10-132">New-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="1ee10-132">New-AzRouteConfig</span></span>](./New-AzRouteConfig.md)

[<span data-ttu-id="1ee10-133">Remove-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="1ee10-133">Remove-AzRouteConfig</span></span>](./Remove-AzRouteConfig.md)

[<span data-ttu-id="1ee10-134">Set-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="1ee10-134">Set-AzRouteConfig</span></span>](./Set-AzRouteConfig.md)


