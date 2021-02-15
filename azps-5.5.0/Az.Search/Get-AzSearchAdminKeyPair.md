---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/get-azsearchadminkeypair
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchAdminKeyPair.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchAdminKeyPair.md
ms.openlocfilehash: e6f2495392eed73e5576d8502f86a08e325337f2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112620"
---
# <span data-ttu-id="145fc-101">Get-AzSearchAdminKeyPair</span><span class="sxs-lookup"><span data-stu-id="145fc-101">Get-AzSearchAdminKeyPair</span></span>

## <span data-ttu-id="145fc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="145fc-102">SYNOPSIS</span></span>
<span data-ttu-id="145fc-103">Obtém par de chaves de administrador do serviço pesquisa cognitiva do Azure.</span><span class="sxs-lookup"><span data-stu-id="145fc-103">Gets admin key pair of the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="145fc-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="145fc-104">SYNTAX</span></span>

### <span data-ttu-id="145fc-105">ResourceNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="145fc-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzSearchAdminKeyPair [-ResourceGroupName] <String> [-ServiceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="145fc-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="145fc-106">ParentObjectParameterSet</span></span>
```
Get-AzSearchAdminKeyPair [-ParentObject] <PSSearchService> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="145fc-107">ParentResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="145fc-107">ParentResourceIdParameterSet</span></span>
```
Get-AzSearchAdminKeyPair [-ParentResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="145fc-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="145fc-108">DESCRIPTION</span></span>
<span data-ttu-id="145fc-109">O cmdlet **Get-AzSearchAdminKeyPair** obtém o par de chaves de administrador do serviço pesquisa cognitiva do Azure.</span><span class="sxs-lookup"><span data-stu-id="145fc-109">The **Get-AzSearchAdminKeyPair** cmdlet gets the admin key pair of the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="145fc-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="145fc-110">EXAMPLES</span></span>

### <span data-ttu-id="145fc-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="145fc-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSearchAdminKeyPair -ResourceGroupName felixwa-01 -ServiceName felixwa-basic-search

Primary                          Secondary                       
-------                          ---------                       
3B06A25BDADFF72EC132736BAA2547A1 E643B75A52E04DF13EB690807C451C55
```

<span data-ttu-id="145fc-112">O exemplo obtém o par de chaves de administrador do serviço pesquisa cognitiva do Azure.</span><span class="sxs-lookup"><span data-stu-id="145fc-112">The example gets admin key pair of the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="145fc-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="145fc-113">PARAMETERS</span></span>

### <span data-ttu-id="145fc-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="145fc-114">-DefaultProfile</span></span>
<span data-ttu-id="145fc-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="145fc-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="145fc-116">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="145fc-116">-ParentObject</span></span>
<span data-ttu-id="145fc-117">Objeto de entrada do Serviço de Pesquisa Cognitiva do Azure.</span><span class="sxs-lookup"><span data-stu-id="145fc-117">Azure Cognitive Search Service Input Object.</span></span>

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

### <span data-ttu-id="145fc-118">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="145fc-118">-ParentResourceId</span></span>
<span data-ttu-id="145fc-119">ID do Recurso do Serviço de Pesquisa Cognitiva do Azure.</span><span class="sxs-lookup"><span data-stu-id="145fc-119">Azure Cognitive Search Service Resource Id.</span></span>

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

### <span data-ttu-id="145fc-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="145fc-120">-ResourceGroupName</span></span>
<span data-ttu-id="145fc-121">Nome do Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="145fc-121">Resource Group name.</span></span>

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

### <span data-ttu-id="145fc-122">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="145fc-122">-ServiceName</span></span>
<span data-ttu-id="145fc-123">Nome do Serviço de Pesquisa Cognitiva do Azure.</span><span class="sxs-lookup"><span data-stu-id="145fc-123">Azure Cognitive Search Service name.</span></span>

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

### <span data-ttu-id="145fc-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="145fc-124">CommonParameters</span></span>
<span data-ttu-id="145fc-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="145fc-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="145fc-126">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="145fc-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="145fc-127">Entradas</span><span class="sxs-lookup"><span data-stu-id="145fc-127">INPUTS</span></span>

### <span data-ttu-id="145fc-128">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span><span class="sxs-lookup"><span data-stu-id="145fc-128">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="145fc-129">System.String</span><span class="sxs-lookup"><span data-stu-id="145fc-129">System.String</span></span>

## <span data-ttu-id="145fc-130">Saídas</span><span class="sxs-lookup"><span data-stu-id="145fc-130">OUTPUTS</span></span>

### <span data-ttu-id="145fc-131">Microsoft.Azure.Commands.Management.Search.Models.PSSearchAdminKey</span><span class="sxs-lookup"><span data-stu-id="145fc-131">Microsoft.Azure.Commands.Management.Search.Models.PSSearchAdminKey</span></span>

## <span data-ttu-id="145fc-132">Notas</span><span class="sxs-lookup"><span data-stu-id="145fc-132">NOTES</span></span>

## <span data-ttu-id="145fc-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="145fc-133">RELATED LINKS</span></span>

[<span data-ttu-id="145fc-134">New-AzSearchAdminKey</span><span class="sxs-lookup"><span data-stu-id="145fc-134">New-AzSearchAdminKey</span></span>](./New-AzSearchAdminKey.md)
