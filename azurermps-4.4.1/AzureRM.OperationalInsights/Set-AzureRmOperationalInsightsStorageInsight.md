---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 010328F9-C878-4F16-AFD7-2135465A1968
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Set-AzureRmOperationalInsightsStorageInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Set-AzureRmOperationalInsightsStorageInsight.md
ms.openlocfilehash: 85c85be195df2dfa393cbd4d91ae62d8731dbf93
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610196"
---
# <span data-ttu-id="0dc31-101">Set-AzureRmOperationalInsightsStorageInsight</span><span class="sxs-lookup"><span data-stu-id="0dc31-101">Set-AzureRmOperationalInsightsStorageInsight</span></span>

## <span data-ttu-id="0dc31-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0dc31-102">SYNOPSIS</span></span>
<span data-ttu-id="0dc31-103">Atualiza uma percepção do armazenamento.</span><span class="sxs-lookup"><span data-stu-id="0dc31-103">Updates a Storage Insight.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0dc31-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0dc31-104">SYNTAX</span></span>

### <span data-ttu-id="0dc31-105">ByWorkspaceName (padrão)</span><span class="sxs-lookup"><span data-stu-id="0dc31-105">ByWorkspaceName (Default)</span></span>
```
Set-AzureRmOperationalInsightsStorageInsight [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [[-StorageAccountKey] <String>] [[-Tables] <String[]>] [[-Containers] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0dc31-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="0dc31-106">ByWorkspaceObject</span></span>
```
Set-AzureRmOperationalInsightsStorageInsight [-Workspace] <PSWorkspace> [-Name] <String>
 [[-StorageAccountKey] <String>] [[-Tables] <String[]>] [[-Containers] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0dc31-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0dc31-107">DESCRIPTION</span></span>
<span data-ttu-id="0dc31-108">O cmdlet **set-AzureRmOperationalInsightsStorageInsight** altera a configuração de uma percepção do armazenamento.</span><span class="sxs-lookup"><span data-stu-id="0dc31-108">The **Set-AzureRmOperationalInsightsStorageInsight** cmdlet changes the configuration of a Storage Insight.</span></span>

## <span data-ttu-id="0dc31-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0dc31-109">EXAMPLES</span></span>

### <span data-ttu-id="0dc31-110">Exemplo 1: modificar uma visão do armazenamento por nome</span><span class="sxs-lookup"><span data-stu-id="0dc31-110">Example 1: Modify a Storage Insight by name</span></span>
```
PS C:\>Set-AzureRmOperationalInsightsStorageInsight -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "MyWorkspace" -Name "MyStorageInsight" -Tables @("WADWindowsEventLogsTable")
```

<span data-ttu-id="0dc31-111">Esse comando modifica as tabelas das quais a percepção do armazenamento chamada MyStorageInsight lê.</span><span class="sxs-lookup"><span data-stu-id="0dc31-111">This command modifies the tables from which the Storage Insight named MyStorageInsight reads.</span></span>

### <span data-ttu-id="0dc31-112">Exemplo 2: modificar uma visão do armazenamento usando um objeto do espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="0dc31-112">Example 2: Modify a Storage Insight by using a workspace object</span></span>
```
PS C:\>$Workspace = Get-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"

PS C:\>Set-AzureRmOperationalInsightsStorageInsight -Workspace $Workspace -Name "MyStorageInsight" -Containers @("wad-iis-logfiles")
```

<span data-ttu-id="0dc31-113">O primeiro comando usa o cmdlet Get-AzureRmOperationalInsightsWorkspace para obter o espaço de trabalho chamado MyWorkspace e, em seguida, armazena-o na variável $Workspace.</span><span class="sxs-lookup"><span data-stu-id="0dc31-113">The first command uses the Get-AzureRmOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkspace, and then stores it in the $Workspace variable.</span></span>

<span data-ttu-id="0dc31-114">O segundo comando modifica os contêineres dos quais a percepção do armazenamento chamada MyStorageInsight lê.</span><span class="sxs-lookup"><span data-stu-id="0dc31-114">The second command modifies the containers from which the Storage Insight named MyStorageInsight reads.</span></span>

## <span data-ttu-id="0dc31-115">OS</span><span class="sxs-lookup"><span data-stu-id="0dc31-115">PARAMETERS</span></span>

### <span data-ttu-id="0dc31-116">-Contêineres</span><span class="sxs-lookup"><span data-stu-id="0dc31-116">-Containers</span></span>
<span data-ttu-id="0dc31-117">Especifica a lista de contêineres que fornecem os dados.</span><span class="sxs-lookup"><span data-stu-id="0dc31-117">Specifies the list of containers that provide the data.</span></span>

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

### <span data-ttu-id="0dc31-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="0dc31-118">-Name</span></span>
<span data-ttu-id="0dc31-119">Especifica o nome de uma informação sobre o armazenamento.</span><span class="sxs-lookup"><span data-stu-id="0dc31-119">Specifies the name of a Storage Insight.</span></span>

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

### <span data-ttu-id="0dc31-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0dc31-120">-ResourceGroupName</span></span>
<span data-ttu-id="0dc31-121">Especifica o nome de um grupo de recursos do Azure que contém um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="0dc31-121">Specifies the name of an Azure resource group that contains a workspace.</span></span>

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

### <span data-ttu-id="0dc31-122">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="0dc31-122">-StorageAccountKey</span></span>
<span data-ttu-id="0dc31-123">Especifica a tecla de acesso para a conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="0dc31-123">Specifies the access key for the storage account.</span></span>

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

### <span data-ttu-id="0dc31-124">-Tabelas</span><span class="sxs-lookup"><span data-stu-id="0dc31-124">-Tables</span></span>
<span data-ttu-id="0dc31-125">Especifica a lista de tabelas que contêm os dados.</span><span class="sxs-lookup"><span data-stu-id="0dc31-125">Specifies the list of tables that contain the data.</span></span>

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

### <span data-ttu-id="0dc31-126">-Espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="0dc31-126">-Workspace</span></span>
<span data-ttu-id="0dc31-127">Especifica o espaço de trabalho que contém a percepção do armazenamento.</span><span class="sxs-lookup"><span data-stu-id="0dc31-127">Specifies the workspace that contains the Storage Insight.</span></span>

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

### <span data-ttu-id="0dc31-128">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="0dc31-128">-WorkspaceName</span></span>
<span data-ttu-id="0dc31-129">Especifica o nome de um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="0dc31-129">Specifies the name of a workspace.</span></span>

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

### <span data-ttu-id="0dc31-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0dc31-130">-DefaultProfile</span></span>
<span data-ttu-id="0dc31-131">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0dc31-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0dc31-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0dc31-132">CommonParameters</span></span>
<span data-ttu-id="0dc31-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0dc31-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0dc31-134">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0dc31-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0dc31-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0dc31-135">INPUTS</span></span>

### <span data-ttu-id="0dc31-136">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="0dc31-136">PSWorkspace</span></span>
<span data-ttu-id="0dc31-137">O parâmetro ' Workspace ' aceita o valor do tipo ' PSWorkspace ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="0dc31-137">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

## <span data-ttu-id="0dc31-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0dc31-138">OUTPUTS</span></span>

### <span data-ttu-id="0dc31-139">Microsoft. Azure. Commands. OperationalInsights. Models. PSStorageInsight</span><span class="sxs-lookup"><span data-stu-id="0dc31-139">Microsoft.Azure.Commands.OperationalInsights.Models.PSStorageInsight</span></span>

## <span data-ttu-id="0dc31-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0dc31-140">NOTES</span></span>

## <span data-ttu-id="0dc31-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0dc31-141">RELATED LINKS</span></span>

[<span data-ttu-id="0dc31-142">Cmdlets do Azure Operational insights</span><span class="sxs-lookup"><span data-stu-id="0dc31-142">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)

[<span data-ttu-id="0dc31-143">Get-AzureRmOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="0dc31-143">Get-AzureRmOperationalInsightsWorkspace</span></span>](./Get-AzureRmOperationalInsightsWorkspace.md)


