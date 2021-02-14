---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBAccountKey.md
ms.openlocfilehash: b9e78e4ff9811f5ff52b64369fd546d5f5a8c474
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116487"
---
# <span data-ttu-id="46df7-101">Get-AzCosmosDBAccountKey</span><span class="sxs-lookup"><span data-stu-id="46df7-101">Get-AzCosmosDBAccountKey</span></span>

## <span data-ttu-id="46df7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="46df7-102">SYNOPSIS</span></span>
<span data-ttu-id="46df7-103">Get Keys{"ConnectionKeys", "PrimaryReadOnly" or "Keys"} for the given CosmosDB Account.</span><span class="sxs-lookup"><span data-stu-id="46df7-103">Get Keys{"ConnectionKeys", "PrimaryReadOnly" or "Keys"} for the given CosmosDB Account.</span></span> 

## <span data-ttu-id="46df7-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="46df7-104">SYNTAX</span></span>

### <span data-ttu-id="46df7-105">ByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="46df7-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBAccountKey -ResourceGroupName <String> -Name <String> [-Type <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="46df7-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="46df7-106">ByResourceIdParameterSet</span></span>
```
Get-AzCosmosDBAccountKey [-Type <String>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="46df7-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="46df7-107">ByObjectParameterSet</span></span>
```
Get-AzCosmosDBAccountKey [-Type <String>] -InputObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="46df7-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="46df7-108">DESCRIPTION</span></span>
<span data-ttu-id="46df7-109">Obter a lista de teclas de conexão.</span><span class="sxs-lookup"><span data-stu-id="46df7-109">Get the list of connection keys.</span></span>

## <span data-ttu-id="46df7-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="46df7-110">EXAMPLES</span></span>

### <span data-ttu-id="46df7-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="46df7-111">Example 1</span></span>
```powershell
PS C:\>  Get-AzCosmosDBAccountKey -ResourceGroupName rg1 -Name dbname -Type "ReadOnlyKeys"

Name                           Value
----                           -----
PrimaryReadonlyMasterKey       qjw0ISW1WNN0BIVPeaI7Tm3H8uZ1h7ESQjxaUendxHmIUNQowVvcL84fTqeXoC2HFgyu8Zo1mCFEcg0jZJHPjA==
SecondaryReadonlyMasterKey     9YRcTABuOHcKyHAKf0lmCeHsrcXu02aeID1g3wjXjlX8SU4s2WNlEB5htJoy3xqxNDqIyGfnq3dblLbrZDbesg==
```

<span data-ttu-id="46df7-112">Lista as chaves da Conta do CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="46df7-112">Lists the keys for CosmosDB Account.</span></span> <span data-ttu-id="46df7-113">O Tipo de Chave pode ser o valor de : ConnectionStrings, Keys e ReadOnlyKeys.</span><span class="sxs-lookup"><span data-stu-id="46df7-113">The Key Type can be value from : ConnectionStrings, Keys and ReadOnlyKeys.</span></span> <span data-ttu-id="46df7-114">O padrão é Teclas.</span><span class="sxs-lookup"><span data-stu-id="46df7-114">Default is Keys.</span></span>

## <span data-ttu-id="46df7-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="46df7-115">PARAMETERS</span></span>

### <span data-ttu-id="46df7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46df7-116">-DefaultProfile</span></span>
<span data-ttu-id="46df7-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="46df7-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="46df7-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="46df7-118">-InputObject</span></span>
<span data-ttu-id="46df7-119">Objeto conta doDbDb</span><span class="sxs-lookup"><span data-stu-id="46df7-119">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccountGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="46df7-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="46df7-120">-Name</span></span>
<span data-ttu-id="46df7-121">Nome da conta de banco de dados Do Db Db.</span><span class="sxs-lookup"><span data-stu-id="46df7-121">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="46df7-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46df7-122">-ResourceGroupName</span></span>
<span data-ttu-id="46df7-123">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="46df7-123">Name of resource group.</span></span>

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

### <span data-ttu-id="46df7-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="46df7-124">-ResourceId</span></span>
<span data-ttu-id="46df7-125">ResourceId do recurso.</span><span class="sxs-lookup"><span data-stu-id="46df7-125">ResourceId of the resource.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46df7-126">-Tipo</span><span class="sxs-lookup"><span data-stu-id="46df7-126">-Type</span></span>
<span data-ttu-id="46df7-127">Valor de: {ConnectionStrings, Keys, ReadOnlyKeys}.</span><span class="sxs-lookup"><span data-stu-id="46df7-127">Value from: {ConnectionStrings, Keys, ReadOnlyKeys}.</span></span>
<span data-ttu-id="46df7-128">O padrão é Teclas.</span><span class="sxs-lookup"><span data-stu-id="46df7-128">Default is Keys.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46df7-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46df7-129">CommonParameters</span></span>
<span data-ttu-id="46df7-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46df7-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46df7-131">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="46df7-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46df7-132">Entradas</span><span class="sxs-lookup"><span data-stu-id="46df7-132">INPUTS</span></span>

### <span data-ttu-id="46df7-133">Nenhum</span><span class="sxs-lookup"><span data-stu-id="46df7-133">None</span></span>

## <span data-ttu-id="46df7-134">Saídas</span><span class="sxs-lookup"><span data-stu-id="46df7-134">OUTPUTS</span></span>

### <span data-ttu-id="46df7-135">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountListConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="46df7-135">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountListConnectionStrings</span></span>

### <span data-ttu-id="46df7-136">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountListKeysResult</span><span class="sxs-lookup"><span data-stu-id="46df7-136">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountListKeysResult</span></span>

### <span data-ttu-id="46df7-137">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountListReadOnlyKeysResult</span><span class="sxs-lookup"><span data-stu-id="46df7-137">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountListReadOnlyKeysResult</span></span>

## <span data-ttu-id="46df7-138">Notas</span><span class="sxs-lookup"><span data-stu-id="46df7-138">NOTES</span></span>

## <span data-ttu-id="46df7-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="46df7-139">RELATED LINKS</span></span>
