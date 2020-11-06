---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5c686faa457d83ab0ddffb932b20ab5fcd168ff0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93426128"
---
# <span data-ttu-id="a3b52-101">Get-AzsMacAddressPool</span><span class="sxs-lookup"><span data-stu-id="a3b52-101">Get-AzsMacAddressPool</span></span>

## <span data-ttu-id="a3b52-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a3b52-102">SYNOPSIS</span></span>
<span data-ttu-id="a3b52-103">Retorna uma lista de todos os pools de endereços MAC em um local.</span><span class="sxs-lookup"><span data-stu-id="a3b52-103">Returns a list of all MAC address pools at a location.</span></span>

## <span data-ttu-id="a3b52-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a3b52-104">SYNTAX</span></span>

### <span data-ttu-id="a3b52-105">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="a3b52-105">List (Default)</span></span>
```
Get-AzsMacAddressPool [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="a3b52-106">Obter</span><span class="sxs-lookup"><span data-stu-id="a3b52-106">Get</span></span>
```
Get-AzsMacAddressPool [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="a3b52-107">Identificação</span><span class="sxs-lookup"><span data-stu-id="a3b52-107">ResourceId</span></span>
```
Get-AzsMacAddressPool -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="a3b52-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a3b52-108">DESCRIPTION</span></span>
<span data-ttu-id="a3b52-109">Retorna uma lista de todos os pools de endereços MAC em um local.</span><span class="sxs-lookup"><span data-stu-id="a3b52-109">Returns a list of all MAC address pools at a location.</span></span>

## <span data-ttu-id="a3b52-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a3b52-110">EXAMPLES</span></span>

### <span data-ttu-id="a3b52-111">--------------------------EXEMPLO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="a3b52-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsMacAddressPool
```

<span data-ttu-id="a3b52-112">Obter todos os pools de endereços MAC em um local.</span><span class="sxs-lookup"><span data-stu-id="a3b52-112">Get all MAC address pools at a location.</span></span>

### <span data-ttu-id="a3b52-113">--------------------------EXEMPLO 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="a3b52-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsMacAddressPool -Name "8197fd09-8a69-417e-a55c-10c2c61f5ee7"
```

<span data-ttu-id="a3b52-114">Obtenha um pool de endereços MAC específico em um local com base no nome.</span><span class="sxs-lookup"><span data-stu-id="a3b52-114">Get a specific MAC address pool at a location based on name.</span></span>

## <span data-ttu-id="a3b52-115">OS</span><span class="sxs-lookup"><span data-stu-id="a3b52-115">PARAMETERS</span></span>

### <span data-ttu-id="a3b52-116">-Filtro</span><span class="sxs-lookup"><span data-stu-id="a3b52-116">-Filter</span></span>
<span data-ttu-id="a3b52-117">Parâmetro de filtro OData.</span><span class="sxs-lookup"><span data-stu-id="a3b52-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="a3b52-118">-Local</span><span class="sxs-lookup"><span data-stu-id="a3b52-118">-Location</span></span>
<span data-ttu-id="a3b52-119">Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="a3b52-119">Location of the resource.</span></span>

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

### <span data-ttu-id="a3b52-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="a3b52-120">-Name</span></span>
<span data-ttu-id="a3b52-121">Nome do pool de endereços MAC.</span><span class="sxs-lookup"><span data-stu-id="a3b52-121">Name of the MAC address pool.</span></span>

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

### <span data-ttu-id="a3b52-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3b52-122">-ResourceGroupName</span></span>
<span data-ttu-id="a3b52-123">Grupo de recursos no qual o provedor de recursos foi registrado.</span><span class="sxs-lookup"><span data-stu-id="a3b52-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="a3b52-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a3b52-124">-ResourceId</span></span>
<span data-ttu-id="a3b52-125">A ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="a3b52-125">The resource id.</span></span>

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

### <span data-ttu-id="a3b52-126">-Skip</span><span class="sxs-lookup"><span data-stu-id="a3b52-126">-Skip</span></span>
<span data-ttu-id="a3b52-127">Ignorar os primeiros N itens conforme especificado pelo valor do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="a3b52-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="a3b52-128">-Início</span><span class="sxs-lookup"><span data-stu-id="a3b52-128">-Top</span></span>
<span data-ttu-id="a3b52-129">Retorne os N principais itens conforme especificado pelo valor do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="a3b52-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="a3b52-130">Aplica-se após o parâmetro-Skip.</span><span class="sxs-lookup"><span data-stu-id="a3b52-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="a3b52-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3b52-131">CommonParameters</span></span>
<span data-ttu-id="a3b52-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3b52-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3b52-133">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a3b52-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3b52-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a3b52-134">INPUTS</span></span>

## <span data-ttu-id="a3b52-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a3b52-135">OUTPUTS</span></span>

### <span data-ttu-id="a3b52-136">Microsoft. AzureStack. Management. Fabric. admin. Models. MacAddressPool</span><span class="sxs-lookup"><span data-stu-id="a3b52-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.MacAddressPool</span></span>

## <span data-ttu-id="a3b52-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a3b52-137">NOTES</span></span>

## <span data-ttu-id="a3b52-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a3b52-138">RELATED LINKS</span></span>
