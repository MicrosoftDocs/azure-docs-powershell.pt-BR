---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: ced1207f07360c0a18674d6f8ae4170be9b87beb
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2020
ms.locfileid: "93774653"
---
# <span data-ttu-id="81cfc-101">Add-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="81cfc-101">Add-AzsScaleUnitNode</span></span>

## <span data-ttu-id="81cfc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="81cfc-102">SYNOPSIS</span></span>
<span data-ttu-id="81cfc-103">Adicionar uma nova unidade de escala.</span><span class="sxs-lookup"><span data-stu-id="81cfc-103">Add a new scale unit.</span></span>

## <span data-ttu-id="81cfc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="81cfc-104">SYNTAX</span></span>

### <span data-ttu-id="81cfc-105">Dimensionamento (padrão)</span><span class="sxs-lookup"><span data-stu-id="81cfc-105">ScaleOut (Default)</span></span>
```
Add-AzsScaleUnitNode -Name <String> -NodeList <ScaleOutScaleUnitParameters[]> [-AwaitStorageConvergence]
 [-Location <String>] [-ResourceGroupName <String>] [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="81cfc-106">Identificação</span><span class="sxs-lookup"><span data-stu-id="81cfc-106">ResourceId</span></span>
```
Add-AzsScaleUnitNode -NodeList <ScaleOutScaleUnitParameters[]> [-AwaitStorageConvergence] -ResourceId <String>
 [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="81cfc-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="81cfc-107">DESCRIPTION</span></span>
<span data-ttu-id="81cfc-108">Adicionar uma nova unidade de escala.</span><span class="sxs-lookup"><span data-stu-id="81cfc-108">Add a new scale unit.</span></span>

## <span data-ttu-id="81cfc-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="81cfc-109">EXAMPLES</span></span>

### <span data-ttu-id="81cfc-110">--------------------------EXEMPLO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="81cfc-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Add-AzsScaleUnitNode -ScaleUnitName "Azs-ERC03" -NodeList $nodeList
```

<span data-ttu-id="81cfc-111">Adicionar um novo nó de unidade de escala.</span><span class="sxs-lookup"><span data-stu-id="81cfc-111">Add a new scale unit node.</span></span>

## <span data-ttu-id="81cfc-112">OS</span><span class="sxs-lookup"><span data-stu-id="81cfc-112">PARAMETERS</span></span>

### <span data-ttu-id="81cfc-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="81cfc-113">-AsJob</span></span>
<span data-ttu-id="81cfc-114">Executar assíncrono como um trabalho e retornar o objeto de trabalho.</span><span class="sxs-lookup"><span data-stu-id="81cfc-114">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="81cfc-115">-AwaitStorageConvergence</span><span class="sxs-lookup"><span data-stu-id="81cfc-115">-AwaitStorageConvergence</span></span>
<span data-ttu-id="81cfc-116">Sinalizador indica se a operação deve aguardar que o armazenamento convergesse antes de retornar.</span><span class="sxs-lookup"><span data-stu-id="81cfc-116">Flag indicates if the operation should wait for storage to converge before returning.</span></span>

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

### <span data-ttu-id="81cfc-117">-Force</span><span class="sxs-lookup"><span data-stu-id="81cfc-117">-Force</span></span>
<span data-ttu-id="81cfc-118">Não pedir confirmação</span><span class="sxs-lookup"><span data-stu-id="81cfc-118">Don't ask for confirmation</span></span>

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

### <span data-ttu-id="81cfc-119">-Local</span><span class="sxs-lookup"><span data-stu-id="81cfc-119">-Location</span></span>
<span data-ttu-id="81cfc-120">Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="81cfc-120">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: ScaleOut
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81cfc-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="81cfc-121">-Name</span></span>
<span data-ttu-id="81cfc-122">{{Descrição do nome do preenchimento}}</span><span class="sxs-lookup"><span data-stu-id="81cfc-122">{{Fill Name Description}}</span></span>

```yaml
Type: String
Parameter Sets: ScaleOut
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81cfc-123">-NodeList</span><span class="sxs-lookup"><span data-stu-id="81cfc-123">-NodeList</span></span>
<span data-ttu-id="81cfc-124">Lista de nós na unidade de escala.</span><span class="sxs-lookup"><span data-stu-id="81cfc-124">List of nodes in the scale unit.</span></span>

```yaml
Type: ScaleOutScaleUnitParameters[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81cfc-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81cfc-125">-ResourceGroupName</span></span>
<span data-ttu-id="81cfc-126">Grupo de recursos no qual o provedor de recursos foi registrado.</span><span class="sxs-lookup"><span data-stu-id="81cfc-126">Resource group in which the resource provider has been registered.</span></span>

```yaml
Type: String
Parameter Sets: ScaleOut
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81cfc-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="81cfc-127">-ResourceId</span></span>
<span data-ttu-id="81cfc-128">ID do recurso do nó de unidade de escala.</span><span class="sxs-lookup"><span data-stu-id="81cfc-128">Scale unit node resource ID.</span></span>

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

### <span data-ttu-id="81cfc-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="81cfc-129">-Confirm</span></span>
<span data-ttu-id="81cfc-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="81cfc-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81cfc-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="81cfc-131">-WhatIf</span></span>
<span data-ttu-id="81cfc-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="81cfc-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="81cfc-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="81cfc-133">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81cfc-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81cfc-134">CommonParameters</span></span>
<span data-ttu-id="81cfc-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81cfc-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81cfc-136">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="81cfc-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81cfc-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="81cfc-137">INPUTS</span></span>

## <span data-ttu-id="81cfc-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="81cfc-138">OUTPUTS</span></span>

## <span data-ttu-id="81cfc-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="81cfc-139">NOTES</span></span>

## <span data-ttu-id="81cfc-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="81cfc-140">RELATED LINKS</span></span>

