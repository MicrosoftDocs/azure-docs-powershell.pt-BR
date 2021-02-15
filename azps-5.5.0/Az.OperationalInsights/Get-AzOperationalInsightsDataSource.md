---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 1F094EBA-E4AE-4B3E-BA20-858818C6FD12
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsDataSource.md
ms.openlocfilehash: 4fb6a38ff9c79a16d150402d3a2e2be135e0c004
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111528"
---
# <span data-ttu-id="2e96f-101">Get-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="2e96f-101">Get-AzOperationalInsightsDataSource</span></span>

## <span data-ttu-id="2e96f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2e96f-102">SYNOPSIS</span></span>
<span data-ttu-id="2e96f-103">Obter recursos de dados no espaço de trabalho do Azure Log Analytics.</span><span class="sxs-lookup"><span data-stu-id="2e96f-103">Get datasources under Azure Log Analytics workspace.</span></span>

## <span data-ttu-id="2e96f-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2e96f-104">SYNTAX</span></span>

### <span data-ttu-id="2e96f-105">ByWorkspaceNameByName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="2e96f-105">ByWorkspaceNameByKind (Default)</span></span>
```
Get-AzOperationalInsightsDataSource [[-ResourceGroupName] <String>] [[-WorkspaceName] <String>]
 [-Kind] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2e96f-106">ByWorkspaceObjectByName</span><span class="sxs-lookup"><span data-stu-id="2e96f-106">ByWorkspaceObjectByName</span></span>
```
Get-AzOperationalInsightsDataSource [-Workspace] <PSWorkspace> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2e96f-107">ByWorkspaceObjectByBjectByBj</span><span class="sxs-lookup"><span data-stu-id="2e96f-107">ByWorkspaceObjectByKind</span></span>
```
Get-AzOperationalInsightsDataSource [[-Workspace] <PSWorkspace>] [[-Kind] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2e96f-108">ByWorkspaceNameByName</span><span class="sxs-lookup"><span data-stu-id="2e96f-108">ByWorkspaceNameByName</span></span>
```
Get-AzOperationalInsightsDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2e96f-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="2e96f-109">DESCRIPTION</span></span>
<span data-ttu-id="2e96f-110">O **cmdlet Get-AzOperationalInsightsDataSource** obtém fontes de dados.</span><span class="sxs-lookup"><span data-stu-id="2e96f-110">The **Get-AzOperationalInsightsDataSource** cmdlet gets data sources.</span></span>
<span data-ttu-id="2e96f-111">Você pode especificar uma fonte de dados para obter.</span><span class="sxs-lookup"><span data-stu-id="2e96f-111">You can specify a data source to get.</span></span>
<span data-ttu-id="2e96f-112">Você pode filtrar os resultados com base no tipo de fonte de dados.</span><span class="sxs-lookup"><span data-stu-id="2e96f-112">You can filter the results based on the kind of data source.</span></span>

## <span data-ttu-id="2e96f-113">Exemplos</span><span class="sxs-lookup"><span data-stu-id="2e96f-113">EXAMPLES</span></span>

## <span data-ttu-id="2e96f-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2e96f-114">PARAMETERS</span></span>

### <span data-ttu-id="2e96f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e96f-115">-DefaultProfile</span></span>
<span data-ttu-id="2e96f-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="2e96f-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2e96f-117">-Tipo</span><span class="sxs-lookup"><span data-stu-id="2e96f-117">-Kind</span></span>
<span data-ttu-id="2e96f-118">Especifica o tipo de fontes de dados a obter.</span><span class="sxs-lookup"><span data-stu-id="2e96f-118">Specifies the kind of data sources to get.</span></span>
<span data-ttu-id="2e96f-119">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="2e96f-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="2e96f-120">AzureActivityLog</span><span class="sxs-lookup"><span data-stu-id="2e96f-120">AzureActivityLog</span></span> 
- <span data-ttu-id="2e96f-121">CustomLog</span><span class="sxs-lookup"><span data-stu-id="2e96f-121">CustomLog</span></span> 
- <span data-ttu-id="2e96f-122">LinuxPerformanceObject</span><span class="sxs-lookup"><span data-stu-id="2e96f-122">LinuxPerformanceObject</span></span> 
- <span data-ttu-id="2e96f-123">LinuxSyslog</span><span class="sxs-lookup"><span data-stu-id="2e96f-123">LinuxSyslog</span></span> 
- <span data-ttu-id="2e96f-124">WindowsEvent</span><span class="sxs-lookup"><span data-stu-id="2e96f-124">WindowsEvent</span></span> 
- <span data-ttu-id="2e96f-125">WindowsPerformanceCounter</span><span class="sxs-lookup"><span data-stu-id="2e96f-125">WindowsPerformanceCounter</span></span>

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

### <span data-ttu-id="2e96f-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="2e96f-126">-Name</span></span>
<span data-ttu-id="2e96f-127">Especifica o nome de uma fonte de dados a ser obter.</span><span class="sxs-lookup"><span data-stu-id="2e96f-127">Specifies the name of a data source to get.</span></span>

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

### <span data-ttu-id="2e96f-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e96f-128">-ResourceGroupName</span></span>
<span data-ttu-id="2e96f-129">Especifica o nome de um grupo de recursos que contém fontes de dados para obter.</span><span class="sxs-lookup"><span data-stu-id="2e96f-129">Specifies the name of a resource group that contains data sources to get.</span></span>

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

### <span data-ttu-id="2e96f-130">-Espaço de Trabalho</span><span class="sxs-lookup"><span data-stu-id="2e96f-130">-Workspace</span></span>
<span data-ttu-id="2e96f-131">Especifica um espaço de trabalho no qual este cmdlet opera.</span><span class="sxs-lookup"><span data-stu-id="2e96f-131">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="2e96f-132">-NomedoEspacial de Trabalho</span><span class="sxs-lookup"><span data-stu-id="2e96f-132">-WorkspaceName</span></span>
<span data-ttu-id="2e96f-133">Especifica o nome de um espaço de trabalho no qual este cmdlet opera.</span><span class="sxs-lookup"><span data-stu-id="2e96f-133">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="2e96f-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e96f-134">CommonParameters</span></span>
<span data-ttu-id="2e96f-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e96f-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e96f-136">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2e96f-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e96f-137">Entradas</span><span class="sxs-lookup"><span data-stu-id="2e96f-137">INPUTS</span></span>

### <span data-ttu-id="2e96f-138">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="2e96f-138">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="2e96f-139">System.String</span><span class="sxs-lookup"><span data-stu-id="2e96f-139">System.String</span></span>

## <span data-ttu-id="2e96f-140">Saídas</span><span class="sxs-lookup"><span data-stu-id="2e96f-140">OUTPUTS</span></span>

### <span data-ttu-id="2e96f-141">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="2e96f-141">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="2e96f-142">Notas</span><span class="sxs-lookup"><span data-stu-id="2e96f-142">NOTES</span></span>
* <span data-ttu-id="2e96f-143">Palavras-chave: azure, azurerm, arm, resource, management, manager, operational, insights</span><span class="sxs-lookup"><span data-stu-id="2e96f-143">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="2e96f-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2e96f-144">RELATED LINKS</span></span>

[<span data-ttu-id="2e96f-145">Remove-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="2e96f-145">Remove-AzOperationalInsightsDataSource</span></span>](./Remove-AzOperationalInsightsDataSource.md)

[<span data-ttu-id="2e96f-146">Set-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="2e96f-146">Set-AzOperationalInsightsDataSource</span></span>](./Set-AzOperationalInsightsDataSource.md)


