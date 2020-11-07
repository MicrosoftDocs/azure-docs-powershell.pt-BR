---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/set-azcosmosdbsqluserdefinedfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBSqlUserDefinedFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBSqlUserDefinedFunction.md
ms.openlocfilehash: 27363873996505a15e8eccd3dcb3620a2f88c1a8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93777295"
---
# <span data-ttu-id="a905b-101">Set-AzCosmosDBSqlUserDefinedFunction</span><span class="sxs-lookup"><span data-stu-id="a905b-101">Set-AzCosmosDBSqlUserDefinedFunction</span></span>

## <span data-ttu-id="a905b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a905b-102">SYNOPSIS</span></span>
<span data-ttu-id="a905b-103">Cria um novo ou atualiza um CosmosDB SQL UserDefinedFunction existente.</span><span class="sxs-lookup"><span data-stu-id="a905b-103">Creates a new or updates an existing CosmosDB Sql UserDefinedFunction.</span></span>

## <span data-ttu-id="a905b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a905b-104">SYNTAX</span></span>

### <span data-ttu-id="a905b-105">ByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="a905b-105">ByNameParameterSet (Default)</span></span>
```
Set-AzCosmosDBSqlUserDefinedFunction -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> -Name <String> -Body <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a905b-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a905b-106">ByParentObjectParameterSet</span></span>
```
Set-AzCosmosDBSqlUserDefinedFunction -Name <String> -Body <String> -InputObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a905b-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a905b-107">DESCRIPTION</span></span>
<span data-ttu-id="a905b-108">O cmdlet **set-AzCosmosDBSqlUserDefinedFunction** cria um novo ou atualiza um CosmosDB SQL UserDefinedFunction existente.</span><span class="sxs-lookup"><span data-stu-id="a905b-108">The **Set-AzCosmosDBSqlUserDefinedFunction** cmdlet creates a new or updates an existing CosmosDB Sql UserDefinedFunction.</span></span>

## <span data-ttu-id="a905b-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a905b-109">EXAMPLES</span></span>

### <span data-ttu-id="a905b-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a905b-110">Example 1</span></span>
```powershell
PS C:\> Set-AzCosmosDBSqlUserDefinedFunction -AccountName {accountName} -ResourceGroupName {resourceGroupName} -DatabaseName {databaseName} -Name {udfName} -ContainerName {containerName} -Body {sampleBody}

Name                               : {udfName}
Id                                 : {udfId}
SqlUserDefinedFunctionGetResultsId :
Body                               :
_rid                               :
_ts                                :
_etag                              :
```

## <span data-ttu-id="a905b-111">OS</span><span class="sxs-lookup"><span data-stu-id="a905b-111">PARAMETERS</span></span>

### <span data-ttu-id="a905b-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="a905b-112">-AccountName</span></span>
<span data-ttu-id="a905b-113">Nome da conta de banco de dados de banco de dados do cosmos.</span><span class="sxs-lookup"><span data-stu-id="a905b-113">Name of the Cosmos DB database account.</span></span>

```yaml
Type: String
Parameter Sets: ByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a905b-114">-Corpo</span><span class="sxs-lookup"><span data-stu-id="a905b-114">-Body</span></span>
<span data-ttu-id="a905b-115">O corpo da função definida pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="a905b-115">The body of the User Defined Function.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a905b-116">-Confirme</span><span class="sxs-lookup"><span data-stu-id="a905b-116">-Confirm</span></span>
<span data-ttu-id="a905b-117">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a905b-117">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a905b-118">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="a905b-118">-ContainerName</span></span>
<span data-ttu-id="a905b-119">Nome do contêiner.</span><span class="sxs-lookup"><span data-stu-id="a905b-119">Container name.</span></span>

```yaml
Type: String
Parameter Sets: ByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a905b-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="a905b-120">-DatabaseName</span></span>
<span data-ttu-id="a905b-121">Nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="a905b-121">Database name.</span></span>

```yaml
Type: String
Parameter Sets: ByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a905b-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a905b-122">-DefaultProfile</span></span>
<span data-ttu-id="a905b-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a905b-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a905b-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a905b-124">-InputObject</span></span>
<span data-ttu-id="a905b-125">Objeto contêiner SQL.</span><span class="sxs-lookup"><span data-stu-id="a905b-125">Sql Container object.</span></span>

```yaml
Type: PSSqlContainerGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a905b-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="a905b-126">-Name</span></span>
<span data-ttu-id="a905b-127">Nome da função definida pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="a905b-127">User Defined Function Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a905b-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a905b-128">-ResourceGroupName</span></span>
<span data-ttu-id="a905b-129">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a905b-129">Name of resource group.</span></span>

```yaml
Type: String
Parameter Sets: ByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a905b-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a905b-130">-WhatIf</span></span>
<span data-ttu-id="a905b-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a905b-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a905b-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a905b-132">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a905b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a905b-133">CommonParameters</span></span>
<span data-ttu-id="a905b-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a905b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a905b-135">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a905b-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a905b-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a905b-136">INPUTS</span></span>

### <span data-ttu-id="a905b-137">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="a905b-137">None</span></span>

## <span data-ttu-id="a905b-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a905b-138">OUTPUTS</span></span>

### <span data-ttu-id="a905b-139">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlUserDefinedFunctionGetResults</span><span class="sxs-lookup"><span data-stu-id="a905b-139">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUserDefinedFunctionGetResults</span></span>

## <span data-ttu-id="a905b-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a905b-140">NOTES</span></span>

## <span data-ttu-id="a905b-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a905b-141">RELATED LINKS</span></span>
