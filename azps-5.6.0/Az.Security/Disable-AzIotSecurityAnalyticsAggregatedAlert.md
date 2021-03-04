---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Disable-AzIotSecurityAnalyticsAggregatedAlert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Disable-AzIotSecurityAnalyticsAggregatedAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Disable-AzIotSecurityAnalyticsAggregatedAlert.md
ms.openlocfilehash: c698c91f8b4115fb811ebcda41eaf43662f0bf08
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889754"
---
# <span data-ttu-id="52cc3-101">Disable-AzIotSecurityAnalyticsAggregatedAlert</span><span class="sxs-lookup"><span data-stu-id="52cc3-101">Disable-AzIotSecurityAnalyticsAggregatedAlert</span></span>

## <span data-ttu-id="52cc3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="52cc3-102">SYNOPSIS</span></span>
<span data-ttu-id="52cc3-103">Descartar alerta agregado de Iot</span><span class="sxs-lookup"><span data-stu-id="52cc3-103">Dismiss Iot aggregated alert</span></span>

## <span data-ttu-id="52cc3-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="52cc3-104">SYNTAX</span></span>

### <span data-ttu-id="52cc3-105">SolutionLevelResource (Padrão)</span><span class="sxs-lookup"><span data-stu-id="52cc3-105">SolutionLevelResource (Default)</span></span>
```
Disable-AzIotSecurityAnalyticsAggregatedAlert -ResourceGroupName <String> -SolutionName <String> -Name <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="52cc3-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="52cc3-106">InputObject</span></span>
```
Disable-AzIotSecurityAnalyticsAggregatedAlert -InputObject <PSIoTSecurityAggregatedAlert> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="52cc3-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="52cc3-107">ResourceId</span></span>
```
Disable-AzIotSecurityAnalyticsAggregatedAlert -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="52cc3-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="52cc3-108">DESCRIPTION</span></span>
<span data-ttu-id="52cc3-109">O Disable-AzIotSecurityAnalyticsAggregatedAlert cmdlet descarta um alerta aggragateado específico em dispositivos de hub iot.</span><span class="sxs-lookup"><span data-stu-id="52cc3-109">The Disable-AzIotSecurityAnalyticsAggregatedAlert cmdlet dismisses a specific aggragated alert on devices of iot hub.</span></span> <span data-ttu-id="52cc3-110">O nome dos alertas agregados é uma combinação do tipo de alerta e a data agravada do alerta, separada por '/'.</span><span class="sxs-lookup"><span data-stu-id="52cc3-110">The name of the aggregated alerts is a combination of the alert type and the alert aggragted date, separated by '/'.</span></span>

## <span data-ttu-id="52cc3-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="52cc3-111">EXAMPLES</span></span>

### <span data-ttu-id="52cc3-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="52cc3-112">Example 1</span></span>
```powershell
PS C:\> Disable-AzIotSecurityAnalyticsAggregatedAlert -ResourceGroupName "MyResourceGroup" -SolutionName "MySolutionName" -Name "IoT_SucessfulLocalLogin/2020-03-15"
```

<span data-ttu-id="52cc3-113">Descartar alerta agregado "IoT_SucessfulLocalLogin/2020-03-15" (nome combinado do tipo de alerta e sua data agregada) da solução de segurança de IoT "MySolutionName" no grupo de recursos "MyResourceGroup"</span><span class="sxs-lookup"><span data-stu-id="52cc3-113">Dismiss aggregated alert "IoT_SucessfulLocalLogin/2020-03-15" (name combined from alert type and its aggregated date) from the IoT security solution "MySolutionName" in resource group "MyResourceGroup"</span></span>

### <span data-ttu-id="52cc3-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="52cc3-114">Example 2</span></span>
```powershell
PS C:\> Disable-AzIotSecurityAnalyticsAggregatedAlert -ResourceId "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Security/iotSecuritySolutions/MySolutionName/analyticsModels/default/aggregatedAlerts/IoT_SucessfulLocalLogin/2020-03-15"
```

<span data-ttu-id="52cc3-115">Descartar alerta agregado com id de recurso "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Security/iotSecuritySolutions/MySolutionName/analyticsModels/default/aggregatedAlerts/IoT_SucessfulLocalLogin/2020-03-15"</span><span class="sxs-lookup"><span data-stu-id="52cc3-115">Dismiss aggregated alert with resource Id "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Security/iotSecuritySolutions/MySolutionName/analyticsModels/default/aggregatedAlerts/IoT_SucessfulLocalLogin/2020-03-15"</span></span>

## <span data-ttu-id="52cc3-116">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="52cc3-116">PARAMETERS</span></span>

### <span data-ttu-id="52cc3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52cc3-117">-DefaultProfile</span></span>
<span data-ttu-id="52cc3-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="52cc3-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="52cc3-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="52cc3-119">-InputObject</span></span>
<span data-ttu-id="52cc3-120">Objeto Input.</span><span class="sxs-lookup"><span data-stu-id="52cc3-120">Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.IotSecuritySolutionAnalytics.PSIoTSecurityAggregatedAlert
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="52cc3-121">-Name</span><span class="sxs-lookup"><span data-stu-id="52cc3-121">-Name</span></span>
<span data-ttu-id="52cc3-122">Nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="52cc3-122">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SolutionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52cc3-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="52cc3-123">-PassThru</span></span>
<span data-ttu-id="52cc3-124">Retorne se a operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="52cc3-124">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="52cc3-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52cc3-125">-ResourceGroupName</span></span>
<span data-ttu-id="52cc3-126">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="52cc3-126">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: SolutionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52cc3-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="52cc3-127">-ResourceId</span></span>
<span data-ttu-id="52cc3-128">ID do recurso de segurança em que você deseja invocar o comando.</span><span class="sxs-lookup"><span data-stu-id="52cc3-128">ID of the security resource that you want to invoke the command on.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52cc3-129">-SolutionName</span><span class="sxs-lookup"><span data-stu-id="52cc3-129">-SolutionName</span></span>
<span data-ttu-id="52cc3-130">Nome da solução</span><span class="sxs-lookup"><span data-stu-id="52cc3-130">Solution name</span></span>

```yaml
Type: System.String
Parameter Sets: SolutionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52cc3-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="52cc3-131">-Confirm</span></span>
<span data-ttu-id="52cc3-132">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="52cc3-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="52cc3-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="52cc3-133">-WhatIf</span></span>
<span data-ttu-id="52cc3-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="52cc3-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="52cc3-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="52cc3-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="52cc3-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52cc3-136">CommonParameters</span></span>
<span data-ttu-id="52cc3-137">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52cc3-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52cc3-138">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="52cc3-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52cc3-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="52cc3-139">INPUTS</span></span>

### <span data-ttu-id="52cc3-140">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutionAnalytics.PSIoTSecurityAggregatedAlert</span><span class="sxs-lookup"><span data-stu-id="52cc3-140">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutionAnalytics.PSIoTSecurityAggregatedAlert</span></span>

### <span data-ttu-id="52cc3-141">System.String</span><span class="sxs-lookup"><span data-stu-id="52cc3-141">System.String</span></span>

## <span data-ttu-id="52cc3-142">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="52cc3-142">OUTPUTS</span></span>

### <span data-ttu-id="52cc3-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="52cc3-143">System.Boolean</span></span>

## <span data-ttu-id="52cc3-144">NOTES</span><span class="sxs-lookup"><span data-stu-id="52cc3-144">NOTES</span></span>

## <span data-ttu-id="52cc3-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="52cc3-145">RELATED LINKS</span></span>
