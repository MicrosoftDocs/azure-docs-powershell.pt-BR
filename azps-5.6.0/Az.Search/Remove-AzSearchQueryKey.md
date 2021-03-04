---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/powershell/module/az.search/remove-azsearchquerykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Remove-AzSearchQueryKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Remove-AzSearchQueryKey.md
ms.openlocfilehash: 79e7ff902d75387180e519bbaf8a5cdc3e2431a1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901578"
---
# <span data-ttu-id="fcab0-101">Remove-AzSearchQueryKey</span><span class="sxs-lookup"><span data-stu-id="fcab0-101">Remove-AzSearchQueryKey</span></span>

## <span data-ttu-id="fcab0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fcab0-102">SYNOPSIS</span></span>
<span data-ttu-id="fcab0-103">Remova a chave de consulta do serviço de Pesquisa Cognitiva do Azure.</span><span class="sxs-lookup"><span data-stu-id="fcab0-103">Remove the query key from the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="fcab0-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="fcab0-104">SYNTAX</span></span>

### <span data-ttu-id="fcab0-105">ResourceNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="fcab0-105">ResourceNameParameterSet (Default)</span></span>
```
Remove-AzSearchQueryKey [-ResourceGroupName] <String> [-ServiceName] <String> -KeyValue <String> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fcab0-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fcab0-106">ParentObjectParameterSet</span></span>
```
Remove-AzSearchQueryKey [-ParentObject] <PSSearchService> -KeyValue <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fcab0-107">ParentResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fcab0-107">ParentResourceIdParameterSet</span></span>
```
Remove-AzSearchQueryKey [-ParentResourceId] <String> -KeyValue <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fcab0-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="fcab0-108">DESCRIPTION</span></span>
<span data-ttu-id="fcab0-109">O cmdlet **Remove-AzSearchQueryKey** remove a chave de consulta do serviço de Pesquisa Cognitiva do Azure.</span><span class="sxs-lookup"><span data-stu-id="fcab0-109">The **Remove-AzSearchQueryKey** cmdlet removes the query key from the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="fcab0-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fcab0-110">EXAMPLES</span></span>

### <span data-ttu-id="fcab0-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="fcab0-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSearchQueryKey -ResourceGroupName "TestAzureSearchPsGroup" -ServiceName "pstestazuresearch01"

Name         Key                             
----         ---                             
             D260F448EA192EBC19D59F7E5670E8BB
NewQueryKey1 B4C13E3F6FA76100D3488673CFDCD438

PS C:\> Remove-AzSearchQueryKey -ResourceGroupName "TestAzureSearchPsGroup" -ServiceName "pstestazuresearch01" -KeyValue B4C13E3F6FA76100D3488673CFDCD438

Confirm
Are you sure you want to remove query key 'B4C13E3F6FA76100D3488673CFDCD438'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
PS C:\>
```

<span data-ttu-id="fcab0-112">O exemplo remove a chave de consulta do serviço de Pesquisa Cognitiva do Azure.</span><span class="sxs-lookup"><span data-stu-id="fcab0-112">The example removes the query key from the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="fcab0-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="fcab0-113">PARAMETERS</span></span>

### <span data-ttu-id="fcab0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fcab0-114">-DefaultProfile</span></span>
<span data-ttu-id="fcab0-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fcab0-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fcab0-116">-Force</span><span class="sxs-lookup"><span data-stu-id="fcab0-116">-Force</span></span>
<span data-ttu-id="fcab0-117">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="fcab0-117">Do not ask for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fcab0-118">-KeyValue</span><span class="sxs-lookup"><span data-stu-id="fcab0-118">-KeyValue</span></span>
<span data-ttu-id="fcab0-119">Valor da chave de consulta do Serviço de Pesquisa Cognitiva do Azure.</span><span class="sxs-lookup"><span data-stu-id="fcab0-119">Azure Cognitive Search Service query key value.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fcab0-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="fcab0-120">-ParentObject</span></span>
<span data-ttu-id="fcab0-121">Objeto de entrada do Serviço de Pesquisa Cognitiva do Azure.</span><span class="sxs-lookup"><span data-stu-id="fcab0-121">Azure Cognitive Search Service Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Search.Models.PSSearchService
Parameter Sets: ParentObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fcab0-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="fcab0-122">-ParentResourceId</span></span>
<span data-ttu-id="fcab0-123">ID do Recurso do Serviço de Pesquisa Cognitiva do Azure.</span><span class="sxs-lookup"><span data-stu-id="fcab0-123">Azure Cognitive Search Service Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ParentResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fcab0-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fcab0-124">-PassThru</span></span>
<span data-ttu-id="fcab0-125">Este Cmdlet não retorna um objeto por padrão.</span><span class="sxs-lookup"><span data-stu-id="fcab0-125">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="fcab0-126">Se essa opção for especificada, ela retornará true se tiver êxito.</span><span class="sxs-lookup"><span data-stu-id="fcab0-126">If this switch is specified, it returns true if successful.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fcab0-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fcab0-127">-ResourceGroupName</span></span>
<span data-ttu-id="fcab0-128">Nome do Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="fcab0-128">Resource Group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fcab0-129">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="fcab0-129">-ServiceName</span></span>
<span data-ttu-id="fcab0-130">Nome do Serviço de Pesquisa Cognitiva do Azure.</span><span class="sxs-lookup"><span data-stu-id="fcab0-130">Azure Cognitive Search Service name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fcab0-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fcab0-131">-Confirm</span></span>
<span data-ttu-id="fcab0-132">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fcab0-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fcab0-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fcab0-133">-WhatIf</span></span>
<span data-ttu-id="fcab0-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="fcab0-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fcab0-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="fcab0-135">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fcab0-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fcab0-136">CommonParameters</span></span>
<span data-ttu-id="fcab0-137">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fcab0-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fcab0-138">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fcab0-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fcab0-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fcab0-139">INPUTS</span></span>

### <span data-ttu-id="fcab0-140">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span><span class="sxs-lookup"><span data-stu-id="fcab0-140">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="fcab0-141">System.String</span><span class="sxs-lookup"><span data-stu-id="fcab0-141">System.String</span></span>

## <span data-ttu-id="fcab0-142">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="fcab0-142">OUTPUTS</span></span>

### <span data-ttu-id="fcab0-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="fcab0-143">System.Boolean</span></span>

## <span data-ttu-id="fcab0-144">NOTES</span><span class="sxs-lookup"><span data-stu-id="fcab0-144">NOTES</span></span>

## <span data-ttu-id="fcab0-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fcab0-145">RELATED LINKS</span></span>

[<span data-ttu-id="fcab0-146">New-AzSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="fcab0-146">New-AzSearchQueryKey.md</span></span>](./New-AzSearchQueryKey.md)

[<span data-ttu-id="fcab0-147">Get-AzSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="fcab0-147">Get-AzSearchQueryKey.md</span></span>](./Get-AzSearchQueryKey.md)
