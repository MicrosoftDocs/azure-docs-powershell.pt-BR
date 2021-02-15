---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/new-azsearchquerykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/New-AzSearchQueryKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/New-AzSearchQueryKey.md
ms.openlocfilehash: 7edca2e338c4972550d44cc6409187dbc53ab40b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114892"
---
# <span data-ttu-id="5cf93-101">New-AzSearchQueryKey</span><span class="sxs-lookup"><span data-stu-id="5cf93-101">New-AzSearchQueryKey</span></span>

## <span data-ttu-id="5cf93-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5cf93-102">SYNOPSIS</span></span>
<span data-ttu-id="5cf93-103">Crie uma nova chave de consulta para o serviço pesquisa cognitiva do Azure.</span><span class="sxs-lookup"><span data-stu-id="5cf93-103">Create a new query key for the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="5cf93-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5cf93-104">SYNTAX</span></span>

### <span data-ttu-id="5cf93-105">ResourceNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="5cf93-105">ResourceNameParameterSet (Default)</span></span>
```
New-AzSearchQueryKey [-ResourceGroupName] <String> [-ServiceName] <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5cf93-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5cf93-106">ParentObjectParameterSet</span></span>
```
New-AzSearchQueryKey [-ParentObject] <PSSearchService> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5cf93-107">ParentResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5cf93-107">ParentResourceIdParameterSet</span></span>
```
New-AzSearchQueryKey [-ParentResourceId] <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5cf93-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="5cf93-108">DESCRIPTION</span></span>
<span data-ttu-id="5cf93-109">O **cmdlet New-AzSearchQueryKey** cria uma nova chave de consulta para o serviço de Pesquisa Cognitiva do Azure.</span><span class="sxs-lookup"><span data-stu-id="5cf93-109">The **New-AzSearchQueryKey** cmdlet creates a new query key for the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="5cf93-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="5cf93-110">EXAMPLES</span></span>

### <span data-ttu-id="5cf93-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="5cf93-111">Example 1</span></span>
```powershell
PS C:\> New-AzSearchQueryKey -ResourceGroupName "TestAzureSearchPsGroup" -ServiceName "pstestazuresearch01" -Name "NewQueryKey1" -Force

Name         Key                             
----         ---                             
NewQueryKey1 65FBCF561228C5F0E01F8F2114C80459
```

<span data-ttu-id="5cf93-112">O exemplo cria uma nova chave de consulta para o serviço pesquisa cognitiva do Azure.</span><span class="sxs-lookup"><span data-stu-id="5cf93-112">The example creates a new query key for the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="5cf93-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5cf93-113">PARAMETERS</span></span>

### <span data-ttu-id="5cf93-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5cf93-114">-DefaultProfile</span></span>
<span data-ttu-id="5cf93-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5cf93-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5cf93-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="5cf93-116">-Name</span></span>
<span data-ttu-id="5cf93-117">Nome da chave da consulta do Serviço de Pesquisa Cognitiva do Azure.</span><span class="sxs-lookup"><span data-stu-id="5cf93-117">Azure Cognitive Search Service query key name.</span></span>

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

### <span data-ttu-id="5cf93-118">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="5cf93-118">-ParentObject</span></span>
<span data-ttu-id="5cf93-119">Objeto de entrada do Serviço de Pesquisa Cognitiva do Azure.</span><span class="sxs-lookup"><span data-stu-id="5cf93-119">Azure Cognitive Search Service Input Object.</span></span>

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

### <span data-ttu-id="5cf93-120">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="5cf93-120">-ParentResourceId</span></span>
<span data-ttu-id="5cf93-121">ID do Recurso do Serviço de Pesquisa Cognitiva do Azure.</span><span class="sxs-lookup"><span data-stu-id="5cf93-121">Azure Cognitive Search Service Resource Id.</span></span>

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

### <span data-ttu-id="5cf93-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5cf93-122">-ResourceGroupName</span></span>
<span data-ttu-id="5cf93-123">Nome do Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="5cf93-123">Resource Group name.</span></span>

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

### <span data-ttu-id="5cf93-124">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="5cf93-124">-ServiceName</span></span>
<span data-ttu-id="5cf93-125">Nome do Serviço de Pesquisa Cognitiva do Azure.</span><span class="sxs-lookup"><span data-stu-id="5cf93-125">Azure Cognitive Search Service name.</span></span>

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

### <span data-ttu-id="5cf93-126">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="5cf93-126">-Confirm</span></span>
<span data-ttu-id="5cf93-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5cf93-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5cf93-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5cf93-128">-WhatIf</span></span>
<span data-ttu-id="5cf93-129">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="5cf93-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5cf93-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5cf93-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5cf93-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5cf93-131">CommonParameters</span></span>
<span data-ttu-id="5cf93-132">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5cf93-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5cf93-133">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5cf93-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5cf93-134">Entradas</span><span class="sxs-lookup"><span data-stu-id="5cf93-134">INPUTS</span></span>

### <span data-ttu-id="5cf93-135">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span><span class="sxs-lookup"><span data-stu-id="5cf93-135">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="5cf93-136">System.String</span><span class="sxs-lookup"><span data-stu-id="5cf93-136">System.String</span></span>

## <span data-ttu-id="5cf93-137">Saídas</span><span class="sxs-lookup"><span data-stu-id="5cf93-137">OUTPUTS</span></span>

### <span data-ttu-id="5cf93-138">Microsoft.Azure.Commands.Management.Search.Models.PSSearchQueryKey</span><span class="sxs-lookup"><span data-stu-id="5cf93-138">Microsoft.Azure.Commands.Management.Search.Models.PSSearchQueryKey</span></span>

## <span data-ttu-id="5cf93-139">Notas</span><span class="sxs-lookup"><span data-stu-id="5cf93-139">NOTES</span></span>

## <span data-ttu-id="5cf93-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5cf93-140">RELATED LINKS</span></span>

[<span data-ttu-id="5cf93-141">Get-AzSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="5cf93-141">Get-AzSearchQueryKey.md</span></span>](./Get-AzSearchQueryKey.md)

[<span data-ttu-id="5cf93-142">Remove-AzSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="5cf93-142">Remove-AzSearchQueryKey.md</span></span>](./Remove-AzSearchQueryKey.md)
