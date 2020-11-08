---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbgremlinconflictresolutionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinConflictResolutionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinConflictResolutionPolicy.md
ms.openlocfilehash: 4662368f89f77c331619472feefe16736c40ef55
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94112380"
---
# <span data-ttu-id="024cc-101">New-AzCosmosDBGremlinConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="024cc-101">New-AzCosmosDBGremlinConflictResolutionPolicy</span></span>

## <span data-ttu-id="024cc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="024cc-102">SYNOPSIS</span></span>
<span data-ttu-id="024cc-103">Cria um novo objeto do tipo PSConflictResolutionPolicy.</span><span class="sxs-lookup"><span data-stu-id="024cc-103">Creates a new object of type PSConflictResolutionPolicy.</span></span> <span data-ttu-id="024cc-104">Ele pode ser passado como um valor de parâmetro para Set-AzCosmosDBGremlinGraph.</span><span class="sxs-lookup"><span data-stu-id="024cc-104">It can be passed as a parameter value for Set-AzCosmosDBGremlinGraph.</span></span>

## <span data-ttu-id="024cc-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="024cc-105">SYNTAX</span></span>

```
New-AzCosmosDBGremlinConflictResolutionPolicy -Type <String> [-Path <String>]
 [-ConflictResolutionProcedure <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="024cc-106">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="024cc-106">DESCRIPTION</span></span>
<span data-ttu-id="024cc-107">Objeto correspondente ao ConflictResolutionPolicy da API Gremlin.</span><span class="sxs-lookup"><span data-stu-id="024cc-107">Object corresponding to Gremlin API's ConflictResolutionPolicy.</span></span>

## <span data-ttu-id="024cc-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="024cc-108">EXAMPLES</span></span>

### <span data-ttu-id="024cc-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="024cc-109">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBGremlinConflictResolutionPolicy -Type LastWriterWins -Path "/myPath"

Mode           ConflictResolutionPath ConflictResolutionProcedure
----           ---------------------- ---------------------------
LastWriterWins /myPath
```

## <span data-ttu-id="024cc-110">OS</span><span class="sxs-lookup"><span data-stu-id="024cc-110">PARAMETERS</span></span>

### <span data-ttu-id="024cc-111">-ConflictResolutionProcedure</span><span class="sxs-lookup"><span data-stu-id="024cc-111">-ConflictResolutionProcedure</span></span>
<span data-ttu-id="024cc-112">Seja fornecida quando o tipo for personalizado.</span><span class="sxs-lookup"><span data-stu-id="024cc-112">To be provided when the type is custom.</span></span>

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

### <span data-ttu-id="024cc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="024cc-113">-DefaultProfile</span></span>
<span data-ttu-id="024cc-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="024cc-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="024cc-115">-Caminho</span><span class="sxs-lookup"><span data-stu-id="024cc-115">-Path</span></span>
<span data-ttu-id="024cc-116">Seja fornecida quando o tipo for LastWriterWins.</span><span class="sxs-lookup"><span data-stu-id="024cc-116">To be provided when the type is LastWriterWins.</span></span>

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

### <span data-ttu-id="024cc-117">-Digite</span><span class="sxs-lookup"><span data-stu-id="024cc-117">-Type</span></span>
<span data-ttu-id="024cc-118">Pode ter os valores: LastWriterWins, Custom, manual.</span><span class="sxs-lookup"><span data-stu-id="024cc-118">Can have the values: LastWriterWins, Custom, Manual.</span></span>

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

### <span data-ttu-id="024cc-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="024cc-119">CommonParameters</span></span>
<span data-ttu-id="024cc-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="024cc-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="024cc-121">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="024cc-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="024cc-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="024cc-122">INPUTS</span></span>

### <span data-ttu-id="024cc-123">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="024cc-123">None</span></span>

## <span data-ttu-id="024cc-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="024cc-124">OUTPUTS</span></span>

### <span data-ttu-id="024cc-125">Microsoft. Azure. Commands. CosmosDB. Models. PSConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="024cc-125">Microsoft.Azure.Commands.CosmosDB.Models.PSConflictResolutionPolicy</span></span>

## <span data-ttu-id="024cc-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="024cc-126">NOTES</span></span>

## <span data-ttu-id="024cc-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="024cc-127">RELATED LINKS</span></span>
