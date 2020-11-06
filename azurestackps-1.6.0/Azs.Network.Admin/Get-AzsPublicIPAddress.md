---
external help file: Azs.Network.Admin-help.xml
Module Name: Azs.Network.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3996096b692a7e242fc6cf42288508bdc4625cd2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93426091"
---
# <span data-ttu-id="a8959-101">Get-AzsPublicIPAddress</span><span class="sxs-lookup"><span data-stu-id="a8959-101">Get-AzsPublicIPAddress</span></span>

## <span data-ttu-id="a8959-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a8959-102">SYNOPSIS</span></span>
<span data-ttu-id="a8959-103">Lista de endereços IP públicos.</span><span class="sxs-lookup"><span data-stu-id="a8959-103">List of public IP addresses.</span></span>

## <span data-ttu-id="a8959-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a8959-104">SYNTAX</span></span>

```
Get-AzsPublicIPAddress [[-Filter] <String>] [[-OrderBy] <String>] [[-Skip] <Int32>] [[-Top] <Int32>]
 [[-InlineCount] <String>] [<CommonParameters>]
```

## <span data-ttu-id="a8959-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a8959-105">DESCRIPTION</span></span>
<span data-ttu-id="a8959-106">Lista de endereços IP públicos.</span><span class="sxs-lookup"><span data-stu-id="a8959-106">List of public IP addresses.</span></span>

## <span data-ttu-id="a8959-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a8959-107">EXAMPLES</span></span>

### <span data-ttu-id="a8959-108">--------------------------EXEMPLO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="a8959-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsPublicIPAddress
```

<span data-ttu-id="a8959-109">Obter a lista de endereços IP públicos, atribuídos ou não atribuídos.</span><span class="sxs-lookup"><span data-stu-id="a8959-109">Get the list of public ip addresses, either allocated or not allocated.</span></span>

## <span data-ttu-id="a8959-110">OS</span><span class="sxs-lookup"><span data-stu-id="a8959-110">PARAMETERS</span></span>

### <span data-ttu-id="a8959-111">-Filtro</span><span class="sxs-lookup"><span data-stu-id="a8959-111">-Filter</span></span>
<span data-ttu-id="a8959-112">Parâmetro de filtro OData.</span><span class="sxs-lookup"><span data-stu-id="a8959-112">OData filter parameter.</span></span>

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

### <span data-ttu-id="a8959-113">-InlineCount</span><span class="sxs-lookup"><span data-stu-id="a8959-113">-InlineCount</span></span>
<span data-ttu-id="a8959-114">Parâmetro de contagem embutida do OData.</span><span class="sxs-lookup"><span data-stu-id="a8959-114">OData inline count parameter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8959-115">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="a8959-115">-OrderBy</span></span>
<span data-ttu-id="a8959-116">Parâmetro orderBy do OData.</span><span class="sxs-lookup"><span data-stu-id="a8959-116">OData orderBy parameter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8959-117">-Skip</span><span class="sxs-lookup"><span data-stu-id="a8959-117">-Skip</span></span>
<span data-ttu-id="a8959-118">Ignorar os primeiros N itens conforme especificado pelo valor do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="a8959-118">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8959-119">-Início</span><span class="sxs-lookup"><span data-stu-id="a8959-119">-Top</span></span>
<span data-ttu-id="a8959-120">Retorne os N principais itens conforme especificado pelo valor do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="a8959-120">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="a8959-121">Aplica-se após o parâmetro-Skip.</span><span class="sxs-lookup"><span data-stu-id="a8959-121">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8959-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8959-122">CommonParameters</span></span>
<span data-ttu-id="a8959-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a8959-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8959-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a8959-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8959-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a8959-125">INPUTS</span></span>

## <span data-ttu-id="a8959-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a8959-126">OUTPUTS</span></span>

### <span data-ttu-id="a8959-127">Microsoft. AzureStack. Management. Network. admin. Models. PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="a8959-127">Microsoft.AzureStack.Management.Network.Admin.Models.PublicIpAddress</span></span>

## <span data-ttu-id="a8959-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a8959-128">NOTES</span></span>

## <span data-ttu-id="a8959-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a8959-129">RELATED LINKS</span></span>

