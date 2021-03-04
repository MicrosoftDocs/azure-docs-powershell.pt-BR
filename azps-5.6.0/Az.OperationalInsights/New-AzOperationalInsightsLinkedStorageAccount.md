---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/new-azoperationalinsightslinkedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsLinkedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsLinkedStorageAccount.md
ms.openlocfilehash: f1b920c3a67865cbed66c15bc686e3e38e3562db
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888611"
---
# <span data-ttu-id="c5b70-101">New-AzOperationalInsightsLinkedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c5b70-101">New-AzOperationalInsightsLinkedStorageAccount</span></span>

## <span data-ttu-id="c5b70-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c5b70-102">SYNOPSIS</span></span>
<span data-ttu-id="c5b70-103">Criar conta de armazenamento vinculada para espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="c5b70-103">Create linked storage account for workspace</span></span>

## <span data-ttu-id="c5b70-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="c5b70-104">SYNTAX</span></span>

```
New-AzOperationalInsightsLinkedStorageAccount [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DataSourceType] <String> [-StorageAccountIds] <String[]> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c5b70-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="c5b70-105">DESCRIPTION</span></span>
<span data-ttu-id="c5b70-106">Criar conta de armazenamento vinculada para espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="c5b70-106">Create linked storage account for workspace</span></span>

## <span data-ttu-id="c5b70-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c5b70-107">EXAMPLES</span></span>

### <span data-ttu-id="c5b70-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c5b70-108">Example 1</span></span>
```powershell
$account = Get-AzStorageAccount -ResourceGroupName {rg-name} -Name {account-name}

New-AzOperationalInsightsLinkedStorageAccount -ResourceGroupName {rg-name} -WorkspaceName {workspace-name} -DataSourceType CustomLogs -StorageAccountIds $account.Id

Id                : /subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.OperationalInsights/workspaces/{workspace-name}/linkedStorageAccounts/CustomLogs
Name              : customlogs
Type              : Microsoft.OperationalInsights/workspaces/linkedStorageAccounts
DataSourceType    : CustomLogs
StorageAccountIds : {/subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.Storage/storageAccounts/{storage-account}}
```

<span data-ttu-id="c5b70-109">Adicionar armazenamento vinculado para espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="c5b70-109">Add linked storage for workspace</span></span>

## <span data-ttu-id="c5b70-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="c5b70-110">PARAMETERS</span></span>

### <span data-ttu-id="c5b70-111">-DataSourceType</span><span class="sxs-lookup"><span data-stu-id="c5b70-111">-DataSourceType</span></span>
<span data-ttu-id="c5b70-112">O Tipo de Fonte de Dados deve ser um dos 'CustomLogs', 'AzureWatson'.</span><span class="sxs-lookup"><span data-stu-id="c5b70-112">Data Source Type should be one of 'CustomLogs', 'AzureWatson'.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: CustomLogs, AzureWatson

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5b70-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5b70-113">-DefaultProfile</span></span>
<span data-ttu-id="c5b70-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c5b70-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5b70-115">-Force</span><span class="sxs-lookup"><span data-stu-id="c5b70-115">-Force</span></span>
<span data-ttu-id="c5b70-116">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="c5b70-116">Don't ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5b70-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5b70-117">-ResourceGroupName</span></span>
<span data-ttu-id="c5b70-118">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c5b70-118">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5b70-119">-StorageAccountIds</span><span class="sxs-lookup"><span data-stu-id="c5b70-119">-StorageAccountIds</span></span>
<span data-ttu-id="c5b70-120">lista de ID da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="c5b70-120">list of storage account Id.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5b70-121">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="c5b70-121">-WorkspaceName</span></span>
<span data-ttu-id="c5b70-122">O nome do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="c5b70-122">The workspace name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5b70-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c5b70-123">-Confirm</span></span>
<span data-ttu-id="c5b70-124">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c5b70-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5b70-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c5b70-125">-WhatIf</span></span>
<span data-ttu-id="c5b70-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c5b70-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c5b70-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c5b70-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5b70-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5b70-128">CommonParameters</span></span>
<span data-ttu-id="c5b70-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c5b70-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5b70-130">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c5b70-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5b70-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c5b70-131">INPUTS</span></span>

### <span data-ttu-id="c5b70-132">System.String</span><span class="sxs-lookup"><span data-stu-id="c5b70-132">System.String</span></span>

## <span data-ttu-id="c5b70-133">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="c5b70-133">OUTPUTS</span></span>

### <span data-ttu-id="c5b70-134">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedStorageAccountsResource</span><span class="sxs-lookup"><span data-stu-id="c5b70-134">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedStorageAccountsResource</span></span>

## <span data-ttu-id="c5b70-135">NOTES</span><span class="sxs-lookup"><span data-stu-id="c5b70-135">NOTES</span></span>

## <span data-ttu-id="c5b70-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c5b70-136">RELATED LINKS</span></span>
