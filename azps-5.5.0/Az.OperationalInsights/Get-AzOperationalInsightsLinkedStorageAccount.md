---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightslinkedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsLinkedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsLinkedStorageAccount.md
ms.openlocfilehash: 5095a3d9f989a6600776140239b9207ba3293d53
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111527"
---
# <span data-ttu-id="b724d-101">Get-AzOperationalInsightsLinkedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b724d-101">Get-AzOperationalInsightsLinkedStorageAccount</span></span>

## <span data-ttu-id="b724d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b724d-102">SYNOPSIS</span></span>
<span data-ttu-id="b724d-103">Obter ou listar uma conta de armazenamento vinculada</span><span class="sxs-lookup"><span data-stu-id="b724d-103">Get or list linked storage account</span></span>

## <span data-ttu-id="b724d-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b724d-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsLinkedStorageAccount [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [[-DataSourceType] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b724d-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="b724d-105">DESCRIPTION</span></span>
<span data-ttu-id="b724d-106">Obter conta de armazenamento vinculada, listar todas as contas de armazenamento vinculadas quando "-DataSourceType" não foi especificado</span><span class="sxs-lookup"><span data-stu-id="b724d-106">Get linked storage account, list all linked storage accounts when "-DataSourceType" was not specified</span></span>

## <span data-ttu-id="b724d-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="b724d-107">EXAMPLES</span></span>

### <span data-ttu-id="b724d-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b724d-108">Example 1</span></span>
```powershell
Get-AzOperationalInsightsLinkedStorageAccount -ResourceGroupName {rg-name} -WorkspaceName {workspace-name}

Id                : /subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.OperationalInsights/workspaces/{workspace-name}/linkedStorageAccounts/customlogs
Name              :
Type              : Microsoft.OperationalInsights/workspaces/linkedStorageAccounts
DataSourceType    : CustomLogs
StorageAccountIds : {/subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.Storage/storageAccounts/{account}}
```

<span data-ttu-id="b724d-109">lista de participantes de armazenamento vinculado para espaço de trabalho {workspace-name}</span><span class="sxs-lookup"><span data-stu-id="b724d-109">list linked storage accoounts for workspace {workspace-name}</span></span>

## <span data-ttu-id="b724d-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b724d-110">PARAMETERS</span></span>

### <span data-ttu-id="b724d-111">-DataSourceType</span><span class="sxs-lookup"><span data-stu-id="b724d-111">-DataSourceType</span></span>
<span data-ttu-id="b724d-112">O Tipo de Fonte de Dados deve ser um dos 'CustomLogs', 'Azure Widget'.</span><span class="sxs-lookup"><span data-stu-id="b724d-112">Data Source Type should be one of 'CustomLogs', 'AzureWatson'.</span></span>

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

### <span data-ttu-id="b724d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b724d-113">-DefaultProfile</span></span>
<span data-ttu-id="b724d-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b724d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b724d-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b724d-115">-ResourceGroupName</span></span>
<span data-ttu-id="b724d-116">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b724d-116">The resource group name.</span></span>

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

### <span data-ttu-id="b724d-117">-NomedoEspacial de Trabalho</span><span class="sxs-lookup"><span data-stu-id="b724d-117">-WorkspaceName</span></span>
<span data-ttu-id="b724d-118">O nome do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="b724d-118">The workspace name.</span></span>

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

### <span data-ttu-id="b724d-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b724d-119">CommonParameters</span></span>
<span data-ttu-id="b724d-120">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b724d-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b724d-121">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b724d-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b724d-122">Entradas</span><span class="sxs-lookup"><span data-stu-id="b724d-122">INPUTS</span></span>

### <span data-ttu-id="b724d-123">System.String</span><span class="sxs-lookup"><span data-stu-id="b724d-123">System.String</span></span>

## <span data-ttu-id="b724d-124">Saídas</span><span class="sxs-lookup"><span data-stu-id="b724d-124">OUTPUTS</span></span>

### <span data-ttu-id="b724d-125">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedStorageAccountsResource</span><span class="sxs-lookup"><span data-stu-id="b724d-125">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedStorageAccountsResource</span></span>

## <span data-ttu-id="b724d-126">Notas</span><span class="sxs-lookup"><span data-stu-id="b724d-126">NOTES</span></span>

## <span data-ttu-id="b724d-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b724d-127">RELATED LINKS</span></span>