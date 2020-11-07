---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Update-AzWebAppTrafficRouting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Update-AzWebAppTrafficRouting.md
ms.openlocfilehash: 7fba74a3778df0c8c26ed4b581e5d2777ff75029
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93942588"
---
# <span data-ttu-id="76455-101">Update-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="76455-101">Update-AzWebAppTrafficRouting</span></span>

## <span data-ttu-id="76455-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="76455-102">SYNOPSIS</span></span>
<span data-ttu-id="76455-103">Atualize uma regra de roteamento para o slot.</span><span class="sxs-lookup"><span data-stu-id="76455-103">Update a routing Rule to the Slot.</span></span>

## <span data-ttu-id="76455-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="76455-104">SYNTAX</span></span>

```
Update-AzWebAppTrafficRouting -ResourceGroupName <String> -WebAppName <String> -RoutingRule <Hashtable>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="76455-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="76455-105">DESCRIPTION</span></span>
<span data-ttu-id="76455-106">O cmdlet **Update-AzWebAppTrafficRouting** atualiza a configuração da regra de roteamento para um slot do aplicativo Web do Azure.</span><span class="sxs-lookup"><span data-stu-id="76455-106">The **Update-AzWebAppTrafficRouting** cmdlet updates the routing rule configuration for an Azure Web App Slot.</span></span>

## <span data-ttu-id="76455-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="76455-107">EXAMPLES</span></span>

### <span data-ttu-id="76455-108">Exemplo 1 atualizar uma regra de roteamento para transferir 15% do tráfego de produção para o slot STG</span><span class="sxs-lookup"><span data-stu-id="76455-108">Example 1 Update a routing rule to transfer 15% of production traffice to  Stg slot</span></span>
```powershell
PS C:\>Update-AzWebAppTrafficRouting -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" 
- RoutingRule @{AtionHostName='XXXX.azurewebsites.net';ReroutePercentage=15;Name='Stg'}
```

<span data-ttu-id="76455-109">Esse comando atualiza uma regra de roteamento para transferir 15% do tráfego de produção para o slot STG.</span><span class="sxs-lookup"><span data-stu-id="76455-109">This command updates a routing rule to transfer 15% of production traffic to Stg slot.</span></span>

### <span data-ttu-id="76455-110">Exemplo 2 Atualize uma regra de roteamento para transferir o tráfego de produção para STG intervalos de slot de 50% a 90% na maneira mais incremental.</span><span class="sxs-lookup"><span data-stu-id="76455-110">Example 2 Update a routing rule to transfer the production traffice to Stg slot ranges from 50% to 90% in incremental manner.</span></span>
```powershell
PS C:\>Update-AzWebAppTrafficRouting -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" 
-RoutingRule @{ActionHostName='XXXX.azurewebsites.net';ReroutePercentage=50;ChangeIntervalInMinutes=1;
MinReroutePercentage=50;MaxReroutePercentage=90;Name='Stg';ChangeStep=10}
```

<span data-ttu-id="76455-111">Esse comando atualiza uma regra de roteamento para transferir o tráfego de produção para STG intervalos de slot de 50% a 90% na maneira mais incremental.</span><span class="sxs-lookup"><span data-stu-id="76455-111">This command Updates a routing rule to transfer the production traffice to Stg slot ranges from 50% to 90% in incremental manner.</span></span>

## <span data-ttu-id="76455-112">OS</span><span class="sxs-lookup"><span data-stu-id="76455-112">PARAMETERS</span></span>

### <span data-ttu-id="76455-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76455-113">-DefaultProfile</span></span>
<span data-ttu-id="76455-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="76455-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="76455-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76455-115">-ResourceGroupName</span></span>
<span data-ttu-id="76455-116">ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76455-116">ResourceGroupName</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76455-117">-RoutingRule</span><span class="sxs-lookup"><span data-stu-id="76455-117">-RoutingRule</span></span>
<span data-ttu-id="76455-118">Web App RoutingRule.</span><span class="sxs-lookup"><span data-stu-id="76455-118">Web App RoutingRule.</span></span>
<span data-ttu-id="76455-119">Exemplo:-RoutingRule @ {ActionHostName = $slot. DefaultHostName; ReroutePercentage = $ReroutePercentage; Name = $slotName}</span><span class="sxs-lookup"><span data-stu-id="76455-119">Example: -RoutingRule @{ActionHostName=$slot.DefaultHostName ; ReroutePercentage=$ReroutePercentage ; Name=$slotName}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76455-120">-WebAppname</span><span class="sxs-lookup"><span data-stu-id="76455-120">-WebAppName</span></span>
<span data-ttu-id="76455-121">Nome do WebApp</span><span class="sxs-lookup"><span data-stu-id="76455-121">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76455-122">-Confirme</span><span class="sxs-lookup"><span data-stu-id="76455-122">-Confirm</span></span>
<span data-ttu-id="76455-123">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="76455-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="76455-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="76455-124">-WhatIf</span></span>
<span data-ttu-id="76455-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="76455-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="76455-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="76455-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="76455-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76455-127">CommonParameters</span></span>
<span data-ttu-id="76455-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76455-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76455-129">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="76455-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76455-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="76455-130">INPUTS</span></span>

### <span data-ttu-id="76455-131">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="76455-131">None</span></span>

## <span data-ttu-id="76455-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="76455-132">OUTPUTS</span></span>

### <span data-ttu-id="76455-133">Microsoft. Azure. Management. WebSites. Models. RampUpRule</span><span class="sxs-lookup"><span data-stu-id="76455-133">Microsoft.Azure.Management.WebSites.Models.RampUpRule</span></span>

## <span data-ttu-id="76455-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="76455-134">NOTES</span></span>

## <span data-ttu-id="76455-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="76455-135">RELATED LINKS</span></span>

[<span data-ttu-id="76455-136">Add-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="76455-136">Add-AzWebAppTrafficRouting</span></span>](./Add-AzWebAppTrafficRouting.md)

[<span data-ttu-id="76455-137">Get-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="76455-137">Get-AzWebAppTrafficRouting</span></span>](./Get-AzWebAppTrafficRouting.md)

[<span data-ttu-id="76455-138">Remove-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="76455-138">Remove-AzWebAppTrafficRouting</span></span>](./Remove-AzWebAppTrafficRouting.md)