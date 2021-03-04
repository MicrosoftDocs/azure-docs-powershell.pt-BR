---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdbsqlconflictresolutionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlConflictResolutionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlConflictResolutionPolicy.md
ms.openlocfilehash: e5742cde3a39cb2bf7dc96b952b3129d353235f0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889551"
---
# <span data-ttu-id="b43b6-101">New-AzCosmosDBSqlConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="b43b6-101">New-AzCosmosDBSqlConflictResolutionPolicy</span></span>

## <span data-ttu-id="b43b6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b43b6-102">SYNOPSIS</span></span>
<span data-ttu-id="b43b6-103">Cria um novo objeto do tipo PSSqlConflictResolutionPolicy.</span><span class="sxs-lookup"><span data-stu-id="b43b6-103">Creates a new object of type PSSqlConflictResolutionPolicy.</span></span> <span data-ttu-id="b43b6-104">Ele pode ser passado como um valor de parâmetro para Set-AzCosmosDBSqlContainer.</span><span class="sxs-lookup"><span data-stu-id="b43b6-104">It can be passed as a parameter value for Set-AzCosmosDBSqlContainer.</span></span>

## <span data-ttu-id="b43b6-105">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="b43b6-105">SYNTAX</span></span>

```
New-AzCosmosDBSqlConflictResolutionPolicy -Type <String> [-Path <String>]
 [-ConflictResolutionProcedure <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b43b6-106">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="b43b6-106">DESCRIPTION</span></span>
<span data-ttu-id="b43b6-107">Objeto correspondente a ConflictResolutionPolicy da API sql.</span><span class="sxs-lookup"><span data-stu-id="b43b6-107">Object corresponding to Sql API's ConflictResolutionPolicy.</span></span>

## <span data-ttu-id="b43b6-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b43b6-108">EXAMPLES</span></span>

### <span data-ttu-id="b43b6-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b43b6-109">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlConflictResolutionPolicy -Type LastWriterWins -Path "/myPath"

Mode           ConflictResolutionPath ConflictResolutionProcedure
----           ---------------------- ---------------------------
LastWriterWins /myPath
```

<span data-ttu-id="b43b6-110">{{ Adicione a descrição do exemplo aqui }}</span><span class="sxs-lookup"><span data-stu-id="b43b6-110">{{ Add example description here }}</span></span>

## <span data-ttu-id="b43b6-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="b43b6-111">PARAMETERS</span></span>

### <span data-ttu-id="b43b6-112">-ConflictResolutionProcedure</span><span class="sxs-lookup"><span data-stu-id="b43b6-112">-ConflictResolutionProcedure</span></span>
<span data-ttu-id="b43b6-113">Para ser fornecido quando o tipo for personalizado.</span><span class="sxs-lookup"><span data-stu-id="b43b6-113">To be provided when the type is custom.</span></span>

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

### <span data-ttu-id="b43b6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b43b6-114">-DefaultProfile</span></span>
<span data-ttu-id="b43b6-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b43b6-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b43b6-116">-Path</span><span class="sxs-lookup"><span data-stu-id="b43b6-116">-Path</span></span>
<span data-ttu-id="b43b6-117">Para ser fornecido quando o tipo for LastWriterWins.</span><span class="sxs-lookup"><span data-stu-id="b43b6-117">To be provided when the type is LastWriterWins.</span></span>

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

### <span data-ttu-id="b43b6-118">-Type</span><span class="sxs-lookup"><span data-stu-id="b43b6-118">-Type</span></span>
<span data-ttu-id="b43b6-119">Pode ter os valores: LastWriterWins, Custom, Manual.</span><span class="sxs-lookup"><span data-stu-id="b43b6-119">Can have the values: LastWriterWins, Custom, Manual.</span></span>

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

### <span data-ttu-id="b43b6-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b43b6-120">CommonParameters</span></span>
<span data-ttu-id="b43b6-121">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b43b6-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b43b6-122">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b43b6-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b43b6-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b43b6-123">INPUTS</span></span>

### <span data-ttu-id="b43b6-124">Nenhum</span><span class="sxs-lookup"><span data-stu-id="b43b6-124">None</span></span>

## <span data-ttu-id="b43b6-125">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="b43b6-125">OUTPUTS</span></span>

### <span data-ttu-id="b43b6-126">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="b43b6-126">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlConflictResolutionPolicy</span></span>

## <span data-ttu-id="b43b6-127">NOTES</span><span class="sxs-lookup"><span data-stu-id="b43b6-127">NOTES</span></span>

## <span data-ttu-id="b43b6-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b43b6-128">RELATED LINKS</span></span>
