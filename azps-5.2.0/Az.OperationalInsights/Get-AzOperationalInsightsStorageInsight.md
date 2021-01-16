---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 29ABCC1B-8590-4243-A629-709F207927B4
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsstorageinsight
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsStorageInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsStorageInsight.md
ms.openlocfilehash: a89b4210fcd498aca3a25451e6f691df20d5510e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98259594"
---
# <span data-ttu-id="fedac-101">Get-AzOperationalInsightsStorageInsight</span><span class="sxs-lookup"><span data-stu-id="fedac-101">Get-AzOperationalInsightsStorageInsight</span></span>

## <span data-ttu-id="fedac-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fedac-102">SYNOPSIS</span></span>
<span data-ttu-id="fedac-103">Obtém informações sobre uma informação sobre o armazenamento.</span><span class="sxs-lookup"><span data-stu-id="fedac-103">Gets information about a Storage Insight.</span></span>

## <span data-ttu-id="fedac-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fedac-104">SYNTAX</span></span>

### <span data-ttu-id="fedac-105">ByWorkspaceName (padrão)</span><span class="sxs-lookup"><span data-stu-id="fedac-105">ByWorkspaceName (Default)</span></span>
```
Get-AzOperationalInsightsStorageInsight [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fedac-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="fedac-106">ByWorkspaceObject</span></span>
```
Get-AzOperationalInsightsStorageInsight [-Workspace] <PSWorkspace> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fedac-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fedac-107">DESCRIPTION</span></span>
<span data-ttu-id="fedac-108">O cmdlet **Get-AzOperationalInsightsStorageInsight** Obtém informações sobre uma visão de armazenamento existente.</span><span class="sxs-lookup"><span data-stu-id="fedac-108">The **Get-AzOperationalInsightsStorageInsight** cmdlet gets information about an existing Storage Insight.</span></span>
<span data-ttu-id="fedac-109">Se um nome de informação do armazenamento for especificado, esse cmdlet obterá informações sobre essa informação sobre o armazenamento.</span><span class="sxs-lookup"><span data-stu-id="fedac-109">If a Storage Insight name is specified, this cmdlet gets information about that Storage Insight.</span></span>
<span data-ttu-id="fedac-110">Se você não especificar um nome, esse cmdlet obterá informações sobre todas as informações de armazenamento em um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="fedac-110">If you do not specify a name, this cmdlet gets information about all storage insights in a workspace.</span></span>

## <span data-ttu-id="fedac-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fedac-111">EXAMPLES</span></span>

### <span data-ttu-id="fedac-112">Exemplo 1: obter uma visão geral do armazenamento por nome</span><span class="sxs-lookup"><span data-stu-id="fedac-112">Example 1: Get a Storage Insight by name</span></span>
```
PS C:\>Get-AzOperationalInsightsStorageInsight -Name "MyStorageInsight" -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```

<span data-ttu-id="fedac-113">Esse comando obtém a percepção do armazenamento chamada MyStorageInsight do espaço de trabalho chamado ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="fedac-113">This command gets the storage insight named MyStorageInsight from the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="fedac-114">Exemplo 2: obter uma visão geral do armazenamento usando um objeto do espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="fedac-114">Example 2: Get a Storage Insight by using a workspace object</span></span>
```
PS C:\>$Workspace = Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"
PS C:\>Get-AzOperationalInsightsStorageInsight -Workspace $Workspace -Name "MyStorageInsight"
```

<span data-ttu-id="fedac-115">O primeiro comando usa o cmdlet **Get-AzOperationalInsightsWorkspace** para obter um espaço de trabalho de insights operacionais e, em seguida, armazena-o na variável $Workspace.</span><span class="sxs-lookup"><span data-stu-id="fedac-115">The first command uses the **Get-AzOperationalInsightsWorkspace** cmdlet to get an Operational Insights workspace, and then stores it in the $Workspace variable.</span></span>
<span data-ttu-id="fedac-116">O segundo comando obtém a informação do armazenamento chamada MyStorageInsight para o espaço de trabalho em $Workspace.</span><span class="sxs-lookup"><span data-stu-id="fedac-116">The second command gets the storage insight named MyStorageInsight for the workspace in $Workspace.</span></span>

## <span data-ttu-id="fedac-117">OS</span><span class="sxs-lookup"><span data-stu-id="fedac-117">PARAMETERS</span></span>

### <span data-ttu-id="fedac-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fedac-118">-DefaultProfile</span></span>
<span data-ttu-id="fedac-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="fedac-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fedac-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="fedac-120">-Name</span></span>
<span data-ttu-id="fedac-121">Especifica o nome do reconhecimento do armazenamento.</span><span class="sxs-lookup"><span data-stu-id="fedac-121">Specifies the Storage Insight name.</span></span>

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

### <span data-ttu-id="fedac-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fedac-122">-ResourceGroupName</span></span>
<span data-ttu-id="fedac-123">Especifica o nome de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="fedac-123">Specifies the name of an Azure resource group.</span></span>

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

### <span data-ttu-id="fedac-124">-Espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="fedac-124">-Workspace</span></span>
<span data-ttu-id="fedac-125">Especifica o espaço de trabalho que contém as informações de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="fedac-125">Specifies the workspace that contains the Storage Insights.</span></span>

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

### <span data-ttu-id="fedac-126">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="fedac-126">-WorkspaceName</span></span>
<span data-ttu-id="fedac-127">Especifica o nome do espaço de trabalho que contém as informações de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="fedac-127">Specifies the name of the workspace that contains the Storage Insights.</span></span>

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

### <span data-ttu-id="fedac-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fedac-128">CommonParameters</span></span>
<span data-ttu-id="fedac-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fedac-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fedac-130">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fedac-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fedac-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fedac-131">INPUTS</span></span>

### <span data-ttu-id="fedac-132">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="fedac-132">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="fedac-133">System. String</span><span class="sxs-lookup"><span data-stu-id="fedac-133">System.String</span></span>

## <span data-ttu-id="fedac-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fedac-134">OUTPUTS</span></span>

### <span data-ttu-id="fedac-135">Microsoft. Azure. Commands. OperationalInsights. Models. PSStorageInsight</span><span class="sxs-lookup"><span data-stu-id="fedac-135">Microsoft.Azure.Commands.OperationalInsights.Models.PSStorageInsight</span></span>

## <span data-ttu-id="fedac-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fedac-136">NOTES</span></span>

## <span data-ttu-id="fedac-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fedac-137">RELATED LINKS</span></span>

[<span data-ttu-id="fedac-138">Cmdlets do Azure Operational insights</span><span class="sxs-lookup"><span data-stu-id="fedac-138">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)


