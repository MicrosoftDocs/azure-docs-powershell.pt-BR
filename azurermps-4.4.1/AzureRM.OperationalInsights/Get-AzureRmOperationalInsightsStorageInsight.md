---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 29ABCC1B-8590-4243-A629-709F207927B4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsStorageInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsStorageInsight.md
ms.openlocfilehash: cd7dad03d8542685339778d0b0cdac967f83ea21
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93609611"
---
# <span data-ttu-id="a6b02-101">Get-AzureRmOperationalInsightsStorageInsight</span><span class="sxs-lookup"><span data-stu-id="a6b02-101">Get-AzureRmOperationalInsightsStorageInsight</span></span>

## <span data-ttu-id="a6b02-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a6b02-102">SYNOPSIS</span></span>
<span data-ttu-id="a6b02-103">Obtém informações sobre uma informação sobre o armazenamento.</span><span class="sxs-lookup"><span data-stu-id="a6b02-103">Gets information about a Storage Insight.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a6b02-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a6b02-104">SYNTAX</span></span>

### <span data-ttu-id="a6b02-105">ByWorkspaceName (padrão)</span><span class="sxs-lookup"><span data-stu-id="a6b02-105">ByWorkspaceName (Default)</span></span>
```
Get-AzureRmOperationalInsightsStorageInsight [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a6b02-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="a6b02-106">ByWorkspaceObject</span></span>
```
Get-AzureRmOperationalInsightsStorageInsight [-Workspace] <PSWorkspace> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a6b02-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a6b02-107">DESCRIPTION</span></span>
<span data-ttu-id="a6b02-108">O cmdlet **Get-AzureRmOperationalInsightsStorageInsight** Obtém informações sobre uma visão de armazenamento existente.</span><span class="sxs-lookup"><span data-stu-id="a6b02-108">The **Get-AzureRmOperationalInsightsStorageInsight** cmdlet gets information about an existing Storage Insight.</span></span>
<span data-ttu-id="a6b02-109">Se um nome de informação do armazenamento for especificado, esse cmdlet obterá informações sobre essa informação sobre o armazenamento.</span><span class="sxs-lookup"><span data-stu-id="a6b02-109">If a Storage Insight name is specified, this cmdlet gets information about that Storage Insight.</span></span>
<span data-ttu-id="a6b02-110">Se você não especificar um nome, esse cmdlet obterá informações sobre todas as informações de armazenamento em um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="a6b02-110">If you do not specify a name, this cmdlet gets information about all storage insights in a workspace.</span></span>

## <span data-ttu-id="a6b02-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a6b02-111">EXAMPLES</span></span>

### <span data-ttu-id="a6b02-112">Exemplo 1: obter uma visão geral do armazenamento por nome</span><span class="sxs-lookup"><span data-stu-id="a6b02-112">Example 1: Get a Storage Insight by name</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsStorageInsight -Name "MyStorageInsight" -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```

<span data-ttu-id="a6b02-113">Esse comando obtém a percepção do armazenamento chamada MyStorageInsight do espaço de trabalho chamado ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="a6b02-113">This command gets the storage insight named MyStorageInsight from the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="a6b02-114">Exemplo 2: obter uma visão geral do armazenamento usando um objeto do espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="a6b02-114">Example 2: Get a Storage Insight by using a workspace object</span></span>
```
PS C:\>$Workspace = Get-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"
PS C:\>Get-AzureRmOperationalInsightsStorageInsight -Workspace $Workspace -Name "MyStorageInsight"
```

<span data-ttu-id="a6b02-115">O primeiro comando usa o cmdlet **Get-AzureRmOperationalInsightsWorkspace** para obter um espaço de trabalho de insights operacionais e, em seguida, armazena-o na variável $Workspace.</span><span class="sxs-lookup"><span data-stu-id="a6b02-115">The first command uses the **Get-AzureRmOperationalInsightsWorkspace** cmdlet to get an Operational Insights workspace, and then stores it in the $Workspace variable.</span></span>

<span data-ttu-id="a6b02-116">O segundo comando obtém a informação do armazenamento chamada MyStorageInsight para o espaço de trabalho em $Workspace.</span><span class="sxs-lookup"><span data-stu-id="a6b02-116">The second command gets the storage insight named MyStorageInsight for the workspace in $Workspace.</span></span>

## <span data-ttu-id="a6b02-117">OS</span><span class="sxs-lookup"><span data-stu-id="a6b02-117">PARAMETERS</span></span>

### <span data-ttu-id="a6b02-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="a6b02-118">-Name</span></span>
<span data-ttu-id="a6b02-119">Especifica o nome do reconhecimento do armazenamento.</span><span class="sxs-lookup"><span data-stu-id="a6b02-119">Specifies the Storage Insight name.</span></span>

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

### <span data-ttu-id="a6b02-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6b02-120">-ResourceGroupName</span></span>
<span data-ttu-id="a6b02-121">Especifica o nome de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="a6b02-121">Specifies the name of an Azure resource group.</span></span>

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

### <span data-ttu-id="a6b02-122">-Espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="a6b02-122">-Workspace</span></span>
<span data-ttu-id="a6b02-123">Especifica o espaço de trabalho que contém as informações de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="a6b02-123">Specifies the workspace that contains the Storage Insights.</span></span>

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

### <span data-ttu-id="a6b02-124">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="a6b02-124">-WorkspaceName</span></span>
<span data-ttu-id="a6b02-125">Especifica o nome do espaço de trabalho que contém as informações de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="a6b02-125">Specifies the name of the workspace that contains the Storage Insights.</span></span>

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

### <span data-ttu-id="a6b02-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6b02-126">-DefaultProfile</span></span>
<span data-ttu-id="a6b02-127">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a6b02-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a6b02-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6b02-128">CommonParameters</span></span>
<span data-ttu-id="a6b02-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6b02-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6b02-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a6b02-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6b02-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a6b02-131">INPUTS</span></span>

### <span data-ttu-id="a6b02-132">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="a6b02-132">PSWorkspace</span></span>
<span data-ttu-id="a6b02-133">O parâmetro ' Workspace ' aceita o valor do tipo ' PSWorkspace ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="a6b02-133">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

## <span data-ttu-id="a6b02-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a6b02-134">OUTPUTS</span></span>

### <span data-ttu-id="a6b02-135">System. Collections. Generic. List ' 1 [Microsoft. Azure. Commands. OperationalInsights. Models. PSStorageInsight]</span><span class="sxs-lookup"><span data-stu-id="a6b02-135">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.OperationalInsights.Models.PSStorageInsight]</span></span>

### <span data-ttu-id="a6b02-136">Microsoft. Azure. Commands. OperationalInsights. Models. PSStorageInsight</span><span class="sxs-lookup"><span data-stu-id="a6b02-136">Microsoft.Azure.Commands.OperationalInsights.Models.PSStorageInsight</span></span>

## <span data-ttu-id="a6b02-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a6b02-137">NOTES</span></span>

## <span data-ttu-id="a6b02-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a6b02-138">RELATED LINKS</span></span>

[<span data-ttu-id="a6b02-139">Cmdlets do Azure Operational insights</span><span class="sxs-lookup"><span data-stu-id="a6b02-139">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)


