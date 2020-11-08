---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/set-azoperationalinsightslinkedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsLinkedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsLinkedStorageAccount.md
ms.openlocfilehash: b6e57494daf556c3b824ee06735711042d3851b9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94116880"
---
# <span data-ttu-id="8e8cf-101">Set-AzOperationalInsightsLinkedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8e8cf-101">Set-AzOperationalInsightsLinkedStorageAccount</span></span>

## <span data-ttu-id="8e8cf-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8e8cf-102">SYNOPSIS</span></span>
<span data-ttu-id="8e8cf-103">Definir conta de armazenamento vinculado para o espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="8e8cf-103">Set linked storage account for workspace</span></span>

## <span data-ttu-id="8e8cf-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8e8cf-104">SYNTAX</span></span>

```
Set-AzOperationalInsightsLinkedStorageAccount [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DataSourceType] <String> [-StorageAccountIds] <String[]> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8e8cf-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8e8cf-105">DESCRIPTION</span></span>
<span data-ttu-id="8e8cf-106">Definir conta de armazenamento vinculado para o espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="8e8cf-106">Set linked storage account for workspace</span></span>

## <span data-ttu-id="8e8cf-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8e8cf-107">EXAMPLES</span></span>

### <span data-ttu-id="8e8cf-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="8e8cf-108">Example 1</span></span>
```powershell
$account = Get-AzStorageAccount -ResourceGroupName {rg-name} -Name {account-name}

Set-AzOperationalInsightsLinkedStorageAccount -ResourceGroupName {rg-name} -WorkspaceName {workspace-name} -DataSourceType CustomLogs -StorageAccountIds $account.Id

Id                : /subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.OperationalInsights/workspaces/{workspace-name}/linkedStorageAccounts/CustomLogs
Name              : customlogs
Type              : Microsoft.OperationalInsights/workspaces/linkedStorageAccounts
DataSourceType    : CustomLogs
StorageAccountIds : {/subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.Storage/storageAccounts/{storage-account}}
```

<span data-ttu-id="8e8cf-109">Definir o armazenamento vinculado para o espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="8e8cf-109">Set linked storage for workspace</span></span>

## <span data-ttu-id="8e8cf-110">OS</span><span class="sxs-lookup"><span data-stu-id="8e8cf-110">PARAMETERS</span></span>

### <span data-ttu-id="8e8cf-111">-DataSourceType</span><span class="sxs-lookup"><span data-stu-id="8e8cf-111">-DataSourceType</span></span>
<span data-ttu-id="8e8cf-112">O tipo de fonte de dados deve ser "CustomLogs", "AzureWatson".</span><span class="sxs-lookup"><span data-stu-id="8e8cf-112">Data Source Type should be one of 'CustomLogs', 'AzureWatson'.</span></span>

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

### <span data-ttu-id="8e8cf-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e8cf-113">-DefaultProfile</span></span>
<span data-ttu-id="8e8cf-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8e8cf-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8e8cf-115">-Force</span><span class="sxs-lookup"><span data-stu-id="8e8cf-115">-Force</span></span>
<span data-ttu-id="8e8cf-116">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="8e8cf-116">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="8e8cf-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e8cf-117">-ResourceGroupName</span></span>
<span data-ttu-id="8e8cf-118">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="8e8cf-118">The resource group name.</span></span>

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

### <span data-ttu-id="8e8cf-119">-StorageAccountIds</span><span class="sxs-lookup"><span data-stu-id="8e8cf-119">-StorageAccountIds</span></span>
<span data-ttu-id="8e8cf-120">lista de ID da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="8e8cf-120">list of storage account Id.</span></span>

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

### <span data-ttu-id="8e8cf-121">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="8e8cf-121">-WorkspaceName</span></span>
<span data-ttu-id="8e8cf-122">O nome do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="8e8cf-122">The workspace name.</span></span>

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

### <span data-ttu-id="8e8cf-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="8e8cf-123">-Confirm</span></span>
<span data-ttu-id="8e8cf-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8e8cf-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8e8cf-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e8cf-125">-WhatIf</span></span>
<span data-ttu-id="8e8cf-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="8e8cf-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8e8cf-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8e8cf-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8e8cf-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e8cf-128">CommonParameters</span></span>
<span data-ttu-id="8e8cf-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e8cf-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e8cf-130">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8e8cf-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e8cf-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8e8cf-131">INPUTS</span></span>

### <span data-ttu-id="8e8cf-132">System. String</span><span class="sxs-lookup"><span data-stu-id="8e8cf-132">System.String</span></span>

## <span data-ttu-id="8e8cf-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8e8cf-133">OUTPUTS</span></span>

### <span data-ttu-id="8e8cf-134">Microsoft. Azure. Commands. OperationalInsights. Models. PSLinkedStorageAccountsResource</span><span class="sxs-lookup"><span data-stu-id="8e8cf-134">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedStorageAccountsResource</span></span>

## <span data-ttu-id="8e8cf-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8e8cf-135">NOTES</span></span>

## <span data-ttu-id="8e8cf-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8e8cf-136">RELATED LINKS</span></span>
