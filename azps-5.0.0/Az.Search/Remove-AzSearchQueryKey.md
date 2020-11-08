---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/remove-azsearchquerykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Remove-AzSearchQueryKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Remove-AzSearchQueryKey.md
ms.openlocfilehash: e7a74fcc6d5e1a80282cfb365070df1b339aea45
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94118188"
---
# <span data-ttu-id="c52c2-101">Remove-AzSearchQueryKey</span><span class="sxs-lookup"><span data-stu-id="c52c2-101">Remove-AzSearchQueryKey</span></span>

## <span data-ttu-id="c52c2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c52c2-102">SYNOPSIS</span></span>
<span data-ttu-id="c52c2-103">Remova a chave de consulta do serviço de pesquisa do Azure.</span><span class="sxs-lookup"><span data-stu-id="c52c2-103">Remove the query key from the Azure Search service.</span></span>

## <span data-ttu-id="c52c2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c52c2-104">SYNTAX</span></span>

### <span data-ttu-id="c52c2-105">ResourceNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="c52c2-105">ResourceNameParameterSet (Default)</span></span>
```
Remove-AzSearchQueryKey [-ResourceGroupName] <String> [-ServiceName] <String> -KeyValue <String> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c52c2-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c52c2-106">ParentObjectParameterSet</span></span>
```
Remove-AzSearchQueryKey [-ParentObject] <PSSearchService> -KeyValue <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c52c2-107">ParentResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c52c2-107">ParentResourceIdParameterSet</span></span>
```
Remove-AzSearchQueryKey [-ParentResourceId] <String> -KeyValue <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c52c2-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c52c2-108">DESCRIPTION</span></span>
<span data-ttu-id="c52c2-109">O cmdlet **Remove-AzSearchQueryKey** remove a chave de consulta do serviço de pesquisa do Azure.</span><span class="sxs-lookup"><span data-stu-id="c52c2-109">The **Remove-AzSearchQueryKey** cmdlet removes the query key from the Azure Search service.</span></span>

## <span data-ttu-id="c52c2-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c52c2-110">EXAMPLES</span></span>

### <span data-ttu-id="c52c2-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c52c2-111">Example 1</span></span>
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

<span data-ttu-id="c52c2-112">O exemplo remove a chave de consulta do serviço de pesquisa do Azure.</span><span class="sxs-lookup"><span data-stu-id="c52c2-112">The example removes the query key from the Azure Search service.</span></span>

## <span data-ttu-id="c52c2-113">OS</span><span class="sxs-lookup"><span data-stu-id="c52c2-113">PARAMETERS</span></span>

### <span data-ttu-id="c52c2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c52c2-114">-DefaultProfile</span></span>
<span data-ttu-id="c52c2-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c52c2-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c52c2-116">-Force</span><span class="sxs-lookup"><span data-stu-id="c52c2-116">-Force</span></span>
<span data-ttu-id="c52c2-117">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="c52c2-117">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="c52c2-118">-KeyValue</span><span class="sxs-lookup"><span data-stu-id="c52c2-118">-KeyValue</span></span>
<span data-ttu-id="c52c2-119">Valor da chave de consulta do serviço de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="c52c2-119">Search Service query key value.</span></span>

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

### <span data-ttu-id="c52c2-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="c52c2-120">-ParentObject</span></span>
<span data-ttu-id="c52c2-121">Objeto de entrada do serviço de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="c52c2-121">Search Service Input Object.</span></span>

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

### <span data-ttu-id="c52c2-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="c52c2-122">-ParentResourceId</span></span>
<span data-ttu-id="c52c2-123">ID do recurso do serviço de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="c52c2-123">Search Service Resource Id.</span></span>

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

### <span data-ttu-id="c52c2-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c52c2-124">-PassThru</span></span>
<span data-ttu-id="c52c2-125">Esse cmdlet não retorna um objeto por padrão.</span><span class="sxs-lookup"><span data-stu-id="c52c2-125">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="c52c2-126">Se essa opção for especificada, retornará true se for bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="c52c2-126">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="c52c2-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c52c2-127">-ResourceGroupName</span></span>
<span data-ttu-id="c52c2-128">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c52c2-128">Resource Group name.</span></span>

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

### <span data-ttu-id="c52c2-129">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="c52c2-129">-ServiceName</span></span>
<span data-ttu-id="c52c2-130">Nome do serviço de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="c52c2-130">Search Service name.</span></span>

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

### <span data-ttu-id="c52c2-131">-Confirme</span><span class="sxs-lookup"><span data-stu-id="c52c2-131">-Confirm</span></span>
<span data-ttu-id="c52c2-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c52c2-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c52c2-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c52c2-133">-WhatIf</span></span>
<span data-ttu-id="c52c2-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c52c2-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c52c2-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c52c2-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c52c2-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c52c2-136">CommonParameters</span></span>
<span data-ttu-id="c52c2-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c52c2-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c52c2-138">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c52c2-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c52c2-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c52c2-139">INPUTS</span></span>

### <span data-ttu-id="c52c2-140">Microsoft. Azure. Commands. Management. Search. Models. PSSearchService</span><span class="sxs-lookup"><span data-stu-id="c52c2-140">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="c52c2-141">System. String</span><span class="sxs-lookup"><span data-stu-id="c52c2-141">System.String</span></span>

## <span data-ttu-id="c52c2-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c52c2-142">OUTPUTS</span></span>

### <span data-ttu-id="c52c2-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c52c2-143">System.Boolean</span></span>

## <span data-ttu-id="c52c2-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c52c2-144">NOTES</span></span>

## <span data-ttu-id="c52c2-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c52c2-145">RELATED LINKS</span></span>

[<span data-ttu-id="c52c2-146">New-AzSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="c52c2-146">New-AzSearchQueryKey.md</span></span>](./New-AzSearchQueryKey.md)

[<span data-ttu-id="c52c2-147">Get-AzSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="c52c2-147">Get-AzSearchQueryKey.md</span></span>](./Get-AzSearchQueryKey.md)
