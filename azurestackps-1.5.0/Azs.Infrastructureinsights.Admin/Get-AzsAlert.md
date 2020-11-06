---
external help file: Azs.InfrastructureInsights.Admin-help.xml
Module Name: Azs.InfrastructureInsights.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: f8fbec7ec2f8bcfc0d7595658f84866cf449d3e0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93425823"
---
# <span data-ttu-id="8c42b-101">Get-AzsAlert</span><span class="sxs-lookup"><span data-stu-id="8c42b-101">Get-AzsAlert</span></span>

## <span data-ttu-id="8c42b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8c42b-102">SYNOPSIS</span></span>
<span data-ttu-id="8c42b-103">Retorna a lista de todos os alertas em um determinado local.</span><span class="sxs-lookup"><span data-stu-id="8c42b-103">Returns the list of all alerts in a given location.</span></span>

## <span data-ttu-id="8c42b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8c42b-104">SYNTAX</span></span>

### <span data-ttu-id="8c42b-105">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="8c42b-105">List (Default)</span></span>
```
Get-AzsAlert [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Top <Int32>]
 [-Skip <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="8c42b-106">Obter</span><span class="sxs-lookup"><span data-stu-id="8c42b-106">Get</span></span>
```
Get-AzsAlert [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="8c42b-107">Identificação</span><span class="sxs-lookup"><span data-stu-id="8c42b-107">ResourceId</span></span>
```
Get-AzsAlert -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="8c42b-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8c42b-108">DESCRIPTION</span></span>
<span data-ttu-id="8c42b-109">Retorna a lista de todos os alertas em um determinado local.</span><span class="sxs-lookup"><span data-stu-id="8c42b-109">Returns the list of all alerts in a given location.</span></span>

## <span data-ttu-id="8c42b-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8c42b-110">EXAMPLES</span></span>

### <span data-ttu-id="8c42b-111">--------------------------EXEMPLO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="8c42b-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsAlert -Name 7f58eb8b-e39f-45d0-8ae7-9920b8f22f5f
```

<span data-ttu-id="8c42b-112">Obter um alerta por nome.</span><span class="sxs-lookup"><span data-stu-id="8c42b-112">Get an alert by Name.</span></span>

### <span data-ttu-id="8c42b-113">--------------------------EXEMPLO 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="8c42b-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsAlert | Where State -EQ 'active' | select FaultTypeId, Title
```

<span data-ttu-id="8c42b-114">Obter todos os alertas ativos e exibir a falha e o cargo.</span><span class="sxs-lookup"><span data-stu-id="8c42b-114">Get all active alerts and display their fault and title.</span></span>

## <span data-ttu-id="8c42b-115">OS</span><span class="sxs-lookup"><span data-stu-id="8c42b-115">PARAMETERS</span></span>

### <span data-ttu-id="8c42b-116">-Filtro</span><span class="sxs-lookup"><span data-stu-id="8c42b-116">-Filter</span></span>
<span data-ttu-id="8c42b-117">Parâmetro de filtro OData.</span><span class="sxs-lookup"><span data-stu-id="8c42b-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="8c42b-118">-Local</span><span class="sxs-lookup"><span data-stu-id="8c42b-118">-Location</span></span>
<span data-ttu-id="8c42b-119">Nome do local.</span><span class="sxs-lookup"><span data-stu-id="8c42b-119">Name of the location.</span></span>

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

### <span data-ttu-id="8c42b-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="8c42b-120">-Name</span></span>
<span data-ttu-id="8c42b-121">O identificador do alerta.</span><span class="sxs-lookup"><span data-stu-id="8c42b-121">The alert identifier.</span></span>

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

### <span data-ttu-id="8c42b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c42b-122">-ResourceGroupName</span></span>
<span data-ttu-id="8c42b-123">Nome do grupo de recursos do qual o recurso reside.</span><span class="sxs-lookup"><span data-stu-id="8c42b-123">Resource group name which the resource resides.</span></span>

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

### <span data-ttu-id="8c42b-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8c42b-124">-ResourceId</span></span>
<span data-ttu-id="8c42b-125">A ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="8c42b-125">The resource id.</span></span>

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

### <span data-ttu-id="8c42b-126">-Skip</span><span class="sxs-lookup"><span data-stu-id="8c42b-126">-Skip</span></span>
<span data-ttu-id="8c42b-127">Ignorar os primeiros N itens conforme especificado pelo valor do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="8c42b-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="8c42b-128">-Início</span><span class="sxs-lookup"><span data-stu-id="8c42b-128">-Top</span></span>
<span data-ttu-id="8c42b-129">Retorne os N principais itens conforme especificado pelo valor do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="8c42b-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="8c42b-130">Aplica-se após o parâmetro-Skip.</span><span class="sxs-lookup"><span data-stu-id="8c42b-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="8c42b-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c42b-131">CommonParameters</span></span>
<span data-ttu-id="8c42b-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8c42b-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c42b-133">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8c42b-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c42b-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8c42b-134">INPUTS</span></span>

## <span data-ttu-id="8c42b-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8c42b-135">OUTPUTS</span></span>

### <span data-ttu-id="8c42b-136">Microsoft. AzureStack. Management. InfrastructureInsights. admin. Models. Alert</span><span class="sxs-lookup"><span data-stu-id="8c42b-136">Microsoft.AzureStack.Management.InfrastructureInsights.Admin.Models.Alert</span></span>

## <span data-ttu-id="8c42b-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8c42b-137">NOTES</span></span>

## <span data-ttu-id="8c42b-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8c42b-138">RELATED LINKS</span></span>
