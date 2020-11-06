---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 7660F1A2-604D-4488-93F1-CB7C502F135E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/new-azurermoperationalinsightsstorageinsight
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsStorageInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsStorageInsight.md
ms.openlocfilehash: 1bea5ce9eda22996eb65b6e5d26fb3af19cd1c88
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429401"
---
# <span data-ttu-id="bbc53-101">New-AzureRmOperationalInsightsStorageInsight</span><span class="sxs-lookup"><span data-stu-id="bbc53-101">New-AzureRmOperationalInsightsStorageInsight</span></span>

## <span data-ttu-id="bbc53-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bbc53-102">SYNOPSIS</span></span>
<span data-ttu-id="bbc53-103">Cria uma percepção do armazenamento dentro de um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="bbc53-103">Creates a Storage Insight inside a workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bbc53-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bbc53-104">SYNTAX</span></span>

### <span data-ttu-id="bbc53-105">ByWorkspaceName (padrão)</span><span class="sxs-lookup"><span data-stu-id="bbc53-105">ByWorkspaceName (Default)</span></span>
```
New-AzureRmOperationalInsightsStorageInsight [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-StorageAccountResourceId] <String> [-StorageAccountKey] <String> [[-Tables] <String[]>]
 [[-Containers] <String[]>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bbc53-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="bbc53-106">ByWorkspaceObject</span></span>
```
New-AzureRmOperationalInsightsStorageInsight [-Workspace] <PSWorkspace> [-Name] <String>
 [-StorageAccountResourceId] <String> [-StorageAccountKey] <String> [[-Tables] <String[]>]
 [[-Containers] <String[]>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bbc53-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="bbc53-107">DESCRIPTION</span></span>
<span data-ttu-id="bbc53-108">O cmdlet **New-AzureRmOperationalInsightsStorageInsight** cria uma nova visão geral do armazenamento em um espaço de trabalho existente.</span><span class="sxs-lookup"><span data-stu-id="bbc53-108">The **New-AzureRmOperationalInsightsStorageInsight** cmdlet creates a new Storage Insight in an existing workspace.</span></span>

## <span data-ttu-id="bbc53-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bbc53-109">EXAMPLES</span></span>

### <span data-ttu-id="bbc53-110">Exemplo 1: criar uma visão geral do armazenamento por nome</span><span class="sxs-lookup"><span data-stu-id="bbc53-110">Example 1: Create a Storage Insight by name</span></span>
```
PS C:\>$Storage = Get-AzureRmStorageAccount -ResourceGroupName "ContosoResourceGroup" -Name "ContosoStorage"

PS C:\>$StorageKey = ($Storage | Get-AzureRmStorageAccountKey).Key1

PS C:\>New-AzureRmOperationalInsightsStorageInsight -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "MyWorkspace" -Name "MyStorageInsight" -StorageAccountResourceId $Storage.Id -StorageAccountKey $StorageKey -Tables @("WADWindowsEventLogsTable")
```

<span data-ttu-id="bbc53-111">O primeiro comando usa o cmdlet Get-AzureRmStorageAccount para obter a conta de armazenamento chamada ContosoStorage e, em seguida, armazena-a na variável $Storage.</span><span class="sxs-lookup"><span data-stu-id="bbc53-111">The first command uses the Get-AzureRmStorageAccount cmdlet to get the storage account named ContosoStorage, and then stores it in the $Storage variable.</span></span>
<span data-ttu-id="bbc53-112">O segundo comando passa a conta de armazenamento em $Storage para o cmdlet Get-AzureRmStorageAccountKey usando o operador de pipeline para obter a chave da conta de armazenamento especificada e, em seguida, armazena-o na variável $StorageKey.</span><span class="sxs-lookup"><span data-stu-id="bbc53-112">The second command passes the storage account in $Storage to the Get-AzureRmStorageAccountKey cmdlet by using the pipeline operator to get the specified storage account key, and then stores it in the $StorageKey variable.</span></span>
<span data-ttu-id="bbc53-113">O comando final cria uma informação de armazenamento chamada MyStorageInsight no espaço de trabalho chamado MyWorkspace.</span><span class="sxs-lookup"><span data-stu-id="bbc53-113">The final command creates a storage insight named MyStorageInsight in the workspace named MyWorkspace.</span></span>
<span data-ttu-id="bbc53-114">Esta informação sobre armazenamento consome dados da tabela WADWindowsEventLogsTable no recurso de conta de armazenamento especificado.</span><span class="sxs-lookup"><span data-stu-id="bbc53-114">This storage insight consumes data from the WADWindowsEventLogsTable table in the specified storage account resource.</span></span>

### <span data-ttu-id="bbc53-115">Exemplo 2: criar uma visão geral do armazenamento usando um objeto do espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="bbc53-115">Example 2: Create a Storage Insight by using a workspace object</span></span>
```
PS C:\>$Workspace = Get-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"

PS C:\>$Storage = Get-AzureRmStorageAccount -ResourceGroupName "ContosoResourceGroup" -Name "ContosoStorage"

PS C:\>$StorageKey = ($Storage | Get-AzureRmStorageAccountKey).Key1

PS C:\>New-AzureRmOperationalInsightsStorageInsight -Workspace $Workspace -Name "MyStorageInsight" -StorageAccountResourceId $Storage.Id -StorageAccountKey $StorageKey -Tables @("WADWindowsEventLogsTable")
```

<span data-ttu-id="bbc53-116">O primeiro comando usa o cmdlet Get-AzureRmOperationalInsightsWorkspace para obter o espaço de trabalho chamado MyWorkspace e, em seguida, armazena-o na variável $Workspace.</span><span class="sxs-lookup"><span data-stu-id="bbc53-116">The first command uses the Get-AzureRmOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkspace, and then stores it in the $Workspace variable.</span></span>
<span data-ttu-id="bbc53-117">O segundo comando usa o cmdlet Get-AzureRmStorageAccount para obter a conta de armazenamento especificada e, em seguida, armazena-o na variável $Storage.</span><span class="sxs-lookup"><span data-stu-id="bbc53-117">The second command uses the Get-AzureRmStorageAccount cmdlet to get the specified storage account, and then stores it in the $Storage variable.</span></span>
<span data-ttu-id="bbc53-118">O terceiro comando passa a conta de armazenamento $Storage para o cmdlet Get-AzureRmStorageAccountKey usando o operador pipeline para obter a chave especificada e, em seguida, armazena-o na variável $StorageKey.</span><span class="sxs-lookup"><span data-stu-id="bbc53-118">The third command passes the storage account in $Storage to the Get-AzureRmStorageAccountKey cmdlet by using the pipeline operator to get the specified key, and then stores it in the $StorageKey variable.</span></span>
<span data-ttu-id="bbc53-119">O comando final cria uma informação de armazenamento chamada MyStorageInsight no espaço de trabalho definido em $Workspace.</span><span class="sxs-lookup"><span data-stu-id="bbc53-119">The final command creates a storage insight named MyStorageInsight in the workspace defined in $Workspace.</span></span>
<span data-ttu-id="bbc53-120">A percepção do armazenamento consome dados da tabela WADWindowsEventLogsTable no recurso de conta de armazenamento especificado.</span><span class="sxs-lookup"><span data-stu-id="bbc53-120">The Storage Insight consumes data from the WADWindowsEventLogsTable table in the specified storage account resource.</span></span>

## <span data-ttu-id="bbc53-121">OS</span><span class="sxs-lookup"><span data-stu-id="bbc53-121">PARAMETERS</span></span>

### <span data-ttu-id="bbc53-122">-Contêineres</span><span class="sxs-lookup"><span data-stu-id="bbc53-122">-Containers</span></span>
<span data-ttu-id="bbc53-123">Especifica a lista de contêineres que contêm os dados.</span><span class="sxs-lookup"><span data-stu-id="bbc53-123">Specifies the list of containers that contain the data.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bbc53-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bbc53-124">-DefaultProfile</span></span>
<span data-ttu-id="bbc53-125">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="bbc53-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bbc53-126">-Force</span><span class="sxs-lookup"><span data-stu-id="bbc53-126">-Force</span></span>
<span data-ttu-id="bbc53-127">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="bbc53-127">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbc53-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="bbc53-128">-Name</span></span>
<span data-ttu-id="bbc53-129">Especifica o nome da informação sobre o armazenamento.</span><span class="sxs-lookup"><span data-stu-id="bbc53-129">Specifies the name of the Storage Insight.</span></span>

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

### <span data-ttu-id="bbc53-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bbc53-130">-ResourceGroupName</span></span>
<span data-ttu-id="bbc53-131">Especifica o nome de um grupo de recursos do Azure que contém um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="bbc53-131">Specifies the name of an Azure resource group that contains a workspace.</span></span>

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

### <span data-ttu-id="bbc53-132">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="bbc53-132">-StorageAccountKey</span></span>
<span data-ttu-id="bbc53-133">Especifica a tecla de acesso para a conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="bbc53-133">Specifies the access key for the storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bbc53-134">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="bbc53-134">-StorageAccountResourceId</span></span>
<span data-ttu-id="bbc53-135">Especifica o recurso do Azure de uma conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="bbc53-135">Specifies the Azure resource of a storage account.</span></span>
<span data-ttu-id="bbc53-136">Isso pode ser recuperado executando o cmdlet Get-AzureRmStorageAccount e acessando o parâmetro *ID* do resultado.</span><span class="sxs-lookup"><span data-stu-id="bbc53-136">This can be retrieved by executing the Get-AzureRmStorageAccount cmdlet and accessing the *Id* parameter of the result.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bbc53-137">-Tabelas</span><span class="sxs-lookup"><span data-stu-id="bbc53-137">-Tables</span></span>
<span data-ttu-id="bbc53-138">Especifica a lista de tabelas que fornecem os dados.</span><span class="sxs-lookup"><span data-stu-id="bbc53-138">Specifies the list of tables that provide the data.</span></span>

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

### <span data-ttu-id="bbc53-139">-Espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="bbc53-139">-Workspace</span></span>
<span data-ttu-id="bbc53-140">Especifica o espaço de trabalho para a nova visão de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="bbc53-140">Specifies the workspace for the new Storage Insight.</span></span>

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

### <span data-ttu-id="bbc53-141">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="bbc53-141">-WorkspaceName</span></span>
<span data-ttu-id="bbc53-142">Especifica o nome de um espaço de trabalho existente.</span><span class="sxs-lookup"><span data-stu-id="bbc53-142">Specifies the name of an existing workspace.</span></span>

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

### <span data-ttu-id="bbc53-143">-Confirme</span><span class="sxs-lookup"><span data-stu-id="bbc53-143">-Confirm</span></span>
<span data-ttu-id="bbc53-144">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bbc53-144">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbc53-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bbc53-145">-WhatIf</span></span>
<span data-ttu-id="bbc53-146">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="bbc53-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bbc53-147">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="bbc53-147">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbc53-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bbc53-148">CommonParameters</span></span>
<span data-ttu-id="bbc53-149">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bbc53-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bbc53-150">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bbc53-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bbc53-151">SENSORES</span><span class="sxs-lookup"><span data-stu-id="bbc53-151">INPUTS</span></span>

### <span data-ttu-id="bbc53-152">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="bbc53-152">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>
<span data-ttu-id="bbc53-153">Parâmetros: espaço de trabalho (ByValue)</span><span class="sxs-lookup"><span data-stu-id="bbc53-153">Parameters: Workspace (ByValue)</span></span>

### <span data-ttu-id="bbc53-154">System. String</span><span class="sxs-lookup"><span data-stu-id="bbc53-154">System.String</span></span>

### <span data-ttu-id="bbc53-155">System. String []</span><span class="sxs-lookup"><span data-stu-id="bbc53-155">System.String[]</span></span>

## <span data-ttu-id="bbc53-156">EXIBE</span><span class="sxs-lookup"><span data-stu-id="bbc53-156">OUTPUTS</span></span>

### <span data-ttu-id="bbc53-157">Microsoft. Azure. Commands. OperationalInsights. Models. PSStorageInsight</span><span class="sxs-lookup"><span data-stu-id="bbc53-157">Microsoft.Azure.Commands.OperationalInsights.Models.PSStorageInsight</span></span>

## <span data-ttu-id="bbc53-158">INFORMA</span><span class="sxs-lookup"><span data-stu-id="bbc53-158">NOTES</span></span>

## <span data-ttu-id="bbc53-159">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bbc53-159">RELATED LINKS</span></span>

[<span data-ttu-id="bbc53-160">Cmdlets do Azure Operational insights</span><span class="sxs-lookup"><span data-stu-id="bbc53-160">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)

[<span data-ttu-id="bbc53-161">Get-AzureRmOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="bbc53-161">Get-AzureRmOperationalInsightsWorkspace</span></span>](./Get-AzureRmOperationalInsightsWorkspace.md)

