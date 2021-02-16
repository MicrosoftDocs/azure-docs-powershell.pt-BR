---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Update-AzWebAppTrafficRouting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Update-AzWebAppTrafficRouting.md
ms.openlocfilehash: 7fba74a3778df0c8c26ed4b581e5d2777ff75029
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118490"
---
# <span data-ttu-id="d7aa8-101">Update-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="d7aa8-101">Update-AzWebAppTrafficRouting</span></span>

## <span data-ttu-id="d7aa8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d7aa8-102">SYNOPSIS</span></span>
<span data-ttu-id="d7aa8-103">Atualizar uma Regra de Roteamento para o Slot.</span><span class="sxs-lookup"><span data-stu-id="d7aa8-103">Update a routing Rule to the Slot.</span></span>

## <span data-ttu-id="d7aa8-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d7aa8-104">SYNTAX</span></span>

```
Update-AzWebAppTrafficRouting -ResourceGroupName <String> -WebAppName <String> -RoutingRule <Hashtable>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d7aa8-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="d7aa8-105">DESCRIPTION</span></span>
<span data-ttu-id="d7aa8-106">O cmdlet **Update-AzWebAppTrafficRouting** atualiza a configuração da regra de roteamento para um Slot do Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="d7aa8-106">The **Update-AzWebAppTrafficRouting** cmdlet updates the routing rule configuration for an Azure Web App Slot.</span></span>

## <span data-ttu-id="d7aa8-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="d7aa8-107">EXAMPLES</span></span>

### <span data-ttu-id="d7aa8-108">Exemplo 1 Atualizar uma regra de roteamento para transferir 15% do tráfego de produção para o slot Stg</span><span class="sxs-lookup"><span data-stu-id="d7aa8-108">Example 1 Update a routing rule to transfer 15% of production traffice to  Stg slot</span></span>
```powershell
PS C:\>Update-AzWebAppTrafficRouting -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" 
- RoutingRule @{AtionHostName='XXXX.azurewebsites.net';ReroutePercentage=15;Name='Stg'}
```

<span data-ttu-id="d7aa8-109">Este comando atualiza uma regra de roteamento para transferir 15% do tráfego de produção para o slot Stg.</span><span class="sxs-lookup"><span data-stu-id="d7aa8-109">This command updates a routing rule to transfer 15% of production traffic to Stg slot.</span></span>

### <span data-ttu-id="d7aa8-110">Exemplo 2 Atualizar uma regra de roteamento para transferir o tráfego de produção para intervalos stg de 50% a 90% de maneira incremental.</span><span class="sxs-lookup"><span data-stu-id="d7aa8-110">Example 2 Update a routing rule to transfer the production traffice to Stg slot ranges from 50% to 90% in incremental manner.</span></span>
```powershell
PS C:\>Update-AzWebAppTrafficRouting -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" 
-RoutingRule @{ActionHostName='XXXX.azurewebsites.net';ReroutePercentage=50;ChangeIntervalInMinutes=1;
MinReroutePercentage=50;MaxReroutePercentage=90;Name='Stg';ChangeStep=10}
```

<span data-ttu-id="d7aa8-111">Este comando atualiza uma regra de roteamento para transferir o tráfego de produção para intervalos stg de 50% a 90% de maneira incremental.</span><span class="sxs-lookup"><span data-stu-id="d7aa8-111">This command Updates a routing rule to transfer the production traffice to Stg slot ranges from 50% to 90% in incremental manner.</span></span>

## <span data-ttu-id="d7aa8-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d7aa8-112">PARAMETERS</span></span>

### <span data-ttu-id="d7aa8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7aa8-113">-DefaultProfile</span></span>
<span data-ttu-id="d7aa8-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d7aa8-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d7aa8-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7aa8-115">-ResourceGroupName</span></span>
<span data-ttu-id="d7aa8-116">ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7aa8-116">ResourceGroupName</span></span>
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

### <span data-ttu-id="d7aa8-117">-RoutingRule</span><span class="sxs-lookup"><span data-stu-id="d7aa8-117">-RoutingRule</span></span>
<span data-ttu-id="d7aa8-118">Roteamento de Aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="d7aa8-118">Web App RoutingRule.</span></span>
<span data-ttu-id="d7aa8-119">Exemplo: -RoutingRule @{ActionHostName=$slot. DefaultHostName; RedirecionarPercentage=$ReroutePercentage; Name=$slotName}</span><span class="sxs-lookup"><span data-stu-id="d7aa8-119">Example: -RoutingRule @{ActionHostName=$slot.DefaultHostName ; ReroutePercentage=$ReroutePercentage ; Name=$slotName}</span></span>

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

### <span data-ttu-id="d7aa8-120">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="d7aa8-120">-WebAppName</span></span>
<span data-ttu-id="d7aa8-121">Nome webapp</span><span class="sxs-lookup"><span data-stu-id="d7aa8-121">WebApp Name</span></span>

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

### <span data-ttu-id="d7aa8-122">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="d7aa8-122">-Confirm</span></span>
<span data-ttu-id="d7aa8-123">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d7aa8-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d7aa8-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d7aa8-124">-WhatIf</span></span>
<span data-ttu-id="d7aa8-125">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="d7aa8-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d7aa8-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d7aa8-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d7aa8-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7aa8-127">CommonParameters</span></span>
<span data-ttu-id="d7aa8-128">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7aa8-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7aa8-129">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d7aa8-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7aa8-130">Entradas</span><span class="sxs-lookup"><span data-stu-id="d7aa8-130">INPUTS</span></span>

### <span data-ttu-id="d7aa8-131">Nenhum</span><span class="sxs-lookup"><span data-stu-id="d7aa8-131">None</span></span>

## <span data-ttu-id="d7aa8-132">Saídas</span><span class="sxs-lookup"><span data-stu-id="d7aa8-132">OUTPUTS</span></span>

### <span data-ttu-id="d7aa8-133">Microsoft.Azure.Management.WebSites.Models.RampUpRule</span><span class="sxs-lookup"><span data-stu-id="d7aa8-133">Microsoft.Azure.Management.WebSites.Models.RampUpRule</span></span>

## <span data-ttu-id="d7aa8-134">Notas</span><span class="sxs-lookup"><span data-stu-id="d7aa8-134">NOTES</span></span>

## <span data-ttu-id="d7aa8-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d7aa8-135">RELATED LINKS</span></span>

[<span data-ttu-id="d7aa8-136">Add-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="d7aa8-136">Add-AzWebAppTrafficRouting</span></span>](./Add-AzWebAppTrafficRouting.md)

[<span data-ttu-id="d7aa8-137">Get-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="d7aa8-137">Get-AzWebAppTrafficRouting</span></span>](./Get-AzWebAppTrafficRouting.md)

[<span data-ttu-id="d7aa8-138">Remove-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="d7aa8-138">Remove-AzWebAppTrafficRouting</span></span>](./Remove-AzWebAppTrafficRouting.md)