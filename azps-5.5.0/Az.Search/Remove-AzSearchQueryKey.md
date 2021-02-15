---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/remove-azsearchquerykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Remove-AzSearchQueryKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Remove-AzSearchQueryKey.md
ms.openlocfilehash: 3d4610f83b348864fc57cf6894db1ab7455a8485
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118119"
---
# <span data-ttu-id="23b0e-101">Remove-AzSearchQueryKey</span><span class="sxs-lookup"><span data-stu-id="23b0e-101">Remove-AzSearchQueryKey</span></span>

## <span data-ttu-id="23b0e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="23b0e-102">SYNOPSIS</span></span>
<span data-ttu-id="23b0e-103">Remova a chave de consulta do serviço pesquisa cognitiva do Azure.</span><span class="sxs-lookup"><span data-stu-id="23b0e-103">Remove the query key from the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="23b0e-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="23b0e-104">SYNTAX</span></span>

### <span data-ttu-id="23b0e-105">ResourceNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="23b0e-105">ResourceNameParameterSet (Default)</span></span>
```
Remove-AzSearchQueryKey [-ResourceGroupName] <String> [-ServiceName] <String> -KeyValue <String> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="23b0e-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="23b0e-106">ParentObjectParameterSet</span></span>
```
Remove-AzSearchQueryKey [-ParentObject] <PSSearchService> -KeyValue <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="23b0e-107">ParentResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="23b0e-107">ParentResourceIdParameterSet</span></span>
```
Remove-AzSearchQueryKey [-ParentResourceId] <String> -KeyValue <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="23b0e-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="23b0e-108">DESCRIPTION</span></span>
<span data-ttu-id="23b0e-109">O cmdlet **Remove-AzSearchQueryKey** remove a chave de consulta do serviço de Pesquisa Cognitiva do Azure.</span><span class="sxs-lookup"><span data-stu-id="23b0e-109">The **Remove-AzSearchQueryKey** cmdlet removes the query key from the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="23b0e-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="23b0e-110">EXAMPLES</span></span>

### <span data-ttu-id="23b0e-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="23b0e-111">Example 1</span></span>
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

<span data-ttu-id="23b0e-112">O exemplo remove a chave de consulta do serviço pesquisa cognitiva do Azure.</span><span class="sxs-lookup"><span data-stu-id="23b0e-112">The example removes the query key from the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="23b0e-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="23b0e-113">PARAMETERS</span></span>

### <span data-ttu-id="23b0e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23b0e-114">-DefaultProfile</span></span>
<span data-ttu-id="23b0e-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="23b0e-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="23b0e-116">-Forçar</span><span class="sxs-lookup"><span data-stu-id="23b0e-116">-Force</span></span>
<span data-ttu-id="23b0e-117">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="23b0e-117">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="23b0e-118">-KeyValue</span><span class="sxs-lookup"><span data-stu-id="23b0e-118">-KeyValue</span></span>
<span data-ttu-id="23b0e-119">Valor da chave de consulta do Serviço de Pesquisa Cognitiva do Azure.</span><span class="sxs-lookup"><span data-stu-id="23b0e-119">Azure Cognitive Search Service query key value.</span></span>

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

### <span data-ttu-id="23b0e-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="23b0e-120">-ParentObject</span></span>
<span data-ttu-id="23b0e-121">Objeto de entrada do Serviço de Pesquisa Cognitiva do Azure.</span><span class="sxs-lookup"><span data-stu-id="23b0e-121">Azure Cognitive Search Service Input Object.</span></span>

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

### <span data-ttu-id="23b0e-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="23b0e-122">-ParentResourceId</span></span>
<span data-ttu-id="23b0e-123">ID do Recurso do Serviço de Pesquisa Cognitiva do Azure.</span><span class="sxs-lookup"><span data-stu-id="23b0e-123">Azure Cognitive Search Service Resource Id.</span></span>

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

### <span data-ttu-id="23b0e-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="23b0e-124">-PassThru</span></span>
<span data-ttu-id="23b0e-125">Este Cmdlet não retorna um objeto por padrão.</span><span class="sxs-lookup"><span data-stu-id="23b0e-125">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="23b0e-126">Se essa opção for especificada, ela retornará verdadeira se for bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="23b0e-126">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="23b0e-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23b0e-127">-ResourceGroupName</span></span>
<span data-ttu-id="23b0e-128">Nome do Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="23b0e-128">Resource Group name.</span></span>

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

### <span data-ttu-id="23b0e-129">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="23b0e-129">-ServiceName</span></span>
<span data-ttu-id="23b0e-130">Nome do Serviço de Pesquisa Cognitiva do Azure.</span><span class="sxs-lookup"><span data-stu-id="23b0e-130">Azure Cognitive Search Service name.</span></span>

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

### <span data-ttu-id="23b0e-131">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="23b0e-131">-Confirm</span></span>
<span data-ttu-id="23b0e-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="23b0e-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="23b0e-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="23b0e-133">-WhatIf</span></span>
<span data-ttu-id="23b0e-134">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="23b0e-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="23b0e-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="23b0e-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="23b0e-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23b0e-136">CommonParameters</span></span>
<span data-ttu-id="23b0e-137">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23b0e-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23b0e-138">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="23b0e-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23b0e-139">Entradas</span><span class="sxs-lookup"><span data-stu-id="23b0e-139">INPUTS</span></span>

### <span data-ttu-id="23b0e-140">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span><span class="sxs-lookup"><span data-stu-id="23b0e-140">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="23b0e-141">System.String</span><span class="sxs-lookup"><span data-stu-id="23b0e-141">System.String</span></span>

## <span data-ttu-id="23b0e-142">Saídas</span><span class="sxs-lookup"><span data-stu-id="23b0e-142">OUTPUTS</span></span>

### <span data-ttu-id="23b0e-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="23b0e-143">System.Boolean</span></span>

## <span data-ttu-id="23b0e-144">Notas</span><span class="sxs-lookup"><span data-stu-id="23b0e-144">NOTES</span></span>

## <span data-ttu-id="23b0e-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="23b0e-145">RELATED LINKS</span></span>

[<span data-ttu-id="23b0e-146">New-AzSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="23b0e-146">New-AzSearchQueryKey.md</span></span>](./New-AzSearchQueryKey.md)

[<span data-ttu-id="23b0e-147">Get-AzSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="23b0e-147">Get-AzSearchQueryKey.md</span></span>](./Get-AzSearchQueryKey.md)
