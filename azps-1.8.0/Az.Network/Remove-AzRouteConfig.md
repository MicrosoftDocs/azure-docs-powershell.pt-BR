---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 03285628-6BD3-4F2F-8129-E3CAE4C70EC8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azrouteconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteConfig.md
ms.openlocfilehash: b8ace5d38878e9acbdbfaa25e3bfd4ebfc185260
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93600126"
---
# <span data-ttu-id="bc91e-101">Remove-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="bc91e-101">Remove-AzRouteConfig</span></span>

## <span data-ttu-id="bc91e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bc91e-102">SYNOPSIS</span></span>
<span data-ttu-id="bc91e-103">Remove uma rota de uma tabela de rota.</span><span class="sxs-lookup"><span data-stu-id="bc91e-103">Removes a route from a route table.</span></span>

## <span data-ttu-id="bc91e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bc91e-104">SYNTAX</span></span>

```
Remove-AzRouteConfig -RouteTable <PSRouteTable> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bc91e-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="bc91e-105">DESCRIPTION</span></span>
<span data-ttu-id="bc91e-106">O cmdlet **Remove-AzRouteConfig** remove uma rota de uma tabela de rota do Azure.</span><span class="sxs-lookup"><span data-stu-id="bc91e-106">The **Remove-AzRouteConfig** cmdlet removes a route from an Azure route table.</span></span>

## <span data-ttu-id="bc91e-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bc91e-107">EXAMPLES</span></span>

### <span data-ttu-id="bc91e-108">Exemplo 1: remover uma rota</span><span class="sxs-lookup"><span data-stu-id="bc91e-108">Example 1: Remove a route</span></span>
```
PS C:\>Get-AzRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01" | Remove-AzRouteConfig -Name "Route02" | Set-AzRouteTable
Name              : RouteTable01
ResourceGroupName : ResourceGroup11
Location          : eastus
Id                : /subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Microsoft.Networ
                    k/routeTables/RouteTable01
Etag              : W/"47099b62-60ec-4bc1-b87b-fad56cb8bed1"
ProvisioningState : Succeeded
Tags              : 
Routes            : [
                      {
                        "Name": "Route07",
                        "Etag": "W/\"47099b62-60ec-4bc1-b87b-fad56cb8bed1\"",
                        "Id": "/subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Micro
                    soft.Network/routeTables/RouteTable01/routes/Route07",
                        "AddressPrefix": "10.1.0.0/16",
                        "NextHopType": "VnetLocal",
                        "NextHopIpAddress": null, 
                        "ProvisioningState": "Succeeded"
                      }
                    ] 
Subnets           : []
```

<span data-ttu-id="bc91e-109">Esse comando obtém a tabela de rota chamada RouteTable01 usando o cmdlet **Get-AzRouteTable** .</span><span class="sxs-lookup"><span data-stu-id="bc91e-109">This command gets the route table named RouteTable01 by using the **Get-AzRouteTable** cmdlet.</span></span>
<span data-ttu-id="bc91e-110">O comando transmite essa tabela para o cmdlet atual usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="bc91e-110">The command passes that table to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="bc91e-111">O cmdlet atual remove a rota chamada Route02 e passa o resultado para o cmdlet **set-AzRouteTable** , que atualiza a tabela para refletir suas alterações.</span><span class="sxs-lookup"><span data-stu-id="bc91e-111">The current cmdlet remove the route named Route02, and the passes the result to the **Set-AzRouteTable** cmdlet, which updates the table to reflect your changes.</span></span>
<span data-ttu-id="bc91e-112">A tabela não contém mais a rota chamada Route02.</span><span class="sxs-lookup"><span data-stu-id="bc91e-112">The table no longer contains the route named Route02.</span></span>

## <span data-ttu-id="bc91e-113">OS</span><span class="sxs-lookup"><span data-stu-id="bc91e-113">PARAMETERS</span></span>

### <span data-ttu-id="bc91e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc91e-114">-DefaultProfile</span></span>
<span data-ttu-id="bc91e-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="bc91e-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bc91e-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="bc91e-116">-Name</span></span>
<span data-ttu-id="bc91e-117">Especifica o nome da rota que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="bc91e-117">Specifies the name of the route that this cmdlet removes.</span></span>

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

### <span data-ttu-id="bc91e-118">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="bc91e-118">-RouteTable</span></span>
<span data-ttu-id="bc91e-119">Especifica a tabela de rota que contém a rota que este cmdlet exclui.</span><span class="sxs-lookup"><span data-stu-id="bc91e-119">Specifies the route table that contains the route that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="bc91e-120">-Confirme</span><span class="sxs-lookup"><span data-stu-id="bc91e-120">-Confirm</span></span>
<span data-ttu-id="bc91e-121">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bc91e-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bc91e-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bc91e-122">-WhatIf</span></span>
<span data-ttu-id="bc91e-123">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="bc91e-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bc91e-124">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="bc91e-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bc91e-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc91e-125">CommonParameters</span></span>
<span data-ttu-id="bc91e-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bc91e-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc91e-127">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bc91e-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc91e-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="bc91e-128">INPUTS</span></span>

### <span data-ttu-id="bc91e-129">Microsoft. Azure. Commands. Network. Models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="bc91e-129">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="bc91e-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="bc91e-130">OUTPUTS</span></span>

### <span data-ttu-id="bc91e-131">Microsoft. Azure. Commands. Network. Models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="bc91e-131">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="bc91e-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="bc91e-132">NOTES</span></span>

## <span data-ttu-id="bc91e-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bc91e-133">RELATED LINKS</span></span>

[<span data-ttu-id="bc91e-134">Add-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="bc91e-134">Add-AzRouteConfig</span></span>](./Add-AzRouteConfig.md)

[<span data-ttu-id="bc91e-135">Get-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="bc91e-135">Get-AzRouteConfig</span></span>](./Get-AzRouteConfig.md)

[<span data-ttu-id="bc91e-136">New-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="bc91e-136">New-AzRouteConfig</span></span>](./New-AzRouteConfig.md)

[<span data-ttu-id="bc91e-137">Set-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="bc91e-137">Set-AzRouteConfig</span></span>](./Set-AzRouteConfig.md)


