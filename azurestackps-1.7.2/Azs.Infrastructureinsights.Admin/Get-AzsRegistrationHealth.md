---
external help file: Azs.InfrastructureInsights.Admin-help.xml
Module Name: Azs.InfrastructureInsights.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: d73e2db2f09ba504e9c6adbf15a0bbc2629452ae
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93774500"
---
# <span data-ttu-id="cf0c3-101">Get-AzsRegistrationHealth</span><span class="sxs-lookup"><span data-stu-id="cf0c3-101">Get-AzsRegistrationHealth</span></span>

## <span data-ttu-id="cf0c3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cf0c3-102">SYNOPSIS</span></span>
<span data-ttu-id="cf0c3-103">Retorna uma lista da integridade de cada recurso em um serviço.</span><span class="sxs-lookup"><span data-stu-id="cf0c3-103">Returns a list of each resource's health under a service.</span></span>

## <span data-ttu-id="cf0c3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cf0c3-104">SYNTAX</span></span>

### <span data-ttu-id="cf0c3-105">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="cf0c3-105">List (Default)</span></span>
```
Get-AzsRegistrationHealth -ServiceRegistrationName <String> [-Location <String>] [-ResourceGroupName <String>]
 [-Filter <String>] [-Top <Int32>] [-Skip <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="cf0c3-106">Obter</span><span class="sxs-lookup"><span data-stu-id="cf0c3-106">Get</span></span>
```
Get-AzsRegistrationHealth -ServiceRegistrationName <String> -Name <String> [-Location <String>]
 [-ResourceGroupName <String>] [-Filter <String>] [<CommonParameters>]
```

### <span data-ttu-id="cf0c3-107">Identificação</span><span class="sxs-lookup"><span data-stu-id="cf0c3-107">ResourceId</span></span>
```
Get-AzsRegistrationHealth -ResourceId <String> [-Filter <String>] [<CommonParameters>]
```

## <span data-ttu-id="cf0c3-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="cf0c3-108">DESCRIPTION</span></span>
<span data-ttu-id="cf0c3-109">Retorna uma lista da integridade de cada recurso em um serviço.</span><span class="sxs-lookup"><span data-stu-id="cf0c3-109">Returns a list of each resource's health under a service.</span></span>

## <span data-ttu-id="cf0c3-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cf0c3-110">EXAMPLES</span></span>

### <span data-ttu-id="cf0c3-111">--------------------------EXEMPLO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="cf0c3-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsRegistrationHealth -ServiceRegistrationName e56bc7b8-c8b5-4e25-b00c-4f951effb22c
```

<span data-ttu-id="cf0c3-112">Retorna uma lista da integridade de cada recurso em um serviço.</span><span class="sxs-lookup"><span data-stu-id="cf0c3-112">Returns a list of each resource's health under a service.</span></span>

### <span data-ttu-id="cf0c3-113">--------------------------EXEMPLO 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="cf0c3-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsRPHealth | Where {$_.NamespaceProperty -eq 'Microsoft.Fabric.Admin'} | % { Get-AzsRegistrationHealth -ServiceRegistrationName $_.RegistrationId } | select ResourceName, HealthState
```

<span data-ttu-id="cf0c3-114">Retorna o status de integridade em a para Microsoft. Fabric. admin.</span><span class="sxs-lookup"><span data-stu-id="cf0c3-114">Returns health status under a for Microsoft.Fabric.Admin.</span></span>

## <span data-ttu-id="cf0c3-115">OS</span><span class="sxs-lookup"><span data-stu-id="cf0c3-115">PARAMETERS</span></span>

### <span data-ttu-id="cf0c3-116">-Filtro</span><span class="sxs-lookup"><span data-stu-id="cf0c3-116">-Filter</span></span>
<span data-ttu-id="cf0c3-117">Parâmetro de filtro OData.</span><span class="sxs-lookup"><span data-stu-id="cf0c3-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="cf0c3-118">-Local</span><span class="sxs-lookup"><span data-stu-id="cf0c3-118">-Location</span></span>
<span data-ttu-id="cf0c3-119">Nome da região</span><span class="sxs-lookup"><span data-stu-id="cf0c3-119">Name of the region</span></span>

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

### <span data-ttu-id="cf0c3-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="cf0c3-120">-Name</span></span>
<span data-ttu-id="cf0c3-121">O nome do recurso do objeto de integridade que corresponde à ID de registro do recurso.</span><span class="sxs-lookup"><span data-stu-id="cf0c3-121">The resource name of the health object which corresponds to the resource registration id.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: ResourceRegistrationId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf0c3-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf0c3-122">-ResourceGroupName</span></span>
<span data-ttu-id="cf0c3-123">Nome do grupo de recursos do qual o recurso reside.</span><span class="sxs-lookup"><span data-stu-id="cf0c3-123">Resource group name which the resource resides.</span></span>

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

### <span data-ttu-id="cf0c3-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cf0c3-124">-ResourceId</span></span>
<span data-ttu-id="cf0c3-125">A ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="cf0c3-125">The resource id.</span></span>

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

### <span data-ttu-id="cf0c3-126">-Canregistrationname</span><span class="sxs-lookup"><span data-stu-id="cf0c3-126">-ServiceRegistrationName</span></span>
<span data-ttu-id="cf0c3-127">ID de registro do serviço.</span><span class="sxs-lookup"><span data-stu-id="cf0c3-127">Service registration id.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases: ServiceRegistrationId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf0c3-128">-Skip</span><span class="sxs-lookup"><span data-stu-id="cf0c3-128">-Skip</span></span>
<span data-ttu-id="cf0c3-129">Ignorar os primeiros N itens conforme especificado pelo valor do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="cf0c3-129">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="cf0c3-130">-Início</span><span class="sxs-lookup"><span data-stu-id="cf0c3-130">-Top</span></span>
<span data-ttu-id="cf0c3-131">Retorne os N principais itens conforme especificado pelo valor do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="cf0c3-131">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="cf0c3-132">Aplica-se após o parâmetro-Skip.</span><span class="sxs-lookup"><span data-stu-id="cf0c3-132">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="cf0c3-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf0c3-133">CommonParameters</span></span>
<span data-ttu-id="cf0c3-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cf0c3-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf0c3-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cf0c3-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf0c3-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="cf0c3-136">INPUTS</span></span>

## <span data-ttu-id="cf0c3-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="cf0c3-137">OUTPUTS</span></span>

### <span data-ttu-id="cf0c3-138">Microsoft. AzureStack. Management. InfrastructureInsights. admin. Models. ResourceHealth</span><span class="sxs-lookup"><span data-stu-id="cf0c3-138">Microsoft.AzureStack.Management.InfrastructureInsights.Admin.Models.ResourceHealth</span></span>

## <span data-ttu-id="cf0c3-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="cf0c3-139">NOTES</span></span>

## <span data-ttu-id="cf0c3-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cf0c3-140">RELATED LINKS</span></span>

