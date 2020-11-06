---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: DBD40431-DD7A-42CB-83AA-568B1065A468
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmRouteConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmRouteConfig.md
ms.openlocfilehash: f0d537e2729fc69f2a65563ab059f332d320e99a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431108"
---
# <span data-ttu-id="d72e1-101">Get-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="d72e1-101">Get-AzureRmRouteConfig</span></span>

## <span data-ttu-id="d72e1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d72e1-102">SYNOPSIS</span></span>
<span data-ttu-id="d72e1-103">Obtém rotas de uma tabela de rota.</span><span class="sxs-lookup"><span data-stu-id="d72e1-103">Gets routes from a route table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d72e1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d72e1-104">SYNTAX</span></span>

```
Get-AzureRmRouteConfig [-Name <String>] -RouteTable <PSRouteTable> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d72e1-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d72e1-105">DESCRIPTION</span></span>
<span data-ttu-id="d72e1-106">O cmdlet **Get-AzureRmRouteConfig** Obtém rotas de uma tabela de rota do Azure.</span><span class="sxs-lookup"><span data-stu-id="d72e1-106">The **Get-AzureRmRouteConfig** cmdlet gets routes from an Azure route table.</span></span>
<span data-ttu-id="d72e1-107">Você pode especificar uma rota por nome.</span><span class="sxs-lookup"><span data-stu-id="d72e1-107">You can specify a route by name.</span></span>

## <span data-ttu-id="d72e1-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d72e1-108">EXAMPLES</span></span>

### <span data-ttu-id="d72e1-109">Exemplo 1: obter uma tabela de rota</span><span class="sxs-lookup"><span data-stu-id="d72e1-109">Example 1: Get a route table</span></span>
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

<span data-ttu-id="d72e1-110">Esse comando obtém a tabela de rota chamada RouteTable01 usando o cmdlet **Get-AzureRmRouteTable** .</span><span class="sxs-lookup"><span data-stu-id="d72e1-110">This command gets the route table named RouteTable01 by using the **Get-AzureRmRouteTable** cmdlet.</span></span>
<span data-ttu-id="d72e1-111">O comando transmite essa tabela para o cmdlet atual usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="d72e1-111">The command passes that table to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="d72e1-112">O cmdlet atual Obtém a rota chamada Route07 na tabela de rota chamada RouteTable01.</span><span class="sxs-lookup"><span data-stu-id="d72e1-112">The current cmdlet gets the route named Route07 in the route table named RouteTable01.</span></span>

## <span data-ttu-id="d72e1-113">OS</span><span class="sxs-lookup"><span data-stu-id="d72e1-113">PARAMETERS</span></span>

### <span data-ttu-id="d72e1-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="d72e1-114">-Name</span></span>
<span data-ttu-id="d72e1-115">Especifica o nome da rota obtida por esse cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d72e1-115">Specifies the name of the route that this cmdlet gets.</span></span>

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

### <span data-ttu-id="d72e1-116">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="d72e1-116">-RouteTable</span></span>
<span data-ttu-id="d72e1-117">Especifica a tabela de rotas da qual esse cmdlet obtém rotas.</span><span class="sxs-lookup"><span data-stu-id="d72e1-117">Specifies the route table from which this cmdlet gets routes.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRouteTable
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d72e1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d72e1-118">-DefaultProfile</span></span>
<span data-ttu-id="d72e1-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d72e1-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d72e1-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d72e1-120">CommonParameters</span></span>
<span data-ttu-id="d72e1-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d72e1-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d72e1-122">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d72e1-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d72e1-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d72e1-123">INPUTS</span></span>

### <span data-ttu-id="d72e1-124">PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="d72e1-124">PSRouteTable</span></span>
<span data-ttu-id="d72e1-125">O parâmetro ' RouteTable ' aceita o valor do tipo ' PSRouteTable ' da pipeline</span><span class="sxs-lookup"><span data-stu-id="d72e1-125">Parameter 'RouteTable' accepts value of type 'PSRouteTable' from the pipeline</span></span>

## <span data-ttu-id="d72e1-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d72e1-126">OUTPUTS</span></span>

### <span data-ttu-id="d72e1-127">Microsoft. Azure. Commands. Network. Models. PSRoute</span><span class="sxs-lookup"><span data-stu-id="d72e1-127">Microsoft.Azure.Commands.Network.Models.PSRoute</span></span>

## <span data-ttu-id="d72e1-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d72e1-128">NOTES</span></span>

## <span data-ttu-id="d72e1-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d72e1-129">RELATED LINKS</span></span>

[<span data-ttu-id="d72e1-130">Add-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="d72e1-130">Add-AzureRmRouteConfig</span></span>](./Add-AzureRmRouteConfig.md)

[<span data-ttu-id="d72e1-131">Get-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="d72e1-131">Get-AzureRmRouteTable</span></span>](./Get-AzureRmRouteTable.md)

[<span data-ttu-id="d72e1-132">New-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="d72e1-132">New-AzureRmRouteConfig</span></span>](./New-AzureRmRouteConfig.md)

[<span data-ttu-id="d72e1-133">Remove-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="d72e1-133">Remove-AzureRmRouteConfig</span></span>](./Remove-AzureRmRouteConfig.md)

[<span data-ttu-id="d72e1-134">Set-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="d72e1-134">Set-AzureRmRouteConfig</span></span>](./Set-AzureRmRouteConfig.md)


