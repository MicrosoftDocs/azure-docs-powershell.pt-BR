---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 7660F1A2-604D-4488-93F1-CB7C502F135E
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightsstorageinsight
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsStorageInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsStorageInsight.md
ms.openlocfilehash: e4f966d542110f96672857c2222d44ae03d331ba
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/13/2020
ms.locfileid: "93785076"
---
# <span data-ttu-id="0ef01-101">New-AzOperationalInsightsStorageInsight</span><span class="sxs-lookup"><span data-stu-id="0ef01-101">New-AzOperationalInsightsStorageInsight</span></span>

## <span data-ttu-id="0ef01-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0ef01-102">SYNOPSIS</span></span>
<span data-ttu-id="0ef01-103">Cria uma percepção do armazenamento dentro de um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="0ef01-103">Creates a Storage Insight inside a workspace.</span></span>

## <span data-ttu-id="0ef01-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0ef01-104">SYNTAX</span></span>

### <span data-ttu-id="0ef01-105">ByWorkspaceName (padrão)</span><span class="sxs-lookup"><span data-stu-id="0ef01-105">ByWorkspaceName (Default)</span></span>
```
New-AzOperationalInsightsStorageInsight [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-StorageAccountResourceId] <String> [-StorageAccountKey] <String> [[-Tables] <String[]>]
 [[-Containers] <String[]>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0ef01-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="0ef01-106">ByWorkspaceObject</span></span>
```
New-AzOperationalInsightsStorageInsight [-Workspace] <PSWorkspace> [-Name] <String>
 [-StorageAccountResourceId] <String> [-StorageAccountKey] <String> [[-Tables] <String[]>]
 [[-Containers] <String[]>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0ef01-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0ef01-107">DESCRIPTION</span></span>
<span data-ttu-id="0ef01-108">O cmdlet **New-AzOperationalInsightsStorageInsight** cria uma nova visão geral do armazenamento em um espaço de trabalho existente.</span><span class="sxs-lookup"><span data-stu-id="0ef01-108">The **New-AzOperationalInsightsStorageInsight** cmdlet creates a new Storage Insight in an existing workspace.</span></span>

## <span data-ttu-id="0ef01-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0ef01-109">EXAMPLES</span></span>

### <span data-ttu-id="0ef01-110">Exemplo 1: criar uma visão geral do armazenamento por nome</span><span class="sxs-lookup"><span data-stu-id="0ef01-110">Example 1: Create a Storage Insight by name</span></span>
```
PS C:\>$Storage = Get-AzStorageAccount -ResourceGroupName "ContosoResourceGroup" -Name "ContosoStorage"

PS C:\>$StorageKey = ($Storage | Get-AzStorageAccountKey).Key1

PS C:\>New-AzOperationalInsightsStorageInsight -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "MyWorkspace" -Name "MyStorageInsight" -StorageAccountResourceId $Storage.Id -StorageAccountKey $StorageKey -Tables @("WADWindowsEventLogsTable")
```

<span data-ttu-id="0ef01-111">O primeiro comando usa o cmdlet Get-AzStorageAccount para obter a conta de armazenamento chamada ContosoStorage e, em seguida, armazena-a na variável $Storage.</span><span class="sxs-lookup"><span data-stu-id="0ef01-111">The first command uses the Get-AzStorageAccount cmdlet to get the storage account named ContosoStorage, and then stores it in the $Storage variable.</span></span>
<span data-ttu-id="0ef01-112">O segundo comando passa a conta de armazenamento em $Storage para o cmdlet Get-AzStorageAccountKey usando o operador de pipeline para obter a chave da conta de armazenamento especificada e, em seguida, armazena-o na variável $StorageKey.</span><span class="sxs-lookup"><span data-stu-id="0ef01-112">The second command passes the storage account in $Storage to the Get-AzStorageAccountKey cmdlet by using the pipeline operator to get the specified storage account key, and then stores it in the $StorageKey variable.</span></span>
<span data-ttu-id="0ef01-113">O comando final cria uma informação de armazenamento chamada MyStorageInsight no espaço de trabalho chamado MyWorkspace.</span><span class="sxs-lookup"><span data-stu-id="0ef01-113">The final command creates a storage insight named MyStorageInsight in the workspace named MyWorkspace.</span></span>
<span data-ttu-id="0ef01-114">Esta informação sobre armazenamento consome dados da tabela WADWindowsEventLogsTable no recurso de conta de armazenamento especificado.</span><span class="sxs-lookup"><span data-stu-id="0ef01-114">This storage insight consumes data from the WADWindowsEventLogsTable table in the specified storage account resource.</span></span>

### <span data-ttu-id="0ef01-115">Exemplo 2: criar uma visão geral do armazenamento usando um objeto do espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="0ef01-115">Example 2: Create a Storage Insight by using a workspace object</span></span>
```
PS C:\>$Workspace = Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"

PS C:\>$Storage = Get-AzStorageAccount -ResourceGroupName "ContosoResourceGroup" -Name "ContosoStorage"

PS C:\>$StorageKey = ($Storage | Get-AzStorageAccountKey).Key1

PS C:\>New-AzOperationalInsightsStorageInsight -Workspace $Workspace -Name "MyStorageInsight" -StorageAccountResourceId $Storage.Id -StorageAccountKey $StorageKey -Tables @("WADWindowsEventLogsTable")
```

<span data-ttu-id="0ef01-116">O primeiro comando usa o cmdlet Get-AzOperationalInsightsWorkspace para obter o espaço de trabalho chamado MyWorkspace e, em seguida, armazena-o na variável $Workspace.</span><span class="sxs-lookup"><span data-stu-id="0ef01-116">The first command uses the Get-AzOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkspace, and then stores it in the $Workspace variable.</span></span>
<span data-ttu-id="0ef01-117">O segundo comando usa o cmdlet Get-AzStorageAccount para obter a conta de armazenamento especificada e, em seguida, armazena-o na variável $Storage.</span><span class="sxs-lookup"><span data-stu-id="0ef01-117">The second command uses the Get-AzStorageAccount cmdlet to get the specified storage account, and then stores it in the $Storage variable.</span></span>
<span data-ttu-id="0ef01-118">O terceiro comando passa a conta de armazenamento $Storage para o cmdlet Get-AzStorageAccountKey usando o operador pipeline para obter a chave especificada e, em seguida, armazena-o na variável $StorageKey.</span><span class="sxs-lookup"><span data-stu-id="0ef01-118">The third command passes the storage account in $Storage to the Get-AzStorageAccountKey cmdlet by using the pipeline operator to get the specified key, and then stores it in the $StorageKey variable.</span></span>
<span data-ttu-id="0ef01-119">O comando final cria uma informação de armazenamento chamada MyStorageInsight no espaço de trabalho definido em $Workspace.</span><span class="sxs-lookup"><span data-stu-id="0ef01-119">The final command creates a storage insight named MyStorageInsight in the workspace defined in $Workspace.</span></span>
<span data-ttu-id="0ef01-120">A percepção do armazenamento consome dados da tabela WADWindowsEventLogsTable no recurso de conta de armazenamento especificado.</span><span class="sxs-lookup"><span data-stu-id="0ef01-120">The Storage Insight consumes data from the WADWindowsEventLogsTable table in the specified storage account resource.</span></span>

## <span data-ttu-id="0ef01-121">OS</span><span class="sxs-lookup"><span data-stu-id="0ef01-121">PARAMETERS</span></span>

### <span data-ttu-id="0ef01-122">-Contêineres</span><span class="sxs-lookup"><span data-stu-id="0ef01-122">-Containers</span></span>
<span data-ttu-id="0ef01-123">Especifica a lista de contêineres que contêm os dados.</span><span class="sxs-lookup"><span data-stu-id="0ef01-123">Specifies the list of containers that contain the data.</span></span>

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

### <span data-ttu-id="0ef01-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ef01-124">-DefaultProfile</span></span>
<span data-ttu-id="0ef01-125">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="0ef01-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0ef01-126">-Force</span><span class="sxs-lookup"><span data-stu-id="0ef01-126">-Force</span></span>
<span data-ttu-id="0ef01-127">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="0ef01-127">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="0ef01-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="0ef01-128">-Name</span></span>
<span data-ttu-id="0ef01-129">Especifica o nome da informação sobre o armazenamento.</span><span class="sxs-lookup"><span data-stu-id="0ef01-129">Specifies the name of the Storage Insight.</span></span>

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

### <span data-ttu-id="0ef01-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0ef01-130">-ResourceGroupName</span></span>
<span data-ttu-id="0ef01-131">Especifica o nome de um grupo de recursos do Azure que contém um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="0ef01-131">Specifies the name of an Azure resource group that contains a workspace.</span></span>

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

### <span data-ttu-id="0ef01-132">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="0ef01-132">-StorageAccountKey</span></span>
<span data-ttu-id="0ef01-133">Especifica a tecla de acesso para a conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="0ef01-133">Specifies the access key for the storage account.</span></span>

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

### <span data-ttu-id="0ef01-134">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="0ef01-134">-StorageAccountResourceId</span></span>
<span data-ttu-id="0ef01-135">Especifica o recurso do Azure de uma conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="0ef01-135">Specifies the Azure resource of a storage account.</span></span>
<span data-ttu-id="0ef01-136">Isso pode ser recuperado executando o cmdlet Get-AzStorageAccount e acessando o parâmetro *ID* do resultado.</span><span class="sxs-lookup"><span data-stu-id="0ef01-136">This can be retrieved by executing the Get-AzStorageAccount cmdlet and accessing the *Id* parameter of the result.</span></span>

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

### <span data-ttu-id="0ef01-137">-Tabelas</span><span class="sxs-lookup"><span data-stu-id="0ef01-137">-Tables</span></span>
<span data-ttu-id="0ef01-138">Especifica a lista de tabelas que fornecem os dados.</span><span class="sxs-lookup"><span data-stu-id="0ef01-138">Specifies the list of tables that provide the data.</span></span>

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

### <span data-ttu-id="0ef01-139">-Espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="0ef01-139">-Workspace</span></span>
<span data-ttu-id="0ef01-140">Especifica o espaço de trabalho para a nova visão de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="0ef01-140">Specifies the workspace for the new Storage Insight.</span></span>

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

### <span data-ttu-id="0ef01-141">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="0ef01-141">-WorkspaceName</span></span>
<span data-ttu-id="0ef01-142">Especifica o nome de um espaço de trabalho existente.</span><span class="sxs-lookup"><span data-stu-id="0ef01-142">Specifies the name of an existing workspace.</span></span>

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

### <span data-ttu-id="0ef01-143">-Confirme</span><span class="sxs-lookup"><span data-stu-id="0ef01-143">-Confirm</span></span>
<span data-ttu-id="0ef01-144">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0ef01-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0ef01-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0ef01-145">-WhatIf</span></span>
<span data-ttu-id="0ef01-146">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="0ef01-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0ef01-147">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0ef01-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0ef01-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ef01-148">CommonParameters</span></span>
<span data-ttu-id="0ef01-149">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0ef01-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ef01-150">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0ef01-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ef01-151">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0ef01-151">INPUTS</span></span>

### <span data-ttu-id="0ef01-152">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="0ef01-152">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="0ef01-153">System. String</span><span class="sxs-lookup"><span data-stu-id="0ef01-153">System.String</span></span>

### <span data-ttu-id="0ef01-154">System. String []</span><span class="sxs-lookup"><span data-stu-id="0ef01-154">System.String[]</span></span>

## <span data-ttu-id="0ef01-155">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0ef01-155">OUTPUTS</span></span>

### <span data-ttu-id="0ef01-156">Microsoft. Azure. Commands. OperationalInsights. Models. PSStorageInsight</span><span class="sxs-lookup"><span data-stu-id="0ef01-156">Microsoft.Azure.Commands.OperationalInsights.Models.PSStorageInsight</span></span>

## <span data-ttu-id="0ef01-157">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0ef01-157">NOTES</span></span>

## <span data-ttu-id="0ef01-158">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0ef01-158">RELATED LINKS</span></span>

[<span data-ttu-id="0ef01-159">Cmdlets do Azure Operational insights</span><span class="sxs-lookup"><span data-stu-id="0ef01-159">Azure Operational Insights Cmdlets</span></span>](/powershell/module/az.operationalinsights)

[<span data-ttu-id="0ef01-160">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="0ef01-160">Get-AzOperationalInsightsWorkspace</span></span>](./Get-AzOperationalInsightsWorkspace.md)


