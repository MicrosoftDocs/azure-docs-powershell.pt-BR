---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: E3D7A3FE-40D4-4495-BA39-493F85F304AD
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightsapplicationinsightsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsApplicationInsightsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsApplicationInsightsDataSource.md
ms.openlocfilehash: 0f238a417ac83cac82305ceb9c9ce20586328976
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118222"
---
# <span data-ttu-id="e0e2f-101">New-AzOperationalInsightsApplicationInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="e0e2f-101">New-AzOperationalInsightsApplicationInsightsDataSource</span></span>

## <span data-ttu-id="e0e2f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e0e2f-102">SYNOPSIS</span></span>
<span data-ttu-id="e0e2f-103">Coletar logs de determinado Application-Insights aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e0e2f-103">Collect logs from given Application-Insights application.</span></span>

## <span data-ttu-id="e0e2f-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e0e2f-104">SYNTAX</span></span>

### <span data-ttu-id="e0e2f-105">ByWorkspaceName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="e0e2f-105">ByWorkspaceName (Default)</span></span>
```
New-AzOperationalInsightsApplicationInsightsDataSource [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e0e2f-106">ByWorkspaceObjectByApplicationParameters</span><span class="sxs-lookup"><span data-stu-id="e0e2f-106">ByWorkspaceObjectByApplicationParameters</span></span>
```
New-AzOperationalInsightsApplicationInsightsDataSource [-Workspace] <PSWorkspace>
 -ApplicationSubscriptionId <String> -ApplicationResourceGroupName <String> -ApplicationName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e0e2f-107">ByWorkspaceObjectByApplicationResourceId</span><span class="sxs-lookup"><span data-stu-id="e0e2f-107">ByWorkspaceObjectByApplicationResourceId</span></span>
```
New-AzOperationalInsightsApplicationInsightsDataSource [-Workspace] <PSWorkspace>
 -ApplicationResourceId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e0e2f-108">ByWorkspaceNameByApplicationParameters</span><span class="sxs-lookup"><span data-stu-id="e0e2f-108">ByWorkspaceNameByApplicationParameters</span></span>
```
New-AzOperationalInsightsApplicationInsightsDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 -ApplicationSubscriptionId <String> -ApplicationResourceGroupName <String> -ApplicationName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e0e2f-109">ByWorkspaceNameByApplicationResourceId</span><span class="sxs-lookup"><span data-stu-id="e0e2f-109">ByWorkspaceNameByApplicationResourceId</span></span>
```
New-AzOperationalInsightsApplicationInsightsDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 -ApplicationResourceId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e0e2f-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="e0e2f-110">DESCRIPTION</span></span>
<span data-ttu-id="e0e2f-111">O cmdlet **New-AzOperationalInsightsApplicationInsightsDataSource** habilita o conjunto de logs de um determinado Application-Insights aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e0e2f-111">The **New-AzOperationalInsightsApplicationInsightsDataSource** cmdlet enables the collection of logs from a given Application-Insights application.</span></span>

## <span data-ttu-id="e0e2f-112">Exemplos</span><span class="sxs-lookup"><span data-stu-id="e0e2f-112">EXAMPLES</span></span>

### <span data-ttu-id="e0e2f-113">Exemplo 1: Criar fonte de dados de insights de aplicativo no espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="e0e2f-113">Example 1: Create application-insights data source in workspace</span></span>
```
PS C:\> New-AzOperationalInsightsApplicationInsightsDataSource -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "MyWorkspace" -ApplicationSubscriptionId "e791a474-ee54-46a2-bb06-5e058302d234" -ApplicationResourceGroupName "ContosoResourceGroup" -ApplicationName "MyAIApplication"

Name              : subscriptions/e791a474-ee54-46a2-bb06-5e058302d234/resourceGroups/ContosoResourceGroup/providers/microsoft.insights/components/MyAIApplication
ResourceGroupName : ContosoResourceGroup
WorkspaceName     : MyWorkspace
ResourceId        : /subscriptions/e791a474-ee54-46a2-bb06-5e058302d234/resourceGroups/ContosoResourceGroup/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace/datasources/subscriptions/e791a474-ee54-46a2-bb06-5e058302d234/resourceGroups/ContosoResourceGroup/providers/microsoft.insights/components/MyAIApplication
Kind              : ApplicationInsights
Properties        : {"linkedResourceId":"subscriptions/e791a474-ee54-46a2-bb06-5e058302d234/resourceGroups/ContosoResourceGroup/providers/microsoft.insights/components/MyAIApplication","status":"Succeeded"}

```

<span data-ttu-id="e0e2f-114">Esse comando cria uma fonte de dados de insights de aplicativo de um determinado aplicativo em um determinado espaço de trabalho de análise de log.</span><span class="sxs-lookup"><span data-stu-id="e0e2f-114">This command creates an application-insights data source of a given application in a given log analytics workspace.</span></span> <span data-ttu-id="e0e2f-115">Isso habilita o conjunto de logs de determinado aplicativo para o espaço de trabalho de análise de log.</span><span class="sxs-lookup"><span data-stu-id="e0e2f-115">This enables the collection of logs from given application to the log analytics workspace.</span></span>

### <span data-ttu-id="e0e2f-116">Exemplo 2: Obter objeto de espaço de trabalho e criar fonte de dados de insights de aplicativo pela ID do recurso de aplicativo</span><span class="sxs-lookup"><span data-stu-id="e0e2f-116">Example 2: Get workspace object and create application-insights data source by the application resource id</span></span>
```
PS C:\> Get-AzureRmOperationalInsightsWorkspace -Name "MyWorkspace" -ResourceGroupName "ContosoResourceGroup" | New-AzOperationalInsightsApplicationInsightsDataSource -ApplicationResourceId "/subscriptions/e791a474-ee54-46a2-bb06-5e058302d234/resourceGroups/ContosoResourceGroup/providers/microsoft.insights/components/MyAIApplication"

Name              : subscriptions/aaaaa474-ee54-4aaa-bb06-5e058302daaa/resourceGroups/ContosoResourceGroup/providers/microsoft.insights/components/MyAIApplication
ResourceGroupName : ContosoResourceGroup
WorkspaceName     : MyWorkspace
ResourceId        : /subscriptions/aaaaa474-ee54-4aaa-bb06-5e058302daaa/resourceGroups/ContosoResourceGroup/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace/datasources/subscriptions/e791a474-ee54-46a2-bb06-5e058302d234/resourceGroups/ContosoResourceGroup/providers/microsoft.insights/components/MyAIApplication
Kind              : ApplicationInsights
Properties        : {"linkedResourceId":"subscriptions/e791a474-ee54-46a2-bb06-5e058302d234/resourceGroups/ContosoResourceGroup/providers/microsoft.insights/components/MyAIApplication","status":"Succeeded"}

```

<span data-ttu-id="e0e2f-117">Esse comando demonstra como obter um objeto de espaço de trabalho de análise de log e, em seguida, passar a saída para criar uma fonte de dados de informações de aplicativo associada pela ID do recurso de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e0e2f-117">This command demonstrates getting a log analytics workspace object and then passing the output to create an associated application-insights data source by the application resource id.</span></span> 

## <span data-ttu-id="e0e2f-118">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e0e2f-118">PARAMETERS</span></span>

### <span data-ttu-id="e0e2f-119">-Nomedo Aplicativo</span><span class="sxs-lookup"><span data-stu-id="e0e2f-119">-ApplicationName</span></span>
<span data-ttu-id="e0e2f-120">O nome do aplicativo vinculado.</span><span class="sxs-lookup"><span data-stu-id="e0e2f-120">The name of the linked application.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceObjectByApplicationParameters, ByWorkspaceNameByApplicationParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0e2f-121">-ApplicationResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0e2f-121">-ApplicationResourceGroupName</span></span>
<span data-ttu-id="e0e2f-122">O nome do grupo de recursos do aplicativo vinculado.</span><span class="sxs-lookup"><span data-stu-id="e0e2f-122">The resource group name of the linked application.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceObjectByApplicationParameters, ByWorkspaceNameByApplicationParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0e2f-123">-ApplicationResourceId</span><span class="sxs-lookup"><span data-stu-id="e0e2f-123">-ApplicationResourceId</span></span>
<span data-ttu-id="e0e2f-124">A ID de recurso do aplicativo vinculado.</span><span class="sxs-lookup"><span data-stu-id="e0e2f-124">The linked application resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceObjectByApplicationResourceId, ByWorkspaceNameByApplicationResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0e2f-125">-ApplicationSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e0e2f-125">-ApplicationSubscriptionId</span></span>
<span data-ttu-id="e0e2f-126">A ID da assinatura do aplicativo vinculado.</span><span class="sxs-lookup"><span data-stu-id="e0e2f-126">The subscription id of the linked application.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceObjectByApplicationParameters, ByWorkspaceNameByApplicationParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0e2f-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0e2f-127">-DefaultProfile</span></span>
<span data-ttu-id="e0e2f-128">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e0e2f-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e0e2f-129">-Forçar</span><span class="sxs-lookup"><span data-stu-id="e0e2f-129">-Force</span></span>
<span data-ttu-id="e0e2f-130">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="e0e2f-130">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="e0e2f-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0e2f-131">-ResourceGroupName</span></span>
<span data-ttu-id="e0e2f-132">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e0e2f-132">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceNameByApplicationParameters, ByWorkspaceNameByApplicationResourceId
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0e2f-133">-Espaço de Trabalho</span><span class="sxs-lookup"><span data-stu-id="e0e2f-133">-Workspace</span></span>
<span data-ttu-id="e0e2f-134">O espaço de trabalho que conterá a fonte de dados.</span><span class="sxs-lookup"><span data-stu-id="e0e2f-134">The workspace that will contain the data source.</span></span>

```yaml
Type: Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace
Parameter Sets: ByWorkspaceObjectByApplicationParameters, ByWorkspaceObjectByApplicationResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e0e2f-135">-NomedoEspacial de Trabalho</span><span class="sxs-lookup"><span data-stu-id="e0e2f-135">-WorkspaceName</span></span>
<span data-ttu-id="e0e2f-136">O nome do espaço de trabalho que conterá a fonte de dados.</span><span class="sxs-lookup"><span data-stu-id="e0e2f-136">The name of the workspace that will contain the data source.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceNameByApplicationParameters, ByWorkspaceNameByApplicationResourceId
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0e2f-137">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="e0e2f-137">-Confirm</span></span>
<span data-ttu-id="e0e2f-138">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e0e2f-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e0e2f-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e0e2f-139">-WhatIf</span></span>
<span data-ttu-id="e0e2f-140">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="e0e2f-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e0e2f-141">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e0e2f-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e0e2f-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0e2f-142">CommonParameters</span></span>
<span data-ttu-id="e0e2f-143">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0e2f-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0e2f-144">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e0e2f-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0e2f-145">Entradas</span><span class="sxs-lookup"><span data-stu-id="e0e2f-145">INPUTS</span></span>

### <span data-ttu-id="e0e2f-146">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="e0e2f-146">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="e0e2f-147">System.String</span><span class="sxs-lookup"><span data-stu-id="e0e2f-147">System.String</span></span>

## <span data-ttu-id="e0e2f-148">Saídas</span><span class="sxs-lookup"><span data-stu-id="e0e2f-148">OUTPUTS</span></span>

### <span data-ttu-id="e0e2f-149">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="e0e2f-149">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="e0e2f-150">Notas</span><span class="sxs-lookup"><span data-stu-id="e0e2f-150">NOTES</span></span>

## <span data-ttu-id="e0e2f-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e0e2f-151">RELATED LINKS</span></span>
