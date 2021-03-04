---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/get-azoperationalinsightslinkedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsLinkedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsLinkedStorageAccount.md
ms.openlocfilehash: 5ae174f31cdbe23a28dd9a21b44b640239e78fdd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888448"
---
# <span data-ttu-id="6797f-101">Get-AzOperationalInsightsLinkedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6797f-101">Get-AzOperationalInsightsLinkedStorageAccount</span></span>

## <span data-ttu-id="6797f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6797f-102">SYNOPSIS</span></span>
<span data-ttu-id="6797f-103">Obter ou listar conta de armazenamento vinculado</span><span class="sxs-lookup"><span data-stu-id="6797f-103">Get or list linked storage account</span></span>

## <span data-ttu-id="6797f-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="6797f-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsLinkedStorageAccount [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [[-DataSourceType] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6797f-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="6797f-105">DESCRIPTION</span></span>
<span data-ttu-id="6797f-106">Obter conta de armazenamento vinculado, listar todas as contas de armazenamento vinculadas quando "-DataSourceType" não foi especificado</span><span class="sxs-lookup"><span data-stu-id="6797f-106">Get linked storage account, list all linked storage accounts when "-DataSourceType" was not specified</span></span>

## <span data-ttu-id="6797f-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6797f-107">EXAMPLES</span></span>

### <span data-ttu-id="6797f-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="6797f-108">Example 1</span></span>
```powershell
Get-AzOperationalInsightsLinkedStorageAccount -ResourceGroupName {rg-name} -WorkspaceName {workspace-name}

Id                : /subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.OperationalInsights/workspaces/{workspace-name}/linkedStorageAccounts/customlogs
Name              :
Type              : Microsoft.OperationalInsights/workspaces/linkedStorageAccounts
DataSourceType    : CustomLogs
StorageAccountIds : {/subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.Storage/storageAccounts/{account}}
```

<span data-ttu-id="6797f-109">listar os accoounts de armazenamento vinculados para o espaço de trabalho {workspace-name}</span><span class="sxs-lookup"><span data-stu-id="6797f-109">list linked storage accoounts for workspace {workspace-name}</span></span>

## <span data-ttu-id="6797f-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="6797f-110">PARAMETERS</span></span>

### <span data-ttu-id="6797f-111">-DataSourceType</span><span class="sxs-lookup"><span data-stu-id="6797f-111">-DataSourceType</span></span>
<span data-ttu-id="6797f-112">O Tipo de Fonte de Dados deve ser um dos 'CustomLogs', 'AzureWatson'.</span><span class="sxs-lookup"><span data-stu-id="6797f-112">Data Source Type should be one of 'CustomLogs', 'AzureWatson'.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: CustomLogs, AzureWatson

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6797f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6797f-113">-DefaultProfile</span></span>
<span data-ttu-id="6797f-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6797f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6797f-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6797f-115">-ResourceGroupName</span></span>
<span data-ttu-id="6797f-116">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="6797f-116">The resource group name.</span></span>

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

### <span data-ttu-id="6797f-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="6797f-117">-WorkspaceName</span></span>
<span data-ttu-id="6797f-118">O nome do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="6797f-118">The workspace name.</span></span>

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

### <span data-ttu-id="6797f-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6797f-119">CommonParameters</span></span>
<span data-ttu-id="6797f-120">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6797f-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6797f-121">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6797f-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6797f-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6797f-122">INPUTS</span></span>

### <span data-ttu-id="6797f-123">System.String</span><span class="sxs-lookup"><span data-stu-id="6797f-123">System.String</span></span>

## <span data-ttu-id="6797f-124">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="6797f-124">OUTPUTS</span></span>

### <span data-ttu-id="6797f-125">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedStorageAccountsResource</span><span class="sxs-lookup"><span data-stu-id="6797f-125">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedStorageAccountsResource</span></span>

## <span data-ttu-id="6797f-126">NOTES</span><span class="sxs-lookup"><span data-stu-id="6797f-126">NOTES</span></span>

## <span data-ttu-id="6797f-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6797f-127">RELATED LINKS</span></span>