---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 29ABCC1B-8590-4243-A629-709F207927B4
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/get-azoperationalinsightsstorageinsight
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsStorageInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsStorageInsight.md
ms.openlocfilehash: adbe725557ccf1535a83f5f411cfdc44fd69c6a2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889097"
---
# <span data-ttu-id="bbf50-101">Get-AzOperationalInsightsStorageInsight</span><span class="sxs-lookup"><span data-stu-id="bbf50-101">Get-AzOperationalInsightsStorageInsight</span></span>

## <span data-ttu-id="bbf50-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bbf50-102">SYNOPSIS</span></span>
<span data-ttu-id="bbf50-103">Obtém informações sobre um Storage Insight.</span><span class="sxs-lookup"><span data-stu-id="bbf50-103">Gets information about a Storage Insight.</span></span>

## <span data-ttu-id="bbf50-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="bbf50-104">SYNTAX</span></span>

### <span data-ttu-id="bbf50-105">ByWorkspaceName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="bbf50-105">ByWorkspaceName (Default)</span></span>
```
Get-AzOperationalInsightsStorageInsight [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bbf50-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="bbf50-106">ByWorkspaceObject</span></span>
```
Get-AzOperationalInsightsStorageInsight [-Workspace] <PSWorkspace> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bbf50-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="bbf50-107">DESCRIPTION</span></span>
<span data-ttu-id="bbf50-108">O cmdlet **Get-AzOperationalInsightsStorageInsight** obtém informações sobre um Insight de armazenamento existente.</span><span class="sxs-lookup"><span data-stu-id="bbf50-108">The **Get-AzOperationalInsightsStorageInsight** cmdlet gets information about an existing Storage Insight.</span></span>
<span data-ttu-id="bbf50-109">Se um nome do Storage Insight for especificado, esse cmdlet obterá informações sobre esse Storage Insight.</span><span class="sxs-lookup"><span data-stu-id="bbf50-109">If a Storage Insight name is specified, this cmdlet gets information about that Storage Insight.</span></span>
<span data-ttu-id="bbf50-110">Se você não especificar um nome, este cmdlet obterá informações sobre todas as informações de armazenamento em um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="bbf50-110">If you do not specify a name, this cmdlet gets information about all storage insights in a workspace.</span></span>

## <span data-ttu-id="bbf50-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bbf50-111">EXAMPLES</span></span>

### <span data-ttu-id="bbf50-112">Exemplo 1: Obter um Insight de Armazenamento pelo nome</span><span class="sxs-lookup"><span data-stu-id="bbf50-112">Example 1: Get a Storage Insight by name</span></span>
```
PS C:\>Get-AzOperationalInsightsStorageInsight -Name "MyStorageInsight" -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```

<span data-ttu-id="bbf50-113">Este comando obtém o insight de armazenamento chamado MyStorageInsight do espaço de trabalho chamado ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="bbf50-113">This command gets the storage insight named MyStorageInsight from the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="bbf50-114">Exemplo 2: Obter uma Visão de Armazenamento usando um objeto workspace</span><span class="sxs-lookup"><span data-stu-id="bbf50-114">Example 2: Get a Storage Insight by using a workspace object</span></span>
```
PS C:\>$Workspace = Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"
PS C:\>Get-AzOperationalInsightsStorageInsight -Workspace $Workspace -Name "MyStorageInsight"
```

<span data-ttu-id="bbf50-115">O primeiro comando usa o cmdlet **Get-AzOperationalInsightsWorkspace** para obter um espaço de trabalho de Insights Operacionais e, em seguida, o armazena na variável $Workspace.</span><span class="sxs-lookup"><span data-stu-id="bbf50-115">The first command uses the **Get-AzOperationalInsightsWorkspace** cmdlet to get an Operational Insights workspace, and then stores it in the $Workspace variable.</span></span>
<span data-ttu-id="bbf50-116">O segundo comando obtém o insight de armazenamento chamado MyStorageInsight para o espaço de trabalho em $Workspace.</span><span class="sxs-lookup"><span data-stu-id="bbf50-116">The second command gets the storage insight named MyStorageInsight for the workspace in $Workspace.</span></span>

## <span data-ttu-id="bbf50-117">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="bbf50-117">PARAMETERS</span></span>

### <span data-ttu-id="bbf50-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bbf50-118">-DefaultProfile</span></span>
<span data-ttu-id="bbf50-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="bbf50-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bbf50-120">-Name</span><span class="sxs-lookup"><span data-stu-id="bbf50-120">-Name</span></span>
<span data-ttu-id="bbf50-121">Especifica o nome do Storage Insight.</span><span class="sxs-lookup"><span data-stu-id="bbf50-121">Specifies the Storage Insight name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bbf50-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bbf50-122">-ResourceGroupName</span></span>
<span data-ttu-id="bbf50-123">Especifica o nome de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="bbf50-123">Specifies the name of an Azure resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bbf50-124">-Workspace</span><span class="sxs-lookup"><span data-stu-id="bbf50-124">-Workspace</span></span>
<span data-ttu-id="bbf50-125">Especifica o espaço de trabalho que contém as Informações de Armazenamento.</span><span class="sxs-lookup"><span data-stu-id="bbf50-125">Specifies the workspace that contains the Storage Insights.</span></span>

```yaml
Type: Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace
Parameter Sets: ByWorkspaceObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bbf50-126">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="bbf50-126">-WorkspaceName</span></span>
<span data-ttu-id="bbf50-127">Especifica o nome do espaço de trabalho que contém o Storage Insights.</span><span class="sxs-lookup"><span data-stu-id="bbf50-127">Specifies the name of the workspace that contains the Storage Insights.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bbf50-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bbf50-128">CommonParameters</span></span>
<span data-ttu-id="bbf50-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bbf50-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bbf50-130">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bbf50-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bbf50-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bbf50-131">INPUTS</span></span>

### <span data-ttu-id="bbf50-132">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="bbf50-132">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="bbf50-133">System.String</span><span class="sxs-lookup"><span data-stu-id="bbf50-133">System.String</span></span>

## <span data-ttu-id="bbf50-134">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="bbf50-134">OUTPUTS</span></span>

### <span data-ttu-id="bbf50-135">Microsoft.Azure.Commands.OperationalInsights.Models.PSStorageInsight</span><span class="sxs-lookup"><span data-stu-id="bbf50-135">Microsoft.Azure.Commands.OperationalInsights.Models.PSStorageInsight</span></span>

## <span data-ttu-id="bbf50-136">NOTES</span><span class="sxs-lookup"><span data-stu-id="bbf50-136">NOTES</span></span>

## <span data-ttu-id="bbf50-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bbf50-137">RELATED LINKS</span></span>

[<span data-ttu-id="bbf50-138">Cmdlets do Insights Operacionais do Azure</span><span class="sxs-lookup"><span data-stu-id="bbf50-138">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)


