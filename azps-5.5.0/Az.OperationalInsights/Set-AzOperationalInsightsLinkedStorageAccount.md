---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/set-azoperationalinsightslinkedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsLinkedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsLinkedStorageAccount.md
ms.openlocfilehash: b6e57494daf556c3b824ee06735711042d3851b9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118217"
---
# <span data-ttu-id="37afd-101">Set-AzOperationalInsightsLinkedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="37afd-101">Set-AzOperationalInsightsLinkedStorageAccount</span></span>

## <span data-ttu-id="37afd-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="37afd-102">SYNOPSIS</span></span>
<span data-ttu-id="37afd-103">Definir conta de armazenamento vinculada para espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="37afd-103">Set linked storage account for workspace</span></span>

## <span data-ttu-id="37afd-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="37afd-104">SYNTAX</span></span>

```
Set-AzOperationalInsightsLinkedStorageAccount [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DataSourceType] <String> [-StorageAccountIds] <String[]> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="37afd-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="37afd-105">DESCRIPTION</span></span>
<span data-ttu-id="37afd-106">Definir conta de armazenamento vinculada para espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="37afd-106">Set linked storage account for workspace</span></span>

## <span data-ttu-id="37afd-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="37afd-107">EXAMPLES</span></span>

### <span data-ttu-id="37afd-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="37afd-108">Example 1</span></span>
```powershell
$account = Get-AzStorageAccount -ResourceGroupName {rg-name} -Name {account-name}

Set-AzOperationalInsightsLinkedStorageAccount -ResourceGroupName {rg-name} -WorkspaceName {workspace-name} -DataSourceType CustomLogs -StorageAccountIds $account.Id

Id                : /subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.OperationalInsights/workspaces/{workspace-name}/linkedStorageAccounts/CustomLogs
Name              : customlogs
Type              : Microsoft.OperationalInsights/workspaces/linkedStorageAccounts
DataSourceType    : CustomLogs
StorageAccountIds : {/subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.Storage/storageAccounts/{storage-account}}
```

<span data-ttu-id="37afd-109">Definir armazenamento vinculado para espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="37afd-109">Set linked storage for workspace</span></span>

## <span data-ttu-id="37afd-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="37afd-110">PARAMETERS</span></span>

### <span data-ttu-id="37afd-111">-DataSourceType</span><span class="sxs-lookup"><span data-stu-id="37afd-111">-DataSourceType</span></span>
<span data-ttu-id="37afd-112">O Tipo de Fonte de Dados deve ser um dos 'CustomLogs', 'Azure Widget'.</span><span class="sxs-lookup"><span data-stu-id="37afd-112">Data Source Type should be one of 'CustomLogs', 'AzureWatson'.</span></span>

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

### <span data-ttu-id="37afd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37afd-113">-DefaultProfile</span></span>
<span data-ttu-id="37afd-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="37afd-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="37afd-115">-Forçar</span><span class="sxs-lookup"><span data-stu-id="37afd-115">-Force</span></span>
<span data-ttu-id="37afd-116">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="37afd-116">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="37afd-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37afd-117">-ResourceGroupName</span></span>
<span data-ttu-id="37afd-118">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="37afd-118">The resource group name.</span></span>

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

### <span data-ttu-id="37afd-119">-StorageAccountIds</span><span class="sxs-lookup"><span data-stu-id="37afd-119">-StorageAccountIds</span></span>
<span data-ttu-id="37afd-120">lista de ID da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="37afd-120">list of storage account Id.</span></span>

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

### <span data-ttu-id="37afd-121">-NomedoEspacial de Trabalho</span><span class="sxs-lookup"><span data-stu-id="37afd-121">-WorkspaceName</span></span>
<span data-ttu-id="37afd-122">O nome do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="37afd-122">The workspace name.</span></span>

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

### <span data-ttu-id="37afd-123">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="37afd-123">-Confirm</span></span>
<span data-ttu-id="37afd-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="37afd-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="37afd-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="37afd-125">-WhatIf</span></span>
<span data-ttu-id="37afd-126">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="37afd-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="37afd-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="37afd-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="37afd-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37afd-128">CommonParameters</span></span>
<span data-ttu-id="37afd-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37afd-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37afd-130">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="37afd-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37afd-131">Entradas</span><span class="sxs-lookup"><span data-stu-id="37afd-131">INPUTS</span></span>

### <span data-ttu-id="37afd-132">System.String</span><span class="sxs-lookup"><span data-stu-id="37afd-132">System.String</span></span>

## <span data-ttu-id="37afd-133">Saídas</span><span class="sxs-lookup"><span data-stu-id="37afd-133">OUTPUTS</span></span>

### <span data-ttu-id="37afd-134">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedStorageAccountsResource</span><span class="sxs-lookup"><span data-stu-id="37afd-134">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedStorageAccountsResource</span></span>

## <span data-ttu-id="37afd-135">Notas</span><span class="sxs-lookup"><span data-stu-id="37afd-135">NOTES</span></span>

## <span data-ttu-id="37afd-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="37afd-136">RELATED LINKS</span></span>
