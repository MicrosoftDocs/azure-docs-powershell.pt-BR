---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/remove-azoperationalinsightslinkedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsLinkedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsLinkedStorageAccount.md
ms.openlocfilehash: 56f9f5b86e3e98ca9bba13604c3086d2189c45c5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94118079"
---
# <span data-ttu-id="3e37f-101">Remove-AzOperationalInsightsLinkedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3e37f-101">Remove-AzOperationalInsightsLinkedStorageAccount</span></span>

## <span data-ttu-id="3e37f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3e37f-102">SYNOPSIS</span></span>
<span data-ttu-id="3e37f-103">Excluir conta de armazenamento vinculado do espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="3e37f-103">Delete linked storage account for workspace</span></span>

## <span data-ttu-id="3e37f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3e37f-104">SYNTAX</span></span>

```
Remove-AzOperationalInsightsLinkedStorageAccount [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [[-DataSourceType] <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3e37f-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3e37f-105">DESCRIPTION</span></span>
<span data-ttu-id="3e37f-106">Excluir conta de armazenamento vinculado do espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="3e37f-106">Delete linked storage account for workspace</span></span>

## <span data-ttu-id="3e37f-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3e37f-107">EXAMPLES</span></span>

### <span data-ttu-id="3e37f-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="3e37f-108">Example 1</span></span>
```powershell
Remove-AzOperationalInsightsLinkedStorageAccount -ResourceGroupName {rg-name} -WorkspaceName {workspace-name} -DataSourceType CustomLogs
True
```

<span data-ttu-id="3e37f-109">Excluir conta de armazenamento vinculado com o tipo "CustomLogs" para {Workspace-Name}</span><span class="sxs-lookup"><span data-stu-id="3e37f-109">Delete linked storage account with type "CustomLogs" for {workspace-name}</span></span>

## <span data-ttu-id="3e37f-110">OS</span><span class="sxs-lookup"><span data-stu-id="3e37f-110">PARAMETERS</span></span>

### <span data-ttu-id="3e37f-111">-DataSourceType</span><span class="sxs-lookup"><span data-stu-id="3e37f-111">-DataSourceType</span></span>
<span data-ttu-id="3e37f-112">O tipo de fonte de dados deve ser "CustomLogs", "AzureWatson".</span><span class="sxs-lookup"><span data-stu-id="3e37f-112">Data Source Type should be one of 'CustomLogs', 'AzureWatson'.</span></span>

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

### <span data-ttu-id="3e37f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e37f-113">-DefaultProfile</span></span>
<span data-ttu-id="3e37f-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3e37f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3e37f-115">-Force</span><span class="sxs-lookup"><span data-stu-id="3e37f-115">-Force</span></span>
<span data-ttu-id="3e37f-116">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="3e37f-116">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="3e37f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e37f-117">-ResourceGroupName</span></span>
<span data-ttu-id="3e37f-118">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="3e37f-118">The resource group name.</span></span>

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

### <span data-ttu-id="3e37f-119">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="3e37f-119">-WorkspaceName</span></span>
<span data-ttu-id="3e37f-120">O nome do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="3e37f-120">The workspace name.</span></span>

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

### <span data-ttu-id="3e37f-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="3e37f-121">-Confirm</span></span>
<span data-ttu-id="3e37f-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3e37f-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3e37f-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3e37f-123">-WhatIf</span></span>
<span data-ttu-id="3e37f-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="3e37f-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3e37f-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3e37f-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3e37f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e37f-126">CommonParameters</span></span>
<span data-ttu-id="3e37f-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e37f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e37f-128">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3e37f-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e37f-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3e37f-129">INPUTS</span></span>

### <span data-ttu-id="3e37f-130">System. String</span><span class="sxs-lookup"><span data-stu-id="3e37f-130">System.String</span></span>

## <span data-ttu-id="3e37f-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3e37f-131">OUTPUTS</span></span>

### <span data-ttu-id="3e37f-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3e37f-132">System.Boolean</span></span>

## <span data-ttu-id="3e37f-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3e37f-133">NOTES</span></span>

## <span data-ttu-id="3e37f-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3e37f-134">RELATED LINKS</span></span>
