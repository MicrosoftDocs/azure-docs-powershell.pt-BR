---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 010328F9-C878-4F16-AFD7-2135465A1968
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/set-azoperationalinsightsstorageinsight
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsStorageInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsStorageInsight.md
ms.openlocfilehash: 53482eade80e1fdc3d719160185941741e447258
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113391"
---
# <span data-ttu-id="96c2d-101">Set-AzOperationalInsightsStorageInsight</span><span class="sxs-lookup"><span data-stu-id="96c2d-101">Set-AzOperationalInsightsStorageInsight</span></span>

## <span data-ttu-id="96c2d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="96c2d-102">SYNOPSIS</span></span>
<span data-ttu-id="96c2d-103">Atualiza um Insights de Armazenamento.</span><span class="sxs-lookup"><span data-stu-id="96c2d-103">Updates a Storage Insight.</span></span>

## <span data-ttu-id="96c2d-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="96c2d-104">SYNTAX</span></span>

### <span data-ttu-id="96c2d-105">ByWorkspaceName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="96c2d-105">ByWorkspaceName (Default)</span></span>
```
Set-AzOperationalInsightsStorageInsight [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [[-StorageAccountKey] <String>] [[-Tables] <String[]>] [[-Containers] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="96c2d-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="96c2d-106">ByWorkspaceObject</span></span>
```
Set-AzOperationalInsightsStorageInsight [-Workspace] <PSWorkspace> [-Name] <String>
 [[-StorageAccountKey] <String>] [[-Tables] <String[]>] [[-Containers] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="96c2d-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="96c2d-107">DESCRIPTION</span></span>
<span data-ttu-id="96c2d-108">O cmdlet **Set-AzOperationalInsightsStorageInsight** altera a configuração de um Insight de Armazenamento.</span><span class="sxs-lookup"><span data-stu-id="96c2d-108">The **Set-AzOperationalInsightsStorageInsight** cmdlet changes the configuration of a Storage Insight.</span></span>

## <span data-ttu-id="96c2d-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="96c2d-109">EXAMPLES</span></span>

### <span data-ttu-id="96c2d-110">Exemplo 1: Modificar uma Visão de Armazenamento por nome</span><span class="sxs-lookup"><span data-stu-id="96c2d-110">Example 1: Modify a Storage Insight by name</span></span>
```
PS C:\>Set-AzOperationalInsightsStorageInsight -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "MyWorkspace" -Name "MyStorageInsight" -Tables @("WADWindowsEventLogsTable")
```

<span data-ttu-id="96c2d-111">Esse comando modifica as tabelas das quais o Insights de Armazenamento chamado MyStorageInsight lê.</span><span class="sxs-lookup"><span data-stu-id="96c2d-111">This command modifies the tables from which the Storage Insight named MyStorageInsight reads.</span></span>

### <span data-ttu-id="96c2d-112">Exemplo 2: Modificar uma Visão de Armazenamento usando um objeto de espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="96c2d-112">Example 2: Modify a Storage Insight by using a workspace object</span></span>
```
PS C:\>$Workspace = Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"

PS C:\>Set-AzOperationalInsightsStorageInsight -Workspace $Workspace -Name "MyStorageInsight" -Containers @("wad-iis-logfiles")
```

<span data-ttu-id="96c2d-113">O primeiro comando usa o cmdlet Get-AzOperationalInsightsWorkspace para obter o espaço de trabalho chamado MyWorkspace e, em seguida, armazena-o na variável $Workspace dados.</span><span class="sxs-lookup"><span data-stu-id="96c2d-113">The first command uses the Get-AzOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkspace, and then stores it in the $Workspace variable.</span></span>
<span data-ttu-id="96c2d-114">O segundo comando modifica os contêineres dos quais o Insights de Armazenamento chamado MyStorageInsight lê.</span><span class="sxs-lookup"><span data-stu-id="96c2d-114">The second command modifies the containers from which the Storage Insight named MyStorageInsight reads.</span></span>

## <span data-ttu-id="96c2d-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="96c2d-115">PARAMETERS</span></span>

### <span data-ttu-id="96c2d-116">-Contêineres</span><span class="sxs-lookup"><span data-stu-id="96c2d-116">-Containers</span></span>
<span data-ttu-id="96c2d-117">Especifica a lista de contêineres que fornecem os dados.</span><span class="sxs-lookup"><span data-stu-id="96c2d-117">Specifies the list of containers that provide the data.</span></span>

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

### <span data-ttu-id="96c2d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96c2d-118">-DefaultProfile</span></span>
<span data-ttu-id="96c2d-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="96c2d-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="96c2d-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="96c2d-120">-Name</span></span>
<span data-ttu-id="96c2d-121">Especifica o nome de uma Visão de Armazenamento.</span><span class="sxs-lookup"><span data-stu-id="96c2d-121">Specifies the name of a Storage Insight.</span></span>

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

### <span data-ttu-id="96c2d-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="96c2d-122">-ResourceGroupName</span></span>
<span data-ttu-id="96c2d-123">Especifica o nome de um grupo de recursos do Azure que contém um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="96c2d-123">Specifies the name of an Azure resource group that contains a workspace.</span></span>

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

### <span data-ttu-id="96c2d-124">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="96c2d-124">-StorageAccountKey</span></span>
<span data-ttu-id="96c2d-125">Especifica a chave de acesso para a conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="96c2d-125">Specifies the access key for the storage account.</span></span>

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

### <span data-ttu-id="96c2d-126">-Tabelas</span><span class="sxs-lookup"><span data-stu-id="96c2d-126">-Tables</span></span>
<span data-ttu-id="96c2d-127">Especifica a lista de tabelas que contêm os dados.</span><span class="sxs-lookup"><span data-stu-id="96c2d-127">Specifies the list of tables that contain the data.</span></span>

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

### <span data-ttu-id="96c2d-128">-Espaço de Trabalho</span><span class="sxs-lookup"><span data-stu-id="96c2d-128">-Workspace</span></span>
<span data-ttu-id="96c2d-129">Especifica o espaço de trabalho que contém o Insights de Armazenamento.</span><span class="sxs-lookup"><span data-stu-id="96c2d-129">Specifies the workspace that contains the Storage Insight.</span></span>

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

### <span data-ttu-id="96c2d-130">-NomedoEspacial de Trabalho</span><span class="sxs-lookup"><span data-stu-id="96c2d-130">-WorkspaceName</span></span>
<span data-ttu-id="96c2d-131">Especifica o nome de um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="96c2d-131">Specifies the name of a workspace.</span></span>

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

### <span data-ttu-id="96c2d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96c2d-132">CommonParameters</span></span>
<span data-ttu-id="96c2d-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="96c2d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96c2d-134">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="96c2d-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96c2d-135">Entradas</span><span class="sxs-lookup"><span data-stu-id="96c2d-135">INPUTS</span></span>

### <span data-ttu-id="96c2d-136">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="96c2d-136">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="96c2d-137">System.String</span><span class="sxs-lookup"><span data-stu-id="96c2d-137">System.String</span></span>

### <span data-ttu-id="96c2d-138">System.String[]</span><span class="sxs-lookup"><span data-stu-id="96c2d-138">System.String[]</span></span>

## <span data-ttu-id="96c2d-139">Saídas</span><span class="sxs-lookup"><span data-stu-id="96c2d-139">OUTPUTS</span></span>

### <span data-ttu-id="96c2d-140">Microsoft.Azure.Commands.OperationalInsights.Models.PSStorageInsight</span><span class="sxs-lookup"><span data-stu-id="96c2d-140">Microsoft.Azure.Commands.OperationalInsights.Models.PSStorageInsight</span></span>

## <span data-ttu-id="96c2d-141">Notas</span><span class="sxs-lookup"><span data-stu-id="96c2d-141">NOTES</span></span>

## <span data-ttu-id="96c2d-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="96c2d-142">RELATED LINKS</span></span>

[<span data-ttu-id="96c2d-143">Cmdlets de Insights Operacionais do Azure</span><span class="sxs-lookup"><span data-stu-id="96c2d-143">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)

[<span data-ttu-id="96c2d-144">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="96c2d-144">Get-AzOperationalInsightsWorkspace</span></span>](./Get-AzOperationalInsightsWorkspace.md)


