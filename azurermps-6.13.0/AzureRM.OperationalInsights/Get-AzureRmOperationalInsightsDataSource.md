---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 1F094EBA-E4AE-4B3E-BA20-858818C6FD12
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/get-azurermoperationalinsightsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsDataSource.md
ms.openlocfilehash: 5d13fb4c432a0b40fdfd90a5eea55ea44a8b6ef2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428438"
---
# <span data-ttu-id="2ba76-101">Get-AzureRmOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="2ba76-101">Get-AzureRmOperationalInsightsDataSource</span></span>

## <span data-ttu-id="2ba76-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2ba76-102">SYNOPSIS</span></span>
<span data-ttu-id="2ba76-103">Obter fontes de trabalho no espaço de trabalho da análise de logs do Azure.</span><span class="sxs-lookup"><span data-stu-id="2ba76-103">Get datasources under Azure Log Analytics workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2ba76-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2ba76-104">SYNTAX</span></span>

### <span data-ttu-id="2ba76-105">ByWorkspaceName (padrão)</span><span class="sxs-lookup"><span data-stu-id="2ba76-105">ByWorkspaceName (Default)</span></span>
```
Get-AzureRmOperationalInsightsDataSource [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2ba76-106">ByWorkspaceObjectByName</span><span class="sxs-lookup"><span data-stu-id="2ba76-106">ByWorkspaceObjectByName</span></span>
```
Get-AzureRmOperationalInsightsDataSource [-Workspace] <PSWorkspace> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2ba76-107">ByWorkspaceObjectByKind</span><span class="sxs-lookup"><span data-stu-id="2ba76-107">ByWorkspaceObjectByKind</span></span>
```
Get-AzureRmOperationalInsightsDataSource [[-Workspace] <PSWorkspace>] [[-Kind] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2ba76-108">ByWorkspaceNameByName</span><span class="sxs-lookup"><span data-stu-id="2ba76-108">ByWorkspaceNameByName</span></span>
```
Get-AzureRmOperationalInsightsDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2ba76-109">ByWorkspaceNameByKind</span><span class="sxs-lookup"><span data-stu-id="2ba76-109">ByWorkspaceNameByKind</span></span>
```
Get-AzureRmOperationalInsightsDataSource [[-ResourceGroupName] <String>] [[-WorkspaceName] <String>]
 [-Kind] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2ba76-110">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2ba76-110">DESCRIPTION</span></span>
<span data-ttu-id="2ba76-111">O cmdlet **Get-AzureRmOperationalInsightsDataSource** Obtém fontes de dados.</span><span class="sxs-lookup"><span data-stu-id="2ba76-111">The **Get-AzureRmOperationalInsightsDataSource** cmdlet gets data sources.</span></span>
<span data-ttu-id="2ba76-112">Você pode especificar uma fonte de dados para obter.</span><span class="sxs-lookup"><span data-stu-id="2ba76-112">You can specify a data source to get.</span></span>
<span data-ttu-id="2ba76-113">Você pode filtrar os resultados com base no tipo de fonte de dados.</span><span class="sxs-lookup"><span data-stu-id="2ba76-113">You can filter the results based on the kind of data source.</span></span>

## <span data-ttu-id="2ba76-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2ba76-114">EXAMPLES</span></span>

## <span data-ttu-id="2ba76-115">OS</span><span class="sxs-lookup"><span data-stu-id="2ba76-115">PARAMETERS</span></span>

### <span data-ttu-id="2ba76-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ba76-116">-DefaultProfile</span></span>
<span data-ttu-id="2ba76-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="2ba76-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ba76-118">-Kind</span><span class="sxs-lookup"><span data-stu-id="2ba76-118">-Kind</span></span>
<span data-ttu-id="2ba76-119">Especifica o tipo de fonte de dados a ser obtida.</span><span class="sxs-lookup"><span data-stu-id="2ba76-119">Specifies the kind of data sources to get.</span></span>
<span data-ttu-id="2ba76-120">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="2ba76-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="2ba76-121">AzureActivityLog</span><span class="sxs-lookup"><span data-stu-id="2ba76-121">AzureActivityLog</span></span> 
- <span data-ttu-id="2ba76-122">CustomLog</span><span class="sxs-lookup"><span data-stu-id="2ba76-122">CustomLog</span></span> 
- <span data-ttu-id="2ba76-123">LinuxPerformanceObject</span><span class="sxs-lookup"><span data-stu-id="2ba76-123">LinuxPerformanceObject</span></span> 
- <span data-ttu-id="2ba76-124">LinuxSyslog</span><span class="sxs-lookup"><span data-stu-id="2ba76-124">LinuxSyslog</span></span> 
- <span data-ttu-id="2ba76-125">WindowsEvent</span><span class="sxs-lookup"><span data-stu-id="2ba76-125">WindowsEvent</span></span> 
- <span data-ttu-id="2ba76-126">WindowsPerformanceCounter</span><span class="sxs-lookup"><span data-stu-id="2ba76-126">WindowsPerformanceCounter</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceObjectByKind
Aliases:
Accepted values: AzureAuditLog, AzureActivityLog, CustomLog, LinuxPerformanceObject, LinuxSyslog, WindowsEvent, WindowsPerformanceCounter

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByWorkspaceNameByKind
Aliases:
Accepted values: AzureAuditLog, AzureActivityLog, CustomLog, LinuxPerformanceObject, LinuxSyslog, WindowsEvent, WindowsPerformanceCounter

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ba76-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="2ba76-127">-Name</span></span>
<span data-ttu-id="2ba76-128">Especifica o nome de uma fonte de dados a ser obtida.</span><span class="sxs-lookup"><span data-stu-id="2ba76-128">Specifies the name of a data source to get.</span></span>

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

### <span data-ttu-id="2ba76-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ba76-129">-ResourceGroupName</span></span>
<span data-ttu-id="2ba76-130">Especifica o nome de um grupo de recursos que contém fontes de dados para obter.</span><span class="sxs-lookup"><span data-stu-id="2ba76-130">Specifies the name of a resource group that contains data sources to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceNameByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByWorkspaceNameByKind
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ba76-131">-Espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="2ba76-131">-Workspace</span></span>
<span data-ttu-id="2ba76-132">Especifica um espaço de trabalho no qual esse cmdlet Opera.</span><span class="sxs-lookup"><span data-stu-id="2ba76-132">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="2ba76-133">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="2ba76-133">-WorkspaceName</span></span>
<span data-ttu-id="2ba76-134">Especifica o nome de um espaço de trabalho no qual esse cmdlet Opera.</span><span class="sxs-lookup"><span data-stu-id="2ba76-134">Specifies the name of a workspace in which this cmdlet operates.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceNameByName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByWorkspaceNameByKind
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ba76-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ba76-135">CommonParameters</span></span>
<span data-ttu-id="2ba76-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ba76-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ba76-137">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ba76-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ba76-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2ba76-138">INPUTS</span></span>

### <span data-ttu-id="2ba76-139">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="2ba76-139">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>
<span data-ttu-id="2ba76-140">Parâmetros: espaço de trabalho (ByValue)</span><span class="sxs-lookup"><span data-stu-id="2ba76-140">Parameters: Workspace (ByValue)</span></span>

### <span data-ttu-id="2ba76-141">System. String</span><span class="sxs-lookup"><span data-stu-id="2ba76-141">System.String</span></span>

## <span data-ttu-id="2ba76-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2ba76-142">OUTPUTS</span></span>

### <span data-ttu-id="2ba76-143">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="2ba76-143">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="2ba76-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2ba76-144">NOTES</span></span>
* <span data-ttu-id="2ba76-145">Palavras-chave: Azure, azurerm, ARM, Resource, Management, Manager, Operational, insights</span><span class="sxs-lookup"><span data-stu-id="2ba76-145">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="2ba76-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2ba76-146">RELATED LINKS</span></span>

[<span data-ttu-id="2ba76-147">Remove-AzureRmOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="2ba76-147">Remove-AzureRmOperationalInsightsDataSource</span></span>](./Remove-AzureRmOperationalInsightsDataSource.md)

[<span data-ttu-id="2ba76-148">Set-AzureRmOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="2ba76-148">Set-AzureRmOperationalInsightsDataSource</span></span>](./Set-AzureRmOperationalInsightsDataSource.md)


