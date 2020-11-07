---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: c5fe6e28ff87cfd3f365441d0e09f09ef21dc454
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/08/2020
ms.locfileid: "93947097"
---
# <span data-ttu-id="e3f2b-101">Get-AzsInfrastructureRoleInstance</span><span class="sxs-lookup"><span data-stu-id="e3f2b-101">Get-AzsInfrastructureRoleInstance</span></span>

## <span data-ttu-id="e3f2b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e3f2b-102">SYNOPSIS</span></span>
<span data-ttu-id="e3f2b-103">Retorna uma lista de todas as instâncias de função de infraestrutura em um local.</span><span class="sxs-lookup"><span data-stu-id="e3f2b-103">Returns a list of all infrastructure role instances at a location.</span></span>

## <span data-ttu-id="e3f2b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e3f2b-104">SYNTAX</span></span>

### <span data-ttu-id="e3f2b-105">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="e3f2b-105">List (Default)</span></span>
```
Get-AzsInfrastructureRoleInstance [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>]
 [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="e3f2b-106">Obter</span><span class="sxs-lookup"><span data-stu-id="e3f2b-106">Get</span></span>
```
Get-AzsInfrastructureRoleInstance [-Name] <String> [-Location <String>] [-ResourceGroupName <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="e3f2b-107">Identificação</span><span class="sxs-lookup"><span data-stu-id="e3f2b-107">ResourceId</span></span>
```
Get-AzsInfrastructureRoleInstance -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="e3f2b-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e3f2b-108">DESCRIPTION</span></span>
<span data-ttu-id="e3f2b-109">Retorna uma lista de todas as instâncias de função de infraestrutura em um local.</span><span class="sxs-lookup"><span data-stu-id="e3f2b-109">Returns a list of all infrastructure role instances at a location.</span></span>

## <span data-ttu-id="e3f2b-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e3f2b-110">EXAMPLES</span></span>

### <span data-ttu-id="e3f2b-111">EXEMPLO 1</span><span class="sxs-lookup"><span data-stu-id="e3f2b-111">EXAMPLE 1</span></span>
```
Get-AzsInfrastructureRoleInstance
```

<span data-ttu-id="e3f2b-112">Retorne uma lista de todas as instâncias de função de infraestrutura.</span><span class="sxs-lookup"><span data-stu-id="e3f2b-112">Return a list of all infrastructure role instances.</span></span>

### <span data-ttu-id="e3f2b-113">EXEMPLO 2</span><span class="sxs-lookup"><span data-stu-id="e3f2b-113">EXAMPLE 2</span></span>
```
Get-AzsInfrastructureRoleInstance -Name "AzS-ACS01"
```

<span data-ttu-id="e3f2b-114">Retornar uma única instância de função de infraestrutura com base no nome.</span><span class="sxs-lookup"><span data-stu-id="e3f2b-114">Return a single infrastructure role instance based on name.</span></span>

## <span data-ttu-id="e3f2b-115">OS</span><span class="sxs-lookup"><span data-stu-id="e3f2b-115">PARAMETERS</span></span>

### <span data-ttu-id="e3f2b-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="e3f2b-116">-Name</span></span>
<span data-ttu-id="e3f2b-117">Nome de uma instância de função de infraestrutura.</span><span class="sxs-lookup"><span data-stu-id="e3f2b-117">Name of an infrastructure role instance.</span></span>

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

### <span data-ttu-id="e3f2b-118">-Local</span><span class="sxs-lookup"><span data-stu-id="e3f2b-118">-Location</span></span>
<span data-ttu-id="e3f2b-119">Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="e3f2b-119">Location of the resource.</span></span>

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

### <span data-ttu-id="e3f2b-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3f2b-120">-ResourceGroupName</span></span>
<span data-ttu-id="e3f2b-121">Grupo de recursos no qual o provedor de recursos foi registrado.</span><span class="sxs-lookup"><span data-stu-id="e3f2b-121">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="e3f2b-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e3f2b-122">-ResourceId</span></span>
<span data-ttu-id="e3f2b-123">A ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="e3f2b-123">The resource id.</span></span>

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

### <span data-ttu-id="e3f2b-124">-Filtro</span><span class="sxs-lookup"><span data-stu-id="e3f2b-124">-Filter</span></span>
<span data-ttu-id="e3f2b-125">Parâmetro de filtro OData.</span><span class="sxs-lookup"><span data-stu-id="e3f2b-125">OData filter parameter.</span></span>

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

### <span data-ttu-id="e3f2b-126">-Skip</span><span class="sxs-lookup"><span data-stu-id="e3f2b-126">-Skip</span></span>
<span data-ttu-id="e3f2b-127">Ignorar os primeiros N itens conforme especificado pelo valor do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="e3f2b-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="e3f2b-128">-Início</span><span class="sxs-lookup"><span data-stu-id="e3f2b-128">-Top</span></span>
<span data-ttu-id="e3f2b-129">Retorne os N principais itens conforme especificado pelo valor do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="e3f2b-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="e3f2b-130">Aplica-se após o parâmetro-Skip.</span><span class="sxs-lookup"><span data-stu-id="e3f2b-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="e3f2b-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3f2b-131">CommonParameters</span></span>
<span data-ttu-id="e3f2b-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3f2b-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3f2b-133">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3f2b-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3f2b-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e3f2b-134">INPUTS</span></span>

## <span data-ttu-id="e3f2b-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e3f2b-135">OUTPUTS</span></span>

### <span data-ttu-id="e3f2b-136">Microsoft. AzureStack. Management. Fabric. admin. Models. InfraRoleInstance</span><span class="sxs-lookup"><span data-stu-id="e3f2b-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.InfraRoleInstance</span></span>

## <span data-ttu-id="e3f2b-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e3f2b-137">NOTES</span></span>

## <span data-ttu-id="e3f2b-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e3f2b-138">RELATED LINKS</span></span>
