---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 4F487FCA-930D-4D56-8D28-7693312E1A01
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermroutetable
schema: 2.0.0
ms.openlocfilehash: 9498b93d2062bc84d6af423c89eb351c6680eddd
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785329"
---
# <span data-ttu-id="4e0a5-101">Get-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="4e0a5-101">Get-AzureRmRouteTable</span></span>

## <span data-ttu-id="4e0a5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4e0a5-102">SYNOPSIS</span></span>
<span data-ttu-id="4e0a5-103">Obtém tabelas de rota.</span><span class="sxs-lookup"><span data-stu-id="4e0a5-103">Gets route tables.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4e0a5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4e0a5-104">SYNTAX</span></span>

### <span data-ttu-id="4e0a5-105">Amplie</span><span class="sxs-lookup"><span data-stu-id="4e0a5-105">Expand</span></span>
```
Get-AzureRmRouteTable -ResourceGroupName <String> -Name <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4e0a5-106">NOEXPAND</span><span class="sxs-lookup"><span data-stu-id="4e0a5-106">NoExpand</span></span>
```
Get-AzureRmRouteTable [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4e0a5-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4e0a5-107">DESCRIPTION</span></span>
<span data-ttu-id="4e0a5-108">O cmdlet **Get-AzureRmRouteTable** Obtém as tabelas de rotas do Azure.</span><span class="sxs-lookup"><span data-stu-id="4e0a5-108">The **Get-AzureRmRouteTable** cmdlet gets Azure route tables.</span></span>
<span data-ttu-id="4e0a5-109">Você pode obter uma única tabela de rota ou obter todas as tabelas de rota em um grupo de recursos ou na sua assinatura.</span><span class="sxs-lookup"><span data-stu-id="4e0a5-109">You can get a single route table, or get all the route tables in a resource group or in your subscription.</span></span>

## <span data-ttu-id="4e0a5-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4e0a5-110">EXAMPLES</span></span>

### <span data-ttu-id="4e0a5-111">Exemplo 1: obter uma tabela de rota</span><span class="sxs-lookup"><span data-stu-id="4e0a5-111">Example 1: Get a route table</span></span>
```
PS C:\>Get-AzureRmRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01"
Name              : routetable01
ResourceGroupName : ResourceGroup11
Location          : eastus
Id                : /subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Microsoft.Networ
                    k/routeTables/routetable01
Etag              : W/"db5f4e12-3f34-465b-92dd-0ab3bf6fc274"
ProvisioningState : Succeeded
Tags              : 
Routes            : [
                      {
                        "Name": "route07",
                        "Etag": "W/\"db5f4e12-3f34-465b-92dd-0ab3bf6fc274\"",
                        "Id": "/subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Micro
                    soft.Network/routeTables/routetable01/routes/route07",
                        "AddressPrefix": "10.1.0.0/16",
                        "NextHopType": "VnetLocal",
                        "NextHopIpAddress": null, 
                        "ProvisioningState": "Succeeded"
                      }
                    ] 
Subnets           : []
```

<span data-ttu-id="4e0a5-112">Esse comando obtém a tabela de rota chamada RouteTable01 no grupo de recursos chamado ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="4e0a5-112">This command gets the route table named RouteTable01 in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="4e0a5-113">OS</span><span class="sxs-lookup"><span data-stu-id="4e0a5-113">PARAMETERS</span></span>

### <span data-ttu-id="4e0a5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e0a5-114">-DefaultProfile</span></span>
<span data-ttu-id="4e0a5-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4e0a5-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4e0a5-116">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="4e0a5-116">-ExpandResource</span></span>
```yaml
Type: String
Parameter Sets: Expand
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e0a5-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="4e0a5-117">-Name</span></span>
<span data-ttu-id="4e0a5-118">Especifica o nome da tabela de rota obtida por esse cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4e0a5-118">Specifies the name of the route table that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: Expand
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: NoExpand
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e0a5-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e0a5-119">-ResourceGroupName</span></span>
<span data-ttu-id="4e0a5-120">Especifica o nome do grupo de recursos que contém as tabelas de rota obtidas por esse cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4e0a5-120">Specifies the name of the resource group that contains the route tables that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: Expand
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: NoExpand
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e0a5-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e0a5-121">CommonParameters</span></span>
<span data-ttu-id="4e0a5-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4e0a5-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e0a5-123">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4e0a5-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e0a5-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4e0a5-124">INPUTS</span></span>

## <span data-ttu-id="4e0a5-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4e0a5-125">OUTPUTS</span></span>

### <span data-ttu-id="4e0a5-126">Microsoft. Azure. Commands. Network. Models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="4e0a5-126">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="4e0a5-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4e0a5-127">NOTES</span></span>

## <span data-ttu-id="4e0a5-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4e0a5-128">RELATED LINKS</span></span>

[<span data-ttu-id="4e0a5-129">New-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="4e0a5-129">New-AzureRmRouteTable</span></span>](./New-AzureRmRouteTable.md)

[<span data-ttu-id="4e0a5-130">Remove-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="4e0a5-130">Remove-AzureRmRouteTable</span></span>](./Remove-AzureRmRouteTable.md)

[<span data-ttu-id="4e0a5-131">Set-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="4e0a5-131">Set-AzureRmRouteTable</span></span>](./Set-AzureRmRouteTable.md)


