---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/remove-azoperationalinsightslinkedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsLinkedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsLinkedStorageAccount.md
ms.openlocfilehash: 8e4dd13b93a0aadf8c69325bc6d79a2a1b3e1359
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890206"
---
# <span data-ttu-id="481d7-101">Remove-AzOperationalInsightsLinkedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="481d7-101">Remove-AzOperationalInsightsLinkedStorageAccount</span></span>

## <span data-ttu-id="481d7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="481d7-102">SYNOPSIS</span></span>
<span data-ttu-id="481d7-103">Excluir conta de armazenamento vinculado para espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="481d7-103">Delete linked storage account for workspace</span></span>

## <span data-ttu-id="481d7-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="481d7-104">SYNTAX</span></span>

```
Remove-AzOperationalInsightsLinkedStorageAccount [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [[-DataSourceType] <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="481d7-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="481d7-105">DESCRIPTION</span></span>
<span data-ttu-id="481d7-106">Excluir conta de armazenamento vinculado para espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="481d7-106">Delete linked storage account for workspace</span></span>

## <span data-ttu-id="481d7-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="481d7-107">EXAMPLES</span></span>

### <span data-ttu-id="481d7-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="481d7-108">Example 1</span></span>
```powershell
Remove-AzOperationalInsightsLinkedStorageAccount -ResourceGroupName {rg-name} -WorkspaceName {workspace-name} -DataSourceType CustomLogs
True
```

<span data-ttu-id="481d7-109">Excluir conta de armazenamento vinculada com o tipo "CustomLogs" para {workspace-name}</span><span class="sxs-lookup"><span data-stu-id="481d7-109">Delete linked storage account with type "CustomLogs" for {workspace-name}</span></span>

## <span data-ttu-id="481d7-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="481d7-110">PARAMETERS</span></span>

### <span data-ttu-id="481d7-111">-DataSourceType</span><span class="sxs-lookup"><span data-stu-id="481d7-111">-DataSourceType</span></span>
<span data-ttu-id="481d7-112">O Tipo de Fonte de Dados deve ser um dos 'CustomLogs', 'AzureWatson'.</span><span class="sxs-lookup"><span data-stu-id="481d7-112">Data Source Type should be one of 'CustomLogs', 'AzureWatson'.</span></span>

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

### <span data-ttu-id="481d7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="481d7-113">-DefaultProfile</span></span>
<span data-ttu-id="481d7-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="481d7-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="481d7-115">-Force</span><span class="sxs-lookup"><span data-stu-id="481d7-115">-Force</span></span>
<span data-ttu-id="481d7-116">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="481d7-116">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="481d7-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="481d7-117">-ResourceGroupName</span></span>
<span data-ttu-id="481d7-118">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="481d7-118">The resource group name.</span></span>

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

### <span data-ttu-id="481d7-119">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="481d7-119">-WorkspaceName</span></span>
<span data-ttu-id="481d7-120">O nome do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="481d7-120">The workspace name.</span></span>

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

### <span data-ttu-id="481d7-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="481d7-121">-Confirm</span></span>
<span data-ttu-id="481d7-122">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="481d7-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="481d7-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="481d7-123">-WhatIf</span></span>
<span data-ttu-id="481d7-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="481d7-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="481d7-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="481d7-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="481d7-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="481d7-126">CommonParameters</span></span>
<span data-ttu-id="481d7-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="481d7-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="481d7-128">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="481d7-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="481d7-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="481d7-129">INPUTS</span></span>

### <span data-ttu-id="481d7-130">System.String</span><span class="sxs-lookup"><span data-stu-id="481d7-130">System.String</span></span>

## <span data-ttu-id="481d7-131">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="481d7-131">OUTPUTS</span></span>

### <span data-ttu-id="481d7-132">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="481d7-132">System.Boolean</span></span>

## <span data-ttu-id="481d7-133">NOTES</span><span class="sxs-lookup"><span data-stu-id="481d7-133">NOTES</span></span>

## <span data-ttu-id="481d7-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="481d7-134">RELATED LINKS</span></span>
