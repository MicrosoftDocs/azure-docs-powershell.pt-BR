---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 1CE2A30A-6DF8-4C4C-8348-C3C1CD4D0146
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmRouteTable.md
ms.openlocfilehash: 6848b00d090b8d365b0c26fb3948a4eec3ad047d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93441301"
---
# <span data-ttu-id="73f0b-101">Set-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="73f0b-101">Set-AzureRmRouteTable</span></span>

## <span data-ttu-id="73f0b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="73f0b-102">SYNOPSIS</span></span>
<span data-ttu-id="73f0b-103">Define o estado da meta para uma tabela de rota.</span><span class="sxs-lookup"><span data-stu-id="73f0b-103">Sets the goal state for a route table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="73f0b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="73f0b-104">SYNTAX</span></span>

```
Set-AzureRmRouteTable -RouteTable <PSRouteTable> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="73f0b-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="73f0b-105">DESCRIPTION</span></span>
<span data-ttu-id="73f0b-106">O cmdlet **set-AzureRmRouteTable** define o estado da meta para uma tabela de rota do Azure.</span><span class="sxs-lookup"><span data-stu-id="73f0b-106">The **Set-AzureRmRouteTable** cmdlet sets the goal state for an Azure route table.</span></span>

## <span data-ttu-id="73f0b-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="73f0b-107">EXAMPLES</span></span>

### <span data-ttu-id="73f0b-108">Exemplo 1: adicionar uma rota e, em seguida, definir o estado da meta da tabela de rota</span><span class="sxs-lookup"><span data-stu-id="73f0b-108">Example 1: Add a route and then set the goal state of the route table</span></span>
```
PS C:\>Get-AzureRmRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01" | Add-AzureRmRouteConfig -Name "Route07" -AddressPrefix 10.2.0.0/16 -NextHopType "VnetLocal" | Set-AzureRmRouteTable
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

<span data-ttu-id="73f0b-109">Esse comando obtém a tabela de rota chamada RouteTable01 usando o cmdlet Get-AzureRmRouteTable.</span><span class="sxs-lookup"><span data-stu-id="73f0b-109">This command gets the route table named RouteTable01 by using Get-AzureRmRouteTable cmdlet.</span></span>
<span data-ttu-id="73f0b-110">O comando passa essa tabela para o cmdlet Add-AzureRmRouteConfig usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="73f0b-110">The command passes that table to the Add-AzureRmRouteConfig cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="73f0b-111">**Add-AzureRmRouteConfig** adiciona a rota chamada Route07 e, em seguida, passa o resultado para o cmdlet atual, que atualiza a tabela para refletir suas alterações.</span><span class="sxs-lookup"><span data-stu-id="73f0b-111">**Add-AzureRmRouteConfig** adds the route named Route07, and then passes the result to the current cmdlet, which updates the table to reflect your changes.</span></span>

## <span data-ttu-id="73f0b-112">OS</span><span class="sxs-lookup"><span data-stu-id="73f0b-112">PARAMETERS</span></span>

### <span data-ttu-id="73f0b-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="73f0b-113">-AsJob</span></span>
<span data-ttu-id="73f0b-114">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="73f0b-114">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73f0b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73f0b-115">-DefaultProfile</span></span>
<span data-ttu-id="73f0b-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="73f0b-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="73f0b-117">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="73f0b-117">-RouteTable</span></span>
<span data-ttu-id="73f0b-118">Especifica um objeto de tabela de rota que representa o estado da meta para o qual esse cmdlet define a tabela de rota.</span><span class="sxs-lookup"><span data-stu-id="73f0b-118">Specifies a route table object that represents the goal state to which this cmdlet sets the route table.</span></span>

```yaml
Type: PSRouteTable
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="73f0b-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="73f0b-119">-Confirm</span></span>
<span data-ttu-id="73f0b-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="73f0b-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73f0b-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="73f0b-121">-WhatIf</span></span>
<span data-ttu-id="73f0b-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="73f0b-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="73f0b-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="73f0b-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73f0b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73f0b-124">CommonParameters</span></span>
<span data-ttu-id="73f0b-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="73f0b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73f0b-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="73f0b-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73f0b-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="73f0b-127">INPUTS</span></span>

### <span data-ttu-id="73f0b-128">PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="73f0b-128">PSRouteTable</span></span>
<span data-ttu-id="73f0b-129">O parâmetro ' RouteTable ' aceita o valor do tipo ' PSRouteTable ' da pipeline</span><span class="sxs-lookup"><span data-stu-id="73f0b-129">Parameter 'RouteTable' accepts value of type 'PSRouteTable' from the pipeline</span></span>

## <span data-ttu-id="73f0b-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="73f0b-130">OUTPUTS</span></span>

### <span data-ttu-id="73f0b-131">Microsoft. Azure. Commands. Network. Models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="73f0b-131">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="73f0b-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="73f0b-132">NOTES</span></span>

## <span data-ttu-id="73f0b-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="73f0b-133">RELATED LINKS</span></span>

[<span data-ttu-id="73f0b-134">Add-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="73f0b-134">Add-AzureRmRouteConfig</span></span>](./Add-AzureRmRouteConfig.md)

[<span data-ttu-id="73f0b-135">Get-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="73f0b-135">Get-AzureRmRouteTable</span></span>](./Get-AzureRmRouteTable.md)

[<span data-ttu-id="73f0b-136">New-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="73f0b-136">New-AzureRmRouteTable</span></span>](./New-AzureRmRouteTable.md)

[<span data-ttu-id="73f0b-137">Remove-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="73f0b-137">Remove-AzureRmRouteTable</span></span>](./Remove-AzureRmRouteTable.md)


