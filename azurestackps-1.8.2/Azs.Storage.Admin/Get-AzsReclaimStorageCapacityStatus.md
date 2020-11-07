---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: fd62756b3a41af82a245a39d4f80478d47d90e1c
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/08/2020
ms.locfileid: "93946896"
---
# <span data-ttu-id="ea9ff-101">Get-AzsReclaimStorageCapacityStatus</span><span class="sxs-lookup"><span data-stu-id="ea9ff-101">Get-AzsReclaimStorageCapacityStatus</span></span>

## <span data-ttu-id="ea9ff-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ea9ff-102">SYNOPSIS</span></span>
<span data-ttu-id="ea9ff-103">Retorna o estado do trabalho de coleta de lixo.</span><span class="sxs-lookup"><span data-stu-id="ea9ff-103">Returns the state of the garbage collection job.</span></span>

## <span data-ttu-id="ea9ff-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ea9ff-104">SYNTAX</span></span>

```
Get-AzsReclaimStorageCapacityStatus [-FarmName] <String> [-JobId] <String> [[-ResourceGroupName] <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="ea9ff-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ea9ff-105">DESCRIPTION</span></span>
<span data-ttu-id="ea9ff-106">Retorna o estado do trabalho de coleta de lixo.</span><span class="sxs-lookup"><span data-stu-id="ea9ff-106">Returns the state of the garbage collection job.</span></span>

## <span data-ttu-id="ea9ff-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ea9ff-107">EXAMPLES</span></span>

### <span data-ttu-id="ea9ff-108">EXEMPLO 1</span><span class="sxs-lookup"><span data-stu-id="ea9ff-108">EXAMPLE 1</span></span>
```
Get-AzsReclaimStorageCapacityStatus -FarmName "6ddbfe6e-8781-4a3d-b370-4a8b20a494d8" -JobId "92360f29-cd21-429d-a20b-9b11ab5902a0"
```

<span data-ttu-id="ea9ff-109">Retorna informações sobre o status da coleta de lixo.</span><span class="sxs-lookup"><span data-stu-id="ea9ff-109">Return information about the status of garbage collection.</span></span>

## <span data-ttu-id="ea9ff-110">OS</span><span class="sxs-lookup"><span data-stu-id="ea9ff-110">PARAMETERS</span></span>

### <span data-ttu-id="ea9ff-111">-Farmname</span><span class="sxs-lookup"><span data-stu-id="ea9ff-111">-FarmName</span></span>
<span data-ttu-id="ea9ff-112">ID do farm.</span><span class="sxs-lookup"><span data-stu-id="ea9ff-112">Farm Id.</span></span>

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

### <span data-ttu-id="ea9ff-113">-JobId</span><span class="sxs-lookup"><span data-stu-id="ea9ff-113">-JobId</span></span>
<span data-ttu-id="ea9ff-114">ID da operação.</span><span class="sxs-lookup"><span data-stu-id="ea9ff-114">Operation Id.</span></span>

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

### <span data-ttu-id="ea9ff-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea9ff-115">-ResourceGroupName</span></span>
<span data-ttu-id="ea9ff-116">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ea9ff-116">Resource group name.</span></span>

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

### <span data-ttu-id="ea9ff-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea9ff-117">CommonParameters</span></span>
<span data-ttu-id="ea9ff-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea9ff-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea9ff-119">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea9ff-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea9ff-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ea9ff-120">INPUTS</span></span>

## <span data-ttu-id="ea9ff-121">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ea9ff-121">OUTPUTS</span></span>

## <span data-ttu-id="ea9ff-122">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ea9ff-122">NOTES</span></span>

## <span data-ttu-id="ea9ff-123">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ea9ff-123">RELATED LINKS</span></span>
