---
external help file: Microsoft.Azure.Commands.Management.Search.dll-Help.xml
Module Name: AzureRM.Search
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.search/new-azurermsearchadminkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Search/Commands.Management.Search/help/New-AzureRmSearchAdminKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Search/Commands.Management.Search/help/New-AzureRmSearchAdminKey.md
ms.openlocfilehash: fa7ea6f1e53b94a349d51856432f1c01b2e89ba0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93603131"
---
# <span data-ttu-id="a6404-101">New-AzureRmSearchAdminKey</span><span class="sxs-lookup"><span data-stu-id="a6404-101">New-AzureRmSearchAdminKey</span></span>

## <span data-ttu-id="a6404-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a6404-102">SYNOPSIS</span></span>
<span data-ttu-id="a6404-103">Regenera a chave de administração do serviço de pesquisa do Azure.</span><span class="sxs-lookup"><span data-stu-id="a6404-103">Regenerates an admin key of the Azure Search service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a6404-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a6404-104">SYNTAX</span></span>

### <span data-ttu-id="a6404-105">ResourceNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="a6404-105">ResourceNameParameterSet (Default)</span></span>
```
New-AzureRmSearchAdminKey [-ResourceGroupName] <String> [-ServiceName] <String> -KeyKind <PSSearchAdminKeyKind>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a6404-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a6404-106">ParentObjectParameterSet</span></span>
```
New-AzureRmSearchAdminKey [-ParentObject] <PSSearchService> -KeyKind <PSSearchAdminKeyKind> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a6404-107">ParentResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a6404-107">ParentResourceIdParameterSet</span></span>
```
New-AzureRmSearchAdminKey [-ParentResourceId] <String> -KeyKind <PSSearchAdminKeyKind> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a6404-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a6404-108">DESCRIPTION</span></span>
<span data-ttu-id="a6404-109">O cmdlet **New-AzureRmSearchAdminKey** regenera uma chave de administração do serviço de pesquisa do Azure.</span><span class="sxs-lookup"><span data-stu-id="a6404-109">The **New-AzureRmSearchAdminKey** cmdlet regenerates an admin key of the Azure Search service.</span></span>

## <span data-ttu-id="a6404-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a6404-110">EXAMPLES</span></span>

### <span data-ttu-id="a6404-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a6404-111">Example 1</span></span>
```powershell
PS C:\> New-AzureRmSearchAdminKey -ResourceGroupName "TestAzureSearchPsGroup" -ServiceName "pstestazuresearch01" -KeyKind Primary

Confirm
Are you sure you want to regenerate 'Primary' key for Search Service 'pstestazuresearch01'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y

Primary                          Secondary
-------                          ---------
85B3813D11904B591BE8A196C2C743A1 CEF791D5BAC2E6C0B232C56702F21E87
```

<span data-ttu-id="a6404-112">O exemplo regenera a chave primária do serviço de pesquisa do Azure.</span><span class="sxs-lookup"><span data-stu-id="a6404-112">The example regenerates Primary key of the Azure Search Service.</span></span>

## <span data-ttu-id="a6404-113">OS</span><span class="sxs-lookup"><span data-stu-id="a6404-113">PARAMETERS</span></span>

### <span data-ttu-id="a6404-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6404-114">-DefaultProfile</span></span>
<span data-ttu-id="a6404-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a6404-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a6404-116">-Force</span><span class="sxs-lookup"><span data-stu-id="a6404-116">-Force</span></span>
<span data-ttu-id="a6404-117">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="a6404-117">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="a6404-118">-Keykind</span><span class="sxs-lookup"><span data-stu-id="a6404-118">-KeyKind</span></span>
<span data-ttu-id="a6404-119">Tipo de chave de administração do serviço de pesquisa (principal/secundário).</span><span class="sxs-lookup"><span data-stu-id="a6404-119">Search Service admin key kind (Primary/Secondary).</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Search.Models.PSSearchAdminKeyKind
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6404-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="a6404-120">-ParentObject</span></span>
<span data-ttu-id="a6404-121">Objeto de entrada do serviço de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="a6404-121">Search Service Input Object.</span></span>

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

### <span data-ttu-id="a6404-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="a6404-122">-ParentResourceId</span></span>
<span data-ttu-id="a6404-123">ID do recurso do serviço de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="a6404-123">Search Service Resource Id.</span></span>

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

### <span data-ttu-id="a6404-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6404-124">-ResourceGroupName</span></span>
<span data-ttu-id="a6404-125">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a6404-125">Resource Group name.</span></span>

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

### <span data-ttu-id="a6404-126">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="a6404-126">-ServiceName</span></span>
<span data-ttu-id="a6404-127">Nome do serviço de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="a6404-127">Search Service name.</span></span>

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

### <span data-ttu-id="a6404-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="a6404-128">-Confirm</span></span>
<span data-ttu-id="a6404-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a6404-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a6404-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a6404-130">-WhatIf</span></span>
<span data-ttu-id="a6404-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a6404-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a6404-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a6404-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a6404-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6404-133">CommonParameters</span></span>
<span data-ttu-id="a6404-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6404-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6404-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a6404-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6404-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a6404-136">INPUTS</span></span>

### <span data-ttu-id="a6404-137">Microsoft. Azure. Commands. Management. Search. Models. PSSearchService</span><span class="sxs-lookup"><span data-stu-id="a6404-137">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>
<span data-ttu-id="a6404-138">Parâmetros: ParentObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="a6404-138">Parameters: ParentObject (ByValue)</span></span>

### <span data-ttu-id="a6404-139">System. String</span><span class="sxs-lookup"><span data-stu-id="a6404-139">System.String</span></span>

## <span data-ttu-id="a6404-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a6404-140">OUTPUTS</span></span>

### <span data-ttu-id="a6404-141">Microsoft. Azure. Commands. Management. Search. Models. PSSearchAdminKey</span><span class="sxs-lookup"><span data-stu-id="a6404-141">Microsoft.Azure.Commands.Management.Search.Models.PSSearchAdminKey</span></span>

## <span data-ttu-id="a6404-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a6404-142">NOTES</span></span>

## <span data-ttu-id="a6404-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a6404-143">RELATED LINKS</span></span>

[<span data-ttu-id="a6404-144">Get-AzureRmSearchAdminKeyPair</span><span class="sxs-lookup"><span data-stu-id="a6404-144">Get-AzureRmSearchAdminKeyPair</span></span>](./Get-AzureRmSearchAdminKeyPair.md)
