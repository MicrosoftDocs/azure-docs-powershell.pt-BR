---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Add-AzWebAppTrafficRouting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Add-AzWebAppTrafficRouting.md
ms.openlocfilehash: 8a3949397b12b54062c5cc68f367187f691fb02d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112346"
---
# <span data-ttu-id="87d9a-101">Add-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="87d9a-101">Add-AzWebAppTrafficRouting</span></span>

## <span data-ttu-id="87d9a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="87d9a-102">SYNOPSIS</span></span>
<span data-ttu-id="87d9a-103">Adicione uma Regra de Roteamento ao Slot.</span><span class="sxs-lookup"><span data-stu-id="87d9a-103">Add a routing Rule to the Slot.</span></span>

## <span data-ttu-id="87d9a-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="87d9a-104">SYNTAX</span></span>

```
Add-AzWebAppTrafficRouting -ResourceGroupName <String> -WebAppName <String> -RoutingRule <Hashtable>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="87d9a-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="87d9a-105">DESCRIPTION</span></span>
<span data-ttu-id="87d9a-106">O cmdlet **Add-AzWebAppTrafficRouting** adiciona uma regra de Roteamento a um Slot do Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="87d9a-106">The **Add-AzWebAppTrafficRouting** cmdlet adds a Routing rule to an Azure Web App Slot.</span></span>

## <span data-ttu-id="87d9a-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="87d9a-107">EXAMPLES</span></span>

### <span data-ttu-id="87d9a-108">Exemplo 1 Adicionar uma regra de roteamento para transferir 15% do tráfego de produção para o slot Stg</span><span class="sxs-lookup"><span data-stu-id="87d9a-108">Example 1 Add a routing rule to transfer 15% of production traffice to  Stg slot</span></span>
```powershell
PS C:\>Add-AzWebAppTrafficRouting -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" 
-RoutingRule @{ActionHostName='XXXX.azurewebsites.net';ReroutePercentage=15;Name='Stg'}
```

<span data-ttu-id="87d9a-109">Este comando adiciona uma regra de roteamento para transferir 15% do tráfego de produção para o slot Stg</span><span class="sxs-lookup"><span data-stu-id="87d9a-109">This command adds a routing rule to transfer 15% of production traffice to  Stg slot</span></span>

### <span data-ttu-id="87d9a-110">Exemplo 2 Adicionar uma regra de roteamento para transferir o tráfego de produção para intervalos stg de 50% a 90% de maneira incremental.</span><span class="sxs-lookup"><span data-stu-id="87d9a-110">Example 2 Add a routing rule to transfer the production traffice to Stg slot ranges from 50% to 90% in incremental manner.</span></span>
```powershell
PS C:\>Add-AzWebAppTrafficRouting -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" 
-RoutingRule @{ActionHostName='XXXX.azurewebsites.net';ReroutePercentage=50;ChangeIntervalInMinutes=1;
MinReroutePercentage=50;MaxReroutePercentage=90;Name='Stg';ChangeStep=10}
```

<span data-ttu-id="87d9a-111">Esse comando adiciona uma regra de roteamento para transferir o tráfego de produção para intervalos stg de 50% a 90% de maneira incremental.</span><span class="sxs-lookup"><span data-stu-id="87d9a-111">This command adds a routing rule to transfer the production traffice to Stg slot ranges from 50% to 90% in incremental manner.</span></span>

## <span data-ttu-id="87d9a-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="87d9a-112">PARAMETERS</span></span>

### <span data-ttu-id="87d9a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87d9a-113">-DefaultProfile</span></span>
<span data-ttu-id="87d9a-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="87d9a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="87d9a-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="87d9a-115">-ResourceGroupName</span></span>
<span data-ttu-id="87d9a-116">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="87d9a-116">Resource Group Name</span></span>

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

### <span data-ttu-id="87d9a-117">-RoutingRule</span><span class="sxs-lookup"><span data-stu-id="87d9a-117">-RoutingRule</span></span>
<span data-ttu-id="87d9a-118">Roteamento de Aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="87d9a-118">Web App RoutingRule.</span></span>
<span data-ttu-id="87d9a-119">Exemplo: -RoutingRule @{ActionHostName=$slot. DefaultHostName; RedirecionarPercentage=$ReroutePercentage; Name=$slotName}</span><span class="sxs-lookup"><span data-stu-id="87d9a-119">Example: -RoutingRule @{ActionHostName=$slot.DefaultHostName ; ReroutePercentage=$ReroutePercentage ; Name=$slotName}</span></span>

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

### <span data-ttu-id="87d9a-120">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="87d9a-120">-WebAppName</span></span>
<span data-ttu-id="87d9a-121">Nome webapp</span><span class="sxs-lookup"><span data-stu-id="87d9a-121">WebApp Name</span></span>

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

### <span data-ttu-id="87d9a-122">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="87d9a-122">-Confirm</span></span>
<span data-ttu-id="87d9a-123">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="87d9a-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="87d9a-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="87d9a-124">-WhatIf</span></span>
<span data-ttu-id="87d9a-125">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="87d9a-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="87d9a-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="87d9a-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="87d9a-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87d9a-127">CommonParameters</span></span>
<span data-ttu-id="87d9a-128">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87d9a-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87d9a-129">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="87d9a-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87d9a-130">Entradas</span><span class="sxs-lookup"><span data-stu-id="87d9a-130">INPUTS</span></span>

### <span data-ttu-id="87d9a-131">Nenhum</span><span class="sxs-lookup"><span data-stu-id="87d9a-131">None</span></span>

## <span data-ttu-id="87d9a-132">Saídas</span><span class="sxs-lookup"><span data-stu-id="87d9a-132">OUTPUTS</span></span>

### <span data-ttu-id="87d9a-133">Microsoft.Azure.Management.WebSites.Models.RampUpRule</span><span class="sxs-lookup"><span data-stu-id="87d9a-133">Microsoft.Azure.Management.WebSites.Models.RampUpRule</span></span>

## <span data-ttu-id="87d9a-134">Notas</span><span class="sxs-lookup"><span data-stu-id="87d9a-134">NOTES</span></span>

## <span data-ttu-id="87d9a-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="87d9a-135">RELATED LINKS</span></span>
[<span data-ttu-id="87d9a-136">Update-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="87d9a-136">Update-AzWebAppTrafficRouting</span></span>](./Update-AzWebAppTrafficRouting.md)

[<span data-ttu-id="87d9a-137">Get-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="87d9a-137">Get-AzWebAppTrafficRouting</span></span>](./Get-AzWebAppTrafficRouting.md)

[<span data-ttu-id="87d9a-138">Remove-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="87d9a-138">Remove-AzWebAppTrafficRouting</span></span>](./Remove-AzWebAppTrafficRouting.md)
