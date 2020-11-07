---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqlconflictresolutionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlConflictResolutionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlConflictResolutionPolicy.md
ms.openlocfilehash: b11142be65935522a73d3a068be0ee329994e2ee
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93943642"
---
# <span data-ttu-id="703f1-101">New-AzCosmosDBSqlConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="703f1-101">New-AzCosmosDBSqlConflictResolutionPolicy</span></span>

## <span data-ttu-id="703f1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="703f1-102">SYNOPSIS</span></span>
<span data-ttu-id="703f1-103">Cria um novo objeto do tipo PSSqlConflictResolutionPolicy.</span><span class="sxs-lookup"><span data-stu-id="703f1-103">Creates a new object of type PSSqlConflictResolutionPolicy.</span></span> <span data-ttu-id="703f1-104">Ele pode ser passado como um valor de parâmetro para Set-AzCosmosDBSqlContainer.</span><span class="sxs-lookup"><span data-stu-id="703f1-104">It can be passed as a parameter value for Set-AzCosmosDBSqlContainer.</span></span>

## <span data-ttu-id="703f1-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="703f1-105">SYNTAX</span></span>

```
New-AzCosmosDBSqlConflictResolutionPolicy -Type <String> [-Path <String>]
 [-ConflictResolutionProcedure <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="703f1-106">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="703f1-106">DESCRIPTION</span></span>
<span data-ttu-id="703f1-107">Objeto correspondente ao ConflictResolutionPolicy da API SQL.</span><span class="sxs-lookup"><span data-stu-id="703f1-107">Object corresponding to Sql API's ConflictResolutionPolicy.</span></span>

## <span data-ttu-id="703f1-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="703f1-108">EXAMPLES</span></span>

### <span data-ttu-id="703f1-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="703f1-109">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlConflictResolutionPolicy -Type LastWriterWins -Path "/myPath"

Mode           ConflictResolutionPath ConflictResolutionProcedure
----           ---------------------- ---------------------------
LastWriterWins /myPath
```

<span data-ttu-id="703f1-110">{{Adicionar exemplo de descrição aqui}}</span><span class="sxs-lookup"><span data-stu-id="703f1-110">{{ Add example description here }}</span></span>

## <span data-ttu-id="703f1-111">OS</span><span class="sxs-lookup"><span data-stu-id="703f1-111">PARAMETERS</span></span>

### <span data-ttu-id="703f1-112">-ConflictResolutionProcedure</span><span class="sxs-lookup"><span data-stu-id="703f1-112">-ConflictResolutionProcedure</span></span>
<span data-ttu-id="703f1-113">Seja fornecida quando o tipo for personalizado.</span><span class="sxs-lookup"><span data-stu-id="703f1-113">To be provided when the type is custom.</span></span>

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

### <span data-ttu-id="703f1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="703f1-114">-DefaultProfile</span></span>
<span data-ttu-id="703f1-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="703f1-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="703f1-116">-Caminho</span><span class="sxs-lookup"><span data-stu-id="703f1-116">-Path</span></span>
<span data-ttu-id="703f1-117">Seja fornecida quando o tipo for LastWriterWins.</span><span class="sxs-lookup"><span data-stu-id="703f1-117">To be provided when the type is LastWriterWins.</span></span>

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

### <span data-ttu-id="703f1-118">-Digite</span><span class="sxs-lookup"><span data-stu-id="703f1-118">-Type</span></span>
<span data-ttu-id="703f1-119">Pode ter os valores: LastWriterWins, Custom, manual.</span><span class="sxs-lookup"><span data-stu-id="703f1-119">Can have the values: LastWriterWins, Custom, Manual.</span></span>

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

### <span data-ttu-id="703f1-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="703f1-120">CommonParameters</span></span>
<span data-ttu-id="703f1-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="703f1-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="703f1-122">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="703f1-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="703f1-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="703f1-123">INPUTS</span></span>

### <span data-ttu-id="703f1-124">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="703f1-124">None</span></span>

## <span data-ttu-id="703f1-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="703f1-125">OUTPUTS</span></span>

### <span data-ttu-id="703f1-126">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="703f1-126">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlConflictResolutionPolicy</span></span>

## <span data-ttu-id="703f1-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="703f1-127">NOTES</span></span>

## <span data-ttu-id="703f1-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="703f1-128">RELATED LINKS</span></span>
