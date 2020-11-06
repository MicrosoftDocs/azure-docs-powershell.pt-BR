---
external help file: Microsoft.Azure.Commands.Management.Search.dll-Help.xml
Module Name: AzureRM.Search
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.search/new-azurermsearchquerykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Search/Commands.Management.Search/help/New-AzureRmSearchQueryKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Search/Commands.Management.Search/help/New-AzureRmSearchQueryKey.md
ms.openlocfilehash: 417e1a546777824df86b72f3740079ac91835192
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432264"
---
# <span data-ttu-id="8432d-101">New-AzureRmSearchQueryKey</span><span class="sxs-lookup"><span data-stu-id="8432d-101">New-AzureRmSearchQueryKey</span></span>

## <span data-ttu-id="8432d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8432d-102">SYNOPSIS</span></span>
<span data-ttu-id="8432d-103">Crie uma nova chave de consulta para o serviço de pesquisa do Azure.</span><span class="sxs-lookup"><span data-stu-id="8432d-103">Create a new query key for the Azure Search service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8432d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8432d-104">SYNTAX</span></span>

### <span data-ttu-id="8432d-105">ResourceNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="8432d-105">ResourceNameParameterSet (Default)</span></span>
```
New-AzureRmSearchQueryKey [-ResourceGroupName] <String> [-ServiceName] <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8432d-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8432d-106">ParentObjectParameterSet</span></span>
```
New-AzureRmSearchQueryKey [-ParentObject] <PSSearchService> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8432d-107">ParentResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8432d-107">ParentResourceIdParameterSet</span></span>
```
New-AzureRmSearchQueryKey [-ParentResourceId] <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8432d-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8432d-108">DESCRIPTION</span></span>
<span data-ttu-id="8432d-109">O cmdlet **New-AzureRmSearchQueryKey** cria uma nova chave de consulta para o serviço de pesquisa do Azure.</span><span class="sxs-lookup"><span data-stu-id="8432d-109">The **New-AzureRmSearchQueryKey** cmdlet creates a new query key for the Azure Search Service.</span></span>

## <span data-ttu-id="8432d-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8432d-110">EXAMPLES</span></span>

### <span data-ttu-id="8432d-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="8432d-111">Example 1</span></span>
```powershell
PS C:\> New-AzureRmSearchQueryKey -ResourceGroupName "TestAzureSearchPsGroup" -ServiceName "pstestazuresearch01" -Name "NewQueryKey1" -Force

Name         Key                             
----         ---                             
NewQueryKey1 65FBCF561228C5F0E01F8F2114C80459
```

<span data-ttu-id="8432d-112">O exemplo cria uma nova chave de consulta para o serviço de pesquisa do Azure.</span><span class="sxs-lookup"><span data-stu-id="8432d-112">The example creates a new query key for the Azure Search service.</span></span>

## <span data-ttu-id="8432d-113">OS</span><span class="sxs-lookup"><span data-stu-id="8432d-113">PARAMETERS</span></span>

### <span data-ttu-id="8432d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8432d-114">-DefaultProfile</span></span>
<span data-ttu-id="8432d-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8432d-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8432d-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="8432d-116">-Name</span></span>
<span data-ttu-id="8432d-117">Nome da chave de consulta do serviço de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="8432d-117">Search Service query key name.</span></span>

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

### <span data-ttu-id="8432d-118">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="8432d-118">-ParentObject</span></span>
<span data-ttu-id="8432d-119">Objeto de entrada do serviço de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="8432d-119">Search Service Input Object.</span></span>

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

### <span data-ttu-id="8432d-120">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="8432d-120">-ParentResourceId</span></span>
<span data-ttu-id="8432d-121">ID do recurso do serviço de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="8432d-121">Search Service Resource Id.</span></span>

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

### <span data-ttu-id="8432d-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8432d-122">-ResourceGroupName</span></span>
<span data-ttu-id="8432d-123">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="8432d-123">Resource Group name.</span></span>

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

### <span data-ttu-id="8432d-124">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="8432d-124">-ServiceName</span></span>
<span data-ttu-id="8432d-125">Nome do serviço de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="8432d-125">Search Service name.</span></span>

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

### <span data-ttu-id="8432d-126">-Confirme</span><span class="sxs-lookup"><span data-stu-id="8432d-126">-Confirm</span></span>
<span data-ttu-id="8432d-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8432d-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8432d-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8432d-128">-WhatIf</span></span>
<span data-ttu-id="8432d-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="8432d-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8432d-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8432d-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8432d-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8432d-131">CommonParameters</span></span>
<span data-ttu-id="8432d-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8432d-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8432d-133">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8432d-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8432d-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8432d-134">INPUTS</span></span>

### <span data-ttu-id="8432d-135">Microsoft. Azure. Commands. Management. Search. Models. PSSearchService</span><span class="sxs-lookup"><span data-stu-id="8432d-135">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>
<span data-ttu-id="8432d-136">Parâmetros: ParentObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="8432d-136">Parameters: ParentObject (ByValue)</span></span>

### <span data-ttu-id="8432d-137">System. String</span><span class="sxs-lookup"><span data-stu-id="8432d-137">System.String</span></span>

## <span data-ttu-id="8432d-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8432d-138">OUTPUTS</span></span>

### <span data-ttu-id="8432d-139">Microsoft. Azure. Commands. Management. Search. Models. PSSearchQueryKey</span><span class="sxs-lookup"><span data-stu-id="8432d-139">Microsoft.Azure.Commands.Management.Search.Models.PSSearchQueryKey</span></span>

## <span data-ttu-id="8432d-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8432d-140">NOTES</span></span>

## <span data-ttu-id="8432d-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8432d-141">RELATED LINKS</span></span>

[<span data-ttu-id="8432d-142">Get-AzureRmSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="8432d-142">Get-AzureRmSearchQueryKey.md</span></span>](./Get-AzureRmSearchQueryKey.md)

[<span data-ttu-id="8432d-143">Remove-AzureRmSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="8432d-143">Remove-AzureRmSearchQueryKey.md</span></span>](./Remove-AzureRmSearchQueryKey.md)
