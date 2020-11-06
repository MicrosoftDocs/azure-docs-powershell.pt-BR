---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: fdf0c09e087779e9a08161f2af6f9070f193c31b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93426229"
---
# <span data-ttu-id="d0638-101">Get-AzsLogicalNetwork</span><span class="sxs-lookup"><span data-stu-id="d0638-101">Get-AzsLogicalNetwork</span></span>

## <span data-ttu-id="d0638-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d0638-102">SYNOPSIS</span></span>
<span data-ttu-id="d0638-103">Retorna uma lista de todas as redes lógicas em um local.</span><span class="sxs-lookup"><span data-stu-id="d0638-103">Returns a list of all logical networks at a location.</span></span>

## <span data-ttu-id="d0638-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d0638-104">SYNTAX</span></span>

### <span data-ttu-id="d0638-105">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="d0638-105">List (Default)</span></span>
```
Get-AzsLogicalNetwork [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="d0638-106">Obter</span><span class="sxs-lookup"><span data-stu-id="d0638-106">Get</span></span>
```
Get-AzsLogicalNetwork [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="d0638-107">Identificação</span><span class="sxs-lookup"><span data-stu-id="d0638-107">ResourceId</span></span>
```
Get-AzsLogicalNetwork -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="d0638-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d0638-108">DESCRIPTION</span></span>
<span data-ttu-id="d0638-109">Retorna uma lista de todas as redes lógicas em um local.</span><span class="sxs-lookup"><span data-stu-id="d0638-109">Returns a list of all logical networks at a location.</span></span>

## <span data-ttu-id="d0638-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d0638-110">EXAMPLES</span></span>

### <span data-ttu-id="d0638-111">--------------------------EXEMPLO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="d0638-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsLogicalNetwork
```

<span data-ttu-id="d0638-112">Obter todas as redes lógicas em um local.</span><span class="sxs-lookup"><span data-stu-id="d0638-112">Get all logical networks at a location.</span></span>

### <span data-ttu-id="d0638-113">--------------------------EXEMPLO 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="d0638-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsLogicalNetwork -Name "bb6c6f28-bad9-441b-8e62-57d2be255904"
```

<span data-ttu-id="d0638-114">Obter redes lógicas específicas em um local com base em um nome.</span><span class="sxs-lookup"><span data-stu-id="d0638-114">Get a specific logical networks at a location based on a name.</span></span>

## <span data-ttu-id="d0638-115">OS</span><span class="sxs-lookup"><span data-stu-id="d0638-115">PARAMETERS</span></span>

### <span data-ttu-id="d0638-116">-Filtro</span><span class="sxs-lookup"><span data-stu-id="d0638-116">-Filter</span></span>
<span data-ttu-id="d0638-117">Parâmetro de filtro OData.</span><span class="sxs-lookup"><span data-stu-id="d0638-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="d0638-118">-Local</span><span class="sxs-lookup"><span data-stu-id="d0638-118">-Location</span></span>
<span data-ttu-id="d0638-119">Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="d0638-119">Location of the resource.</span></span>

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

### <span data-ttu-id="d0638-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="d0638-120">-Name</span></span>
<span data-ttu-id="d0638-121">Nome da rede lógica.</span><span class="sxs-lookup"><span data-stu-id="d0638-121">Name of the logical network.</span></span>

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

### <span data-ttu-id="d0638-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d0638-122">-ResourceGroupName</span></span>
<span data-ttu-id="d0638-123">Grupo de recursos no qual o provedor de recursos foi registrado.</span><span class="sxs-lookup"><span data-stu-id="d0638-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="d0638-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d0638-124">-ResourceId</span></span>
<span data-ttu-id="d0638-125">A ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="d0638-125">The resource id.</span></span>

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

### <span data-ttu-id="d0638-126">-Skip</span><span class="sxs-lookup"><span data-stu-id="d0638-126">-Skip</span></span>
<span data-ttu-id="d0638-127">Ignorar os primeiros N itens conforme especificado pelo valor do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="d0638-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="d0638-128">-Início</span><span class="sxs-lookup"><span data-stu-id="d0638-128">-Top</span></span>
<span data-ttu-id="d0638-129">Retorne os N principais itens conforme especificado pelo valor do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="d0638-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="d0638-130">Aplica-se após o parâmetro-Skip.</span><span class="sxs-lookup"><span data-stu-id="d0638-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="d0638-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0638-131">CommonParameters</span></span>
<span data-ttu-id="d0638-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0638-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0638-133">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d0638-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0638-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d0638-134">INPUTS</span></span>

## <span data-ttu-id="d0638-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d0638-135">OUTPUTS</span></span>

### <span data-ttu-id="d0638-136">Microsoft. AzureStack. Management. Fabric. admin. Models. LogicalNetwork</span><span class="sxs-lookup"><span data-stu-id="d0638-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.LogicalNetwork</span></span>

## <span data-ttu-id="d0638-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d0638-137">NOTES</span></span>

## <span data-ttu-id="d0638-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d0638-138">RELATED LINKS</span></span>

