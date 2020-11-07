---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 4F487FCA-930D-4D56-8D28-7693312E1A01
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzRouteTable.md
ms.openlocfilehash: a881e438166729aea8956dc633b7a635499d3752
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775482"
---
# <span data-ttu-id="ff9b2-101">Get-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="ff9b2-101">Get-AzRouteTable</span></span>

## <span data-ttu-id="ff9b2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ff9b2-102">SYNOPSIS</span></span>
<span data-ttu-id="ff9b2-103">Obtém tabelas de rota.</span><span class="sxs-lookup"><span data-stu-id="ff9b2-103">Gets route tables.</span></span>

## <span data-ttu-id="ff9b2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ff9b2-104">SYNTAX</span></span>

### <span data-ttu-id="ff9b2-105">Amplie</span><span class="sxs-lookup"><span data-stu-id="ff9b2-105">Expand</span></span>
```
Get-AzRouteTable -ResourceGroupName <String> -Name <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ff9b2-106">NOEXPAND</span><span class="sxs-lookup"><span data-stu-id="ff9b2-106">NoExpand</span></span>
```
Get-AzRouteTable [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ff9b2-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ff9b2-107">DESCRIPTION</span></span>
<span data-ttu-id="ff9b2-108">O cmdlet **Get-AzRouteTable** Obtém as tabelas de rotas do Azure.</span><span class="sxs-lookup"><span data-stu-id="ff9b2-108">The **Get-AzRouteTable** cmdlet gets Azure route tables.</span></span>
<span data-ttu-id="ff9b2-109">Você pode obter uma única tabela de rota ou obter todas as tabelas de rota em um grupo de recursos ou na sua assinatura.</span><span class="sxs-lookup"><span data-stu-id="ff9b2-109">You can get a single route table, or get all the route tables in a resource group or in your subscription.</span></span>

## <span data-ttu-id="ff9b2-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ff9b2-110">EXAMPLES</span></span>

### <span data-ttu-id="ff9b2-111">Exemplo 1: obter uma tabela de rota</span><span class="sxs-lookup"><span data-stu-id="ff9b2-111">Example 1: Get a route table</span></span>
```
PS C:\>Get-AzRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01"
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

<span data-ttu-id="ff9b2-112">Esse comando obtém a tabela de rota chamada RouteTable01 no grupo de recursos chamado ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="ff9b2-112">This command gets the route table named RouteTable01 in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="ff9b2-113">OS</span><span class="sxs-lookup"><span data-stu-id="ff9b2-113">PARAMETERS</span></span>

### <span data-ttu-id="ff9b2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff9b2-114">-DefaultProfile</span></span>
<span data-ttu-id="ff9b2-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ff9b2-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ff9b2-116">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="ff9b2-116">-ExpandResource</span></span>
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

### <span data-ttu-id="ff9b2-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="ff9b2-117">-Name</span></span>
<span data-ttu-id="ff9b2-118">Especifica o nome da tabela de rota obtida por esse cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ff9b2-118">Specifies the name of the route table that this cmdlet gets.</span></span>

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

### <span data-ttu-id="ff9b2-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff9b2-119">-ResourceGroupName</span></span>
<span data-ttu-id="ff9b2-120">Especifica o nome do grupo de recursos que contém as tabelas de rota obtidas por esse cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ff9b2-120">Specifies the name of the resource group that contains the route tables that this cmdlet gets.</span></span>

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

### <span data-ttu-id="ff9b2-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff9b2-121">CommonParameters</span></span>
<span data-ttu-id="ff9b2-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff9b2-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff9b2-123">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff9b2-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff9b2-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ff9b2-124">INPUTS</span></span>

## <span data-ttu-id="ff9b2-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ff9b2-125">OUTPUTS</span></span>

### <span data-ttu-id="ff9b2-126">Microsoft. Azure. Commands. Network. Models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="ff9b2-126">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="ff9b2-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ff9b2-127">NOTES</span></span>

## <span data-ttu-id="ff9b2-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ff9b2-128">RELATED LINKS</span></span>

[<span data-ttu-id="ff9b2-129">New-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="ff9b2-129">New-AzRouteTable</span></span>](./New-AzRouteTable.md)

[<span data-ttu-id="ff9b2-130">Remove-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="ff9b2-130">Remove-AzRouteTable</span></span>](./Remove-AzRouteTable.md)

[<span data-ttu-id="ff9b2-131">Set-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="ff9b2-131">Set-AzRouteTable</span></span>](./Set-AzRouteTable.md)


