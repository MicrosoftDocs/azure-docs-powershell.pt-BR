---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6A278F91-C078-4DD4-82D0-2E4FA549A089
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRouteTable.md
ms.openlocfilehash: ac7b370a6a10aff5a9524a2536b5f4dedaff5a9f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93772344"
---
# <span data-ttu-id="4350b-101">New-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="4350b-101">New-AzRouteTable</span></span>

## <span data-ttu-id="4350b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4350b-102">SYNOPSIS</span></span>
<span data-ttu-id="4350b-103">Cria uma tabela de rota.</span><span class="sxs-lookup"><span data-stu-id="4350b-103">Creates a route table.</span></span>

## <span data-ttu-id="4350b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4350b-104">SYNTAX</span></span>

```
New-AzRouteTable -ResourceGroupName <String> -Name <String> [-DisableBgpRoutePropagation] -Location <String>
 [-Tag <Hashtable>] [-Route <PSRoute[]>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4350b-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4350b-105">DESCRIPTION</span></span>
<span data-ttu-id="4350b-106">O cmdlet **New-AzRouteTable** cria uma tabela de rota do Azure.</span><span class="sxs-lookup"><span data-stu-id="4350b-106">The **New-AzRouteTable** cmdlet creates an Azure route table.</span></span>

## <span data-ttu-id="4350b-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4350b-107">EXAMPLES</span></span>

### <span data-ttu-id="4350b-108">Exemplo 1: criar uma tabela de rota que contenha uma rota</span><span class="sxs-lookup"><span data-stu-id="4350b-108">Example 1: Create a route table that contains a route</span></span>
```
PS C:\>$Route = New-AzRouteConfig -Name "Route07" -AddressPrefix 10.1.0.0/16 -NextHopType "VnetLocal"
PS C:\> New-AzRouteTable -Name "RouteTable01" -ResourceGroupName "ResourceGroup11" -Location "EASTUS" -Route $Route
Name              : routetable01
ResourceGroupName : ResourceGroup11
Location          : eastus
Id                : /subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Microsoft.Networ
                    k/routeTables/myroutetable
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

<span data-ttu-id="4350b-109">O primeiro comando cria uma rota chamada Route07 usando o cmdlet New-AzRouteConfig e a armazena na variável $Route.</span><span class="sxs-lookup"><span data-stu-id="4350b-109">The first command creates a route named Route07 by using the New-AzRouteConfig cmdlet, and then stores it in the $Route variable.</span></span> <span data-ttu-id="4350b-110">Essa rota encaminha pacotes para a rede virtual local.</span><span class="sxs-lookup"><span data-stu-id="4350b-110">This route forwards packets to the local virtual network.</span></span>
<span data-ttu-id="4350b-111">O segundo comando cria uma tabela de rota chamada RouteTable01 e adiciona a rota armazenada no $Route para a nova tabela.</span><span class="sxs-lookup"><span data-stu-id="4350b-111">The second command creates a route table named RouteTable01, and adds the route stored in $Route to the new table.</span></span> <span data-ttu-id="4350b-112">O comando especifica o grupo de recursos ao qual a tabela pertence e o local da tabela.</span><span class="sxs-lookup"><span data-stu-id="4350b-112">The command specifies the resource group to which the table belongs and the location for the table.</span></span>

## <span data-ttu-id="4350b-113">OS</span><span class="sxs-lookup"><span data-stu-id="4350b-113">PARAMETERS</span></span>

### <span data-ttu-id="4350b-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4350b-114">-AsJob</span></span>
<span data-ttu-id="4350b-115">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="4350b-115">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4350b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4350b-116">-DefaultProfile</span></span>
<span data-ttu-id="4350b-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4350b-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4350b-118">-DisableBgpRoutePropagation</span><span class="sxs-lookup"><span data-stu-id="4350b-118">-DisableBgpRoutePropagation</span></span>
<span data-ttu-id="4350b-119">Desabilitar a propagação automática de rota BGP.</span><span class="sxs-lookup"><span data-stu-id="4350b-119">Disable BGP Route auto propagation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4350b-120">-Force</span><span class="sxs-lookup"><span data-stu-id="4350b-120">-Force</span></span>
<span data-ttu-id="4350b-121">Indica que esse cmdlet cria uma tabela de rota mesmo que uma tabela de rota com o mesmo nome já exista.</span><span class="sxs-lookup"><span data-stu-id="4350b-121">Indicates that this cmdlet creates a route table even if a route table that has the same name already exists.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4350b-122">-Local</span><span class="sxs-lookup"><span data-stu-id="4350b-122">-Location</span></span>
<span data-ttu-id="4350b-123">Especifica a região do Azure na qual esse cmdlet cria uma tabela de rota.</span><span class="sxs-lookup"><span data-stu-id="4350b-123">Specifies the Azure region in which this cmdlet creates a route table.</span></span>
<span data-ttu-id="4350b-124">Para obter mais informações, consulte [regiões do Azure](https://azure.microsoft.com/en-us/regions/).</span><span class="sxs-lookup"><span data-stu-id="4350b-124">For more information, see [Azure Regions](https://azure.microsoft.com/en-us/regions/).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4350b-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="4350b-125">-Name</span></span>
<span data-ttu-id="4350b-126">Especifica um nome para a tabela de rota.</span><span class="sxs-lookup"><span data-stu-id="4350b-126">Specifies a name for the route table.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4350b-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4350b-127">-ResourceGroupName</span></span>
<span data-ttu-id="4350b-128">Especifica o nome do grupo de recursos em que esse cmdlet cria uma tabela de rota.</span><span class="sxs-lookup"><span data-stu-id="4350b-128">Specifies the name of the resource group in which this cmdlet creates a route table.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4350b-129">-Rota</span><span class="sxs-lookup"><span data-stu-id="4350b-129">-Route</span></span>
<span data-ttu-id="4350b-130">Especifica uma matriz de objetos de **rota** a serem associados à tabela de rota.</span><span class="sxs-lookup"><span data-stu-id="4350b-130">Specifies an array of **Route** objects to associate with the route table.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRoute[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4350b-131">-Marca</span><span class="sxs-lookup"><span data-stu-id="4350b-131">-Tag</span></span>
<span data-ttu-id="4350b-132">Pares de valores chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="4350b-132">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="4350b-133">Por exemplo: @ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="4350b-133">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4350b-134">-Confirme</span><span class="sxs-lookup"><span data-stu-id="4350b-134">-Confirm</span></span>
<span data-ttu-id="4350b-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4350b-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4350b-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4350b-136">-WhatIf</span></span>
<span data-ttu-id="4350b-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="4350b-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4350b-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4350b-138">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4350b-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4350b-139">CommonParameters</span></span>
<span data-ttu-id="4350b-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4350b-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4350b-141">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4350b-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4350b-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4350b-142">INPUTS</span></span>

### <span data-ttu-id="4350b-143">System. String</span><span class="sxs-lookup"><span data-stu-id="4350b-143">System.String</span></span>

### <span data-ttu-id="4350b-144">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="4350b-144">System.Collections.Hashtable</span></span>

### <span data-ttu-id="4350b-145">Microsoft. Azure. Commands. Network. Models. PSRoute []</span><span class="sxs-lookup"><span data-stu-id="4350b-145">Microsoft.Azure.Commands.Network.Models.PSRoute[]</span></span>

## <span data-ttu-id="4350b-146">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4350b-146">OUTPUTS</span></span>

### <span data-ttu-id="4350b-147">Microsoft. Azure. Commands. Network. Models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="4350b-147">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="4350b-148">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4350b-148">NOTES</span></span>

## <span data-ttu-id="4350b-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4350b-149">RELATED LINKS</span></span>

[<span data-ttu-id="4350b-150">Get-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="4350b-150">Get-AzRouteTable</span></span>](./Get-AzRouteTable.md)

[<span data-ttu-id="4350b-151">New-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="4350b-151">New-AzRouteConfig</span></span>](./New-AzRouteConfig.md)

[<span data-ttu-id="4350b-152">Remove-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="4350b-152">Remove-AzRouteTable</span></span>](./Remove-AzRouteTable.md)

[<span data-ttu-id="4350b-153">Set-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="4350b-153">Set-AzRouteTable</span></span>](./Set-AzRouteTable.md)