---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 010328F9-C878-4F16-AFD7-2135465A1968
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/set-azoperationalinsightsstorageinsight
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsStorageInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsStorageInsight.md
ms.openlocfilehash: c2a622b110bdc17fe325934b50c59ac7e9b8f3ee
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890186"
---
# <span data-ttu-id="f7c44-101">Set-AzOperationalInsightsStorageInsight</span><span class="sxs-lookup"><span data-stu-id="f7c44-101">Set-AzOperationalInsightsStorageInsight</span></span>

## <span data-ttu-id="f7c44-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f7c44-102">SYNOPSIS</span></span>
<span data-ttu-id="f7c44-103">Atualiza um Storage Insight.</span><span class="sxs-lookup"><span data-stu-id="f7c44-103">Updates a Storage Insight.</span></span>

## <span data-ttu-id="f7c44-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="f7c44-104">SYNTAX</span></span>

### <span data-ttu-id="f7c44-105">ByWorkspaceName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="f7c44-105">ByWorkspaceName (Default)</span></span>
```
Set-AzOperationalInsightsStorageInsight [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [[-StorageAccountKey] <String>] [[-Tables] <String[]>] [[-Containers] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f7c44-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="f7c44-106">ByWorkspaceObject</span></span>
```
Set-AzOperationalInsightsStorageInsight [-Workspace] <PSWorkspace> [-Name] <String>
 [[-StorageAccountKey] <String>] [[-Tables] <String[]>] [[-Containers] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f7c44-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="f7c44-107">DESCRIPTION</span></span>
<span data-ttu-id="f7c44-108">O cmdlet **Set-AzOperationalInsightsStorageInsight** altera a configuração de um Storage Insight.</span><span class="sxs-lookup"><span data-stu-id="f7c44-108">The **Set-AzOperationalInsightsStorageInsight** cmdlet changes the configuration of a Storage Insight.</span></span>

## <span data-ttu-id="f7c44-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f7c44-109">EXAMPLES</span></span>

### <span data-ttu-id="f7c44-110">Exemplo 1: Modificar um Insight de Armazenamento pelo nome</span><span class="sxs-lookup"><span data-stu-id="f7c44-110">Example 1: Modify a Storage Insight by name</span></span>
```
PS C:\>Set-AzOperationalInsightsStorageInsight -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "MyWorkspace" -Name "MyStorageInsight" -Tables @("WADWindowsEventLogsTable")
```

<span data-ttu-id="f7c44-111">Este comando modifica as tabelas das quais o Storage Insight chamado MyStorageInsight lê.</span><span class="sxs-lookup"><span data-stu-id="f7c44-111">This command modifies the tables from which the Storage Insight named MyStorageInsight reads.</span></span>

### <span data-ttu-id="f7c44-112">Exemplo 2: Modificar uma Visão de Armazenamento usando um objeto workspace</span><span class="sxs-lookup"><span data-stu-id="f7c44-112">Example 2: Modify a Storage Insight by using a workspace object</span></span>
```
PS C:\>$Workspace = Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"

PS C:\>Set-AzOperationalInsightsStorageInsight -Workspace $Workspace -Name "MyStorageInsight" -Containers @("wad-iis-logfiles")
```

<span data-ttu-id="f7c44-113">O primeiro comando usa o cmdlet Get-AzOperationalInsightsWorkspace para obter o espaço de trabalho chamado MyWorkspace e, em seguida, o armazena na variável $Workspace.</span><span class="sxs-lookup"><span data-stu-id="f7c44-113">The first command uses the Get-AzOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkspace, and then stores it in the $Workspace variable.</span></span>
<span data-ttu-id="f7c44-114">O segundo comando modifica os contêineres dos quais o Storage Insight chamado MyStorageInsight lê.</span><span class="sxs-lookup"><span data-stu-id="f7c44-114">The second command modifies the containers from which the Storage Insight named MyStorageInsight reads.</span></span>

## <span data-ttu-id="f7c44-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="f7c44-115">PARAMETERS</span></span>

### <span data-ttu-id="f7c44-116">-Containers</span><span class="sxs-lookup"><span data-stu-id="f7c44-116">-Containers</span></span>
<span data-ttu-id="f7c44-117">Especifica a lista de contêineres que fornecem os dados.</span><span class="sxs-lookup"><span data-stu-id="f7c44-117">Specifies the list of containers that provide the data.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7c44-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7c44-118">-DefaultProfile</span></span>
<span data-ttu-id="f7c44-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="f7c44-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f7c44-120">-Name</span><span class="sxs-lookup"><span data-stu-id="f7c44-120">-Name</span></span>
<span data-ttu-id="f7c44-121">Especifica o nome de um Storage Insight.</span><span class="sxs-lookup"><span data-stu-id="f7c44-121">Specifies the name of a Storage Insight.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7c44-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7c44-122">-ResourceGroupName</span></span>
<span data-ttu-id="f7c44-123">Especifica o nome de um grupo de recursos do Azure que contém um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="f7c44-123">Specifies the name of an Azure resource group that contains a workspace.</span></span>

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

### <span data-ttu-id="f7c44-124">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="f7c44-124">-StorageAccountKey</span></span>
<span data-ttu-id="f7c44-125">Especifica a chave de acesso para a conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="f7c44-125">Specifies the access key for the storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7c44-126">-Tables</span><span class="sxs-lookup"><span data-stu-id="f7c44-126">-Tables</span></span>
<span data-ttu-id="f7c44-127">Especifica a lista de tabelas que contêm os dados.</span><span class="sxs-lookup"><span data-stu-id="f7c44-127">Specifies the list of tables that contain the data.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7c44-128">-Workspace</span><span class="sxs-lookup"><span data-stu-id="f7c44-128">-Workspace</span></span>
<span data-ttu-id="f7c44-129">Especifica o espaço de trabalho que contém o Storage Insight.</span><span class="sxs-lookup"><span data-stu-id="f7c44-129">Specifies the workspace that contains the Storage Insight.</span></span>

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

### <span data-ttu-id="f7c44-130">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="f7c44-130">-WorkspaceName</span></span>
<span data-ttu-id="f7c44-131">Especifica o nome de um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="f7c44-131">Specifies the name of a workspace.</span></span>

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

### <span data-ttu-id="f7c44-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7c44-132">CommonParameters</span></span>
<span data-ttu-id="f7c44-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7c44-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7c44-134">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f7c44-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7c44-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f7c44-135">INPUTS</span></span>

### <span data-ttu-id="f7c44-136">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="f7c44-136">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="f7c44-137">System.String</span><span class="sxs-lookup"><span data-stu-id="f7c44-137">System.String</span></span>

### <span data-ttu-id="f7c44-138">System.String[]</span><span class="sxs-lookup"><span data-stu-id="f7c44-138">System.String[]</span></span>

## <span data-ttu-id="f7c44-139">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="f7c44-139">OUTPUTS</span></span>

### <span data-ttu-id="f7c44-140">Microsoft.Azure.Commands.OperationalInsights.Models.PSStorageInsight</span><span class="sxs-lookup"><span data-stu-id="f7c44-140">Microsoft.Azure.Commands.OperationalInsights.Models.PSStorageInsight</span></span>

## <span data-ttu-id="f7c44-141">NOTES</span><span class="sxs-lookup"><span data-stu-id="f7c44-141">NOTES</span></span>

## <span data-ttu-id="f7c44-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f7c44-142">RELATED LINKS</span></span>

[<span data-ttu-id="f7c44-143">Cmdlets do Insights Operacionais do Azure</span><span class="sxs-lookup"><span data-stu-id="f7c44-143">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)

[<span data-ttu-id="f7c44-144">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="f7c44-144">Get-AzOperationalInsightsWorkspace</span></span>](./Get-AzOperationalInsightsWorkspace.md)


