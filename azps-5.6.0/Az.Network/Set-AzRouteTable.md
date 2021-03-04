---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 1CE2A30A-6DF8-4C4C-8348-C3C1CD4D0146
online version: https://docs.microsoft.com/powershell/module/az.network/set-azroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzRouteTable.md
ms.openlocfilehash: 6bd40f09089b9030e50d30e7155d13b85b7978a9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892941"
---
# <span data-ttu-id="d46e2-101">Set-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="d46e2-101">Set-AzRouteTable</span></span>

## <span data-ttu-id="d46e2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d46e2-102">SYNOPSIS</span></span>
<span data-ttu-id="d46e2-103">Atualiza uma tabela de rota.</span><span class="sxs-lookup"><span data-stu-id="d46e2-103">Updates a route table.</span></span>

## <span data-ttu-id="d46e2-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="d46e2-104">SYNTAX</span></span>

```
Set-AzRouteTable -RouteTable <PSRouteTable> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d46e2-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="d46e2-105">DESCRIPTION</span></span>
<span data-ttu-id="d46e2-106">O cmdlet **Set-AzRouteTable** atualiza uma tabela de rota.</span><span class="sxs-lookup"><span data-stu-id="d46e2-106">The **Set-AzRouteTable** cmdlet updates a route table.</span></span>

## <span data-ttu-id="d46e2-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d46e2-107">EXAMPLES</span></span>

### <span data-ttu-id="d46e2-108">Exemplo 1: atualizar uma tabela de rota adicionando configuração de rota a ela</span><span class="sxs-lookup"><span data-stu-id="d46e2-108">Example 1: Update a route table by adding route configuration to it</span></span>
```
PS C:\>Get-AzRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01" | Add-AzRouteConfig -Name "Route07" -AddressPrefix 10.2.0.0/16 -NextHopType "VnetLocal" | Set-AzRouteTable
Name              : RouteTable01
ResourceGroupName : ResourceGroup11
Location          : eastus
Id                : /subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Microsoft.Networ
                    k/routeTables/RouteTable01
Etag              : W/"f13e1bc8-d41f-44d0-882d-b8b5a1134f59"
ProvisioningState : Succeeded
Tags              : 
Routes            : [
                      {
                        "Name": "Route07",
                        "Etag": "W/\"f13e1bc8-d41f-44d0-882d-b8b5a1134f59\"",
                        "Id": "/subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Micro
                    soft.Network/RouteTables/RouteTable01/routes/Route07",
                        "AddressPrefix": "10.1.0.0/16",
                        "NextHopType": "VnetLocal",
                        "NextHopIpAddress": null, 
                        "ProvisioningState": "Succeeded"
                      },
                      {
                        "Name": "Route07",
                        "Etag": "W/\"f13e1bc8-d41f-44d0-882d-b8b5a1134f59\"",
                        "Id": "/subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Micro
                    soft.Network/RouteTables/RouteTable01/routes/Route07",
                        "AddressPrefix": "10.2.0.0/16",
                        "NextHopType": "VnetLocal",
                        "NextHopIpAddress": null, 
                        "ProvisioningState": "Succeeded"
                      },
                      {
                        "Name": "Route13",
                        "Etag": null, 
                        "Id": null, 
                        "AddressPrefix": "10.3.0.0/16",
                        "NextHopType": "VnetLocal",
                        "NextHopIpAddress": null, 
                        "ProvisioningState": null
                      }
                    ] 
Subnets           : []
```

<span data-ttu-id="d46e2-109">Este comando obtém a tabela de rota chamada RouteTable01 usando Get-AzRouteTable cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d46e2-109">This command gets the route table named RouteTable01 by using Get-AzRouteTable cmdlet.</span></span>
<span data-ttu-id="d46e2-110">O comando passa essa tabela para o cmdlet Add-AzRouteConfig usando o operador de pipeline.</span><span class="sxs-lookup"><span data-stu-id="d46e2-110">The command passes that table to the Add-AzRouteConfig cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="d46e2-111">**Add-AzRouteConfig** adiciona a rota chamada Route07 e passa o resultado para o cmdlet atual, que atualiza a tabela para refletir suas alterações.</span><span class="sxs-lookup"><span data-stu-id="d46e2-111">**Add-AzRouteConfig** adds the route named Route07, and then passes the result to the current cmdlet, which updates the table to reflect your changes.</span></span>

### <span data-ttu-id="d46e2-112">Exemplo 2: Modificar tabela de rota</span><span class="sxs-lookup"><span data-stu-id="d46e2-112">Example 2: Modify route table</span></span>

```
PS C:\> $rt = Get-AzRouteTable -ResourceGroupName "rgName" -Name "rtName"
PS C:\> $rt.DisableBgpRoutePropagation
False
PS C:\> $rt.DisableBgpRoutePropagation = $true
PS C:\> Set-AzRouteTable -RouteTable $rt
PS C:\> $rt = Get-AzRouteTable -ResourceGroupName "rgName" -Name "rtName"
PS C:\> $rt.DisableBgpRoutePropagation
True
```

<span data-ttu-id="d46e2-113">O primeiro comando obtém a tabela de rota chamada rtName e a armazena na variável $rt de rota.</span><span class="sxs-lookup"><span data-stu-id="d46e2-113">The first command gets the route table named rtName and stores it in the $rt variable.</span></span>
<span data-ttu-id="d46e2-114">O segundo comando exibe o valor disableBgpRoutePropagation.</span><span class="sxs-lookup"><span data-stu-id="d46e2-114">The second command displays the value of DisableBgpRoutePropagation.</span></span>
<span data-ttu-id="d46e2-115">O terceiro comando atualiza o valor de DisableBgpRoutePropagation.</span><span class="sxs-lookup"><span data-stu-id="d46e2-115">The third command updates value of DisableBgpRoutePropagation.</span></span>
<span data-ttu-id="d46e2-116">O quarto comando atualiza a tabela de rota no servidor.</span><span class="sxs-lookup"><span data-stu-id="d46e2-116">The fourth command updates route table on the server.</span></span>
<span data-ttu-id="d46e2-117">O quinto comando obtém a tabela de rota atualizada e a armazena na variável $rt.</span><span class="sxs-lookup"><span data-stu-id="d46e2-117">The fifth command gets updated route table and stores it in the $rt variable.</span></span>
<span data-ttu-id="d46e2-118">O sexto comando exibe o valor disableBgpRoutePropagation.</span><span class="sxs-lookup"><span data-stu-id="d46e2-118">The sixth command displays the value of DisableBgpRoutePropagation.</span></span>

## <span data-ttu-id="d46e2-119">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="d46e2-119">PARAMETERS</span></span>

### <span data-ttu-id="d46e2-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d46e2-120">-AsJob</span></span>
<span data-ttu-id="d46e2-121">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="d46e2-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d46e2-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d46e2-122">-DefaultProfile</span></span>
<span data-ttu-id="d46e2-123">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="d46e2-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d46e2-124">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="d46e2-124">-RouteTable</span></span>
<span data-ttu-id="d46e2-125">Especifica um objeto de tabela de rota que representa o estado para o qual a tabela de rota deve ser definida.</span><span class="sxs-lookup"><span data-stu-id="d46e2-125">Specifies a route table object representing the state to which the route table should be set.</span></span>

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

### <span data-ttu-id="d46e2-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d46e2-126">-Confirm</span></span>
<span data-ttu-id="d46e2-127">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d46e2-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d46e2-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d46e2-128">-WhatIf</span></span>
<span data-ttu-id="d46e2-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d46e2-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d46e2-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d46e2-130">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d46e2-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d46e2-131">CommonParameters</span></span>
<span data-ttu-id="d46e2-132">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d46e2-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d46e2-133">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d46e2-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d46e2-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d46e2-134">INPUTS</span></span>

### <span data-ttu-id="d46e2-135">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="d46e2-135">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="d46e2-136">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="d46e2-136">OUTPUTS</span></span>

### <span data-ttu-id="d46e2-137">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="d46e2-137">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="d46e2-138">NOTES</span><span class="sxs-lookup"><span data-stu-id="d46e2-138">NOTES</span></span>

## <span data-ttu-id="d46e2-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d46e2-139">RELATED LINKS</span></span>

[<span data-ttu-id="d46e2-140">Add-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="d46e2-140">Add-AzRouteConfig</span></span>](./Add-AzRouteConfig.md)

[<span data-ttu-id="d46e2-141">Get-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="d46e2-141">Get-AzRouteTable</span></span>](./Get-AzRouteTable.md)

[<span data-ttu-id="d46e2-142">New-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="d46e2-142">New-AzRouteTable</span></span>](./New-AzRouteTable.md)

[<span data-ttu-id="d46e2-143">Remove-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="d46e2-143">Remove-AzRouteTable</span></span>](./Remove-AzRouteTable.md)


