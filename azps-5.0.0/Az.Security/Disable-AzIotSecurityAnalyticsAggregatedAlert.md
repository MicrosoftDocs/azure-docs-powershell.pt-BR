---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Disable-AzIotSecurityAnalyticsAggregatedAlert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Disable-AzIotSecurityAnalyticsAggregatedAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Disable-AzIotSecurityAnalyticsAggregatedAlert.md
ms.openlocfilehash: 3747109d13fd4224b0f86bc5ecf2992ed4229487
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94118177"
---
# <span data-ttu-id="bed6e-101">Disable-AzIotSecurityAnalyticsAggregatedAlert</span><span class="sxs-lookup"><span data-stu-id="bed6e-101">Disable-AzIotSecurityAnalyticsAggregatedAlert</span></span>

## <span data-ttu-id="bed6e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bed6e-102">SYNOPSIS</span></span>
<span data-ttu-id="bed6e-103">Ignorar alerta de agregação de IOT</span><span class="sxs-lookup"><span data-stu-id="bed6e-103">Dismiss Iot aggregated alert</span></span>

## <span data-ttu-id="bed6e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bed6e-104">SYNTAX</span></span>

### <span data-ttu-id="bed6e-105">SolutionLevelResource (padrão)</span><span class="sxs-lookup"><span data-stu-id="bed6e-105">SolutionLevelResource (Default)</span></span>
```
Disable-AzIotSecurityAnalyticsAggregatedAlert -ResourceGroupName <String> -SolutionName <String> -Name <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bed6e-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="bed6e-106">InputObject</span></span>
```
Disable-AzIotSecurityAnalyticsAggregatedAlert -InputObject <PSIoTSecurityAggregatedAlert> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bed6e-107">Identificação</span><span class="sxs-lookup"><span data-stu-id="bed6e-107">ResourceId</span></span>
```
Disable-AzIotSecurityAnalyticsAggregatedAlert -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bed6e-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="bed6e-108">DESCRIPTION</span></span>
<span data-ttu-id="bed6e-109">O cmdlet Disable-AzIotSecurityAnalyticsAggregatedAlert ignora um alerta de aggragated específico em dispositivos de Hub IOT.</span><span class="sxs-lookup"><span data-stu-id="bed6e-109">The Disable-AzIotSecurityAnalyticsAggregatedAlert cmdlet dismisses a specific aggragated alert on devices of iot hub.</span></span> <span data-ttu-id="bed6e-110">O nome dos alertas agregados é uma combinação do tipo de alerta e a data de aggragted do alerta, separados por '/'.</span><span class="sxs-lookup"><span data-stu-id="bed6e-110">The name of the aggregated alerts is a combination of the alert type and the alert aggragted date, separated by '/'.</span></span>

## <span data-ttu-id="bed6e-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bed6e-111">EXAMPLES</span></span>

### <span data-ttu-id="bed6e-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="bed6e-112">Example 1</span></span>
```powershell
PS C:\> Disable-AzIotSecurityAnalyticsAggregatedAlert -ResourceGroupName "MyResourceGroup" -SolutionName "MySolutionName" -Name "IoT_SucessfulLocalLogin/2020-03-15"
```

<span data-ttu-id="bed6e-113">Ignorar alerta agregado "IoT_SucessfulLocalLogin/2020-03-15" (nome combinado do tipo de alerta e data da agregação) da solução de segurança IoT "MySolutionName" no grupo de recursos "MyResource Group"</span><span class="sxs-lookup"><span data-stu-id="bed6e-113">Dismiss aggregated alert "IoT_SucessfulLocalLogin/2020-03-15" (name combined from alert type and its aggregated date) from the IoT security solution "MySolutionName" in resource group "MyResourceGroup"</span></span>

### <span data-ttu-id="bed6e-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="bed6e-114">Example 2</span></span>
```powershell
PS C:\> Disable-AzIotSecurityAnalyticsAggregatedAlert -ResourceId "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Security/iotSecuritySolutions/MySolutionName/analyticsModels/default/aggregatedAlerts/IoT_SucessfulLocalLogin/2020-03-15"
```

<span data-ttu-id="bed6e-115">Ignorar alerta agregado com a ID do recurso "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Security/iotSecuritySolutions/MySolutionName/analyticsModels/default/aggregatedAlerts/IoT_SucessfulLocalLogin/2020-03-03-15"</span><span class="sxs-lookup"><span data-stu-id="bed6e-115">Dismiss aggregated alert with resource Id "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Security/iotSecuritySolutions/MySolutionName/analyticsModels/default/aggregatedAlerts/IoT_SucessfulLocalLogin/2020-03-15"</span></span>

## <span data-ttu-id="bed6e-116">OS</span><span class="sxs-lookup"><span data-stu-id="bed6e-116">PARAMETERS</span></span>

### <span data-ttu-id="bed6e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bed6e-117">-DefaultProfile</span></span>
<span data-ttu-id="bed6e-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="bed6e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bed6e-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bed6e-119">-InputObject</span></span>
<span data-ttu-id="bed6e-120">Objeto de entrada.</span><span class="sxs-lookup"><span data-stu-id="bed6e-120">Input Object.</span></span>

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

### <span data-ttu-id="bed6e-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="bed6e-121">-Name</span></span>
<span data-ttu-id="bed6e-122">Nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="bed6e-122">Resource name.</span></span>

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

### <span data-ttu-id="bed6e-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bed6e-123">-PassThru</span></span>
<span data-ttu-id="bed6e-124">Retorne se a operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="bed6e-124">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="bed6e-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bed6e-125">-ResourceGroupName</span></span>
<span data-ttu-id="bed6e-126">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="bed6e-126">Resource group name.</span></span>

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

### <span data-ttu-id="bed6e-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bed6e-127">-ResourceId</span></span>
<span data-ttu-id="bed6e-128">ID do recurso de segurança no qual você deseja invocar o comando.</span><span class="sxs-lookup"><span data-stu-id="bed6e-128">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="bed6e-129">-SolutionName</span><span class="sxs-lookup"><span data-stu-id="bed6e-129">-SolutionName</span></span>
<span data-ttu-id="bed6e-130">Nome da solução</span><span class="sxs-lookup"><span data-stu-id="bed6e-130">Solution name</span></span>

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

### <span data-ttu-id="bed6e-131">-Confirme</span><span class="sxs-lookup"><span data-stu-id="bed6e-131">-Confirm</span></span>
<span data-ttu-id="bed6e-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bed6e-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bed6e-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bed6e-133">-WhatIf</span></span>
<span data-ttu-id="bed6e-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="bed6e-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bed6e-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="bed6e-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bed6e-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bed6e-136">CommonParameters</span></span>
<span data-ttu-id="bed6e-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bed6e-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bed6e-138">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bed6e-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bed6e-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="bed6e-139">INPUTS</span></span>

### <span data-ttu-id="bed6e-140">Microsoft. Azure. Commands. Security. Models. IotSecuritySolutionAnalytics. PSIoTSecurityAggregatedAlert</span><span class="sxs-lookup"><span data-stu-id="bed6e-140">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutionAnalytics.PSIoTSecurityAggregatedAlert</span></span>

### <span data-ttu-id="bed6e-141">System. String</span><span class="sxs-lookup"><span data-stu-id="bed6e-141">System.String</span></span>

## <span data-ttu-id="bed6e-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="bed6e-142">OUTPUTS</span></span>

### <span data-ttu-id="bed6e-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="bed6e-143">System.Boolean</span></span>

## <span data-ttu-id="bed6e-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="bed6e-144">NOTES</span></span>

## <span data-ttu-id="bed6e-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bed6e-145">RELATED LINKS</span></span>
