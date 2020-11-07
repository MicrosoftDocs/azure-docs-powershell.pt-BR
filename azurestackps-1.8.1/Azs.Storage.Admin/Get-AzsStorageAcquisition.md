---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3a53b5af4cf77ec961e65f8c0c0d84b05b4adfa1
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2020
ms.locfileid: "93775056"
---
# <span data-ttu-id="0643a-101">Get-AzsStorageAcquisition</span><span class="sxs-lookup"><span data-stu-id="0643a-101">Get-AzsStorageAcquisition</span></span>

## <span data-ttu-id="0643a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0643a-102">SYNOPSIS</span></span>
<span data-ttu-id="0643a-103">Retorna uma lista de Acquistions de BLOB.</span><span class="sxs-lookup"><span data-stu-id="0643a-103">Returns a list of blob acquistions.</span></span>

## <span data-ttu-id="0643a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0643a-104">SYNTAX</span></span>

```
Get-AzsStorageAcquisition [-FarmName] <String> [-ResourceGroupName <String>] [-Filter <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="0643a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0643a-105">DESCRIPTION</span></span>
<span data-ttu-id="0643a-106">Retorna uma lista de Acquistions de BLOB.</span><span class="sxs-lookup"><span data-stu-id="0643a-106">Returns a list of blob acquistions.</span></span>

## <span data-ttu-id="0643a-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0643a-107">EXAMPLES</span></span>

### <span data-ttu-id="0643a-108">EXEMPLO 1</span><span class="sxs-lookup"><span data-stu-id="0643a-108">EXAMPLE 1</span></span>
```
Get-AzsStorageAcquisition -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376
```

<span data-ttu-id="0643a-109">Obtenha a lista de Acquistions de BLOB.</span><span class="sxs-lookup"><span data-stu-id="0643a-109">Get the list of blob acquistions.</span></span>

### <span data-ttu-id="0643a-110">EXEMPLO 2</span><span class="sxs-lookup"><span data-stu-id="0643a-110">EXAMPLE 2</span></span>
```
Get-AzsStorageAcquisition -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376 -Filter "startswith(properties/Storageaccount, 'Test'"
```

<span data-ttu-id="0643a-111">Obtenha a lista de Acquistions de BLOB.</span><span class="sxs-lookup"><span data-stu-id="0643a-111">Get the list of blob acquistions.</span></span>

## <span data-ttu-id="0643a-112">OS</span><span class="sxs-lookup"><span data-stu-id="0643a-112">PARAMETERS</span></span>

### <span data-ttu-id="0643a-113">-Farmname</span><span class="sxs-lookup"><span data-stu-id="0643a-113">-FarmName</span></span>
<span data-ttu-id="0643a-114">ID do farm.</span><span class="sxs-lookup"><span data-stu-id="0643a-114">Farm Id.</span></span>

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

### <span data-ttu-id="0643a-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0643a-115">-ResourceGroupName</span></span>
<span data-ttu-id="0643a-116">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="0643a-116">Resource group name.</span></span>

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

### <span data-ttu-id="0643a-117">-Filtro</span><span class="sxs-lookup"><span data-stu-id="0643a-117">-Filter</span></span>
<span data-ttu-id="0643a-118">Cadeia de caracteres de filtro</span><span class="sxs-lookup"><span data-stu-id="0643a-118">Filter string</span></span>

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

### <span data-ttu-id="0643a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0643a-119">CommonParameters</span></span>
<span data-ttu-id="0643a-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0643a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0643a-121">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0643a-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0643a-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0643a-122">INPUTS</span></span>

## <span data-ttu-id="0643a-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0643a-123">OUTPUTS</span></span>

## <span data-ttu-id="0643a-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0643a-124">NOTES</span></span>

## <span data-ttu-id="0643a-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0643a-125">RELATED LINKS</span></span>
