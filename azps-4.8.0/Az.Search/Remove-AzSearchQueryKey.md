---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/remove-azsearchquerykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Remove-AzSearchQueryKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Remove-AzSearchQueryKey.md
ms.openlocfilehash: e7a74fcc6d5e1a80282cfb365070df1b339aea45
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94111398"
---
# <span data-ttu-id="354c8-101">Remove-AzSearchQueryKey</span><span class="sxs-lookup"><span data-stu-id="354c8-101">Remove-AzSearchQueryKey</span></span>

## <span data-ttu-id="354c8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="354c8-102">SYNOPSIS</span></span>
<span data-ttu-id="354c8-103">Remova a chave de consulta do serviço de pesquisa do Azure.</span><span class="sxs-lookup"><span data-stu-id="354c8-103">Remove the query key from the Azure Search service.</span></span>

## <span data-ttu-id="354c8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="354c8-104">SYNTAX</span></span>

### <span data-ttu-id="354c8-105">ResourceNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="354c8-105">ResourceNameParameterSet (Default)</span></span>
```
Remove-AzSearchQueryKey [-ResourceGroupName] <String> [-ServiceName] <String> -KeyValue <String> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="354c8-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="354c8-106">ParentObjectParameterSet</span></span>
```
Remove-AzSearchQueryKey [-ParentObject] <PSSearchService> -KeyValue <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="354c8-107">ParentResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="354c8-107">ParentResourceIdParameterSet</span></span>
```
Remove-AzSearchQueryKey [-ParentResourceId] <String> -KeyValue <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="354c8-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="354c8-108">DESCRIPTION</span></span>
<span data-ttu-id="354c8-109">O cmdlet **Remove-AzSearchQueryKey** remove a chave de consulta do serviço de pesquisa do Azure.</span><span class="sxs-lookup"><span data-stu-id="354c8-109">The **Remove-AzSearchQueryKey** cmdlet removes the query key from the Azure Search service.</span></span>

## <span data-ttu-id="354c8-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="354c8-110">EXAMPLES</span></span>

### <span data-ttu-id="354c8-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="354c8-111">Example 1</span></span>
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

<span data-ttu-id="354c8-112">O exemplo remove a chave de consulta do serviço de pesquisa do Azure.</span><span class="sxs-lookup"><span data-stu-id="354c8-112">The example removes the query key from the Azure Search service.</span></span>

## <span data-ttu-id="354c8-113">OS</span><span class="sxs-lookup"><span data-stu-id="354c8-113">PARAMETERS</span></span>

### <span data-ttu-id="354c8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="354c8-114">-DefaultProfile</span></span>
<span data-ttu-id="354c8-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="354c8-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="354c8-116">-Force</span><span class="sxs-lookup"><span data-stu-id="354c8-116">-Force</span></span>
<span data-ttu-id="354c8-117">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="354c8-117">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="354c8-118">-KeyValue</span><span class="sxs-lookup"><span data-stu-id="354c8-118">-KeyValue</span></span>
<span data-ttu-id="354c8-119">Valor da chave de consulta do serviço de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="354c8-119">Search Service query key value.</span></span>

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

### <span data-ttu-id="354c8-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="354c8-120">-ParentObject</span></span>
<span data-ttu-id="354c8-121">Objeto de entrada do serviço de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="354c8-121">Search Service Input Object.</span></span>

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

### <span data-ttu-id="354c8-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="354c8-122">-ParentResourceId</span></span>
<span data-ttu-id="354c8-123">ID do recurso do serviço de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="354c8-123">Search Service Resource Id.</span></span>

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

### <span data-ttu-id="354c8-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="354c8-124">-PassThru</span></span>
<span data-ttu-id="354c8-125">Esse cmdlet não retorna um objeto por padrão.</span><span class="sxs-lookup"><span data-stu-id="354c8-125">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="354c8-126">Se essa opção for especificada, retornará true se for bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="354c8-126">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="354c8-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="354c8-127">-ResourceGroupName</span></span>
<span data-ttu-id="354c8-128">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="354c8-128">Resource Group name.</span></span>

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

### <span data-ttu-id="354c8-129">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="354c8-129">-ServiceName</span></span>
<span data-ttu-id="354c8-130">Nome do serviço de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="354c8-130">Search Service name.</span></span>

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

### <span data-ttu-id="354c8-131">-Confirme</span><span class="sxs-lookup"><span data-stu-id="354c8-131">-Confirm</span></span>
<span data-ttu-id="354c8-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="354c8-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="354c8-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="354c8-133">-WhatIf</span></span>
<span data-ttu-id="354c8-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="354c8-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="354c8-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="354c8-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="354c8-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="354c8-136">CommonParameters</span></span>
<span data-ttu-id="354c8-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="354c8-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="354c8-138">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="354c8-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="354c8-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="354c8-139">INPUTS</span></span>

### <span data-ttu-id="354c8-140">Microsoft. Azure. Commands. Management. Search. Models. PSSearchService</span><span class="sxs-lookup"><span data-stu-id="354c8-140">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="354c8-141">System. String</span><span class="sxs-lookup"><span data-stu-id="354c8-141">System.String</span></span>

## <span data-ttu-id="354c8-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="354c8-142">OUTPUTS</span></span>

### <span data-ttu-id="354c8-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="354c8-143">System.Boolean</span></span>

## <span data-ttu-id="354c8-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="354c8-144">NOTES</span></span>

## <span data-ttu-id="354c8-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="354c8-145">RELATED LINKS</span></span>

[<span data-ttu-id="354c8-146">New-AzSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="354c8-146">New-AzSearchQueryKey.md</span></span>](./New-AzSearchQueryKey.md)

[<span data-ttu-id="354c8-147">Get-AzSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="354c8-147">Get-AzSearchQueryKey.md</span></span>](./Get-AzSearchQueryKey.md)
