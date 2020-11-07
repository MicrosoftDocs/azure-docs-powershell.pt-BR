---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 09391f521a2b75663b25731c6cc20ef78a658d5f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93774543"
---
# <span data-ttu-id="76adc-101">Add-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="76adc-101">Add-AzsScaleUnitNode</span></span>

## <span data-ttu-id="76adc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="76adc-102">SYNOPSIS</span></span>
<span data-ttu-id="76adc-103">Expandir uma unidade de escala.</span><span class="sxs-lookup"><span data-stu-id="76adc-103">Scale out a scale unit.</span></span>

## <span data-ttu-id="76adc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="76adc-104">SYNTAX</span></span>

```
Add-AzsScaleUnitNode [-NodeList] <ScaleOutScaleUnitParameters[]> [[-ResourceGroupName] <String>]
 [-ScaleUnit] <String> [[-Location] <String>] [-AwaitStorageConvergence] [-AsJob] [<CommonParameters>]
```

## <span data-ttu-id="76adc-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="76adc-105">DESCRIPTION</span></span>
<span data-ttu-id="76adc-106">Adicione um novo nó de unidade de escala ao seu cluster de unidade de escala.</span><span class="sxs-lookup"><span data-stu-id="76adc-106">Add a new scale unit node to your scale unit cluster.</span></span>

## <span data-ttu-id="76adc-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="76adc-107">EXAMPLES</span></span>

### <span data-ttu-id="76adc-108">--------------------------EXEMPLO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="76adc-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Add-AzsScaleUnitNode -NodeList $Nodes -ScaleUnit $ScaleUnitName
```

<span data-ttu-id="76adc-109">Adiciona uma lista de nós à unidade de escala.</span><span class="sxs-lookup"><span data-stu-id="76adc-109">Adds a list of nodes to the scale unit.</span></span>

## <span data-ttu-id="76adc-110">OS</span><span class="sxs-lookup"><span data-stu-id="76adc-110">PARAMETERS</span></span>

### <span data-ttu-id="76adc-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="76adc-111">-AsJob</span></span>
<span data-ttu-id="76adc-112">Executar assíncrono como um trabalho e retornar o objeto de trabalho.</span><span class="sxs-lookup"><span data-stu-id="76adc-112">Run asynchronous as a job and return the job object.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76adc-113">-AwaitStorageConvergence</span><span class="sxs-lookup"><span data-stu-id="76adc-113">-AwaitStorageConvergence</span></span>
<span data-ttu-id="76adc-114">Aguarde até que a replicação de armazenamento seja concluída antes de retornar o sucesso.</span><span class="sxs-lookup"><span data-stu-id="76adc-114">Wait for storage replication to complete before returning success.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76adc-115">-Local</span><span class="sxs-lookup"><span data-stu-id="76adc-115">-Location</span></span>
<span data-ttu-id="76adc-116">Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="76adc-116">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76adc-117">-NodeList</span><span class="sxs-lookup"><span data-stu-id="76adc-117">-NodeList</span></span>
<span data-ttu-id="76adc-118">Uma lista de dados de entrada que permite adicionar um conjunto de nós de unidade de escala.</span><span class="sxs-lookup"><span data-stu-id="76adc-118">A list of input data that allows for adding a set of scale unit nodes.</span></span>

```yaml
Type: ScaleOutScaleUnitParameters[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76adc-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76adc-119">-ResourceGroupName</span></span>
<span data-ttu-id="76adc-120">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="76adc-120">Name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76adc-121">-ScaleUnit</span><span class="sxs-lookup"><span data-stu-id="76adc-121">-ScaleUnit</span></span>
<span data-ttu-id="76adc-122">Nome das unidades de escala.</span><span class="sxs-lookup"><span data-stu-id="76adc-122">Name of the scale units.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76adc-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76adc-123">CommonParameters</span></span>
<span data-ttu-id="76adc-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76adc-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76adc-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="76adc-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76adc-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="76adc-126">INPUTS</span></span>

## <span data-ttu-id="76adc-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="76adc-127">OUTPUTS</span></span>

## <span data-ttu-id="76adc-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="76adc-128">NOTES</span></span>

## <span data-ttu-id="76adc-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="76adc-129">RELATED LINKS</span></span>
