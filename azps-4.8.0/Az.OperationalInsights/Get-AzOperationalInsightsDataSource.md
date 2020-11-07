---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 1F094EBA-E4AE-4B3E-BA20-858818C6FD12
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsDataSource.md
ms.openlocfilehash: 4fb6a38ff9c79a16d150402d3a2e2be135e0c004
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93954757"
---
# <span data-ttu-id="6800f-101">Get-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="6800f-101">Get-AzOperationalInsightsDataSource</span></span>

## <span data-ttu-id="6800f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6800f-102">SYNOPSIS</span></span>
<span data-ttu-id="6800f-103">Obter fontes de trabalho no espaço de trabalho da análise de logs do Azure.</span><span class="sxs-lookup"><span data-stu-id="6800f-103">Get datasources under Azure Log Analytics workspace.</span></span>

## <span data-ttu-id="6800f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6800f-104">SYNTAX</span></span>

### <span data-ttu-id="6800f-105">ByWorkspaceNameByKind (padrão)</span><span class="sxs-lookup"><span data-stu-id="6800f-105">ByWorkspaceNameByKind (Default)</span></span>
```
Get-AzOperationalInsightsDataSource [[-ResourceGroupName] <String>] [[-WorkspaceName] <String>]
 [-Kind] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6800f-106">ByWorkspaceObjectByName</span><span class="sxs-lookup"><span data-stu-id="6800f-106">ByWorkspaceObjectByName</span></span>
```
Get-AzOperationalInsightsDataSource [-Workspace] <PSWorkspace> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6800f-107">ByWorkspaceObjectByKind</span><span class="sxs-lookup"><span data-stu-id="6800f-107">ByWorkspaceObjectByKind</span></span>
```
Get-AzOperationalInsightsDataSource [[-Workspace] <PSWorkspace>] [[-Kind] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6800f-108">ByWorkspaceNameByName</span><span class="sxs-lookup"><span data-stu-id="6800f-108">ByWorkspaceNameByName</span></span>
```
Get-AzOperationalInsightsDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6800f-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6800f-109">DESCRIPTION</span></span>
<span data-ttu-id="6800f-110">O cmdlet **Get-AzOperationalInsightsDataSource** Obtém fontes de dados.</span><span class="sxs-lookup"><span data-stu-id="6800f-110">The **Get-AzOperationalInsightsDataSource** cmdlet gets data sources.</span></span>
<span data-ttu-id="6800f-111">Você pode especificar uma fonte de dados para obter.</span><span class="sxs-lookup"><span data-stu-id="6800f-111">You can specify a data source to get.</span></span>
<span data-ttu-id="6800f-112">Você pode filtrar os resultados com base no tipo de fonte de dados.</span><span class="sxs-lookup"><span data-stu-id="6800f-112">You can filter the results based on the kind of data source.</span></span>

## <span data-ttu-id="6800f-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6800f-113">EXAMPLES</span></span>

## <span data-ttu-id="6800f-114">OS</span><span class="sxs-lookup"><span data-stu-id="6800f-114">PARAMETERS</span></span>

### <span data-ttu-id="6800f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6800f-115">-DefaultProfile</span></span>
<span data-ttu-id="6800f-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="6800f-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6800f-117">-Kind</span><span class="sxs-lookup"><span data-stu-id="6800f-117">-Kind</span></span>
<span data-ttu-id="6800f-118">Especifica o tipo de fonte de dados a ser obtida.</span><span class="sxs-lookup"><span data-stu-id="6800f-118">Specifies the kind of data sources to get.</span></span>
<span data-ttu-id="6800f-119">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="6800f-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="6800f-120">AzureActivityLog</span><span class="sxs-lookup"><span data-stu-id="6800f-120">AzureActivityLog</span></span> 
- <span data-ttu-id="6800f-121">CustomLog</span><span class="sxs-lookup"><span data-stu-id="6800f-121">CustomLog</span></span> 
- <span data-ttu-id="6800f-122">LinuxPerformanceObject</span><span class="sxs-lookup"><span data-stu-id="6800f-122">LinuxPerformanceObject</span></span> 
- <span data-ttu-id="6800f-123">LinuxSyslog</span><span class="sxs-lookup"><span data-stu-id="6800f-123">LinuxSyslog</span></span> 
- <span data-ttu-id="6800f-124">WindowsEvent</span><span class="sxs-lookup"><span data-stu-id="6800f-124">WindowsEvent</span></span> 
- <span data-ttu-id="6800f-125">WindowsPerformanceCounter</span><span class="sxs-lookup"><span data-stu-id="6800f-125">WindowsPerformanceCounter</span></span>

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

### <span data-ttu-id="6800f-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="6800f-126">-Name</span></span>
<span data-ttu-id="6800f-127">Especifica o nome de uma fonte de dados a ser obtida.</span><span class="sxs-lookup"><span data-stu-id="6800f-127">Specifies the name of a data source to get.</span></span>

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

### <span data-ttu-id="6800f-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6800f-128">-ResourceGroupName</span></span>
<span data-ttu-id="6800f-129">Especifica o nome de um grupo de recursos que contém fontes de dados para obter.</span><span class="sxs-lookup"><span data-stu-id="6800f-129">Specifies the name of a resource group that contains data sources to get.</span></span>

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

### <span data-ttu-id="6800f-130">-Espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="6800f-130">-Workspace</span></span>
<span data-ttu-id="6800f-131">Especifica um espaço de trabalho no qual esse cmdlet Opera.</span><span class="sxs-lookup"><span data-stu-id="6800f-131">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="6800f-132">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="6800f-132">-WorkspaceName</span></span>
<span data-ttu-id="6800f-133">Especifica o nome de um espaço de trabalho no qual esse cmdlet Opera.</span><span class="sxs-lookup"><span data-stu-id="6800f-133">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="6800f-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6800f-134">CommonParameters</span></span>
<span data-ttu-id="6800f-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6800f-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6800f-136">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6800f-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6800f-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6800f-137">INPUTS</span></span>

### <span data-ttu-id="6800f-138">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="6800f-138">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="6800f-139">System. String</span><span class="sxs-lookup"><span data-stu-id="6800f-139">System.String</span></span>

## <span data-ttu-id="6800f-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6800f-140">OUTPUTS</span></span>

### <span data-ttu-id="6800f-141">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="6800f-141">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="6800f-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6800f-142">NOTES</span></span>
* <span data-ttu-id="6800f-143">Palavras-chave: Azure, azurerm, ARM, Resource, Management, Manager, Operational, insights</span><span class="sxs-lookup"><span data-stu-id="6800f-143">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="6800f-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6800f-144">RELATED LINKS</span></span>

[<span data-ttu-id="6800f-145">Remove-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="6800f-145">Remove-AzOperationalInsightsDataSource</span></span>](./Remove-AzOperationalInsightsDataSource.md)

[<span data-ttu-id="6800f-146">Set-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="6800f-146">Set-AzOperationalInsightsDataSource</span></span>](./Set-AzOperationalInsightsDataSource.md)


