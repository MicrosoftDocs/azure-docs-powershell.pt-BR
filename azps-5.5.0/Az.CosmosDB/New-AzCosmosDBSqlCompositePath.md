---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqlcompositepath
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlCompositePath.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlCompositePath.md
ms.openlocfilehash: ff78ad82c89b774f034fe6f1d4499db7868d43c7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112044"
---
# <span data-ttu-id="bdc73-101">New-AzCosmosDBSqlCompositePath</span><span class="sxs-lookup"><span data-stu-id="bdc73-101">New-AzCosmosDBSqlCompositePath</span></span>

## <span data-ttu-id="bdc73-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bdc73-102">SYNOPSIS</span></span>
<span data-ttu-id="bdc73-103">Cria um novo objeto do tipo PSCompositePath.</span><span class="sxs-lookup"><span data-stu-id="bdc73-103">Creates a new object of type PSCompositePath.</span></span> <span data-ttu-id="bdc73-104">Ele pode ser passado como um valor de parâmetro para Set-AzCosmosDBSqlContainer.</span><span class="sxs-lookup"><span data-stu-id="bdc73-104">It can be passed as a parameter value for Set-AzCosmosDBSqlContainer.</span></span>

## <span data-ttu-id="bdc73-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bdc73-105">SYNTAX</span></span>

```
New-AzCosmosDBSqlCompositePath [-Path <String>] [-Order <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bdc73-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="bdc73-106">DESCRIPTION</span></span>
<span data-ttu-id="bdc73-107">Objeto correspondente ao CompositePath da API sql.</span><span class="sxs-lookup"><span data-stu-id="bdc73-107">Object corresponding to Sql API's CompositePath.</span></span>

## <span data-ttu-id="bdc73-108">Exemplos</span><span class="sxs-lookup"><span data-stu-id="bdc73-108">EXAMPLES</span></span>

### <span data-ttu-id="bdc73-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="bdc73-109">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlCompositePath -Path "/abc" -Order Ascending

Path Order
---- -----
/abc Ascending
```

## <span data-ttu-id="bdc73-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bdc73-110">PARAMETERS</span></span>

### <span data-ttu-id="bdc73-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bdc73-111">-DefaultProfile</span></span>
<span data-ttu-id="bdc73-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="bdc73-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bdc73-113">-Pedido</span><span class="sxs-lookup"><span data-stu-id="bdc73-113">-Order</span></span>
<span data-ttu-id="bdc73-114">Obtém ou define a ordem de classificação para caminhos compostos.</span><span class="sxs-lookup"><span data-stu-id="bdc73-114">Gets or sets sort order for composite paths.</span></span>
<span data-ttu-id="bdc73-115">Os valores possíveis incluem: 'Crescente', 'Decrescente'</span><span class="sxs-lookup"><span data-stu-id="bdc73-115">Possible values include: 'Ascending', 'Descending'</span></span>

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

### <span data-ttu-id="bdc73-116">-Caminho</span><span class="sxs-lookup"><span data-stu-id="bdc73-116">-Path</span></span>
<span data-ttu-id="bdc73-117">O caminho ao qual o comportamento de indexação se aplica.</span><span class="sxs-lookup"><span data-stu-id="bdc73-117">The path for which the indexing behavior applies to.</span></span>
<span data-ttu-id="bdc73-118">Os caminhos de índice normalmente começam com raiz e terminam com caractere curinga (/caminho/\*)</span><span class="sxs-lookup"><span data-stu-id="bdc73-118">Index paths typically start with root and end with wildcard (/path/\*)</span></span>

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

### <span data-ttu-id="bdc73-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bdc73-119">CommonParameters</span></span>
<span data-ttu-id="bdc73-120">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bdc73-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bdc73-121">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bdc73-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bdc73-122">Entradas</span><span class="sxs-lookup"><span data-stu-id="bdc73-122">INPUTS</span></span>

### <span data-ttu-id="bdc73-123">Nenhum</span><span class="sxs-lookup"><span data-stu-id="bdc73-123">None</span></span>

## <span data-ttu-id="bdc73-124">Saídas</span><span class="sxs-lookup"><span data-stu-id="bdc73-124">OUTPUTS</span></span>

### <span data-ttu-id="bdc73-125">Microsoft.Azure.Commands.CosmosDB.Models.PSCompositePath</span><span class="sxs-lookup"><span data-stu-id="bdc73-125">Microsoft.Azure.Commands.CosmosDB.Models.PSCompositePath</span></span>

## <span data-ttu-id="bdc73-126">Notas</span><span class="sxs-lookup"><span data-stu-id="bdc73-126">NOTES</span></span>

## <span data-ttu-id="bdc73-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bdc73-127">RELATED LINKS</span></span>
