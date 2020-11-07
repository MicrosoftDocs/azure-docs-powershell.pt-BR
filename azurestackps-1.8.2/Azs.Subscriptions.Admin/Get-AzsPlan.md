---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 02baf67cc13269d9d53c0adb40337adbd9929641
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/08/2020
ms.locfileid: "93946748"
---
# <span data-ttu-id="6940a-101">Get-AzsPlan</span><span class="sxs-lookup"><span data-stu-id="6940a-101">Get-AzsPlan</span></span>

## <span data-ttu-id="6940a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6940a-102">SYNOPSIS</span></span>
<span data-ttu-id="6940a-103">Listar todos os planos em todas as assinaturas.</span><span class="sxs-lookup"><span data-stu-id="6940a-103">List all plans across all subscriptions.</span></span>

## <span data-ttu-id="6940a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6940a-104">SYNTAX</span></span>

### <span data-ttu-id="6940a-105">ListAll (padrão)</span><span class="sxs-lookup"><span data-stu-id="6940a-105">ListAll (Default)</span></span>
```
Get-AzsPlan [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="6940a-106">Obter</span><span class="sxs-lookup"><span data-stu-id="6940a-106">Get</span></span>
```
Get-AzsPlan -Name <String> -ResourceGroupName <String> [<CommonParameters>]
```

### <span data-ttu-id="6940a-107">Programação</span><span class="sxs-lookup"><span data-stu-id="6940a-107">List</span></span>
```
Get-AzsPlan -ResourceGroupName <String> [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="6940a-108">Identificação</span><span class="sxs-lookup"><span data-stu-id="6940a-108">ResourceId</span></span>
```
Get-AzsPlan -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="6940a-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6940a-109">DESCRIPTION</span></span>
<span data-ttu-id="6940a-110">Listar todos os planos em todas as assinaturas.</span><span class="sxs-lookup"><span data-stu-id="6940a-110">List all plans across all subscriptions.</span></span>

## <span data-ttu-id="6940a-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6940a-111">EXAMPLES</span></span>

### <span data-ttu-id="6940a-112">--------------------------EXEMPLO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="6940a-112">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsPlan -ResourceGroupName rg1 -Name plan1
```

<span data-ttu-id="6940a-113">Obtenha um plano do specifc sob estas assinaturas.</span><span class="sxs-lookup"><span data-stu-id="6940a-113">Get a specifc plan under this subscriptions.</span></span>

## <span data-ttu-id="6940a-114">OS</span><span class="sxs-lookup"><span data-stu-id="6940a-114">PARAMETERS</span></span>

### <span data-ttu-id="6940a-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="6940a-115">-Name</span></span>
<span data-ttu-id="6940a-116">Nome do plano.</span><span class="sxs-lookup"><span data-stu-id="6940a-116">Name of the plan.</span></span>

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

### <span data-ttu-id="6940a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6940a-117">-ResourceGroupName</span></span>
<span data-ttu-id="6940a-118">O nome do grupo de recursos no qual o recurso está localizado.</span><span class="sxs-lookup"><span data-stu-id="6940a-118">The name of the resource group the resource is located under.</span></span>

```yaml
Type: String
Parameter Sets: Get, List
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6940a-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6940a-119">-ResourceId</span></span>
<span data-ttu-id="6940a-120">A ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="6940a-120">The resource id.</span></span>

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

### <span data-ttu-id="6940a-121">-Skip</span><span class="sxs-lookup"><span data-stu-id="6940a-121">-Skip</span></span>
<span data-ttu-id="6940a-122">Ignorar os primeiros N itens conforme especificado pelo valor do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="6940a-122">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: ListAll, List
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6940a-123">-Início</span><span class="sxs-lookup"><span data-stu-id="6940a-123">-Top</span></span>
<span data-ttu-id="6940a-124">Retorne os N principais itens conforme especificado pelo valor do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="6940a-124">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="6940a-125">Aplica-se após o parâmetro-Skip.</span><span class="sxs-lookup"><span data-stu-id="6940a-125">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: ListAll, List
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6940a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6940a-126">CommonParameters</span></span>
<span data-ttu-id="6940a-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6940a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6940a-128">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6940a-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6940a-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6940a-129">INPUTS</span></span>

## <span data-ttu-id="6940a-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6940a-130">OUTPUTS</span></span>

### <span data-ttu-id="6940a-131">Microsoft. AzureStack. Management. subscriptions. admin. Models. Plan</span><span class="sxs-lookup"><span data-stu-id="6940a-131">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Plan</span></span>

## <span data-ttu-id="6940a-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6940a-132">NOTES</span></span>

## <span data-ttu-id="6940a-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6940a-133">RELATED LINKS</span></span>

