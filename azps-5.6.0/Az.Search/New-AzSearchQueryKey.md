---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/powershell/module/az.search/new-azsearchquerykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/New-AzSearchQueryKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/New-AzSearchQueryKey.md
ms.openlocfilehash: 3c6335264c0d658b0c068efba30c39b4caca407b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887855"
---
# <span data-ttu-id="be1da-101">New-AzSearchQueryKey</span><span class="sxs-lookup"><span data-stu-id="be1da-101">New-AzSearchQueryKey</span></span>

## <span data-ttu-id="be1da-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="be1da-102">SYNOPSIS</span></span>
<span data-ttu-id="be1da-103">Crie uma nova chave de consulta para o serviço de Pesquisa Cognitiva do Azure.</span><span class="sxs-lookup"><span data-stu-id="be1da-103">Create a new query key for the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="be1da-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="be1da-104">SYNTAX</span></span>

### <span data-ttu-id="be1da-105">ResourceNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="be1da-105">ResourceNameParameterSet (Default)</span></span>
```
New-AzSearchQueryKey [-ResourceGroupName] <String> [-ServiceName] <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="be1da-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="be1da-106">ParentObjectParameterSet</span></span>
```
New-AzSearchQueryKey [-ParentObject] <PSSearchService> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="be1da-107">ParentResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="be1da-107">ParentResourceIdParameterSet</span></span>
```
New-AzSearchQueryKey [-ParentResourceId] <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="be1da-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="be1da-108">DESCRIPTION</span></span>
<span data-ttu-id="be1da-109">O cmdlet **New-AzSearchQueryKey** cria uma nova chave de consulta para o serviço de Pesquisa Cognitiva do Azure.</span><span class="sxs-lookup"><span data-stu-id="be1da-109">The **New-AzSearchQueryKey** cmdlet creates a new query key for the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="be1da-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="be1da-110">EXAMPLES</span></span>

### <span data-ttu-id="be1da-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="be1da-111">Example 1</span></span>
```powershell
PS C:\> New-AzSearchQueryKey -ResourceGroupName "TestAzureSearchPsGroup" -ServiceName "pstestazuresearch01" -Name "NewQueryKey1" -Force

Name         Key                             
----         ---                             
NewQueryKey1 65FBCF561228C5F0E01F8F2114C80459
```

<span data-ttu-id="be1da-112">O exemplo cria uma nova chave de consulta para o serviço de Pesquisa Cognitiva do Azure.</span><span class="sxs-lookup"><span data-stu-id="be1da-112">The example creates a new query key for the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="be1da-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="be1da-113">PARAMETERS</span></span>

### <span data-ttu-id="be1da-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be1da-114">-DefaultProfile</span></span>
<span data-ttu-id="be1da-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="be1da-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="be1da-116">-Name</span><span class="sxs-lookup"><span data-stu-id="be1da-116">-Name</span></span>
<span data-ttu-id="be1da-117">Nome da chave de consulta do Serviço de Pesquisa Cognitiva do Azure.</span><span class="sxs-lookup"><span data-stu-id="be1da-117">Azure Cognitive Search Service query key name.</span></span>

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

### <span data-ttu-id="be1da-118">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="be1da-118">-ParentObject</span></span>
<span data-ttu-id="be1da-119">Objeto de entrada do Serviço de Pesquisa Cognitiva do Azure.</span><span class="sxs-lookup"><span data-stu-id="be1da-119">Azure Cognitive Search Service Input Object.</span></span>

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

### <span data-ttu-id="be1da-120">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="be1da-120">-ParentResourceId</span></span>
<span data-ttu-id="be1da-121">ID do Recurso do Serviço de Pesquisa Cognitiva do Azure.</span><span class="sxs-lookup"><span data-stu-id="be1da-121">Azure Cognitive Search Service Resource Id.</span></span>

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

### <span data-ttu-id="be1da-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="be1da-122">-ResourceGroupName</span></span>
<span data-ttu-id="be1da-123">Nome do Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="be1da-123">Resource Group name.</span></span>

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

### <span data-ttu-id="be1da-124">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="be1da-124">-ServiceName</span></span>
<span data-ttu-id="be1da-125">Nome do Serviço de Pesquisa Cognitiva do Azure.</span><span class="sxs-lookup"><span data-stu-id="be1da-125">Azure Cognitive Search Service name.</span></span>

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

### <span data-ttu-id="be1da-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="be1da-126">-Confirm</span></span>
<span data-ttu-id="be1da-127">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="be1da-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="be1da-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="be1da-128">-WhatIf</span></span>
<span data-ttu-id="be1da-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="be1da-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="be1da-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="be1da-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="be1da-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be1da-131">CommonParameters</span></span>
<span data-ttu-id="be1da-132">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="be1da-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be1da-133">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="be1da-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be1da-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="be1da-134">INPUTS</span></span>

### <span data-ttu-id="be1da-135">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span><span class="sxs-lookup"><span data-stu-id="be1da-135">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="be1da-136">System.String</span><span class="sxs-lookup"><span data-stu-id="be1da-136">System.String</span></span>

## <span data-ttu-id="be1da-137">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="be1da-137">OUTPUTS</span></span>

### <span data-ttu-id="be1da-138">Microsoft.Azure.Commands.Management.Search.Models.PSSearchQueryKey</span><span class="sxs-lookup"><span data-stu-id="be1da-138">Microsoft.Azure.Commands.Management.Search.Models.PSSearchQueryKey</span></span>

## <span data-ttu-id="be1da-139">NOTES</span><span class="sxs-lookup"><span data-stu-id="be1da-139">NOTES</span></span>

## <span data-ttu-id="be1da-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="be1da-140">RELATED LINKS</span></span>

[<span data-ttu-id="be1da-141">Get-AzSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="be1da-141">Get-AzSearchQueryKey.md</span></span>](./Get-AzSearchQueryKey.md)

[<span data-ttu-id="be1da-142">Remove-AzSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="be1da-142">Remove-AzSearchQueryKey.md</span></span>](./Remove-AzSearchQueryKey.md)
