---
external help file: Azs.InfrastructureInsights.Admin-help.xml
Module Name: Azs.InfrastructureInsights.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7e42278eb4ed402d561399dbd1077f819ef3d2cd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93774446"
---
# <span data-ttu-id="9e2c0-101">Get-AzsRPHealth</span><span class="sxs-lookup"><span data-stu-id="9e2c0-101">Get-AzsRPHealth</span></span>

## <span data-ttu-id="9e2c0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9e2c0-102">SYNOPSIS</span></span>
<span data-ttu-id="9e2c0-103">Retorna uma lista da integridade de cada serviço.</span><span class="sxs-lookup"><span data-stu-id="9e2c0-103">Returns a list of each service's health.</span></span>

## <span data-ttu-id="9e2c0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9e2c0-104">SYNTAX</span></span>

### <span data-ttu-id="9e2c0-105">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="9e2c0-105">List (Default)</span></span>
```
Get-AzsRPHealth [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="9e2c0-106">Obter</span><span class="sxs-lookup"><span data-stu-id="9e2c0-106">Get</span></span>
```
Get-AzsRPHealth [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="9e2c0-107">Identificação</span><span class="sxs-lookup"><span data-stu-id="9e2c0-107">ResourceId</span></span>
```
Get-AzsRPHealth -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="9e2c0-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9e2c0-108">DESCRIPTION</span></span>
<span data-ttu-id="9e2c0-109">Retorna uma lista da integridade de cada serviço.</span><span class="sxs-lookup"><span data-stu-id="9e2c0-109">Returns a list of each service's health.</span></span> <span data-ttu-id="9e2c0-110">A propriedade AlertSummary inclui detalhes sobre contagens de aviso/erro.</span><span class="sxs-lookup"><span data-stu-id="9e2c0-110">The AlertSummary property includes details on warning/error counts.</span></span>

## <span data-ttu-id="9e2c0-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9e2c0-111">EXAMPLES</span></span>

### <span data-ttu-id="9e2c0-112">--------------------------EXEMPLO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="9e2c0-112">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsRPHealth
```

<span data-ttu-id="9e2c0-113">Retorna uma lista da integridade de cada serviço.</span><span class="sxs-lookup"><span data-stu-id="9e2c0-113">Returns a list of each service's health.</span></span>

### <span data-ttu-id="9e2c0-114">--------------------------EXEMPLO 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="9e2c0-114">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsRPHealth -Name "e56bc7b8-c8b5-4e25-b00c-4f951effb22c"
```

<span data-ttu-id="9e2c0-115">Retorna a integridade de um serviço.</span><span class="sxs-lookup"><span data-stu-id="9e2c0-115">Returns a service's health.</span></span>

## <span data-ttu-id="9e2c0-116">OS</span><span class="sxs-lookup"><span data-stu-id="9e2c0-116">PARAMETERS</span></span>

### <span data-ttu-id="9e2c0-117">-Filtro</span><span class="sxs-lookup"><span data-stu-id="9e2c0-117">-Filter</span></span>
<span data-ttu-id="9e2c0-118">Parâmetro de filtro OData.</span><span class="sxs-lookup"><span data-stu-id="9e2c0-118">OData filter parameter.</span></span>

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

### <span data-ttu-id="9e2c0-119">-Local</span><span class="sxs-lookup"><span data-stu-id="9e2c0-119">-Location</span></span>
<span data-ttu-id="9e2c0-120">Nome da região</span><span class="sxs-lookup"><span data-stu-id="9e2c0-120">Name of the region</span></span>

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

### <span data-ttu-id="9e2c0-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="9e2c0-121">-Name</span></span>
<span data-ttu-id="9e2c0-122">Nome da integridade do serviço.</span><span class="sxs-lookup"><span data-stu-id="9e2c0-122">Service Health name.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: ServiceHealth

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e2c0-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e2c0-123">-ResourceGroupName</span></span>
<span data-ttu-id="9e2c0-124">Nome do grupo de recursos do qual o recurso reside.</span><span class="sxs-lookup"><span data-stu-id="9e2c0-124">Resource group name which the resource resides.</span></span>

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

### <span data-ttu-id="9e2c0-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9e2c0-125">-ResourceId</span></span>
<span data-ttu-id="9e2c0-126">A ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="9e2c0-126">The resource id.</span></span>

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

### <span data-ttu-id="9e2c0-127">-Skip</span><span class="sxs-lookup"><span data-stu-id="9e2c0-127">-Skip</span></span>
<span data-ttu-id="9e2c0-128">Ignorar os primeiros N itens conforme especificado pelo valor do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="9e2c0-128">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="9e2c0-129">-Início</span><span class="sxs-lookup"><span data-stu-id="9e2c0-129">-Top</span></span>
<span data-ttu-id="9e2c0-130">Retorne os N principais itens conforme especificado pelo valor do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="9e2c0-130">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="9e2c0-131">Aplica-se após o parâmetro-Skip.</span><span class="sxs-lookup"><span data-stu-id="9e2c0-131">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="9e2c0-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e2c0-132">CommonParameters</span></span>
<span data-ttu-id="9e2c0-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e2c0-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e2c0-134">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e2c0-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e2c0-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9e2c0-135">INPUTS</span></span>

## <span data-ttu-id="9e2c0-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9e2c0-136">OUTPUTS</span></span>

### <span data-ttu-id="9e2c0-137">Microsoft. AzureStack. Management. InfrastructureInsights. admin. Models. imhealth</span><span class="sxs-lookup"><span data-stu-id="9e2c0-137">Microsoft.AzureStack.Management.InfrastructureInsights.Admin.Models.ServiceHealth</span></span>

## <span data-ttu-id="9e2c0-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9e2c0-138">NOTES</span></span>

## <span data-ttu-id="9e2c0-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9e2c0-139">RELATED LINKS</span></span>

