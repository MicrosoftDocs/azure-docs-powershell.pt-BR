---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4c51249856d9cd8c8fc47d4968b1bc011040610e
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/08/2020
ms.locfileid: "93946839"
---
# <span data-ttu-id="ea720-101">Start-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="ea720-101">Start-AzsScaleUnitNode</span></span>

## <span data-ttu-id="ea720-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ea720-102">SYNOPSIS</span></span>
<span data-ttu-id="ea720-103">Ative um nó de unidade de escala.</span><span class="sxs-lookup"><span data-stu-id="ea720-103">Power on a scale unit node.</span></span>

## <span data-ttu-id="ea720-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ea720-104">SYNTAX</span></span>

### <span data-ttu-id="ea720-105">Power-out (padrão)</span><span class="sxs-lookup"><span data-stu-id="ea720-105">PowerOn (Default)</span></span>
```
Start-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-AsJob] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea720-106">Identificação</span><span class="sxs-lookup"><span data-stu-id="ea720-106">ResourceId</span></span>
```
Start-AzsScaleUnitNode -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ea720-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ea720-107">DESCRIPTION</span></span>
<span data-ttu-id="ea720-108">Ative um nó de unidade de escala.</span><span class="sxs-lookup"><span data-stu-id="ea720-108">Power on a scale unit node.</span></span>

## <span data-ttu-id="ea720-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ea720-109">EXAMPLES</span></span>

### <span data-ttu-id="ea720-110">EXEMPLO 1</span><span class="sxs-lookup"><span data-stu-id="ea720-110">EXAMPLE 1</span></span>
```
Start-AzsScaleUnitNode -Name "AzS-ACS01"
```

<span data-ttu-id="ea720-111">ProvisioningState: êxito</span><span class="sxs-lookup"><span data-stu-id="ea720-111">ProvisioningState : Succeeded</span></span>

<span data-ttu-id="ea720-112">Ative um nó de unidade de escala.</span><span class="sxs-lookup"><span data-stu-id="ea720-112">Power on a scale unit node.</span></span>

## <span data-ttu-id="ea720-113">OS</span><span class="sxs-lookup"><span data-stu-id="ea720-113">PARAMETERS</span></span>

### <span data-ttu-id="ea720-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="ea720-114">-Name</span></span>
<span data-ttu-id="ea720-115">Nome do nó da unidade de escala.</span><span class="sxs-lookup"><span data-stu-id="ea720-115">Name of the scale unit node.</span></span>

```yaml
Type: String
Parameter Sets: PowerOn
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea720-116">-Local</span><span class="sxs-lookup"><span data-stu-id="ea720-116">-Location</span></span>
<span data-ttu-id="ea720-117">Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="ea720-117">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: PowerOn
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea720-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea720-118">-ResourceGroupName</span></span>
<span data-ttu-id="ea720-119">Grupo de recursos no qual o provedor de recursos foi registrado.</span><span class="sxs-lookup"><span data-stu-id="ea720-119">Resource group in which the resource provider has been registered.</span></span>

```yaml
Type: String
Parameter Sets: PowerOn
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea720-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ea720-120">-ResourceId</span></span>
<span data-ttu-id="ea720-121">ID do recurso do nó de unidade de escala.</span><span class="sxs-lookup"><span data-stu-id="ea720-121">Scale unit node resource ID.</span></span>

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

### <span data-ttu-id="ea720-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ea720-122">-AsJob</span></span>
<span data-ttu-id="ea720-123">Executar assíncrono como um trabalho e retornar o objeto de trabalho.</span><span class="sxs-lookup"><span data-stu-id="ea720-123">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="ea720-124">-Force</span><span class="sxs-lookup"><span data-stu-id="ea720-124">-Force</span></span>
<span data-ttu-id="ea720-125">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="ea720-125">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="ea720-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea720-126">-WhatIf</span></span>
<span data-ttu-id="ea720-127">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ea720-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ea720-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ea720-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ea720-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="ea720-129">-Confirm</span></span>
<span data-ttu-id="ea720-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ea720-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ea720-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea720-131">CommonParameters</span></span>
<span data-ttu-id="ea720-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea720-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea720-133">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea720-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea720-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ea720-134">INPUTS</span></span>

## <span data-ttu-id="ea720-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ea720-135">OUTPUTS</span></span>

## <span data-ttu-id="ea720-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ea720-136">NOTES</span></span>

## <span data-ttu-id="ea720-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ea720-137">RELATED LINKS</span></span>
