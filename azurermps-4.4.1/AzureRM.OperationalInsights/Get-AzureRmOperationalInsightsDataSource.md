---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 1F094EBA-E4AE-4B3E-BA20-858818C6FD12
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsDataSource.md
ms.openlocfilehash: 61846456cfbff2dcbdaffba8c73a9bada87f07dc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93433049"
---
# <span data-ttu-id="e95f5-101">Get-AzureRmOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="e95f5-101">Get-AzureRmOperationalInsightsDataSource</span></span>

## <span data-ttu-id="e95f5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e95f5-102">SYNOPSIS</span></span>
<span data-ttu-id="e95f5-103">Obter fontes de trabalho no espaço de trabalho da análise de logs do Azure.</span><span class="sxs-lookup"><span data-stu-id="e95f5-103">Get datasources under Azure Log Analytics workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e95f5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e95f5-104">SYNTAX</span></span>

### <span data-ttu-id="e95f5-105">ByWorkspaceName (padrão)</span><span class="sxs-lookup"><span data-stu-id="e95f5-105">ByWorkspaceName (Default)</span></span>
```
Get-AzureRmOperationalInsightsDataSource [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e95f5-106">ByWorkspaceObjectByName</span><span class="sxs-lookup"><span data-stu-id="e95f5-106">ByWorkspaceObjectByName</span></span>
```
Get-AzureRmOperationalInsightsDataSource [-Workspace] <PSWorkspace> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e95f5-107">ByWorkspaceObjectByKind</span><span class="sxs-lookup"><span data-stu-id="e95f5-107">ByWorkspaceObjectByKind</span></span>
```
Get-AzureRmOperationalInsightsDataSource [[-Workspace] <PSWorkspace>] [[-Kind] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e95f5-108">ByWorkspaceNameByName</span><span class="sxs-lookup"><span data-stu-id="e95f5-108">ByWorkspaceNameByName</span></span>
```
Get-AzureRmOperationalInsightsDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e95f5-109">ByWorkspaceNameByKind</span><span class="sxs-lookup"><span data-stu-id="e95f5-109">ByWorkspaceNameByKind</span></span>
```
Get-AzureRmOperationalInsightsDataSource [[-ResourceGroupName] <String>] [[-WorkspaceName] <String>]
 [-Kind] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e95f5-110">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e95f5-110">DESCRIPTION</span></span>
<span data-ttu-id="e95f5-111">O cmdlet **Get-AzureRmOperationalInsightsDataSource** Obtém fontes de dados.</span><span class="sxs-lookup"><span data-stu-id="e95f5-111">The **Get-AzureRmOperationalInsightsDataSource** cmdlet gets data sources.</span></span>
<span data-ttu-id="e95f5-112">Você pode especificar uma fonte de dados para obter.</span><span class="sxs-lookup"><span data-stu-id="e95f5-112">You can specify a data source to get.</span></span>
<span data-ttu-id="e95f5-113">Você pode filtrar os resultados com base no tipo de fonte de dados.</span><span class="sxs-lookup"><span data-stu-id="e95f5-113">You can filter the results based on the kind of data source.</span></span>

## <span data-ttu-id="e95f5-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e95f5-114">EXAMPLES</span></span>

## <span data-ttu-id="e95f5-115">OS</span><span class="sxs-lookup"><span data-stu-id="e95f5-115">PARAMETERS</span></span>

### <span data-ttu-id="e95f5-116">-Kind</span><span class="sxs-lookup"><span data-stu-id="e95f5-116">-Kind</span></span>
<span data-ttu-id="e95f5-117">Especifica o tipo de fonte de dados a ser obtida.</span><span class="sxs-lookup"><span data-stu-id="e95f5-117">Specifies the kind of data sources to get.</span></span>
<span data-ttu-id="e95f5-118">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="e95f5-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e95f5-119">AzureActivityLog</span><span class="sxs-lookup"><span data-stu-id="e95f5-119">AzureActivityLog</span></span> 
- <span data-ttu-id="e95f5-120">CustomLog</span><span class="sxs-lookup"><span data-stu-id="e95f5-120">CustomLog</span></span> 
- <span data-ttu-id="e95f5-121">LinuxPerformanceObject</span><span class="sxs-lookup"><span data-stu-id="e95f5-121">LinuxPerformanceObject</span></span> 
- <span data-ttu-id="e95f5-122">LinuxSyslog</span><span class="sxs-lookup"><span data-stu-id="e95f5-122">LinuxSyslog</span></span> 
- <span data-ttu-id="e95f5-123">WindowsEvent</span><span class="sxs-lookup"><span data-stu-id="e95f5-123">WindowsEvent</span></span> 
- <span data-ttu-id="e95f5-124">WindowsPerformanceCounter</span><span class="sxs-lookup"><span data-stu-id="e95f5-124">WindowsPerformanceCounter</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceObjectByKind
Aliases: 
Accepted values: AzureAuditLog, AzureActivityLog, CustomLog, LinuxPerformanceObject, LinuxSyslog, WindowsEvent, WindowsPerformanceCounter, AzureAuditLog, AzureActivityLog, CustomLog, LinuxPerformanceObject, LinuxSyslog, WindowsEvent, WindowsPerformanceCounter

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
Accepted values: AzureAuditLog, AzureActivityLog, CustomLog, LinuxPerformanceObject, LinuxSyslog, WindowsEvent, WindowsPerformanceCounter, AzureAuditLog, AzureActivityLog, CustomLog, LinuxPerformanceObject, LinuxSyslog, WindowsEvent, WindowsPerformanceCounter

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e95f5-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="e95f5-125">-Name</span></span>
<span data-ttu-id="e95f5-126">Especifica o nome de uma fonte de dados a ser obtida.</span><span class="sxs-lookup"><span data-stu-id="e95f5-126">Specifies the name of a data source to get.</span></span>

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

### <span data-ttu-id="e95f5-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e95f5-127">-ResourceGroupName</span></span>
<span data-ttu-id="e95f5-128">Especifica o nome de um grupo de recursos que contém fontes de dados para obter.</span><span class="sxs-lookup"><span data-stu-id="e95f5-128">Specifies the name of a resource group that contains data sources to get.</span></span>

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

### <span data-ttu-id="e95f5-129">-Espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="e95f5-129">-Workspace</span></span>
<span data-ttu-id="e95f5-130">Especifica um espaço de trabalho no qual esse cmdlet Opera.</span><span class="sxs-lookup"><span data-stu-id="e95f5-130">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="e95f5-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="e95f5-131">-WorkspaceName</span></span>
<span data-ttu-id="e95f5-132">Especifica o nome de um espaço de trabalho no qual esse cmdlet Opera.</span><span class="sxs-lookup"><span data-stu-id="e95f5-132">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="e95f5-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e95f5-133">-DefaultProfile</span></span>
<span data-ttu-id="e95f5-134">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e95f5-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e95f5-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e95f5-135">CommonParameters</span></span>
<span data-ttu-id="e95f5-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e95f5-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e95f5-137">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e95f5-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e95f5-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e95f5-138">INPUTS</span></span>

### <span data-ttu-id="e95f5-139">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="e95f5-139">PSWorkspace</span></span>
<span data-ttu-id="e95f5-140">O parâmetro ' Workspace ' aceita o valor do tipo ' PSWorkspace ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="e95f5-140">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

### <span data-ttu-id="e95f5-141">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="e95f5-141">PSWorkspace</span></span>
<span data-ttu-id="e95f5-142">O parâmetro ' Workspace ' aceita o valor do tipo ' PSWorkspace ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="e95f5-142">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

## <span data-ttu-id="e95f5-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e95f5-143">OUTPUTS</span></span>

### <span data-ttu-id="e95f5-144">System. Collections. Generic. List ' 1 [Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource]</span><span class="sxs-lookup"><span data-stu-id="e95f5-144">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource]</span></span>

### <span data-ttu-id="e95f5-145">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="e95f5-145">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="e95f5-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e95f5-146">NOTES</span></span>
* <span data-ttu-id="e95f5-147">Palavras-chave: Azure, azurerm, ARM, Resource, Management, Manager, Operational, insights</span><span class="sxs-lookup"><span data-stu-id="e95f5-147">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="e95f5-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e95f5-148">RELATED LINKS</span></span>

[<span data-ttu-id="e95f5-149">Remove-AzureRmOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="e95f5-149">Remove-AzureRmOperationalInsightsDataSource</span></span>](./Remove-AzureRmOperationalInsightsDataSource.md)

[<span data-ttu-id="e95f5-150">Set-AzureRmOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="e95f5-150">Set-AzureRmOperationalInsightsDataSource</span></span>](./Set-AzureRmOperationalInsightsDataSource.md)


