---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightslinkedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsLinkedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsLinkedStorageAccount.md
ms.openlocfilehash: 1293a2d045da5da1856052495516e9311e42e5f2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98261347"
---
# <span data-ttu-id="c5145-101">New-AzOperationalInsightsLinkedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c5145-101">New-AzOperationalInsightsLinkedStorageAccount</span></span>

## <span data-ttu-id="c5145-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c5145-102">SYNOPSIS</span></span>
<span data-ttu-id="c5145-103">Criar conta de armazenamento vinculado para o espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="c5145-103">Create linked storage account for workspace</span></span>

## <span data-ttu-id="c5145-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c5145-104">SYNTAX</span></span>

```
New-AzOperationalInsightsLinkedStorageAccount [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DataSourceType] <String> [-StorageAccountIds] <String[]> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c5145-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c5145-105">DESCRIPTION</span></span>
<span data-ttu-id="c5145-106">Criar conta de armazenamento vinculado para o espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="c5145-106">Create linked storage account for workspace</span></span>

## <span data-ttu-id="c5145-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c5145-107">EXAMPLES</span></span>

### <span data-ttu-id="c5145-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c5145-108">Example 1</span></span>
```powershell
$account = Get-AzStorageAccount -ResourceGroupName {rg-name} -Name {account-name}

New-AzOperationalInsightsLinkedStorageAccount -ResourceGroupName {rg-name} -WorkspaceName {workspace-name} -DataSourceType CustomLogs -StorageAccountIds $account.Id

Id                : /subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.OperationalInsights/workspaces/{workspace-name}/linkedStorageAccounts/CustomLogs
Name              : customlogs
Type              : Microsoft.OperationalInsights/workspaces/linkedStorageAccounts
DataSourceType    : CustomLogs
StorageAccountIds : {/subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.Storage/storageAccounts/{storage-account}}
```

<span data-ttu-id="c5145-109">Adicionar armazenamento vinculado ao espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="c5145-109">Add linked storage for workspace</span></span>

## <span data-ttu-id="c5145-110">OS</span><span class="sxs-lookup"><span data-stu-id="c5145-110">PARAMETERS</span></span>

### <span data-ttu-id="c5145-111">-DataSourceType</span><span class="sxs-lookup"><span data-stu-id="c5145-111">-DataSourceType</span></span>
<span data-ttu-id="c5145-112">O tipo de fonte de dados deve ser "CustomLogs", "AzureWatson".</span><span class="sxs-lookup"><span data-stu-id="c5145-112">Data Source Type should be one of 'CustomLogs', 'AzureWatson'.</span></span>

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

### <span data-ttu-id="c5145-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5145-113">-DefaultProfile</span></span>
<span data-ttu-id="c5145-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c5145-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c5145-115">-Force</span><span class="sxs-lookup"><span data-stu-id="c5145-115">-Force</span></span>
<span data-ttu-id="c5145-116">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="c5145-116">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="c5145-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5145-117">-ResourceGroupName</span></span>
<span data-ttu-id="c5145-118">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c5145-118">The resource group name.</span></span>

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

### <span data-ttu-id="c5145-119">-StorageAccountIds</span><span class="sxs-lookup"><span data-stu-id="c5145-119">-StorageAccountIds</span></span>
<span data-ttu-id="c5145-120">lista de ID da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="c5145-120">list of storage account Id.</span></span>

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

### <span data-ttu-id="c5145-121">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="c5145-121">-WorkspaceName</span></span>
<span data-ttu-id="c5145-122">O nome do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="c5145-122">The workspace name.</span></span>

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

### <span data-ttu-id="c5145-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="c5145-123">-Confirm</span></span>
<span data-ttu-id="c5145-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c5145-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c5145-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c5145-125">-WhatIf</span></span>
<span data-ttu-id="c5145-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c5145-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c5145-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c5145-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c5145-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5145-128">CommonParameters</span></span>
<span data-ttu-id="c5145-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c5145-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5145-130">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c5145-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5145-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c5145-131">INPUTS</span></span>

### <span data-ttu-id="c5145-132">System. String</span><span class="sxs-lookup"><span data-stu-id="c5145-132">System.String</span></span>

## <span data-ttu-id="c5145-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c5145-133">OUTPUTS</span></span>

### <span data-ttu-id="c5145-134">Microsoft. Azure. Commands. OperationalInsights. Models. PSLinkedStorageAccountsResource</span><span class="sxs-lookup"><span data-stu-id="c5145-134">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedStorageAccountsResource</span></span>

## <span data-ttu-id="c5145-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c5145-135">NOTES</span></span>

## <span data-ttu-id="c5145-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c5145-136">RELATED LINKS</span></span>
