---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 42d6233a99979687b7031ab58a620319fa675a28
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93601694"
---
# <span data-ttu-id="eb06e-101">Get-AzsSlbMuxInstance</span><span class="sxs-lookup"><span data-stu-id="eb06e-101">Get-AzsSlbMuxInstance</span></span>

## <span data-ttu-id="eb06e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="eb06e-102">SYNOPSIS</span></span>
<span data-ttu-id="eb06e-103">Retorna uma lista de todas as instâncias de balanceador de carga de software em um local.</span><span class="sxs-lookup"><span data-stu-id="eb06e-103">Returns a list of all software load balancer instances at a location.</span></span>

## <span data-ttu-id="eb06e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="eb06e-104">SYNTAX</span></span>

### <span data-ttu-id="eb06e-105">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="eb06e-105">List (Default)</span></span>
```
Get-AzsSlbMuxInstance [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="eb06e-106">Obter</span><span class="sxs-lookup"><span data-stu-id="eb06e-106">Get</span></span>
```
Get-AzsSlbMuxInstance [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="eb06e-107">Identificação</span><span class="sxs-lookup"><span data-stu-id="eb06e-107">ResourceId</span></span>
```
Get-AzsSlbMuxInstance -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="eb06e-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="eb06e-108">DESCRIPTION</span></span>
<span data-ttu-id="eb06e-109">Retorna uma lista de todas as instâncias de balanceador de carga de software em um local.</span><span class="sxs-lookup"><span data-stu-id="eb06e-109">Returns a list of all software load balancer instances at a location.</span></span>

## <span data-ttu-id="eb06e-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="eb06e-110">EXAMPLES</span></span>

### <span data-ttu-id="eb06e-111">--------------------------EXEMPLO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="eb06e-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsSlbMuxInstance
```

<span data-ttu-id="eb06e-112">Obtenha todas as instâncias do Multiplexador de balanceamento de carga de software em um local.</span><span class="sxs-lookup"><span data-stu-id="eb06e-112">Get all software load balancer multiplexer instance at a location.</span></span>

### <span data-ttu-id="eb06e-113">--------------------------EXEMPLO 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="eb06e-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsSlbMuxInstance -Name "AzS-SLB01"
```

<span data-ttu-id="eb06e-114">Obtenha uma instância específica do Multiplexador de balanceamento de carga de software em um local em que o nome foi atribuído.</span><span class="sxs-lookup"><span data-stu-id="eb06e-114">Get a specific software load balancer multiplexer instance at a location given a name.</span></span>

## <span data-ttu-id="eb06e-115">OS</span><span class="sxs-lookup"><span data-stu-id="eb06e-115">PARAMETERS</span></span>

### <span data-ttu-id="eb06e-116">-Filtro</span><span class="sxs-lookup"><span data-stu-id="eb06e-116">-Filter</span></span>
<span data-ttu-id="eb06e-117">Parâmetro de filtro OData.</span><span class="sxs-lookup"><span data-stu-id="eb06e-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="eb06e-118">-Local</span><span class="sxs-lookup"><span data-stu-id="eb06e-118">-Location</span></span>
<span data-ttu-id="eb06e-119">Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="eb06e-119">Location of the resource.</span></span>

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

### <span data-ttu-id="eb06e-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="eb06e-120">-Name</span></span>
<span data-ttu-id="eb06e-121">Nome de uma instância de MUX SLB.</span><span class="sxs-lookup"><span data-stu-id="eb06e-121">Name of a SLB MUX instance.</span></span>

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

### <span data-ttu-id="eb06e-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb06e-122">-ResourceGroupName</span></span>
<span data-ttu-id="eb06e-123">Grupo de recursos no qual o provedor de recursos foi registrado.</span><span class="sxs-lookup"><span data-stu-id="eb06e-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="eb06e-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="eb06e-124">-ResourceId</span></span>
<span data-ttu-id="eb06e-125">A ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="eb06e-125">The resource id.</span></span>

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

### <span data-ttu-id="eb06e-126">-Skip</span><span class="sxs-lookup"><span data-stu-id="eb06e-126">-Skip</span></span>
<span data-ttu-id="eb06e-127">Ignorar os primeiros N itens conforme especificado pelo valor do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="eb06e-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="eb06e-128">-Início</span><span class="sxs-lookup"><span data-stu-id="eb06e-128">-Top</span></span>
<span data-ttu-id="eb06e-129">Retorne os N principais itens conforme especificado pelo valor do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="eb06e-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="eb06e-130">Aplica-se após o parâmetro-Skip.</span><span class="sxs-lookup"><span data-stu-id="eb06e-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="eb06e-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb06e-131">CommonParameters</span></span>
<span data-ttu-id="eb06e-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eb06e-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb06e-133">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eb06e-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb06e-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="eb06e-134">INPUTS</span></span>

## <span data-ttu-id="eb06e-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="eb06e-135">OUTPUTS</span></span>

### <span data-ttu-id="eb06e-136">Microsoft. AzureStack. Management. Fabric. admin. Models. SlbMuxInstance</span><span class="sxs-lookup"><span data-stu-id="eb06e-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.SlbMuxInstance</span></span>

## <span data-ttu-id="eb06e-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="eb06e-137">NOTES</span></span>

## <span data-ttu-id="eb06e-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="eb06e-138">RELATED LINKS</span></span>

