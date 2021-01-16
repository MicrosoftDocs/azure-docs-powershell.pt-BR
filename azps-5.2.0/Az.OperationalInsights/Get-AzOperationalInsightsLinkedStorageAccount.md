---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightslinkedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsLinkedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsLinkedStorageAccount.md
ms.openlocfilehash: 5095a3d9f989a6600776140239b9207ba3293d53
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98260345"
---
# <span data-ttu-id="393b5-101">Get-AzOperationalInsightsLinkedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="393b5-101">Get-AzOperationalInsightsLinkedStorageAccount</span></span>

## <span data-ttu-id="393b5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="393b5-102">SYNOPSIS</span></span>
<span data-ttu-id="393b5-103">Obter ou listar a conta de armazenamento vinculado</span><span class="sxs-lookup"><span data-stu-id="393b5-103">Get or list linked storage account</span></span>

## <span data-ttu-id="393b5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="393b5-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsLinkedStorageAccount [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [[-DataSourceType] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="393b5-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="393b5-105">DESCRIPTION</span></span>
<span data-ttu-id="393b5-106">Obter conta de armazenamento vinculado, listar todas as contas de armazenamento vinculadas quando "-DataSourceType" não foi especificado</span><span class="sxs-lookup"><span data-stu-id="393b5-106">Get linked storage account, list all linked storage accounts when "-DataSourceType" was not specified</span></span>

## <span data-ttu-id="393b5-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="393b5-107">EXAMPLES</span></span>

### <span data-ttu-id="393b5-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="393b5-108">Example 1</span></span>
```powershell
Get-AzOperationalInsightsLinkedStorageAccount -ResourceGroupName {rg-name} -WorkspaceName {workspace-name}

Id                : /subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.OperationalInsights/workspaces/{workspace-name}/linkedStorageAccounts/customlogs
Name              :
Type              : Microsoft.OperationalInsights/workspaces/linkedStorageAccounts
DataSourceType    : CustomLogs
StorageAccountIds : {/subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.Storage/storageAccounts/{account}}
```

<span data-ttu-id="393b5-109">lista de armazenamento vinculado accoounts para espaço de trabalho {Workspace-Name}</span><span class="sxs-lookup"><span data-stu-id="393b5-109">list linked storage accoounts for workspace {workspace-name}</span></span>

## <span data-ttu-id="393b5-110">OS</span><span class="sxs-lookup"><span data-stu-id="393b5-110">PARAMETERS</span></span>

### <span data-ttu-id="393b5-111">-DataSourceType</span><span class="sxs-lookup"><span data-stu-id="393b5-111">-DataSourceType</span></span>
<span data-ttu-id="393b5-112">O tipo de fonte de dados deve ser "CustomLogs", "AzureWatson".</span><span class="sxs-lookup"><span data-stu-id="393b5-112">Data Source Type should be one of 'CustomLogs', 'AzureWatson'.</span></span>

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

### <span data-ttu-id="393b5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="393b5-113">-DefaultProfile</span></span>
<span data-ttu-id="393b5-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="393b5-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="393b5-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="393b5-115">-ResourceGroupName</span></span>
<span data-ttu-id="393b5-116">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="393b5-116">The resource group name.</span></span>

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

### <span data-ttu-id="393b5-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="393b5-117">-WorkspaceName</span></span>
<span data-ttu-id="393b5-118">O nome do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="393b5-118">The workspace name.</span></span>

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

### <span data-ttu-id="393b5-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="393b5-119">CommonParameters</span></span>
<span data-ttu-id="393b5-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="393b5-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="393b5-121">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="393b5-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="393b5-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="393b5-122">INPUTS</span></span>

### <span data-ttu-id="393b5-123">System. String</span><span class="sxs-lookup"><span data-stu-id="393b5-123">System.String</span></span>

## <span data-ttu-id="393b5-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="393b5-124">OUTPUTS</span></span>

### <span data-ttu-id="393b5-125">Microsoft. Azure. Commands. OperationalInsights. Models. PSLinkedStorageAccountsResource</span><span class="sxs-lookup"><span data-stu-id="393b5-125">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedStorageAccountsResource</span></span>

## <span data-ttu-id="393b5-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="393b5-126">NOTES</span></span>

## <span data-ttu-id="393b5-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="393b5-127">RELATED LINKS</span></span>