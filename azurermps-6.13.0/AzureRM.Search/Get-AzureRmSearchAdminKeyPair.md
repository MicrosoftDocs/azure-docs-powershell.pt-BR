---
external help file: Microsoft.Azure.Commands.Management.Search.dll-Help.xml
Module Name: AzureRM.Search
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.search/get-azurermsearchadminkeypair
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Search/Commands.Management.Search/help/Get-AzureRmSearchAdminKeyPair.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Search/Commands.Management.Search/help/Get-AzureRmSearchAdminKeyPair.md
ms.openlocfilehash: 92b2e7304c0f837e47f7464e84769478902c973a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431909"
---
# <span data-ttu-id="9ac73-101">Get-AzureRmSearchAdminKeyPair</span><span class="sxs-lookup"><span data-stu-id="9ac73-101">Get-AzureRmSearchAdminKeyPair</span></span>

## <span data-ttu-id="9ac73-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9ac73-102">SYNOPSIS</span></span>
<span data-ttu-id="9ac73-103">Obtém o par de chave de administração do serviço de pesquisa do Azure.</span><span class="sxs-lookup"><span data-stu-id="9ac73-103">Gets admin key pair of the Azure Search service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9ac73-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9ac73-104">SYNTAX</span></span>

### <span data-ttu-id="9ac73-105">ResourceNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="9ac73-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzureRmSearchAdminKeyPair [-ResourceGroupName] <String> [-ServiceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9ac73-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9ac73-106">ParentObjectParameterSet</span></span>
```
Get-AzureRmSearchAdminKeyPair [-ParentObject] <PSSearchService> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9ac73-107">ParentResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9ac73-107">ParentResourceIdParameterSet</span></span>
```
Get-AzureRmSearchAdminKeyPair [-ParentResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9ac73-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9ac73-108">DESCRIPTION</span></span>
<span data-ttu-id="9ac73-109">O cmdlet **Get-AzureRmSearchAdminKeyPair** Obtém o par de chave de administração do serviço de pesquisa do Azure.</span><span class="sxs-lookup"><span data-stu-id="9ac73-109">The **Get-AzureRmSearchAdminKeyPair** cmdlet gets the admin key pair of the Azure Search service.</span></span>

## <span data-ttu-id="9ac73-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9ac73-110">EXAMPLES</span></span>

### <span data-ttu-id="9ac73-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="9ac73-111">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmSearchAdminKeyPair -ResourceGroupName felixwa-01 -ServiceName felixwa-basic-search

Primary                          Secondary                       
-------                          ---------                       
3B06A25BDADFF72EC132736BAA2547A1 E643B75A52E04DF13EB690807C451C55
```

<span data-ttu-id="9ac73-112">O exemplo obtém o par de chave de administração do serviço de pesquisa do Azure.</span><span class="sxs-lookup"><span data-stu-id="9ac73-112">The example gets admin key pair of the Azure Search service.</span></span>

## <span data-ttu-id="9ac73-113">OS</span><span class="sxs-lookup"><span data-stu-id="9ac73-113">PARAMETERS</span></span>

### <span data-ttu-id="9ac73-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ac73-114">-DefaultProfile</span></span>
<span data-ttu-id="9ac73-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9ac73-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9ac73-116">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="9ac73-116">-ParentObject</span></span>
<span data-ttu-id="9ac73-117">Objeto de entrada do serviço de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="9ac73-117">Search Service Input Object.</span></span>

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

### <span data-ttu-id="9ac73-118">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="9ac73-118">-ParentResourceId</span></span>
<span data-ttu-id="9ac73-119">ID do recurso do serviço de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="9ac73-119">Search Service Resource Id.</span></span>

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

### <span data-ttu-id="9ac73-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ac73-120">-ResourceGroupName</span></span>
<span data-ttu-id="9ac73-121">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="9ac73-121">Resource Group name.</span></span>

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

### <span data-ttu-id="9ac73-122">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="9ac73-122">-ServiceName</span></span>
<span data-ttu-id="9ac73-123">Nome do serviço de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="9ac73-123">Search Service name.</span></span>

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

### <span data-ttu-id="9ac73-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ac73-124">CommonParameters</span></span>
<span data-ttu-id="9ac73-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9ac73-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ac73-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9ac73-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ac73-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9ac73-127">INPUTS</span></span>

### <span data-ttu-id="9ac73-128">Microsoft. Azure. Commands. Management. Search. Models. PSSearchService</span><span class="sxs-lookup"><span data-stu-id="9ac73-128">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>
<span data-ttu-id="9ac73-129">Parâmetros: ParentObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="9ac73-129">Parameters: ParentObject (ByValue)</span></span>

### <span data-ttu-id="9ac73-130">System. String</span><span class="sxs-lookup"><span data-stu-id="9ac73-130">System.String</span></span>

## <span data-ttu-id="9ac73-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9ac73-131">OUTPUTS</span></span>

### <span data-ttu-id="9ac73-132">Microsoft. Azure. Commands. Management. Search. Models. PSSearchAdminKey</span><span class="sxs-lookup"><span data-stu-id="9ac73-132">Microsoft.Azure.Commands.Management.Search.Models.PSSearchAdminKey</span></span>

## <span data-ttu-id="9ac73-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9ac73-133">NOTES</span></span>

## <span data-ttu-id="9ac73-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9ac73-134">RELATED LINKS</span></span>

[<span data-ttu-id="9ac73-135">New-AzureRmSearchAdminKey</span><span class="sxs-lookup"><span data-stu-id="9ac73-135">New-AzureRmSearchAdminKey</span></span>](./New-AzureRmSearchAdminKey.md)
