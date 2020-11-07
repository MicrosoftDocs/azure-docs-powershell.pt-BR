---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/new-azsearchadminkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/New-AzSearchAdminKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/New-AzSearchAdminKey.md
ms.openlocfilehash: ddc47a08c7042b61bd77433adb8a10a7f39e8f00
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93773276"
---
# <span data-ttu-id="8162a-101">New-AzSearchAdminKey</span><span class="sxs-lookup"><span data-stu-id="8162a-101">New-AzSearchAdminKey</span></span>

## <span data-ttu-id="8162a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8162a-102">SYNOPSIS</span></span>
<span data-ttu-id="8162a-103">Regenera a chave de administração do serviço de pesquisa do Azure.</span><span class="sxs-lookup"><span data-stu-id="8162a-103">Regenerates an admin key of the Azure Search service.</span></span>

## <span data-ttu-id="8162a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8162a-104">SYNTAX</span></span>

### <span data-ttu-id="8162a-105">ResourceNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="8162a-105">ResourceNameParameterSet (Default)</span></span>
```
New-AzSearchAdminKey [-ResourceGroupName] <String> [-ServiceName] <String> -KeyKind <PSSearchAdminKeyKind>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8162a-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8162a-106">ParentObjectParameterSet</span></span>
```
New-AzSearchAdminKey [-ParentObject] <PSSearchService> -KeyKind <PSSearchAdminKeyKind> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8162a-107">ParentResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8162a-107">ParentResourceIdParameterSet</span></span>
```
New-AzSearchAdminKey [-ParentResourceId] <String> -KeyKind <PSSearchAdminKeyKind> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8162a-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8162a-108">DESCRIPTION</span></span>
<span data-ttu-id="8162a-109">O cmdlet **New-AzSearchAdminKey** regenera uma chave de administração do serviço de pesquisa do Azure.</span><span class="sxs-lookup"><span data-stu-id="8162a-109">The **New-AzSearchAdminKey** cmdlet regenerates an admin key of the Azure Search service.</span></span>

## <span data-ttu-id="8162a-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8162a-110">EXAMPLES</span></span>

### <span data-ttu-id="8162a-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="8162a-111">Example 1</span></span>
```powershell
PS C:\> New-AzSearchAdminKey -ResourceGroupName "TestAzureSearchPsGroup" -ServiceName "pstestazuresearch01" -KeyKind Primary

Confirm
Are you sure you want to regenerate 'Primary' key for Search Service 'pstestazuresearch01'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y

Primary                          Secondary
-------                          ---------
85B3813D11904B591BE8A196C2C743A1 CEF791D5BAC2E6C0B232C56702F21E87
```

<span data-ttu-id="8162a-112">O exemplo regenera a chave primária do serviço de pesquisa do Azure.</span><span class="sxs-lookup"><span data-stu-id="8162a-112">The example regenerates Primary key of the Azure Search Service.</span></span>

## <span data-ttu-id="8162a-113">OS</span><span class="sxs-lookup"><span data-stu-id="8162a-113">PARAMETERS</span></span>

### <span data-ttu-id="8162a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8162a-114">-DefaultProfile</span></span>
<span data-ttu-id="8162a-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8162a-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8162a-116">-Force</span><span class="sxs-lookup"><span data-stu-id="8162a-116">-Force</span></span>
<span data-ttu-id="8162a-117">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="8162a-117">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="8162a-118">-Keykind</span><span class="sxs-lookup"><span data-stu-id="8162a-118">-KeyKind</span></span>
<span data-ttu-id="8162a-119">Tipo de chave de administração do serviço de pesquisa (principal/secundário).</span><span class="sxs-lookup"><span data-stu-id="8162a-119">Search Service admin key kind (Primary/Secondary).</span></span>

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

### <span data-ttu-id="8162a-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="8162a-120">-ParentObject</span></span>
<span data-ttu-id="8162a-121">Objeto de entrada do serviço de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="8162a-121">Search Service Input Object.</span></span>

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

### <span data-ttu-id="8162a-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="8162a-122">-ParentResourceId</span></span>
<span data-ttu-id="8162a-123">ID do recurso do serviço de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="8162a-123">Search Service Resource Id.</span></span>

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

### <span data-ttu-id="8162a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8162a-124">-ResourceGroupName</span></span>
<span data-ttu-id="8162a-125">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="8162a-125">Resource Group name.</span></span>

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

### <span data-ttu-id="8162a-126">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="8162a-126">-ServiceName</span></span>
<span data-ttu-id="8162a-127">Nome do serviço de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="8162a-127">Search Service name.</span></span>

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

### <span data-ttu-id="8162a-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="8162a-128">-Confirm</span></span>
<span data-ttu-id="8162a-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8162a-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8162a-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8162a-130">-WhatIf</span></span>
<span data-ttu-id="8162a-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="8162a-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8162a-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8162a-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8162a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8162a-133">CommonParameters</span></span>
<span data-ttu-id="8162a-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8162a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8162a-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8162a-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8162a-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8162a-136">INPUTS</span></span>

### <span data-ttu-id="8162a-137">Microsoft. Azure. Commands. Management. Search. Models. PSSearchService</span><span class="sxs-lookup"><span data-stu-id="8162a-137">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="8162a-138">System. String</span><span class="sxs-lookup"><span data-stu-id="8162a-138">System.String</span></span>

## <span data-ttu-id="8162a-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8162a-139">OUTPUTS</span></span>

### <span data-ttu-id="8162a-140">Microsoft. Azure. Commands. Management. Search. Models. PSSearchAdminKey</span><span class="sxs-lookup"><span data-stu-id="8162a-140">Microsoft.Azure.Commands.Management.Search.Models.PSSearchAdminKey</span></span>

## <span data-ttu-id="8162a-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8162a-141">NOTES</span></span>

## <span data-ttu-id="8162a-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8162a-142">RELATED LINKS</span></span>

[<span data-ttu-id="8162a-143">Get-AzSearchAdminKeyPair</span><span class="sxs-lookup"><span data-stu-id="8162a-143">Get-AzSearchAdminKeyPair</span></span>](./Get-AzSearchAdminKeyPair.md)
