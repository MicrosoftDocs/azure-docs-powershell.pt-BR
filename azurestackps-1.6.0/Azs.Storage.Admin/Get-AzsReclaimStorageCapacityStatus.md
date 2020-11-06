---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: dbd8de47397e86f2aed9f774b555a587cf69976a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93425989"
---
# <span data-ttu-id="81eb9-101">Get-AzsReclaimStorageCapacityStatus</span><span class="sxs-lookup"><span data-stu-id="81eb9-101">Get-AzsReclaimStorageCapacityStatus</span></span>

## <span data-ttu-id="81eb9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="81eb9-102">SYNOPSIS</span></span>
<span data-ttu-id="81eb9-103">Retorna o estado do trabalho de coleta de lixo.</span><span class="sxs-lookup"><span data-stu-id="81eb9-103">Returns the state of the garbage collection job.</span></span>

## <span data-ttu-id="81eb9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="81eb9-104">SYNTAX</span></span>

```
Get-AzsReclaimStorageCapacityStatus [-FarmName] <String> [-JobId] <String> [[-ResourceGroupName] <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="81eb9-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="81eb9-105">DESCRIPTION</span></span>
<span data-ttu-id="81eb9-106">Retorna o estado do trabalho de coleta de lixo.</span><span class="sxs-lookup"><span data-stu-id="81eb9-106">Returns the state of the garbage collection job.</span></span>

## <span data-ttu-id="81eb9-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="81eb9-107">EXAMPLES</span></span>

### <span data-ttu-id="81eb9-108">--------------------------EXEMPLO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="81eb9-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsReclaimStorageCapacityStatus -FarmName "6ddbfe6e-8781-4a3d-b370-4a8b20a494d8" -JobId "92360f29-cd21-429d-a20b-9b11ab5902a0"
```

<span data-ttu-id="81eb9-109">Retorna informações sobre o status da coleta de lixo.</span><span class="sxs-lookup"><span data-stu-id="81eb9-109">Return information about the status of garbage collection.</span></span>

## <span data-ttu-id="81eb9-110">OS</span><span class="sxs-lookup"><span data-stu-id="81eb9-110">PARAMETERS</span></span>

### <span data-ttu-id="81eb9-111">-Farmname</span><span class="sxs-lookup"><span data-stu-id="81eb9-111">-FarmName</span></span>
<span data-ttu-id="81eb9-112">ID do farm.</span><span class="sxs-lookup"><span data-stu-id="81eb9-112">Farm Id.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81eb9-113">-JobId</span><span class="sxs-lookup"><span data-stu-id="81eb9-113">-JobId</span></span>
<span data-ttu-id="81eb9-114">ID da operação.</span><span class="sxs-lookup"><span data-stu-id="81eb9-114">Operation Id.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81eb9-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81eb9-115">-ResourceGroupName</span></span>
<span data-ttu-id="81eb9-116">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="81eb9-116">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81eb9-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81eb9-117">CommonParameters</span></span>
<span data-ttu-id="81eb9-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81eb9-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81eb9-119">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="81eb9-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81eb9-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="81eb9-120">INPUTS</span></span>

## <span data-ttu-id="81eb9-121">EXIBE</span><span class="sxs-lookup"><span data-stu-id="81eb9-121">OUTPUTS</span></span>

## <span data-ttu-id="81eb9-122">INFORMA</span><span class="sxs-lookup"><span data-stu-id="81eb9-122">NOTES</span></span>

## <span data-ttu-id="81eb9-123">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="81eb9-123">RELATED LINKS</span></span>

