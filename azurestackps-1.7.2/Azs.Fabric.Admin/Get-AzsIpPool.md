---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2528d9b4f9443d8857006b6fc1e94100b0b477ec
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93774478"
---
# <span data-ttu-id="b8cec-101">Get-AzsIpPool</span><span class="sxs-lookup"><span data-stu-id="b8cec-101">Get-AzsIpPool</span></span>

## <span data-ttu-id="b8cec-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b8cec-102">SYNOPSIS</span></span>
<span data-ttu-id="b8cec-103">Retorna uma lista de todos os pools de IP em um determinado local.</span><span class="sxs-lookup"><span data-stu-id="b8cec-103">Returns a list of all IP pools at a certain location.</span></span>

## <span data-ttu-id="b8cec-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b8cec-104">SYNTAX</span></span>

### <span data-ttu-id="b8cec-105">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="b8cec-105">List (Default)</span></span>
```
Get-AzsIpPool [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="b8cec-106">Obter</span><span class="sxs-lookup"><span data-stu-id="b8cec-106">Get</span></span>
```
Get-AzsIpPool [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="b8cec-107">Identificação</span><span class="sxs-lookup"><span data-stu-id="b8cec-107">ResourceId</span></span>
```
Get-AzsIpPool -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="b8cec-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b8cec-108">DESCRIPTION</span></span>
<span data-ttu-id="b8cec-109">Retorna uma lista de todos os pools de IP em um determinado local.</span><span class="sxs-lookup"><span data-stu-id="b8cec-109">Returns a list of all IP pools at a certain location.</span></span>

## <span data-ttu-id="b8cec-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b8cec-110">EXAMPLES</span></span>

### <span data-ttu-id="b8cec-111">--------------------------EXEMPLO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="b8cec-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsIpPool
```

<span data-ttu-id="b8cec-112">Obtenha todos os pools de IP da infra-estrutura.</span><span class="sxs-lookup"><span data-stu-id="b8cec-112">Get an all infrastructure ip pools.</span></span>

### <span data-ttu-id="b8cec-113">--------------------------EXEMPLO 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="b8cec-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsIpPool -Name "08786a0f-ad8c-43aa-a154-06083abfc1ac"
```

<span data-ttu-id="b8cec-114">Obter um pool de IP de infraestrutura com base no nome.</span><span class="sxs-lookup"><span data-stu-id="b8cec-114">Get an infrastructure ip pool based on name.</span></span>

## <span data-ttu-id="b8cec-115">OS</span><span class="sxs-lookup"><span data-stu-id="b8cec-115">PARAMETERS</span></span>

### <span data-ttu-id="b8cec-116">-Filtro</span><span class="sxs-lookup"><span data-stu-id="b8cec-116">-Filter</span></span>
<span data-ttu-id="b8cec-117">Parâmetro de filtro OData.</span><span class="sxs-lookup"><span data-stu-id="b8cec-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="b8cec-118">-Local</span><span class="sxs-lookup"><span data-stu-id="b8cec-118">-Location</span></span>
<span data-ttu-id="b8cec-119">Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="b8cec-119">Location of the resource.</span></span>

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

### <span data-ttu-id="b8cec-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="b8cec-120">-Name</span></span>
<span data-ttu-id="b8cec-121">Nome do pool de IP.</span><span class="sxs-lookup"><span data-stu-id="b8cec-121">IP pool name.</span></span>

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

### <span data-ttu-id="b8cec-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8cec-122">-ResourceGroupName</span></span>
<span data-ttu-id="b8cec-123">Grupo de recursos no qual o provedor de recursos foi registrado.</span><span class="sxs-lookup"><span data-stu-id="b8cec-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="b8cec-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b8cec-124">-ResourceId</span></span>
<span data-ttu-id="b8cec-125">A ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="b8cec-125">The resource id.</span></span>

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

### <span data-ttu-id="b8cec-126">-Skip</span><span class="sxs-lookup"><span data-stu-id="b8cec-126">-Skip</span></span>
<span data-ttu-id="b8cec-127">Ignorar os primeiros N itens conforme especificado pelo valor do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="b8cec-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="b8cec-128">-Início</span><span class="sxs-lookup"><span data-stu-id="b8cec-128">-Top</span></span>
<span data-ttu-id="b8cec-129">Retorne os N principais itens conforme especificado pelo valor do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="b8cec-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="b8cec-130">Aplica-se após o parâmetro-Skip.</span><span class="sxs-lookup"><span data-stu-id="b8cec-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="b8cec-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8cec-131">CommonParameters</span></span>
<span data-ttu-id="b8cec-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b8cec-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8cec-133">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b8cec-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8cec-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b8cec-134">INPUTS</span></span>

## <span data-ttu-id="b8cec-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b8cec-135">OUTPUTS</span></span>

### <span data-ttu-id="b8cec-136">Microsoft. AzureStack. Management. Fabric. admin. Models. IpPool</span><span class="sxs-lookup"><span data-stu-id="b8cec-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.IpPool</span></span>

## <span data-ttu-id="b8cec-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b8cec-137">NOTES</span></span>

## <span data-ttu-id="b8cec-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b8cec-138">RELATED LINKS</span></span>
