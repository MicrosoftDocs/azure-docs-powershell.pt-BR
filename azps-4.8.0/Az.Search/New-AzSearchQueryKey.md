---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/new-azsearchquerykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/New-AzSearchQueryKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/New-AzSearchQueryKey.md
ms.openlocfilehash: e01e5e244bd34e3e18aa287e0f2f5709c5e208ec
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94110909"
---
# <span data-ttu-id="b38d9-101">New-AzSearchQueryKey</span><span class="sxs-lookup"><span data-stu-id="b38d9-101">New-AzSearchQueryKey</span></span>

## <span data-ttu-id="b38d9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b38d9-102">SYNOPSIS</span></span>
<span data-ttu-id="b38d9-103">Crie uma nova chave de consulta para o serviço de pesquisa do Azure.</span><span class="sxs-lookup"><span data-stu-id="b38d9-103">Create a new query key for the Azure Search service.</span></span>

## <span data-ttu-id="b38d9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b38d9-104">SYNTAX</span></span>

### <span data-ttu-id="b38d9-105">ResourceNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="b38d9-105">ResourceNameParameterSet (Default)</span></span>
```
New-AzSearchQueryKey [-ResourceGroupName] <String> [-ServiceName] <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b38d9-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b38d9-106">ParentObjectParameterSet</span></span>
```
New-AzSearchQueryKey [-ParentObject] <PSSearchService> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b38d9-107">ParentResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b38d9-107">ParentResourceIdParameterSet</span></span>
```
New-AzSearchQueryKey [-ParentResourceId] <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b38d9-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b38d9-108">DESCRIPTION</span></span>
<span data-ttu-id="b38d9-109">O cmdlet **New-AzSearchQueryKey** cria uma nova chave de consulta para o serviço de pesquisa do Azure.</span><span class="sxs-lookup"><span data-stu-id="b38d9-109">The **New-AzSearchQueryKey** cmdlet creates a new query key for the Azure Search Service.</span></span>

## <span data-ttu-id="b38d9-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b38d9-110">EXAMPLES</span></span>

### <span data-ttu-id="b38d9-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b38d9-111">Example 1</span></span>
```powershell
PS C:\> New-AzSearchQueryKey -ResourceGroupName "TestAzureSearchPsGroup" -ServiceName "pstestazuresearch01" -Name "NewQueryKey1" -Force

Name         Key                             
----         ---                             
NewQueryKey1 65FBCF561228C5F0E01F8F2114C80459
```

<span data-ttu-id="b38d9-112">O exemplo cria uma nova chave de consulta para o serviço de pesquisa do Azure.</span><span class="sxs-lookup"><span data-stu-id="b38d9-112">The example creates a new query key for the Azure Search service.</span></span>

## <span data-ttu-id="b38d9-113">OS</span><span class="sxs-lookup"><span data-stu-id="b38d9-113">PARAMETERS</span></span>

### <span data-ttu-id="b38d9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b38d9-114">-DefaultProfile</span></span>
<span data-ttu-id="b38d9-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b38d9-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b38d9-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="b38d9-116">-Name</span></span>
<span data-ttu-id="b38d9-117">Nome da chave de consulta do serviço de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="b38d9-117">Search Service query key name.</span></span>

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

### <span data-ttu-id="b38d9-118">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="b38d9-118">-ParentObject</span></span>
<span data-ttu-id="b38d9-119">Objeto de entrada do serviço de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="b38d9-119">Search Service Input Object.</span></span>

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

### <span data-ttu-id="b38d9-120">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="b38d9-120">-ParentResourceId</span></span>
<span data-ttu-id="b38d9-121">ID do recurso do serviço de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="b38d9-121">Search Service Resource Id.</span></span>

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

### <span data-ttu-id="b38d9-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b38d9-122">-ResourceGroupName</span></span>
<span data-ttu-id="b38d9-123">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b38d9-123">Resource Group name.</span></span>

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

### <span data-ttu-id="b38d9-124">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="b38d9-124">-ServiceName</span></span>
<span data-ttu-id="b38d9-125">Nome do serviço de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="b38d9-125">Search Service name.</span></span>

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

### <span data-ttu-id="b38d9-126">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b38d9-126">-Confirm</span></span>
<span data-ttu-id="b38d9-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b38d9-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b38d9-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b38d9-128">-WhatIf</span></span>
<span data-ttu-id="b38d9-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b38d9-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b38d9-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b38d9-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b38d9-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b38d9-131">CommonParameters</span></span>
<span data-ttu-id="b38d9-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b38d9-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b38d9-133">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b38d9-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b38d9-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b38d9-134">INPUTS</span></span>

### <span data-ttu-id="b38d9-135">Microsoft. Azure. Commands. Management. Search. Models. PSSearchService</span><span class="sxs-lookup"><span data-stu-id="b38d9-135">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="b38d9-136">System. String</span><span class="sxs-lookup"><span data-stu-id="b38d9-136">System.String</span></span>

## <span data-ttu-id="b38d9-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b38d9-137">OUTPUTS</span></span>

### <span data-ttu-id="b38d9-138">Microsoft. Azure. Commands. Management. Search. Models. PSSearchQueryKey</span><span class="sxs-lookup"><span data-stu-id="b38d9-138">Microsoft.Azure.Commands.Management.Search.Models.PSSearchQueryKey</span></span>

## <span data-ttu-id="b38d9-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b38d9-139">NOTES</span></span>

## <span data-ttu-id="b38d9-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b38d9-140">RELATED LINKS</span></span>

[<span data-ttu-id="b38d9-141">Get-AzSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="b38d9-141">Get-AzSearchQueryKey.md</span></span>](./Get-AzSearchQueryKey.md)

[<span data-ttu-id="b38d9-142">Remove-AzSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="b38d9-142">Remove-AzSearchQueryKey.md</span></span>](./Remove-AzSearchQueryKey.md)
