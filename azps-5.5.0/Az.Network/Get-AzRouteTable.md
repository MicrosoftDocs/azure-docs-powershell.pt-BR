---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 4F487FCA-930D-4D56-8D28-7693312E1A01
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteTable.md
ms.openlocfilehash: 613519f6d9d3d2d8ce1c83ff0ad5a2d9421859b8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112882"
---
# <span data-ttu-id="34ec9-101">Get-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="34ec9-101">Get-AzRouteTable</span></span>

## <span data-ttu-id="34ec9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="34ec9-102">SYNOPSIS</span></span>
<span data-ttu-id="34ec9-103">Obtém tabelas de rota.</span><span class="sxs-lookup"><span data-stu-id="34ec9-103">Gets route tables.</span></span>

## <span data-ttu-id="34ec9-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="34ec9-104">SYNTAX</span></span>

### <span data-ttu-id="34ec9-105">NoExpand (Padrão)</span><span class="sxs-lookup"><span data-stu-id="34ec9-105">NoExpand (Default)</span></span>
```
Get-AzRouteTable [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="34ec9-106">Expandir</span><span class="sxs-lookup"><span data-stu-id="34ec9-106">Expand</span></span>
```
Get-AzRouteTable -ResourceGroupName <String> -Name <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="34ec9-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="34ec9-107">DESCRIPTION</span></span>
<span data-ttu-id="34ec9-108">O **cmdlet Get-AzRouteTable** obtém tabelas de rota do Azure.</span><span class="sxs-lookup"><span data-stu-id="34ec9-108">The **Get-AzRouteTable** cmdlet gets Azure route tables.</span></span>
<span data-ttu-id="34ec9-109">Você pode obter uma única tabela de rota ou obter todas as tabelas de rota em um grupo de recursos ou em sua assinatura.</span><span class="sxs-lookup"><span data-stu-id="34ec9-109">You can get a single route table, or get all the route tables in a resource group or in your subscription.</span></span>

## <span data-ttu-id="34ec9-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="34ec9-110">EXAMPLES</span></span>

### <span data-ttu-id="34ec9-111">Exemplo 1: Obter uma tabela de rota</span><span class="sxs-lookup"><span data-stu-id="34ec9-111">Example 1: Get a route table</span></span>
```
PS C:\> Get-AzRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01"

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

<span data-ttu-id="34ec9-112">Esse comando obtém a tabela de rota chamada Roteamento01 no grupo de recursos chamado ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="34ec9-112">This command gets the route table named RouteTable01 in the resource group named ResourceGroup11.</span></span>

### <span data-ttu-id="34ec9-113">Exemplo 2: Listar tabelas de roteamento usando filtragem</span><span class="sxs-lookup"><span data-stu-id="34ec9-113">Example 2: List route tables using filtering</span></span>
```
PS C:\> Get-AzRouteTable -Name RouteTable*

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

Name              : routetable02
ResourceGroupName : ResourceGroup11
Location          : eastus
Id                : /subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Microsoft.Networ
                    k/routeTables/routetable02
Etag              : W/"db5f4e12-3f34-465b-92dd-0ab3bf6fc274"
ProvisioningState : Succeeded
Tags              : 
Routes            : [
                      {
                        "Name": "route07",
                        "Etag": "W/\"db5f4e12-3f34-465b-92dd-0ab3bf6fc274\"",
                        "Id": "/subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Micro
                    soft.Network/routeTables/routetable02/routes/route07",
                        "AddressPrefix": "10.1.0.0/16",
                        "NextHopType": "VnetLocal",
                        "NextHopIpAddress": null, 
                        "ProvisioningState": "Succeeded"
                      }
                    ] 
Subnets           : []
```

<span data-ttu-id="34ec9-114">Esse comando obtém todas as tabelas de rota cujo nome começa com "Tabela de Rota"</span><span class="sxs-lookup"><span data-stu-id="34ec9-114">This command gets all route tables whose name starts with "RouteTable"</span></span>

## <span data-ttu-id="34ec9-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="34ec9-115">PARAMETERS</span></span>

### <span data-ttu-id="34ec9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34ec9-116">-DefaultProfile</span></span>
<span data-ttu-id="34ec9-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="34ec9-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="34ec9-118">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="34ec9-118">-ExpandResource</span></span>
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

### <span data-ttu-id="34ec9-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="34ec9-119">-Name</span></span>
<span data-ttu-id="34ec9-120">Especifica o nome da tabela de rota que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="34ec9-120">Specifies the name of the route table that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="34ec9-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34ec9-121">-ResourceGroupName</span></span>
<span data-ttu-id="34ec9-122">Especifica o nome do grupo de recursos que contém as tabelas de rota que esse cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="34ec9-122">Specifies the name of the resource group that contains the route tables that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="34ec9-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34ec9-123">CommonParameters</span></span>
<span data-ttu-id="34ec9-124">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34ec9-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34ec9-125">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="34ec9-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34ec9-126">Entradas</span><span class="sxs-lookup"><span data-stu-id="34ec9-126">INPUTS</span></span>

### <span data-ttu-id="34ec9-127">System.String</span><span class="sxs-lookup"><span data-stu-id="34ec9-127">System.String</span></span>

## <span data-ttu-id="34ec9-128">Saídas</span><span class="sxs-lookup"><span data-stu-id="34ec9-128">OUTPUTS</span></span>

### <span data-ttu-id="34ec9-129">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="34ec9-129">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="34ec9-130">Notas</span><span class="sxs-lookup"><span data-stu-id="34ec9-130">NOTES</span></span>

## <span data-ttu-id="34ec9-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="34ec9-131">RELATED LINKS</span></span>

[<span data-ttu-id="34ec9-132">New-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="34ec9-132">New-AzRouteTable</span></span>](./New-AzRouteTable.md)

[<span data-ttu-id="34ec9-133">Remove-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="34ec9-133">Remove-AzRouteTable</span></span>](./Remove-AzRouteTable.md)

[<span data-ttu-id="34ec9-134">Set-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="34ec9-134">Set-AzRouteTable</span></span>](./Set-AzRouteTable.md)


