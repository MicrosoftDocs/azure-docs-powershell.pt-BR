---
external help file: Azs.InfrastructureInsights.Admin-help.xml
Module Name: Azs.Infrastructureinsights.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4285a7423390f5d9b5384faa63f95c4206840d71
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2020
ms.locfileid: "93775102"
---
# <span data-ttu-id="bdd8a-101">Get-AzsRegistrationHealth</span><span class="sxs-lookup"><span data-stu-id="bdd8a-101">Get-AzsRegistrationHealth</span></span>

## <span data-ttu-id="bdd8a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bdd8a-102">SYNOPSIS</span></span>
<span data-ttu-id="bdd8a-103">Retorna uma lista da integridade de cada recurso em um serviço.</span><span class="sxs-lookup"><span data-stu-id="bdd8a-103">Returns a list of each resource's health under a service.</span></span>

## <span data-ttu-id="bdd8a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bdd8a-104">SYNTAX</span></span>

### <span data-ttu-id="bdd8a-105">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="bdd8a-105">List (Default)</span></span>
```
Get-AzsRegistrationHealth -ServiceRegistrationId <String> [-Location <String>] [-ResourceGroupName <String>]
 [-Filter <String>] [-Top <Int32>] [-Skip <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="bdd8a-106">Obter</span><span class="sxs-lookup"><span data-stu-id="bdd8a-106">Get</span></span>
```
Get-AzsRegistrationHealth -ServiceRegistrationId <String> -ResourceRegistrationId <String> [-Location <String>]
 [-ResourceGroupName <String>] [-Filter <String>] [<CommonParameters>]
```

### <span data-ttu-id="bdd8a-107">Identificação</span><span class="sxs-lookup"><span data-stu-id="bdd8a-107">ResourceId</span></span>
```
Get-AzsRegistrationHealth -ResourceId <String> [-Filter <String>] [<CommonParameters>]
```

## <span data-ttu-id="bdd8a-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="bdd8a-108">DESCRIPTION</span></span>
<span data-ttu-id="bdd8a-109">Retorna uma lista da integridade de cada recurso em um serviço.</span><span class="sxs-lookup"><span data-stu-id="bdd8a-109">Returns a list of each resource's health under a service.</span></span>

## <span data-ttu-id="bdd8a-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bdd8a-110">EXAMPLES</span></span>

### <span data-ttu-id="bdd8a-111">EXEMPLO 1</span><span class="sxs-lookup"><span data-stu-id="bdd8a-111">EXAMPLE 1</span></span>
```
Get-AzsRegistrationHealth -ServiceRegistrationId e56bc7b8-c8b5-4e25-b00c-4f951effb22c
```

<span data-ttu-id="bdd8a-112">Retorna uma lista da integridade de cada recurso em um serviço.</span><span class="sxs-lookup"><span data-stu-id="bdd8a-112">Returns a list of each resource's health under a service.</span></span>

### <span data-ttu-id="bdd8a-113">EXEMPLO 2</span><span class="sxs-lookup"><span data-stu-id="bdd8a-113">EXAMPLE 2</span></span>
```
Get-AzsRPHealth | Where {$_.NamespaceProperty -eq 'Microsoft.Fabric.Admin'} | % { Get-AzsRegistrationHealth -ServiceRegistrationId $_.RegistrationId } | select ResourceName, HealthState
```

<span data-ttu-id="bdd8a-114">Retorna o status de integridade em a para Microsoft. Fabric. admin.</span><span class="sxs-lookup"><span data-stu-id="bdd8a-114">Returns health status under a for Microsoft.Fabric.Admin.</span></span>

## <span data-ttu-id="bdd8a-115">OS</span><span class="sxs-lookup"><span data-stu-id="bdd8a-115">PARAMETERS</span></span>

### <span data-ttu-id="bdd8a-116">-Registroid</span><span class="sxs-lookup"><span data-stu-id="bdd8a-116">-ServiceRegistrationId</span></span>
<span data-ttu-id="bdd8a-117">ID de registro do serviço.</span><span class="sxs-lookup"><span data-stu-id="bdd8a-117">Service registration id.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdd8a-118">-ResourceRegistrationId</span><span class="sxs-lookup"><span data-stu-id="bdd8a-118">-ResourceRegistrationId</span></span>


```yaml
Type: String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdd8a-119">-Local</span><span class="sxs-lookup"><span data-stu-id="bdd8a-119">-Location</span></span>
<span data-ttu-id="bdd8a-120">Nome da região</span><span class="sxs-lookup"><span data-stu-id="bdd8a-120">Name of the region</span></span>

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

### <span data-ttu-id="bdd8a-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bdd8a-121">-ResourceGroupName</span></span>
<span data-ttu-id="bdd8a-122">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="bdd8a-122">Name of the resource group.</span></span>

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

### <span data-ttu-id="bdd8a-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bdd8a-123">-ResourceId</span></span>
<span data-ttu-id="bdd8a-124">A ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="bdd8a-124">The resource id.</span></span>

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

### <span data-ttu-id="bdd8a-125">-Filtro</span><span class="sxs-lookup"><span data-stu-id="bdd8a-125">-Filter</span></span>
<span data-ttu-id="bdd8a-126">Parâmetro de filtro OData.</span><span class="sxs-lookup"><span data-stu-id="bdd8a-126">OData filter parameter.</span></span>

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

### <span data-ttu-id="bdd8a-127">-Início</span><span class="sxs-lookup"><span data-stu-id="bdd8a-127">-Top</span></span>
<span data-ttu-id="bdd8a-128">Retorne os N principais itens conforme especificado pelo valor do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="bdd8a-128">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="bdd8a-129">Aplica-se após o parâmetro-Skip.</span><span class="sxs-lookup"><span data-stu-id="bdd8a-129">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="bdd8a-130">-Skip</span><span class="sxs-lookup"><span data-stu-id="bdd8a-130">-Skip</span></span>
<span data-ttu-id="bdd8a-131">Ignorar os primeiros N itens conforme especificado pelo valor do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="bdd8a-131">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="bdd8a-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bdd8a-132">CommonParameters</span></span>
<span data-ttu-id="bdd8a-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bdd8a-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bdd8a-134">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bdd8a-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bdd8a-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="bdd8a-135">INPUTS</span></span>

## <span data-ttu-id="bdd8a-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="bdd8a-136">OUTPUTS</span></span>

### <span data-ttu-id="bdd8a-137">Microsoft. AzureStack. Management. InfrastructureInsights. admin. Models. ResourceHealth</span><span class="sxs-lookup"><span data-stu-id="bdd8a-137">Microsoft.AzureStack.Management.InfrastructureInsights.Admin.Models.ResourceHealth</span></span>

## <span data-ttu-id="bdd8a-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="bdd8a-138">NOTES</span></span>

## <span data-ttu-id="bdd8a-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bdd8a-139">RELATED LINKS</span></span>
