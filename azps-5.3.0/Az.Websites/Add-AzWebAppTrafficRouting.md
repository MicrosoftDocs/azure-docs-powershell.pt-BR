---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Add-AzWebAppTrafficRouting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Add-AzWebAppTrafficRouting.md
ms.openlocfilehash: 8a3949397b12b54062c5cc68f367187f691fb02d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98271980"
---
# <span data-ttu-id="1071e-101">Add-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="1071e-101">Add-AzWebAppTrafficRouting</span></span>

## <span data-ttu-id="1071e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1071e-102">SYNOPSIS</span></span>
<span data-ttu-id="1071e-103">Adicione uma regra de roteamento ao slot.</span><span class="sxs-lookup"><span data-stu-id="1071e-103">Add a routing Rule to the Slot.</span></span>

## <span data-ttu-id="1071e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1071e-104">SYNTAX</span></span>

```
Add-AzWebAppTrafficRouting -ResourceGroupName <String> -WebAppName <String> -RoutingRule <Hashtable>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1071e-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1071e-105">DESCRIPTION</span></span>
<span data-ttu-id="1071e-106">O cmdlet **Add-AzWebAppTrafficRouting** adiciona uma regra de roteamento a um slot do Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="1071e-106">The **Add-AzWebAppTrafficRouting** cmdlet adds a Routing rule to an Azure Web App Slot.</span></span>

## <span data-ttu-id="1071e-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1071e-107">EXAMPLES</span></span>

### <span data-ttu-id="1071e-108">Exemplo 1 adicionar uma regra de roteamento para transferir 15% do tráfego de produção para o slot STG</span><span class="sxs-lookup"><span data-stu-id="1071e-108">Example 1 Add a routing rule to transfer 15% of production traffice to  Stg slot</span></span>
```powershell
PS C:\>Add-AzWebAppTrafficRouting -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" 
-RoutingRule @{ActionHostName='XXXX.azurewebsites.net';ReroutePercentage=15;Name='Stg'}
```

<span data-ttu-id="1071e-109">Esse comando adiciona uma regra de roteamento para transferir 15% do tráfego de produção para o slot STG</span><span class="sxs-lookup"><span data-stu-id="1071e-109">This command adds a routing rule to transfer 15% of production traffice to  Stg slot</span></span>

### <span data-ttu-id="1071e-110">Exemplo 2 Adicione uma regra de roteamento para transferir o tráfego de produção para STG intervalos de slot de 50% a 90% na maneira mais incremental.</span><span class="sxs-lookup"><span data-stu-id="1071e-110">Example 2 Add a routing rule to transfer the production traffice to Stg slot ranges from 50% to 90% in incremental manner.</span></span>
```powershell
PS C:\>Add-AzWebAppTrafficRouting -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" 
-RoutingRule @{ActionHostName='XXXX.azurewebsites.net';ReroutePercentage=50;ChangeIntervalInMinutes=1;
MinReroutePercentage=50;MaxReroutePercentage=90;Name='Stg';ChangeStep=10}
```

<span data-ttu-id="1071e-111">Esse comando adiciona uma regra de roteamento para transferir o tráfego de produção para STG intervalos de slot de 50% a 90% na maneira mais incremental.</span><span class="sxs-lookup"><span data-stu-id="1071e-111">This command adds a routing rule to transfer the production traffice to Stg slot ranges from 50% to 90% in incremental manner.</span></span>

## <span data-ttu-id="1071e-112">OS</span><span class="sxs-lookup"><span data-stu-id="1071e-112">PARAMETERS</span></span>

### <span data-ttu-id="1071e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1071e-113">-DefaultProfile</span></span>
<span data-ttu-id="1071e-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1071e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1071e-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1071e-115">-ResourceGroupName</span></span>
<span data-ttu-id="1071e-116">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="1071e-116">Resource Group Name</span></span>

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

### <span data-ttu-id="1071e-117">-RoutingRule</span><span class="sxs-lookup"><span data-stu-id="1071e-117">-RoutingRule</span></span>
<span data-ttu-id="1071e-118">Web App RoutingRule.</span><span class="sxs-lookup"><span data-stu-id="1071e-118">Web App RoutingRule.</span></span>
<span data-ttu-id="1071e-119">Exemplo:-RoutingRule @ {ActionHostName = $slot. DefaultHostName; ReroutePercentage = $ReroutePercentage; Name = $slotName}</span><span class="sxs-lookup"><span data-stu-id="1071e-119">Example: -RoutingRule @{ActionHostName=$slot.DefaultHostName ; ReroutePercentage=$ReroutePercentage ; Name=$slotName}</span></span>

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

### <span data-ttu-id="1071e-120">-WebAppname</span><span class="sxs-lookup"><span data-stu-id="1071e-120">-WebAppName</span></span>
<span data-ttu-id="1071e-121">Nome do WebApp</span><span class="sxs-lookup"><span data-stu-id="1071e-121">WebApp Name</span></span>

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

### <span data-ttu-id="1071e-122">-Confirme</span><span class="sxs-lookup"><span data-stu-id="1071e-122">-Confirm</span></span>
<span data-ttu-id="1071e-123">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1071e-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1071e-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1071e-124">-WhatIf</span></span>
<span data-ttu-id="1071e-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="1071e-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1071e-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1071e-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1071e-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1071e-127">CommonParameters</span></span>
<span data-ttu-id="1071e-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1071e-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1071e-129">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1071e-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1071e-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1071e-130">INPUTS</span></span>

### <span data-ttu-id="1071e-131">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="1071e-131">None</span></span>

## <span data-ttu-id="1071e-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1071e-132">OUTPUTS</span></span>

### <span data-ttu-id="1071e-133">Microsoft. Azure. Management. WebSites. Models. RampUpRule</span><span class="sxs-lookup"><span data-stu-id="1071e-133">Microsoft.Azure.Management.WebSites.Models.RampUpRule</span></span>

## <span data-ttu-id="1071e-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1071e-134">NOTES</span></span>

## <span data-ttu-id="1071e-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1071e-135">RELATED LINKS</span></span>
[<span data-ttu-id="1071e-136">Update-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="1071e-136">Update-AzWebAppTrafficRouting</span></span>](./Update-AzWebAppTrafficRouting.md)

[<span data-ttu-id="1071e-137">Get-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="1071e-137">Get-AzWebAppTrafficRouting</span></span>](./Get-AzWebAppTrafficRouting.md)

[<span data-ttu-id="1071e-138">Remove-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="1071e-138">Remove-AzWebAppTrafficRouting</span></span>](./Remove-AzWebAppTrafficRouting.md)
