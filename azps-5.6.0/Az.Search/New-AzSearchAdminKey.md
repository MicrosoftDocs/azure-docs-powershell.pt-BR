---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/powershell/module/az.search/new-azsearchadminkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/New-AzSearchAdminKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/New-AzSearchAdminKey.md
ms.openlocfilehash: 4724b24f995b836bbd63420c852d6f0004089a51
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890345"
---
# <span data-ttu-id="df9f2-101">New-AzSearchAdminKey</span><span class="sxs-lookup"><span data-stu-id="df9f2-101">New-AzSearchAdminKey</span></span>

## <span data-ttu-id="df9f2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="df9f2-102">SYNOPSIS</span></span>
<span data-ttu-id="df9f2-103">Regenera uma chave de administrador do serviço de Pesquisa Cognitiva do Azure.</span><span class="sxs-lookup"><span data-stu-id="df9f2-103">Regenerates an admin key of the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="df9f2-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="df9f2-104">SYNTAX</span></span>

### <span data-ttu-id="df9f2-105">ResourceNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="df9f2-105">ResourceNameParameterSet (Default)</span></span>
```
New-AzSearchAdminKey [-ResourceGroupName] <String> [-ServiceName] <String> -KeyKind <PSSearchAdminKeyKind>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="df9f2-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="df9f2-106">ParentObjectParameterSet</span></span>
```
New-AzSearchAdminKey [-ParentObject] <PSSearchService> -KeyKind <PSSearchAdminKeyKind> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="df9f2-107">ParentResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="df9f2-107">ParentResourceIdParameterSet</span></span>
```
New-AzSearchAdminKey [-ParentResourceId] <String> -KeyKind <PSSearchAdminKeyKind> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="df9f2-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="df9f2-108">DESCRIPTION</span></span>
<span data-ttu-id="df9f2-109">O cmdlet **New-AzSearchAdminKey** regenera uma chave de administrador do serviço de Pesquisa Cognitiva do Azure.</span><span class="sxs-lookup"><span data-stu-id="df9f2-109">The **New-AzSearchAdminKey** cmdlet regenerates an admin key of the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="df9f2-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="df9f2-110">EXAMPLES</span></span>

### <span data-ttu-id="df9f2-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="df9f2-111">Example 1</span></span>
```powershell
PS C:\> New-AzSearchAdminKey -ResourceGroupName "TestAzureSearchPsGroup" -ServiceName "pstestazuresearch01" -KeyKind Primary

Confirm
Are you sure you want to regenerate 'Primary' key for Search Service 'pstestazuresearch01'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y

Primary                          Secondary
-------                          ---------
85B3813D11904B591BE8A196C2C743A1 CEF791D5BAC2E6C0B232C56702F21E87
```

<span data-ttu-id="df9f2-112">O exemplo regenera a chave primária do serviço de Pesquisa Cognitiva do Azure.</span><span class="sxs-lookup"><span data-stu-id="df9f2-112">The example regenerates Primary key of the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="df9f2-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="df9f2-113">PARAMETERS</span></span>

### <span data-ttu-id="df9f2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df9f2-114">-DefaultProfile</span></span>
<span data-ttu-id="df9f2-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="df9f2-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="df9f2-116">-Force</span><span class="sxs-lookup"><span data-stu-id="df9f2-116">-Force</span></span>
<span data-ttu-id="df9f2-117">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="df9f2-117">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="df9f2-118">-KeyKind</span><span class="sxs-lookup"><span data-stu-id="df9f2-118">-KeyKind</span></span>
<span data-ttu-id="df9f2-119">Tipo de chave de administrador do Serviço de Pesquisa Cognitiva do Azure (Primário/Secundário).</span><span class="sxs-lookup"><span data-stu-id="df9f2-119">Azure Cognitive Search Service admin key kind (Primary/Secondary).</span></span>

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

### <span data-ttu-id="df9f2-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="df9f2-120">-ParentObject</span></span>
<span data-ttu-id="df9f2-121">Objeto de entrada do Serviço de Pesquisa Cognitiva do Azure.</span><span class="sxs-lookup"><span data-stu-id="df9f2-121">Azure Cognitive Search Service Input Object.</span></span>

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

### <span data-ttu-id="df9f2-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="df9f2-122">-ParentResourceId</span></span>
<span data-ttu-id="df9f2-123">ID do Recurso do Serviço de Pesquisa Cognitiva do Azure.</span><span class="sxs-lookup"><span data-stu-id="df9f2-123">Azure Cognitive Search Service Resource Id.</span></span>

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

### <span data-ttu-id="df9f2-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df9f2-124">-ResourceGroupName</span></span>
<span data-ttu-id="df9f2-125">Nome do Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="df9f2-125">Resource Group name.</span></span>

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

### <span data-ttu-id="df9f2-126">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="df9f2-126">-ServiceName</span></span>
<span data-ttu-id="df9f2-127">Nome do Serviço de Pesquisa Cognitiva do Azure.</span><span class="sxs-lookup"><span data-stu-id="df9f2-127">Azure Cognitive Search Service name.</span></span>

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

### <span data-ttu-id="df9f2-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="df9f2-128">-Confirm</span></span>
<span data-ttu-id="df9f2-129">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="df9f2-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="df9f2-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="df9f2-130">-WhatIf</span></span>
<span data-ttu-id="df9f2-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="df9f2-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="df9f2-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="df9f2-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="df9f2-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df9f2-133">CommonParameters</span></span>
<span data-ttu-id="df9f2-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df9f2-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df9f2-135">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="df9f2-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df9f2-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="df9f2-136">INPUTS</span></span>

### <span data-ttu-id="df9f2-137">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span><span class="sxs-lookup"><span data-stu-id="df9f2-137">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="df9f2-138">System.String</span><span class="sxs-lookup"><span data-stu-id="df9f2-138">System.String</span></span>

## <span data-ttu-id="df9f2-139">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="df9f2-139">OUTPUTS</span></span>

### <span data-ttu-id="df9f2-140">Microsoft.Azure.Commands.Management.Search.Models.PSSearchAdminKey</span><span class="sxs-lookup"><span data-stu-id="df9f2-140">Microsoft.Azure.Commands.Management.Search.Models.PSSearchAdminKey</span></span>

## <span data-ttu-id="df9f2-141">NOTES</span><span class="sxs-lookup"><span data-stu-id="df9f2-141">NOTES</span></span>

## <span data-ttu-id="df9f2-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="df9f2-142">RELATED LINKS</span></span>

[<span data-ttu-id="df9f2-143">Get-AzSearchAdminKeyPair</span><span class="sxs-lookup"><span data-stu-id="df9f2-143">Get-AzSearchAdminKeyPair</span></span>](./Get-AzSearchAdminKeyPair.md)
