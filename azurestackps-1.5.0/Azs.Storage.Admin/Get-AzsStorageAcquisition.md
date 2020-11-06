---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3562b169211d4c3b1f87260be37a94f6de2e8b85
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93426060"
---
# <span data-ttu-id="24592-101">Get-AzsStorageAcquisition</span><span class="sxs-lookup"><span data-stu-id="24592-101">Get-AzsStorageAcquisition</span></span>

## <span data-ttu-id="24592-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="24592-102">SYNOPSIS</span></span>
<span data-ttu-id="24592-103">Retorna uma lista de Acquistions de BLOB.</span><span class="sxs-lookup"><span data-stu-id="24592-103">Returns a list of blob acquistions.</span></span>

## <span data-ttu-id="24592-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="24592-104">SYNTAX</span></span>

```
Get-AzsStorageAcquisition [-FarmName] <String> [-ResourceGroupName <String>] [-Filter <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="24592-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="24592-105">DESCRIPTION</span></span>
<span data-ttu-id="24592-106">Retorna uma lista de Acquistions de BLOB.</span><span class="sxs-lookup"><span data-stu-id="24592-106">Returns a list of blob acquistions.</span></span>

## <span data-ttu-id="24592-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="24592-107">EXAMPLES</span></span>

### <span data-ttu-id="24592-108">--------------------------EXEMPLO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="24592-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsStorageAcquisition -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376
```

<span data-ttu-id="24592-109">Obtenha a lista de Acquistions de BLOB.</span><span class="sxs-lookup"><span data-stu-id="24592-109">Get the list of blob acquistions.</span></span>

### <span data-ttu-id="24592-110">--------------------------EXEMPLO 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="24592-110">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsStorageAcquisition -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376 -Filter "startswith(properties/Storageaccount, 'Test'"
```

<span data-ttu-id="24592-111">Obtenha a lista de Acquistions de BLOB.</span><span class="sxs-lookup"><span data-stu-id="24592-111">Get the list of blob acquistions.</span></span>

## <span data-ttu-id="24592-112">OS</span><span class="sxs-lookup"><span data-stu-id="24592-112">PARAMETERS</span></span>

### <span data-ttu-id="24592-113">-Farmname</span><span class="sxs-lookup"><span data-stu-id="24592-113">-FarmName</span></span>
<span data-ttu-id="24592-114">ID do farm.</span><span class="sxs-lookup"><span data-stu-id="24592-114">Farm Id.</span></span>

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

### <span data-ttu-id="24592-115">-Filtro</span><span class="sxs-lookup"><span data-stu-id="24592-115">-Filter</span></span>
<span data-ttu-id="24592-116">Cadeia de caracteres de filtro</span><span class="sxs-lookup"><span data-stu-id="24592-116">Filter string</span></span>

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

### <span data-ttu-id="24592-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24592-117">-ResourceGroupName</span></span>
<span data-ttu-id="24592-118">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="24592-118">Resource group name.</span></span>

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

### <span data-ttu-id="24592-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24592-119">CommonParameters</span></span>
<span data-ttu-id="24592-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24592-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24592-121">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24592-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24592-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="24592-122">INPUTS</span></span>

## <span data-ttu-id="24592-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="24592-123">OUTPUTS</span></span>

## <span data-ttu-id="24592-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="24592-124">NOTES</span></span>

## <span data-ttu-id="24592-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="24592-125">RELATED LINKS</span></span>

