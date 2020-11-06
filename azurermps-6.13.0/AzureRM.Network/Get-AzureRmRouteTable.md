---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 4F487FCA-930D-4D56-8D28-7693312E1A01
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmRouteTable.md
ms.openlocfilehash: 04e50033a304918eb37d28c2ef5ea5328d5744c0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430163"
---
# <span data-ttu-id="7d078-101">Get-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="7d078-101">Get-AzureRmRouteTable</span></span>

## <span data-ttu-id="7d078-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7d078-102">SYNOPSIS</span></span>
<span data-ttu-id="7d078-103">Obtém tabelas de rota.</span><span class="sxs-lookup"><span data-stu-id="7d078-103">Gets route tables.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7d078-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7d078-104">SYNTAX</span></span>

### <span data-ttu-id="7d078-105">NOEXPAND (padrão)</span><span class="sxs-lookup"><span data-stu-id="7d078-105">NoExpand (Default)</span></span>
```
Get-AzureRmRouteTable [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7d078-106">Amplie</span><span class="sxs-lookup"><span data-stu-id="7d078-106">Expand</span></span>
```
Get-AzureRmRouteTable -ResourceGroupName <String> -Name <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7d078-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7d078-107">DESCRIPTION</span></span>
<span data-ttu-id="7d078-108">O cmdlet **Get-AzureRmRouteTable** Obtém as tabelas de rotas do Azure.</span><span class="sxs-lookup"><span data-stu-id="7d078-108">The **Get-AzureRmRouteTable** cmdlet gets Azure route tables.</span></span>
<span data-ttu-id="7d078-109">Você pode obter uma única tabela de rota ou obter todas as tabelas de rota em um grupo de recursos ou na sua assinatura.</span><span class="sxs-lookup"><span data-stu-id="7d078-109">You can get a single route table, or get all the route tables in a resource group or in your subscription.</span></span>

## <span data-ttu-id="7d078-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7d078-110">EXAMPLES</span></span>

### <span data-ttu-id="7d078-111">Exemplo 1: obter uma tabela de rota</span><span class="sxs-lookup"><span data-stu-id="7d078-111">Example 1: Get a route table</span></span>
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

<span data-ttu-id="7d078-112">Esse comando obtém a tabela de rota chamada RouteTable01 no grupo de recursos chamado ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="7d078-112">This command gets the route table named RouteTable01 in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="7d078-113">OS</span><span class="sxs-lookup"><span data-stu-id="7d078-113">PARAMETERS</span></span>

### <span data-ttu-id="7d078-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d078-114">-DefaultProfile</span></span>
<span data-ttu-id="7d078-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7d078-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7d078-116">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="7d078-116">-ExpandResource</span></span>
```yaml
Type: System.String
Parameter Sets: Expand
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d078-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="7d078-117">-Name</span></span>
<span data-ttu-id="7d078-118">Especifica o nome da tabela de rota obtida por esse cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7d078-118">Specifies the name of the route table that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d078-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d078-119">-ResourceGroupName</span></span>
<span data-ttu-id="7d078-120">Especifica o nome do grupo de recursos que contém as tabelas de rota obtidas por esse cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7d078-120">Specifies the name of the resource group that contains the route tables that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d078-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d078-121">CommonParameters</span></span>
<span data-ttu-id="7d078-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7d078-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d078-123">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7d078-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d078-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7d078-124">INPUTS</span></span>

### <span data-ttu-id="7d078-125">System. String</span><span class="sxs-lookup"><span data-stu-id="7d078-125">System.String</span></span>

## <span data-ttu-id="7d078-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7d078-126">OUTPUTS</span></span>

### <span data-ttu-id="7d078-127">Microsoft. Azure. Commands. Network. Models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="7d078-127">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="7d078-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7d078-128">NOTES</span></span>

## <span data-ttu-id="7d078-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7d078-129">RELATED LINKS</span></span>

[<span data-ttu-id="7d078-130">New-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="7d078-130">New-AzureRmRouteTable</span></span>](./New-AzureRmRouteTable.md)

[<span data-ttu-id="7d078-131">Remove-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="7d078-131">Remove-AzureRmRouteTable</span></span>](./Remove-AzureRmRouteTable.md)

[<span data-ttu-id="7d078-132">Set-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="7d078-132">Set-AzureRmRouteTable</span></span>](./Set-AzureRmRouteTable.md)

