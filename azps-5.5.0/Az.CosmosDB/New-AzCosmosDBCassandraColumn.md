---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbcassandracolumn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraColumn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraColumn.md
ms.openlocfilehash: 31563c11a1df418d0f53c1eeb80e8bc02691188c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116463"
---
# <span data-ttu-id="c007d-101">New-AzCosmosDBCassandraColumn</span><span class="sxs-lookup"><span data-stu-id="c007d-101">New-AzCosmosDBCassandraColumn</span></span>

## <span data-ttu-id="c007d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c007d-102">SYNOPSIS</span></span>
<span data-ttu-id="c007d-103">Cria uma nova Coluna de YorkDB.</span><span class="sxs-lookup"><span data-stu-id="c007d-103">Creates a new CosmosDB Cassandra Column.</span></span>

## <span data-ttu-id="c007d-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c007d-104">SYNTAX</span></span>

```
New-AzCosmosDBCassandraColumn -Name <String> -Type <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c007d-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="c007d-105">DESCRIPTION</span></span>
<span data-ttu-id="c007d-106">O **Novo-AzCosmosDBCass guidãoColumn** cria uma nova Coluna Deslumluml.</span><span class="sxs-lookup"><span data-stu-id="c007d-106">The **New-AzCosmosDBCassandraColumn** creates a new CosmosDB Cassandra Column.</span></span>

## <span data-ttu-id="c007d-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="c007d-107">EXAMPLES</span></span>

### <span data-ttu-id="c007d-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c007d-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBCassandraColumn -Name "name" -Type int

Name Type
---- ----
name int
```

## <span data-ttu-id="c007d-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c007d-109">PARAMETERS</span></span>

### <span data-ttu-id="c007d-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c007d-110">-DefaultProfile</span></span>
<span data-ttu-id="c007d-111">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c007d-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c007d-112">-Nome</span><span class="sxs-lookup"><span data-stu-id="c007d-112">-Name</span></span>
<span data-ttu-id="c007d-113">Nome da Coluna Descarraia.</span><span class="sxs-lookup"><span data-stu-id="c007d-113">Name of Cassandra Column.</span></span>

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

### <span data-ttu-id="c007d-114">-Tipo</span><span class="sxs-lookup"><span data-stu-id="c007d-114">-Type</span></span>
<span data-ttu-id="c007d-115">Tipo de Coluna de Guida.</span><span class="sxs-lookup"><span data-stu-id="c007d-115">Type of Cassandra Column.</span></span>

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

### <span data-ttu-id="c007d-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c007d-116">CommonParameters</span></span>
<span data-ttu-id="c007d-117">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c007d-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c007d-118">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c007d-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c007d-119">Entradas</span><span class="sxs-lookup"><span data-stu-id="c007d-119">INPUTS</span></span>

### <span data-ttu-id="c007d-120">Nenhum</span><span class="sxs-lookup"><span data-stu-id="c007d-120">None</span></span>

## <span data-ttu-id="c007d-121">Saídas</span><span class="sxs-lookup"><span data-stu-id="c007d-121">OUTPUTS</span></span>

### <span data-ttu-id="c007d-122">Microsoft.Azure.Commands.CosmosDB.Models.PSColumn</span><span class="sxs-lookup"><span data-stu-id="c007d-122">Microsoft.Azure.Commands.CosmosDB.Models.PSColumn</span></span>

## <span data-ttu-id="c007d-123">Notas</span><span class="sxs-lookup"><span data-stu-id="c007d-123">NOTES</span></span>

## <span data-ttu-id="c007d-124">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c007d-124">RELATED LINKS</span></span>
