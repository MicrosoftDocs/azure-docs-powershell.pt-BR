---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 1F094EBA-E4AE-4B3E-BA20-858818C6FD12
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/get-azoperationalinsightsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsDataSource.md
ms.openlocfilehash: c3ca23ae1cbe29c7c2867ec9ac48bea612dd4fc2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888449"
---
# <span data-ttu-id="9a8a5-101">Get-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="9a8a5-101">Get-AzOperationalInsightsDataSource</span></span>

## <span data-ttu-id="9a8a5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9a8a5-102">SYNOPSIS</span></span>
<span data-ttu-id="9a8a5-103">Obter datasources no espaço de trabalho do Azure Log Analytics.</span><span class="sxs-lookup"><span data-stu-id="9a8a5-103">Get datasources under Azure Log Analytics workspace.</span></span>

## <span data-ttu-id="9a8a5-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="9a8a5-104">SYNTAX</span></span>

### <span data-ttu-id="9a8a5-105">ByWorkspaceNameByKind (Padrão)</span><span class="sxs-lookup"><span data-stu-id="9a8a5-105">ByWorkspaceNameByKind (Default)</span></span>
```
Get-AzOperationalInsightsDataSource [[-ResourceGroupName] <String>] [[-WorkspaceName] <String>]
 [-Kind] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9a8a5-106">ByWorkspaceObjectByName</span><span class="sxs-lookup"><span data-stu-id="9a8a5-106">ByWorkspaceObjectByName</span></span>
```
Get-AzOperationalInsightsDataSource [-Workspace] <PSWorkspace> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9a8a5-107">ByWorkspaceObjectByKind</span><span class="sxs-lookup"><span data-stu-id="9a8a5-107">ByWorkspaceObjectByKind</span></span>
```
Get-AzOperationalInsightsDataSource [[-Workspace] <PSWorkspace>] [[-Kind] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9a8a5-108">ByWorkspaceNameByName</span><span class="sxs-lookup"><span data-stu-id="9a8a5-108">ByWorkspaceNameByName</span></span>
```
Get-AzOperationalInsightsDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9a8a5-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="9a8a5-109">DESCRIPTION</span></span>
<span data-ttu-id="9a8a5-110">O cmdlet **Get-AzOperationalInsightsDataSource obtém** fontes de dados.</span><span class="sxs-lookup"><span data-stu-id="9a8a5-110">The **Get-AzOperationalInsightsDataSource** cmdlet gets data sources.</span></span>
<span data-ttu-id="9a8a5-111">Você pode especificar uma fonte de dados para obter.</span><span class="sxs-lookup"><span data-stu-id="9a8a5-111">You can specify a data source to get.</span></span>
<span data-ttu-id="9a8a5-112">Você pode filtrar os resultados com base no tipo de fonte de dados.</span><span class="sxs-lookup"><span data-stu-id="9a8a5-112">You can filter the results based on the kind of data source.</span></span>

## <span data-ttu-id="9a8a5-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9a8a5-113">EXAMPLES</span></span>

## <span data-ttu-id="9a8a5-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="9a8a5-114">PARAMETERS</span></span>

### <span data-ttu-id="9a8a5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a8a5-115">-DefaultProfile</span></span>
<span data-ttu-id="9a8a5-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="9a8a5-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9a8a5-117">-Kind</span><span class="sxs-lookup"><span data-stu-id="9a8a5-117">-Kind</span></span>
<span data-ttu-id="9a8a5-118">Especifica o tipo de fonte de dados a ser obter.</span><span class="sxs-lookup"><span data-stu-id="9a8a5-118">Specifies the kind of data sources to get.</span></span>
<span data-ttu-id="9a8a5-119">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="9a8a5-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="9a8a5-120">AzureActivityLog</span><span class="sxs-lookup"><span data-stu-id="9a8a5-120">AzureActivityLog</span></span> 
- <span data-ttu-id="9a8a5-121">CustomLog</span><span class="sxs-lookup"><span data-stu-id="9a8a5-121">CustomLog</span></span> 
- <span data-ttu-id="9a8a5-122">LinuxPerformanceObject</span><span class="sxs-lookup"><span data-stu-id="9a8a5-122">LinuxPerformanceObject</span></span> 
- <span data-ttu-id="9a8a5-123">LinuxSyslog</span><span class="sxs-lookup"><span data-stu-id="9a8a5-123">LinuxSyslog</span></span> 
- <span data-ttu-id="9a8a5-124">WindowsEvent</span><span class="sxs-lookup"><span data-stu-id="9a8a5-124">WindowsEvent</span></span> 
- <span data-ttu-id="9a8a5-125">WindowsPerformanceCounter</span><span class="sxs-lookup"><span data-stu-id="9a8a5-125">WindowsPerformanceCounter</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceNameByKind
Aliases:
Accepted values: AzureAuditLog, AzureActivityLog, CustomLog, LinuxPerformanceObject, LinuxSyslog, WindowsEvent, WindowsPerformanceCounter, ApplicationInsights

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByWorkspaceObjectByKind
Aliases:
Accepted values: AzureAuditLog, AzureActivityLog, CustomLog, LinuxPerformanceObject, LinuxSyslog, WindowsEvent, WindowsPerformanceCounter, ApplicationInsights

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a8a5-126">-Name</span><span class="sxs-lookup"><span data-stu-id="9a8a5-126">-Name</span></span>
<span data-ttu-id="9a8a5-127">Especifica o nome de uma fonte de dados a ser obter.</span><span class="sxs-lookup"><span data-stu-id="9a8a5-127">Specifies the name of a data source to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceObjectByName
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByWorkspaceNameByName
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a8a5-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9a8a5-128">-ResourceGroupName</span></span>
<span data-ttu-id="9a8a5-129">Especifica o nome de um grupo de recursos que contém fontes de dados a obter.</span><span class="sxs-lookup"><span data-stu-id="9a8a5-129">Specifies the name of a resource group that contains data sources to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceNameByKind
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByWorkspaceNameByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a8a5-130">-Workspace</span><span class="sxs-lookup"><span data-stu-id="9a8a5-130">-Workspace</span></span>
<span data-ttu-id="9a8a5-131">Especifica um espaço de trabalho no qual este cmdlet opera.</span><span class="sxs-lookup"><span data-stu-id="9a8a5-131">Specifies a workspace in which this cmdlet operates.</span></span>

```yaml
Type: Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace
Parameter Sets: ByWorkspaceObjectByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace
Parameter Sets: ByWorkspaceObjectByKind
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9a8a5-132">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="9a8a5-132">-WorkspaceName</span></span>
<span data-ttu-id="9a8a5-133">Especifica o nome de um espaço de trabalho no qual este cmdlet opera.</span><span class="sxs-lookup"><span data-stu-id="9a8a5-133">Specifies the name of a workspace in which this cmdlet operates.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceNameByKind
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByWorkspaceNameByName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a8a5-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a8a5-134">CommonParameters</span></span>
<span data-ttu-id="9a8a5-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9a8a5-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a8a5-136">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9a8a5-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a8a5-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9a8a5-137">INPUTS</span></span>

### <span data-ttu-id="9a8a5-138">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="9a8a5-138">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="9a8a5-139">System.String</span><span class="sxs-lookup"><span data-stu-id="9a8a5-139">System.String</span></span>

## <span data-ttu-id="9a8a5-140">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="9a8a5-140">OUTPUTS</span></span>

### <span data-ttu-id="9a8a5-141">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="9a8a5-141">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="9a8a5-142">NOTES</span><span class="sxs-lookup"><span data-stu-id="9a8a5-142">NOTES</span></span>
* <span data-ttu-id="9a8a5-143">Palavras-chave: azure, azurerm, arm, resource, management, manager, operational, insights</span><span class="sxs-lookup"><span data-stu-id="9a8a5-143">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="9a8a5-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9a8a5-144">RELATED LINKS</span></span>

[<span data-ttu-id="9a8a5-145">Remove-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="9a8a5-145">Remove-AzOperationalInsightsDataSource</span></span>](./Remove-AzOperationalInsightsDataSource.md)

[<span data-ttu-id="9a8a5-146">Set-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="9a8a5-146">Set-AzOperationalInsightsDataSource</span></span>](./Set-AzOperationalInsightsDataSource.md)


