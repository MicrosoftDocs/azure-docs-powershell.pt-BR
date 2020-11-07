---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 793bf4a4b5b9dfb448c5b2a1baf9d74af592a23e
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/08/2020
ms.locfileid: "93946647"
---
# <span data-ttu-id="89bef-101">Get-AzsEdgeGateway</span><span class="sxs-lookup"><span data-stu-id="89bef-101">Get-AzsEdgeGateway</span></span>

## <span data-ttu-id="89bef-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="89bef-102">SYNOPSIS</span></span>
<span data-ttu-id="89bef-103">Retorna a lista de todos os gateways de borda em um determinado local.</span><span class="sxs-lookup"><span data-stu-id="89bef-103">Returns the list of all edge gateways at a certain location.</span></span>

## <span data-ttu-id="89bef-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="89bef-104">SYNTAX</span></span>

### <span data-ttu-id="89bef-105">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="89bef-105">List (Default)</span></span>
```
Get-AzsEdgeGateway [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="89bef-106">Obter</span><span class="sxs-lookup"><span data-stu-id="89bef-106">Get</span></span>
```
Get-AzsEdgeGateway [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="89bef-107">Identificação</span><span class="sxs-lookup"><span data-stu-id="89bef-107">ResourceId</span></span>
```
Get-AzsEdgeGateway -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="89bef-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="89bef-108">DESCRIPTION</span></span>
<span data-ttu-id="89bef-109">Retorna a lista de todos os gateways de borda em um determinado local.</span><span class="sxs-lookup"><span data-stu-id="89bef-109">Returns the list of all edge gateways at a certain location.</span></span>

## <span data-ttu-id="89bef-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="89bef-110">EXAMPLES</span></span>

### <span data-ttu-id="89bef-111">EXEMPLO 1</span><span class="sxs-lookup"><span data-stu-id="89bef-111">EXAMPLE 1</span></span>
```
Get-AzsEdgeGateway
```

<span data-ttu-id="89bef-112">Obter uma lista de todos os gateways de borda.</span><span class="sxs-lookup"><span data-stu-id="89bef-112">Get a list of all edge gateways.</span></span>

### <span data-ttu-id="89bef-113">EXEMPLO 2</span><span class="sxs-lookup"><span data-stu-id="89bef-113">EXAMPLE 2</span></span>
```
Get-AzsEdgeGateway -Name "AzS-Gwy01"
```

<span data-ttu-id="89bef-114">Obter um gateway de borda específico.</span><span class="sxs-lookup"><span data-stu-id="89bef-114">Get a specific edge gateway.</span></span>

## <span data-ttu-id="89bef-115">OS</span><span class="sxs-lookup"><span data-stu-id="89bef-115">PARAMETERS</span></span>

### <span data-ttu-id="89bef-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="89bef-116">-Name</span></span>
<span data-ttu-id="89bef-117">Nome do gateway de borda.</span><span class="sxs-lookup"><span data-stu-id="89bef-117">Name of the edge gateway.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89bef-118">-Local</span><span class="sxs-lookup"><span data-stu-id="89bef-118">-Location</span></span>
<span data-ttu-id="89bef-119">Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="89bef-119">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89bef-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89bef-120">-ResourceGroupName</span></span>
<span data-ttu-id="89bef-121">Grupo de recursos no qual o provedor de recursos foi registrado.</span><span class="sxs-lookup"><span data-stu-id="89bef-121">Resource group in which the resource provider has been registered.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89bef-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="89bef-122">-ResourceId</span></span>
<span data-ttu-id="89bef-123">A ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="89bef-123">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89bef-124">-Filtro</span><span class="sxs-lookup"><span data-stu-id="89bef-124">-Filter</span></span>
<span data-ttu-id="89bef-125">Parâmetro de filtro OData.</span><span class="sxs-lookup"><span data-stu-id="89bef-125">OData filter parameter.</span></span>

```yaml
Type: String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89bef-126">-Skip</span><span class="sxs-lookup"><span data-stu-id="89bef-126">-Skip</span></span>
<span data-ttu-id="89bef-127">Ignorar os primeiros N itens conforme especificado pelo valor do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="89bef-127">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89bef-128">-Início</span><span class="sxs-lookup"><span data-stu-id="89bef-128">-Top</span></span>
<span data-ttu-id="89bef-129">Retorne os N principais itens conforme especificado pelo valor do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="89bef-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="89bef-130">Aplica-se após o parâmetro-Skip.</span><span class="sxs-lookup"><span data-stu-id="89bef-130">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89bef-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89bef-131">CommonParameters</span></span>
<span data-ttu-id="89bef-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89bef-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89bef-133">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="89bef-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89bef-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="89bef-134">INPUTS</span></span>

## <span data-ttu-id="89bef-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="89bef-135">OUTPUTS</span></span>

### <span data-ttu-id="89bef-136">Microsoft. AzureStack. Management. Fabric. admin. Models. EdgeGateway</span><span class="sxs-lookup"><span data-stu-id="89bef-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.EdgeGateway</span></span>

## <span data-ttu-id="89bef-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="89bef-137">NOTES</span></span>

## <span data-ttu-id="89bef-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="89bef-138">RELATED LINKS</span></span>
