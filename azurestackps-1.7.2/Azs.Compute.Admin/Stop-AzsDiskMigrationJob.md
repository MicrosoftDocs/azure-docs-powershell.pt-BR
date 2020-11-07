---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: d38e4bd949a6118f55ce0096a8ca56d08137bb2a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93774544"
---
# <span data-ttu-id="16b38-101">Stop-AzsDiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="16b38-101">Stop-AzsDiskMigrationJob</span></span>

## <span data-ttu-id="16b38-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="16b38-102">SYNOPSIS</span></span>
<span data-ttu-id="16b38-103">Cancelar um trabalho de migração de disco gerenciado.</span><span class="sxs-lookup"><span data-stu-id="16b38-103">Cancel a managed disk migration job.</span></span>

## <span data-ttu-id="16b38-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="16b38-104">SYNTAX</span></span>

```
Stop-AzsDiskMigrationJob [[-Location] <String>] [[-Name] <String>] [<CommonParameters>]
```

## <span data-ttu-id="16b38-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="16b38-105">DESCRIPTION</span></span>
<span data-ttu-id="16b38-106">Cancelar um trabalho de migração de disco.</span><span class="sxs-lookup"><span data-stu-id="16b38-106">Cancel a disk migration job.</span></span>

## <span data-ttu-id="16b38-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="16b38-107">EXAMPLES</span></span>

### <span data-ttu-id="16b38-108">--------------------------EXEMPLO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="16b38-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Stop-AzsDiskMigrationJob -Location local -MigrationId $migration.MigrationId
```

<span data-ttu-id="16b38-109">Cancelar um trabalho de migração de disco gerenciado.</span><span class="sxs-lookup"><span data-stu-id="16b38-109">Cancel a managed disk migration job.</span></span>

## <span data-ttu-id="16b38-110">OS</span><span class="sxs-lookup"><span data-stu-id="16b38-110">PARAMETERS</span></span>

### <span data-ttu-id="16b38-111">-Local</span><span class="sxs-lookup"><span data-stu-id="16b38-111">-Location</span></span>
<span data-ttu-id="16b38-112">Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="16b38-112">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16b38-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="16b38-113">-Name</span></span>
<span data-ttu-id="16b38-114">O nome do GUID do trabalho de migração.</span><span class="sxs-lookup"><span data-stu-id="16b38-114">The migration job guid name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: MigrationId

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16b38-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16b38-115">CommonParameters</span></span>
<span data-ttu-id="16b38-116">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="16b38-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16b38-117">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="16b38-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16b38-118">SENSORES</span><span class="sxs-lookup"><span data-stu-id="16b38-118">INPUTS</span></span>

## <span data-ttu-id="16b38-119">EXIBE</span><span class="sxs-lookup"><span data-stu-id="16b38-119">OUTPUTS</span></span>

### <span data-ttu-id="16b38-120">Microsoft. AzureStack. Management. COMPUTE. admin. Models. DiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="16b38-120">Microsoft.AzureStack.Management.Compute.Admin.Models.DiskMigrationJob</span></span>

## <span data-ttu-id="16b38-121">INFORMA</span><span class="sxs-lookup"><span data-stu-id="16b38-121">NOTES</span></span>

## <span data-ttu-id="16b38-122">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="16b38-122">RELATED LINKS</span></span>

