---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/remove-azoperationalinsightslinkedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsLinkedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsLinkedStorageAccount.md
ms.openlocfilehash: 56f9f5b86e3e98ca9bba13604c3086d2189c45c5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114587"
---
# <span data-ttu-id="5fe40-101">Remove-AzOperationalInsightsLinkedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="5fe40-101">Remove-AzOperationalInsightsLinkedStorageAccount</span></span>

## <span data-ttu-id="5fe40-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5fe40-102">SYNOPSIS</span></span>
<span data-ttu-id="5fe40-103">Excluir conta de armazenamento vinculada para espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="5fe40-103">Delete linked storage account for workspace</span></span>

## <span data-ttu-id="5fe40-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5fe40-104">SYNTAX</span></span>

```
Remove-AzOperationalInsightsLinkedStorageAccount [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [[-DataSourceType] <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5fe40-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="5fe40-105">DESCRIPTION</span></span>
<span data-ttu-id="5fe40-106">Excluir conta de armazenamento vinculada para espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="5fe40-106">Delete linked storage account for workspace</span></span>

## <span data-ttu-id="5fe40-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="5fe40-107">EXAMPLES</span></span>

### <span data-ttu-id="5fe40-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="5fe40-108">Example 1</span></span>
```powershell
Remove-AzOperationalInsightsLinkedStorageAccount -ResourceGroupName {rg-name} -WorkspaceName {workspace-name} -DataSourceType CustomLogs
True
```

<span data-ttu-id="5fe40-109">Excluir conta de armazenamento vinculada com o tipo "CustomLogs" para {workspace-name}</span><span class="sxs-lookup"><span data-stu-id="5fe40-109">Delete linked storage account with type "CustomLogs" for {workspace-name}</span></span>

## <span data-ttu-id="5fe40-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5fe40-110">PARAMETERS</span></span>

### <span data-ttu-id="5fe40-111">-DataSourceType</span><span class="sxs-lookup"><span data-stu-id="5fe40-111">-DataSourceType</span></span>
<span data-ttu-id="5fe40-112">O Tipo de Fonte de Dados deve ser um dos 'CustomLogs', 'Azure Widget'.</span><span class="sxs-lookup"><span data-stu-id="5fe40-112">Data Source Type should be one of 'CustomLogs', 'AzureWatson'.</span></span>

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

### <span data-ttu-id="5fe40-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5fe40-113">-DefaultProfile</span></span>
<span data-ttu-id="5fe40-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5fe40-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5fe40-115">-Forçar</span><span class="sxs-lookup"><span data-stu-id="5fe40-115">-Force</span></span>
<span data-ttu-id="5fe40-116">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="5fe40-116">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="5fe40-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5fe40-117">-ResourceGroupName</span></span>
<span data-ttu-id="5fe40-118">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="5fe40-118">The resource group name.</span></span>

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

### <span data-ttu-id="5fe40-119">-NomedoEspacial de Trabalho</span><span class="sxs-lookup"><span data-stu-id="5fe40-119">-WorkspaceName</span></span>
<span data-ttu-id="5fe40-120">O nome do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="5fe40-120">The workspace name.</span></span>

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

### <span data-ttu-id="5fe40-121">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="5fe40-121">-Confirm</span></span>
<span data-ttu-id="5fe40-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5fe40-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5fe40-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5fe40-123">-WhatIf</span></span>
<span data-ttu-id="5fe40-124">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="5fe40-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5fe40-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5fe40-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5fe40-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5fe40-126">CommonParameters</span></span>
<span data-ttu-id="5fe40-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5fe40-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5fe40-128">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5fe40-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5fe40-129">Entradas</span><span class="sxs-lookup"><span data-stu-id="5fe40-129">INPUTS</span></span>

### <span data-ttu-id="5fe40-130">System.String</span><span class="sxs-lookup"><span data-stu-id="5fe40-130">System.String</span></span>

## <span data-ttu-id="5fe40-131">Saídas</span><span class="sxs-lookup"><span data-stu-id="5fe40-131">OUTPUTS</span></span>

### <span data-ttu-id="5fe40-132">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="5fe40-132">System.Boolean</span></span>

## <span data-ttu-id="5fe40-133">Notas</span><span class="sxs-lookup"><span data-stu-id="5fe40-133">NOTES</span></span>

## <span data-ttu-id="5fe40-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5fe40-134">RELATED LINKS</span></span>
