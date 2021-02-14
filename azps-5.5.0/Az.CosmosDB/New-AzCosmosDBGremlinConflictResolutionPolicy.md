---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbgremlinconflictresolutionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinConflictResolutionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinConflictResolutionPolicy.md
ms.openlocfilehash: 4662368f89f77c331619472feefe16736c40ef55
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116458"
---
# <span data-ttu-id="992d2-101">New-AzCosmosDBGremlinConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="992d2-101">New-AzCosmosDBGremlinConflictResolutionPolicy</span></span>

## <span data-ttu-id="992d2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="992d2-102">SYNOPSIS</span></span>
<span data-ttu-id="992d2-103">Cria um novo objeto do tipo PSConflictResolutionPolicy.</span><span class="sxs-lookup"><span data-stu-id="992d2-103">Creates a new object of type PSConflictResolutionPolicy.</span></span> <span data-ttu-id="992d2-104">Ele pode ser passado como um valor de parâmetro para Set-AzCosmosDBGremlinGraph.</span><span class="sxs-lookup"><span data-stu-id="992d2-104">It can be passed as a parameter value for Set-AzCosmosDBGremlinGraph.</span></span>

## <span data-ttu-id="992d2-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="992d2-105">SYNTAX</span></span>

```
New-AzCosmosDBGremlinConflictResolutionPolicy -Type <String> [-Path <String>]
 [-ConflictResolutionProcedure <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="992d2-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="992d2-106">DESCRIPTION</span></span>
<span data-ttu-id="992d2-107">Objeto correspondente ao ConflictResolutionPolicy da API de Gremlin.</span><span class="sxs-lookup"><span data-stu-id="992d2-107">Object corresponding to Gremlin API's ConflictResolutionPolicy.</span></span>

## <span data-ttu-id="992d2-108">Exemplos</span><span class="sxs-lookup"><span data-stu-id="992d2-108">EXAMPLES</span></span>

### <span data-ttu-id="992d2-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="992d2-109">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBGremlinConflictResolutionPolicy -Type LastWriterWins -Path "/myPath"

Mode           ConflictResolutionPath ConflictResolutionProcedure
----           ---------------------- ---------------------------
LastWriterWins /myPath
```

## <span data-ttu-id="992d2-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="992d2-110">PARAMETERS</span></span>

### <span data-ttu-id="992d2-111">-ConflictResolutionProcedure</span><span class="sxs-lookup"><span data-stu-id="992d2-111">-ConflictResolutionProcedure</span></span>
<span data-ttu-id="992d2-112">A ser fornecida quando o tipo for personalizado.</span><span class="sxs-lookup"><span data-stu-id="992d2-112">To be provided when the type is custom.</span></span>

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

### <span data-ttu-id="992d2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="992d2-113">-DefaultProfile</span></span>
<span data-ttu-id="992d2-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="992d2-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="992d2-115">-Caminho</span><span class="sxs-lookup"><span data-stu-id="992d2-115">-Path</span></span>
<span data-ttu-id="992d2-116">A ser fornecida quando o tipo for LastWriterWins.</span><span class="sxs-lookup"><span data-stu-id="992d2-116">To be provided when the type is LastWriterWins.</span></span>

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

### <span data-ttu-id="992d2-117">-Tipo</span><span class="sxs-lookup"><span data-stu-id="992d2-117">-Type</span></span>
<span data-ttu-id="992d2-118">Pode ter os valores: LastWriterWins, Custom, Manual.</span><span class="sxs-lookup"><span data-stu-id="992d2-118">Can have the values: LastWriterWins, Custom, Manual.</span></span>

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

### <span data-ttu-id="992d2-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="992d2-119">CommonParameters</span></span>
<span data-ttu-id="992d2-120">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="992d2-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="992d2-121">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="992d2-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="992d2-122">Entradas</span><span class="sxs-lookup"><span data-stu-id="992d2-122">INPUTS</span></span>

### <span data-ttu-id="992d2-123">Nenhum</span><span class="sxs-lookup"><span data-stu-id="992d2-123">None</span></span>

## <span data-ttu-id="992d2-124">Saídas</span><span class="sxs-lookup"><span data-stu-id="992d2-124">OUTPUTS</span></span>

### <span data-ttu-id="992d2-125">Microsoft.Azure.Commands.CosmosDB.Models.PSConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="992d2-125">Microsoft.Azure.Commands.CosmosDB.Models.PSConflictResolutionPolicy</span></span>

## <span data-ttu-id="992d2-126">Notas</span><span class="sxs-lookup"><span data-stu-id="992d2-126">NOTES</span></span>

## <span data-ttu-id="992d2-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="992d2-127">RELATED LINKS</span></span>
