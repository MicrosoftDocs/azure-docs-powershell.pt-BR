---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 03285628-6BD3-4F2F-8129-E3CAE4C70EC8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azrouteconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteConfig.md
ms.openlocfilehash: 57ef72599cdb0500a9903aeb09f67437fe5cc2f6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111586"
---
# <span data-ttu-id="eea89-101">Remove-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="eea89-101">Remove-AzRouteConfig</span></span>

## <span data-ttu-id="eea89-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="eea89-102">SYNOPSIS</span></span>
<span data-ttu-id="eea89-103">Remove uma rota de uma tabela de rota.</span><span class="sxs-lookup"><span data-stu-id="eea89-103">Removes a route from a route table.</span></span>

## <span data-ttu-id="eea89-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="eea89-104">SYNTAX</span></span>

```
Remove-AzRouteConfig -RouteTable <PSRouteTable> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eea89-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="eea89-105">DESCRIPTION</span></span>
<span data-ttu-id="eea89-106">O cmdlet **Remove-AzRouteConfig** remove uma rota de uma tabela de rota do Azure.</span><span class="sxs-lookup"><span data-stu-id="eea89-106">The **Remove-AzRouteConfig** cmdlet removes a route from an Azure route table.</span></span>

## <span data-ttu-id="eea89-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="eea89-107">EXAMPLES</span></span>

### <span data-ttu-id="eea89-108">Exemplo 1: Remover uma rota</span><span class="sxs-lookup"><span data-stu-id="eea89-108">Example 1: Remove a route</span></span>
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

<span data-ttu-id="eea89-109">Esse comando obtém a tabela de rota chamada Roteável01 usando o cmdlet **Get-AzRouteTable.**</span><span class="sxs-lookup"><span data-stu-id="eea89-109">This command gets the route table named RouteTable01 by using the **Get-AzRouteTable** cmdlet.</span></span>
<span data-ttu-id="eea89-110">O comando passa essa tabela para o cmdlet atual usando o operador de pipeline.</span><span class="sxs-lookup"><span data-stu-id="eea89-110">The command passes that table to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="eea89-111">O cmdlet atual remove a rota chamada Rota02 e o passa o resultado para o cmdlet **Set-AzRouteTable,** que atualiza a tabela para refletir suas alterações.</span><span class="sxs-lookup"><span data-stu-id="eea89-111">The current cmdlet remove the route named Route02, and the passes the result to the **Set-AzRouteTable** cmdlet, which updates the table to reflect your changes.</span></span>
<span data-ttu-id="eea89-112">A tabela não contém mais a rota chamada Rota02.</span><span class="sxs-lookup"><span data-stu-id="eea89-112">The table no longer contains the route named Route02.</span></span>

## <span data-ttu-id="eea89-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="eea89-113">PARAMETERS</span></span>

### <span data-ttu-id="eea89-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eea89-114">-DefaultProfile</span></span>
<span data-ttu-id="eea89-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="eea89-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eea89-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="eea89-116">-Name</span></span>
<span data-ttu-id="eea89-117">Especifica o nome da rota que este cmdlet remove.</span><span class="sxs-lookup"><span data-stu-id="eea89-117">Specifies the name of the route that this cmdlet removes.</span></span>

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

### <span data-ttu-id="eea89-118">-Tabela de Rota</span><span class="sxs-lookup"><span data-stu-id="eea89-118">-RouteTable</span></span>
<span data-ttu-id="eea89-119">Especifica a tabela de rota que contém a rota que este cmdlet exclui.</span><span class="sxs-lookup"><span data-stu-id="eea89-119">Specifies the route table that contains the route that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="eea89-120">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="eea89-120">-Confirm</span></span>
<span data-ttu-id="eea89-121">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eea89-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eea89-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eea89-122">-WhatIf</span></span>
<span data-ttu-id="eea89-123">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="eea89-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="eea89-124">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="eea89-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eea89-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eea89-125">CommonParameters</span></span>
<span data-ttu-id="eea89-126">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eea89-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eea89-127">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eea89-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eea89-128">Entradas</span><span class="sxs-lookup"><span data-stu-id="eea89-128">INPUTS</span></span>

### <span data-ttu-id="eea89-129">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="eea89-129">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="eea89-130">Saídas</span><span class="sxs-lookup"><span data-stu-id="eea89-130">OUTPUTS</span></span>

### <span data-ttu-id="eea89-131">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="eea89-131">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="eea89-132">Notas</span><span class="sxs-lookup"><span data-stu-id="eea89-132">NOTES</span></span>

## <span data-ttu-id="eea89-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="eea89-133">RELATED LINKS</span></span>

[<span data-ttu-id="eea89-134">Add-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="eea89-134">Add-AzRouteConfig</span></span>](./Add-AzRouteConfig.md)

[<span data-ttu-id="eea89-135">Get-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="eea89-135">Get-AzRouteConfig</span></span>](./Get-AzRouteConfig.md)

[<span data-ttu-id="eea89-136">New-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="eea89-136">New-AzRouteConfig</span></span>](./New-AzRouteConfig.md)

[<span data-ttu-id="eea89-137">Set-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="eea89-137">Set-AzRouteConfig</span></span>](./Set-AzRouteConfig.md)


