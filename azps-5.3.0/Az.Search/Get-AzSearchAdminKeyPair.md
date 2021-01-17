---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/get-azsearchadminkeypair
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchAdminKeyPair.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchAdminKeyPair.md
ms.openlocfilehash: dafc9da9669a7c07f982e4fee87a37e1581af40a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98428001"
---
# <span data-ttu-id="3f049-101">Get-AzSearchAdminKeyPair</span><span class="sxs-lookup"><span data-stu-id="3f049-101">Get-AzSearchAdminKeyPair</span></span>

## <span data-ttu-id="3f049-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3f049-102">SYNOPSIS</span></span>
<span data-ttu-id="3f049-103">Obtém o par de chave de administração do serviço de pesquisa do Azure.</span><span class="sxs-lookup"><span data-stu-id="3f049-103">Gets admin key pair of the Azure Search service.</span></span>

## <span data-ttu-id="3f049-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3f049-104">SYNTAX</span></span>

### <span data-ttu-id="3f049-105">ResourceNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="3f049-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzSearchAdminKeyPair [-ResourceGroupName] <String> [-ServiceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3f049-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3f049-106">ParentObjectParameterSet</span></span>
```
Get-AzSearchAdminKeyPair [-ParentObject] <PSSearchService> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3f049-107">ParentResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3f049-107">ParentResourceIdParameterSet</span></span>
```
Get-AzSearchAdminKeyPair [-ParentResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3f049-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3f049-108">DESCRIPTION</span></span>
<span data-ttu-id="3f049-109">O cmdlet **Get-AzSearchAdminKeyPair** Obtém o par de chave de administração do serviço de pesquisa do Azure.</span><span class="sxs-lookup"><span data-stu-id="3f049-109">The **Get-AzSearchAdminKeyPair** cmdlet gets the admin key pair of the Azure Search service.</span></span>

## <span data-ttu-id="3f049-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3f049-110">EXAMPLES</span></span>

### <span data-ttu-id="3f049-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="3f049-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSearchAdminKeyPair -ResourceGroupName felixwa-01 -ServiceName felixwa-basic-search

Primary                          Secondary                       
-------                          ---------                       
3B06A25BDADFF72EC132736BAA2547A1 E643B75A52E04DF13EB690807C451C55
```

<span data-ttu-id="3f049-112">O exemplo obtém o par de chave de administração do serviço de pesquisa do Azure.</span><span class="sxs-lookup"><span data-stu-id="3f049-112">The example gets admin key pair of the Azure Search service.</span></span>

## <span data-ttu-id="3f049-113">OS</span><span class="sxs-lookup"><span data-stu-id="3f049-113">PARAMETERS</span></span>

### <span data-ttu-id="3f049-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f049-114">-DefaultProfile</span></span>
<span data-ttu-id="3f049-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3f049-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3f049-116">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="3f049-116">-ParentObject</span></span>
<span data-ttu-id="3f049-117">Objeto de entrada do serviço de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="3f049-117">Search Service Input Object.</span></span>

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

### <span data-ttu-id="3f049-118">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="3f049-118">-ParentResourceId</span></span>
<span data-ttu-id="3f049-119">ID do recurso do serviço de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="3f049-119">Search Service Resource Id.</span></span>

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

### <span data-ttu-id="3f049-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f049-120">-ResourceGroupName</span></span>
<span data-ttu-id="3f049-121">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="3f049-121">Resource Group name.</span></span>

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

### <span data-ttu-id="3f049-122">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="3f049-122">-ServiceName</span></span>
<span data-ttu-id="3f049-123">Nome do serviço de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="3f049-123">Search Service name.</span></span>

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

### <span data-ttu-id="3f049-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f049-124">CommonParameters</span></span>
<span data-ttu-id="3f049-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f049-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f049-126">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3f049-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f049-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3f049-127">INPUTS</span></span>

### <span data-ttu-id="3f049-128">Microsoft. Azure. Commands. Management. Search. Models. PSSearchService</span><span class="sxs-lookup"><span data-stu-id="3f049-128">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="3f049-129">System. String</span><span class="sxs-lookup"><span data-stu-id="3f049-129">System.String</span></span>

## <span data-ttu-id="3f049-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3f049-130">OUTPUTS</span></span>

### <span data-ttu-id="3f049-131">Microsoft. Azure. Commands. Management. Search. Models. PSSearchAdminKey</span><span class="sxs-lookup"><span data-stu-id="3f049-131">Microsoft.Azure.Commands.Management.Search.Models.PSSearchAdminKey</span></span>

## <span data-ttu-id="3f049-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3f049-132">NOTES</span></span>

## <span data-ttu-id="3f049-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3f049-133">RELATED LINKS</span></span>

[<span data-ttu-id="3f049-134">New-AzSearchAdminKey</span><span class="sxs-lookup"><span data-stu-id="3f049-134">New-AzSearchAdminKey</span></span>](./New-AzSearchAdminKey.md)
