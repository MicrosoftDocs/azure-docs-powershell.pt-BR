---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightslinkedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsLinkedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsLinkedStorageAccount.md
ms.openlocfilehash: 5095a3d9f989a6600776140239b9207ba3293d53
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94114736"
---
# <span data-ttu-id="7a01e-101">Get-AzOperationalInsightsLinkedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7a01e-101">Get-AzOperationalInsightsLinkedStorageAccount</span></span>

## <span data-ttu-id="7a01e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7a01e-102">SYNOPSIS</span></span>
<span data-ttu-id="7a01e-103">Obter ou listar a conta de armazenamento vinculado</span><span class="sxs-lookup"><span data-stu-id="7a01e-103">Get or list linked storage account</span></span>

## <span data-ttu-id="7a01e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7a01e-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsLinkedStorageAccount [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [[-DataSourceType] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7a01e-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7a01e-105">DESCRIPTION</span></span>
<span data-ttu-id="7a01e-106">Obter conta de armazenamento vinculado, listar todas as contas de armazenamento vinculadas quando "-DataSourceType" não foi especificado</span><span class="sxs-lookup"><span data-stu-id="7a01e-106">Get linked storage account, list all linked storage accounts when "-DataSourceType" was not specified</span></span>

## <span data-ttu-id="7a01e-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7a01e-107">EXAMPLES</span></span>

### <span data-ttu-id="7a01e-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="7a01e-108">Example 1</span></span>
```powershell
Get-AzOperationalInsightsLinkedStorageAccount -ResourceGroupName {rg-name} -WorkspaceName {workspace-name}

Id                : /subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.OperationalInsights/workspaces/{workspace-name}/linkedStorageAccounts/customlogs
Name              :
Type              : Microsoft.OperationalInsights/workspaces/linkedStorageAccounts
DataSourceType    : CustomLogs
StorageAccountIds : {/subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.Storage/storageAccounts/{account}}
```

<span data-ttu-id="7a01e-109">lista de armazenamento vinculado accoounts para espaço de trabalho {Workspace-Name}</span><span class="sxs-lookup"><span data-stu-id="7a01e-109">list linked storage accoounts for workspace {workspace-name}</span></span>

## <span data-ttu-id="7a01e-110">OS</span><span class="sxs-lookup"><span data-stu-id="7a01e-110">PARAMETERS</span></span>

### <span data-ttu-id="7a01e-111">-DataSourceType</span><span class="sxs-lookup"><span data-stu-id="7a01e-111">-DataSourceType</span></span>
<span data-ttu-id="7a01e-112">O tipo de fonte de dados deve ser "CustomLogs", "AzureWatson".</span><span class="sxs-lookup"><span data-stu-id="7a01e-112">Data Source Type should be one of 'CustomLogs', 'AzureWatson'.</span></span>

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

### <span data-ttu-id="7a01e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a01e-113">-DefaultProfile</span></span>
<span data-ttu-id="7a01e-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7a01e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7a01e-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a01e-115">-ResourceGroupName</span></span>
<span data-ttu-id="7a01e-116">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="7a01e-116">The resource group name.</span></span>

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

### <span data-ttu-id="7a01e-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="7a01e-117">-WorkspaceName</span></span>
<span data-ttu-id="7a01e-118">O nome do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="7a01e-118">The workspace name.</span></span>

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

### <span data-ttu-id="7a01e-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a01e-119">CommonParameters</span></span>
<span data-ttu-id="7a01e-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a01e-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a01e-121">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7a01e-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a01e-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7a01e-122">INPUTS</span></span>

### <span data-ttu-id="7a01e-123">System. String</span><span class="sxs-lookup"><span data-stu-id="7a01e-123">System.String</span></span>

## <span data-ttu-id="7a01e-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7a01e-124">OUTPUTS</span></span>

### <span data-ttu-id="7a01e-125">Microsoft. Azure. Commands. OperationalInsights. Models. PSLinkedStorageAccountsResource</span><span class="sxs-lookup"><span data-stu-id="7a01e-125">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedStorageAccountsResource</span></span>

## <span data-ttu-id="7a01e-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7a01e-126">NOTES</span></span>

## <span data-ttu-id="7a01e-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7a01e-127">RELATED LINKS</span></span>