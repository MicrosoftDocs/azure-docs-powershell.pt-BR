---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/powershell/module/az.search/get-azsearchadminkeypair
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchAdminKeyPair.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchAdminKeyPair.md
ms.openlocfilehash: bef03e951982854e00412d08c609146b55e54ef3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885516"
---
# <span data-ttu-id="675b8-101">Get-AzSearchAdminKeyPair</span><span class="sxs-lookup"><span data-stu-id="675b8-101">Get-AzSearchAdminKeyPair</span></span>

## <span data-ttu-id="675b8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="675b8-102">SYNOPSIS</span></span>
<span data-ttu-id="675b8-103">Obtém o par de chaves de administrador do serviço de Pesquisa Cognitiva do Azure.</span><span class="sxs-lookup"><span data-stu-id="675b8-103">Gets admin key pair of the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="675b8-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="675b8-104">SYNTAX</span></span>

### <span data-ttu-id="675b8-105">ResourceNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="675b8-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzSearchAdminKeyPair [-ResourceGroupName] <String> [-ServiceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="675b8-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="675b8-106">ParentObjectParameterSet</span></span>
```
Get-AzSearchAdminKeyPair [-ParentObject] <PSSearchService> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="675b8-107">ParentResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="675b8-107">ParentResourceIdParameterSet</span></span>
```
Get-AzSearchAdminKeyPair [-ParentResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="675b8-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="675b8-108">DESCRIPTION</span></span>
<span data-ttu-id="675b8-109">O cmdlet **Get-AzSearchAdminKeyPair** obtém o par de chaves de administrador do serviço de Pesquisa Cognitiva do Azure.</span><span class="sxs-lookup"><span data-stu-id="675b8-109">The **Get-AzSearchAdminKeyPair** cmdlet gets the admin key pair of the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="675b8-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="675b8-110">EXAMPLES</span></span>

### <span data-ttu-id="675b8-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="675b8-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSearchAdminKeyPair -ResourceGroupName felixwa-01 -ServiceName felixwa-basic-search

Primary                          Secondary                       
-------                          ---------                       
3B06A25BDADFF72EC132736BAA2547A1 E643B75A52E04DF13EB690807C451C55
```

<span data-ttu-id="675b8-112">O exemplo obtém o par de chaves de administrador do serviço de Pesquisa Cognitiva do Azure.</span><span class="sxs-lookup"><span data-stu-id="675b8-112">The example gets admin key pair of the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="675b8-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="675b8-113">PARAMETERS</span></span>

### <span data-ttu-id="675b8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="675b8-114">-DefaultProfile</span></span>
<span data-ttu-id="675b8-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="675b8-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="675b8-116">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="675b8-116">-ParentObject</span></span>
<span data-ttu-id="675b8-117">Objeto de entrada do Serviço de Pesquisa Cognitiva do Azure.</span><span class="sxs-lookup"><span data-stu-id="675b8-117">Azure Cognitive Search Service Input Object.</span></span>

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

### <span data-ttu-id="675b8-118">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="675b8-118">-ParentResourceId</span></span>
<span data-ttu-id="675b8-119">ID do Recurso do Serviço de Pesquisa Cognitiva do Azure.</span><span class="sxs-lookup"><span data-stu-id="675b8-119">Azure Cognitive Search Service Resource Id.</span></span>

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

### <span data-ttu-id="675b8-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="675b8-120">-ResourceGroupName</span></span>
<span data-ttu-id="675b8-121">Nome do Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="675b8-121">Resource Group name.</span></span>

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

### <span data-ttu-id="675b8-122">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="675b8-122">-ServiceName</span></span>
<span data-ttu-id="675b8-123">Nome do Serviço de Pesquisa Cognitiva do Azure.</span><span class="sxs-lookup"><span data-stu-id="675b8-123">Azure Cognitive Search Service name.</span></span>

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

### <span data-ttu-id="675b8-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="675b8-124">CommonParameters</span></span>
<span data-ttu-id="675b8-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="675b8-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="675b8-126">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="675b8-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="675b8-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="675b8-127">INPUTS</span></span>

### <span data-ttu-id="675b8-128">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span><span class="sxs-lookup"><span data-stu-id="675b8-128">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="675b8-129">System.String</span><span class="sxs-lookup"><span data-stu-id="675b8-129">System.String</span></span>

## <span data-ttu-id="675b8-130">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="675b8-130">OUTPUTS</span></span>

### <span data-ttu-id="675b8-131">Microsoft.Azure.Commands.Management.Search.Models.PSSearchAdminKey</span><span class="sxs-lookup"><span data-stu-id="675b8-131">Microsoft.Azure.Commands.Management.Search.Models.PSSearchAdminKey</span></span>

## <span data-ttu-id="675b8-132">NOTES</span><span class="sxs-lookup"><span data-stu-id="675b8-132">NOTES</span></span>

## <span data-ttu-id="675b8-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="675b8-133">RELATED LINKS</span></span>

[<span data-ttu-id="675b8-134">New-AzSearchAdminKey</span><span class="sxs-lookup"><span data-stu-id="675b8-134">New-AzSearchAdminKey</span></span>](./New-AzSearchAdminKey.md)
