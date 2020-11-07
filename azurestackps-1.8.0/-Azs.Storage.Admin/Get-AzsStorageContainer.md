---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4847310f65a0b652d15321cd49583212ef5844d8
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2020
ms.locfileid: "93774837"
---
# <span data-ttu-id="b3bef-101">Get-AzsStorageContainer</span><span class="sxs-lookup"><span data-stu-id="b3bef-101">Get-AzsStorageContainer</span></span>

## <span data-ttu-id="b3bef-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b3bef-102">SYNOPSIS</span></span>
<span data-ttu-id="b3bef-103">Retorna a lista de contêineres que podem ser migrados no compartilhamento especificado.</span><span class="sxs-lookup"><span data-stu-id="b3bef-103">Returns the list of containers which can be migrated in the specified share.</span></span>

## <span data-ttu-id="b3bef-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b3bef-104">SYNTAX</span></span>

```
Get-AzsStorageContainer [-FarmName] <String> [-ShareName] <String> [[-ResourceGroupName] <String>]
 [[-MaxCount] <Int32>] [[-StartIndex] <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="b3bef-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b3bef-105">DESCRIPTION</span></span>
<span data-ttu-id="b3bef-106">Retorna a lista de contêineres que podem ser migrados no compartilhamento especificado.</span><span class="sxs-lookup"><span data-stu-id="b3bef-106">Returns the list of containers which can be migrated in the specified share.</span></span>

## <span data-ttu-id="b3bef-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b3bef-107">EXAMPLES</span></span>

### <span data-ttu-id="b3bef-108">--------------------------EXEMPLO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="b3bef-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsStorageContainer -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376 -ShareName "||SU1FileServer.azurestack.local|SU1_ObjStore"
```

<span data-ttu-id="b3bef-109">Obter uma lista de contêineres que podem ser migrados no compartilhamento especificado.</span><span class="sxs-lookup"><span data-stu-id="b3bef-109">Get a list of containers which can be migrated in the specified share.</span></span>

## <span data-ttu-id="b3bef-110">OS</span><span class="sxs-lookup"><span data-stu-id="b3bef-110">PARAMETERS</span></span>

### <span data-ttu-id="b3bef-111">-Farmname</span><span class="sxs-lookup"><span data-stu-id="b3bef-111">-FarmName</span></span>
<span data-ttu-id="b3bef-112">ID do farm.</span><span class="sxs-lookup"><span data-stu-id="b3bef-112">Farm Id.</span></span>

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

### <span data-ttu-id="b3bef-113">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="b3bef-113">-MaxCount</span></span>
<span data-ttu-id="b3bef-114">A contagem máx de contêineres.</span><span class="sxs-lookup"><span data-stu-id="b3bef-114">The max count of containers.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: 100000000
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3bef-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3bef-115">-ResourceGroupName</span></span>
<span data-ttu-id="b3bef-116">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b3bef-116">Resource group name.</span></span>

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

### <span data-ttu-id="b3bef-117">-ShareName</span><span class="sxs-lookup"><span data-stu-id="b3bef-117">-ShareName</span></span>
<span data-ttu-id="b3bef-118">Nome do compartilhamento que mantém os contêineres de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="b3bef-118">Share name which holds the storage containers.</span></span>

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

### <span data-ttu-id="b3bef-119">-StartIndex</span><span class="sxs-lookup"><span data-stu-id="b3bef-119">-StartIndex</span></span>
<span data-ttu-id="b3bef-120">O índice inicial de contêineres Get.</span><span class="sxs-lookup"><span data-stu-id="b3bef-120">The start index of get containers.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3bef-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3bef-121">CommonParameters</span></span>
<span data-ttu-id="b3bef-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b3bef-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3bef-123">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b3bef-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3bef-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b3bef-124">INPUTS</span></span>

## <span data-ttu-id="b3bef-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b3bef-125">OUTPUTS</span></span>

## <span data-ttu-id="b3bef-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b3bef-126">NOTES</span></span>

## <span data-ttu-id="b3bef-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b3bef-127">RELATED LINKS</span></span>

