---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 010328F9-C878-4F16-AFD7-2135465A1968
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/set-azurermoperationalinsightsstorageinsight
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Set-AzureRmOperationalInsightsStorageInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Set-AzureRmOperationalInsightsStorageInsight.md
ms.openlocfilehash: 9eb2b145f6a5968f460ba9a9506a4e0956793d01
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428130"
---
# <span data-ttu-id="eabb8-101">Set-AzureRmOperationalInsightsStorageInsight</span><span class="sxs-lookup"><span data-stu-id="eabb8-101">Set-AzureRmOperationalInsightsStorageInsight</span></span>

## <span data-ttu-id="eabb8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="eabb8-102">SYNOPSIS</span></span>
<span data-ttu-id="eabb8-103">Atualiza uma percepção do armazenamento.</span><span class="sxs-lookup"><span data-stu-id="eabb8-103">Updates a Storage Insight.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eabb8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="eabb8-104">SYNTAX</span></span>

### <span data-ttu-id="eabb8-105">ByWorkspaceName (padrão)</span><span class="sxs-lookup"><span data-stu-id="eabb8-105">ByWorkspaceName (Default)</span></span>
```
Set-AzureRmOperationalInsightsStorageInsight [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [[-StorageAccountKey] <String>] [[-Tables] <String[]>] [[-Containers] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eabb8-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="eabb8-106">ByWorkspaceObject</span></span>
```
Set-AzureRmOperationalInsightsStorageInsight [-Workspace] <PSWorkspace> [-Name] <String>
 [[-StorageAccountKey] <String>] [[-Tables] <String[]>] [[-Containers] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eabb8-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="eabb8-107">DESCRIPTION</span></span>
<span data-ttu-id="eabb8-108">O cmdlet **set-AzureRmOperationalInsightsStorageInsight** altera a configuração de uma percepção do armazenamento.</span><span class="sxs-lookup"><span data-stu-id="eabb8-108">The **Set-AzureRmOperationalInsightsStorageInsight** cmdlet changes the configuration of a Storage Insight.</span></span>

## <span data-ttu-id="eabb8-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="eabb8-109">EXAMPLES</span></span>

### <span data-ttu-id="eabb8-110">Exemplo 1: modificar uma visão do armazenamento por nome</span><span class="sxs-lookup"><span data-stu-id="eabb8-110">Example 1: Modify a Storage Insight by name</span></span>
```
PS C:\>Set-AzureRmOperationalInsightsStorageInsight -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "MyWorkspace" -Name "MyStorageInsight" -Tables @("WADWindowsEventLogsTable")
```

<span data-ttu-id="eabb8-111">Esse comando modifica as tabelas das quais a percepção do armazenamento chamada MyStorageInsight lê.</span><span class="sxs-lookup"><span data-stu-id="eabb8-111">This command modifies the tables from which the Storage Insight named MyStorageInsight reads.</span></span>

### <span data-ttu-id="eabb8-112">Exemplo 2: modificar uma visão do armazenamento usando um objeto do espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="eabb8-112">Example 2: Modify a Storage Insight by using a workspace object</span></span>
```
PS C:\>$Workspace = Get-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"

PS C:\>Set-AzureRmOperationalInsightsStorageInsight -Workspace $Workspace -Name "MyStorageInsight" -Containers @("wad-iis-logfiles")
```

<span data-ttu-id="eabb8-113">O primeiro comando usa o cmdlet Get-AzureRmOperationalInsightsWorkspace para obter o espaço de trabalho chamado MyWorkspace e, em seguida, armazena-o na variável $Workspace.</span><span class="sxs-lookup"><span data-stu-id="eabb8-113">The first command uses the Get-AzureRmOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkspace, and then stores it in the $Workspace variable.</span></span>

<span data-ttu-id="eabb8-114">O segundo comando modifica os contêineres dos quais a percepção do armazenamento chamada MyStorageInsight lê.</span><span class="sxs-lookup"><span data-stu-id="eabb8-114">The second command modifies the containers from which the Storage Insight named MyStorageInsight reads.</span></span>

## <span data-ttu-id="eabb8-115">OS</span><span class="sxs-lookup"><span data-stu-id="eabb8-115">PARAMETERS</span></span>

### <span data-ttu-id="eabb8-116">-Contêineres</span><span class="sxs-lookup"><span data-stu-id="eabb8-116">-Containers</span></span>
<span data-ttu-id="eabb8-117">Especifica a lista de contêineres que fornecem os dados.</span><span class="sxs-lookup"><span data-stu-id="eabb8-117">Specifies the list of containers that provide the data.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eabb8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eabb8-118">-DefaultProfile</span></span>
<span data-ttu-id="eabb8-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="eabb8-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eabb8-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="eabb8-120">-Name</span></span>
<span data-ttu-id="eabb8-121">Especifica o nome de uma informação sobre o armazenamento.</span><span class="sxs-lookup"><span data-stu-id="eabb8-121">Specifies the name of a Storage Insight.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eabb8-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eabb8-122">-ResourceGroupName</span></span>
<span data-ttu-id="eabb8-123">Especifica o nome de um grupo de recursos do Azure que contém um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="eabb8-123">Specifies the name of an Azure resource group that contains a workspace.</span></span>

```yaml
Type: String
Parameter Sets: ByWorkspaceName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eabb8-124">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="eabb8-124">-StorageAccountKey</span></span>
<span data-ttu-id="eabb8-125">Especifica a tecla de acesso para a conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="eabb8-125">Specifies the access key for the storage account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eabb8-126">-Tabelas</span><span class="sxs-lookup"><span data-stu-id="eabb8-126">-Tables</span></span>
<span data-ttu-id="eabb8-127">Especifica a lista de tabelas que contêm os dados.</span><span class="sxs-lookup"><span data-stu-id="eabb8-127">Specifies the list of tables that contain the data.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eabb8-128">-Espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="eabb8-128">-Workspace</span></span>
<span data-ttu-id="eabb8-129">Especifica o espaço de trabalho que contém a percepção do armazenamento.</span><span class="sxs-lookup"><span data-stu-id="eabb8-129">Specifies the workspace that contains the Storage Insight.</span></span>

```yaml
Type: PSWorkspace
Parameter Sets: ByWorkspaceObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="eabb8-130">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="eabb8-130">-WorkspaceName</span></span>
<span data-ttu-id="eabb8-131">Especifica o nome de um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="eabb8-131">Specifies the name of a workspace.</span></span>

```yaml
Type: String
Parameter Sets: ByWorkspaceName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eabb8-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eabb8-132">CommonParameters</span></span>
<span data-ttu-id="eabb8-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eabb8-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eabb8-134">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eabb8-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eabb8-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="eabb8-135">INPUTS</span></span>

### <span data-ttu-id="eabb8-136">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="eabb8-136">PSWorkspace</span></span>
<span data-ttu-id="eabb8-137">O parâmetro ' Workspace ' aceita o valor do tipo ' PSWorkspace ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="eabb8-137">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

## <span data-ttu-id="eabb8-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="eabb8-138">OUTPUTS</span></span>

### <span data-ttu-id="eabb8-139">Microsoft. Azure. Commands. OperationalInsights. Models. PSStorageInsight</span><span class="sxs-lookup"><span data-stu-id="eabb8-139">Microsoft.Azure.Commands.OperationalInsights.Models.PSStorageInsight</span></span>

## <span data-ttu-id="eabb8-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="eabb8-140">NOTES</span></span>

## <span data-ttu-id="eabb8-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="eabb8-141">RELATED LINKS</span></span>

[<span data-ttu-id="eabb8-142">Cmdlets do Azure Operational insights</span><span class="sxs-lookup"><span data-stu-id="eabb8-142">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)

[<span data-ttu-id="eabb8-143">Get-AzureRmOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="eabb8-143">Get-AzureRmOperationalInsightsWorkspace</span></span>](./Get-AzureRmOperationalInsightsWorkspace.md)


