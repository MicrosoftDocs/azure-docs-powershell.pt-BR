---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9c5de84b66283d683d121c99c0cf2e0ea27a4a66
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93774462"
---
# <span data-ttu-id="b52a2-101">Start-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="b52a2-101">Start-AzsScaleUnitNode</span></span>

## <span data-ttu-id="b52a2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b52a2-102">SYNOPSIS</span></span>
<span data-ttu-id="b52a2-103">Ative um nó de unidade de escala.</span><span class="sxs-lookup"><span data-stu-id="b52a2-103">Power on a scale unit node.</span></span>

## <span data-ttu-id="b52a2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b52a2-104">SYNTAX</span></span>

### <span data-ttu-id="b52a2-105">Power-out (padrão)</span><span class="sxs-lookup"><span data-stu-id="b52a2-105">PowerOn (Default)</span></span>
```
Start-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-AsJob] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b52a2-106">Identificação</span><span class="sxs-lookup"><span data-stu-id="b52a2-106">ResourceId</span></span>
```
Start-AzsScaleUnitNode -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b52a2-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b52a2-107">DESCRIPTION</span></span>
<span data-ttu-id="b52a2-108">Ative um nó de unidade de escala.</span><span class="sxs-lookup"><span data-stu-id="b52a2-108">Power on a scale unit node.</span></span>

## <span data-ttu-id="b52a2-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b52a2-109">EXAMPLES</span></span>

### <span data-ttu-id="b52a2-110">--------------------------EXEMPLO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="b52a2-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Start-AzsScaleUnitNode -Name "AzS-ACS01"
```

<span data-ttu-id="b52a2-111">ProvisioningState: êxito</span><span class="sxs-lookup"><span data-stu-id="b52a2-111">ProvisioningState : Succeeded</span></span>

<span data-ttu-id="b52a2-112">Ative um nó de unidade de escala.</span><span class="sxs-lookup"><span data-stu-id="b52a2-112">Power on a scale unit node.</span></span>

## <span data-ttu-id="b52a2-113">OS</span><span class="sxs-lookup"><span data-stu-id="b52a2-113">PARAMETERS</span></span>

### <span data-ttu-id="b52a2-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b52a2-114">-AsJob</span></span>
<span data-ttu-id="b52a2-115">Executar assíncrono como um trabalho e retornar o objeto de trabalho.</span><span class="sxs-lookup"><span data-stu-id="b52a2-115">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="b52a2-116">-Force</span><span class="sxs-lookup"><span data-stu-id="b52a2-116">-Force</span></span>
<span data-ttu-id="b52a2-117">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="b52a2-117">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="b52a2-118">-Local</span><span class="sxs-lookup"><span data-stu-id="b52a2-118">-Location</span></span>
<span data-ttu-id="b52a2-119">Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="b52a2-119">Location of the resource.</span></span>

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

### <span data-ttu-id="b52a2-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="b52a2-120">-Name</span></span>
<span data-ttu-id="b52a2-121">Nome do nó da unidade de escala.</span><span class="sxs-lookup"><span data-stu-id="b52a2-121">Name of the scale unit node.</span></span>

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

### <span data-ttu-id="b52a2-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b52a2-122">-ResourceGroupName</span></span>
<span data-ttu-id="b52a2-123">Grupo de recursos no qual o provedor de recursos foi registrado.</span><span class="sxs-lookup"><span data-stu-id="b52a2-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="b52a2-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b52a2-124">-ResourceId</span></span>
<span data-ttu-id="b52a2-125">ID do recurso do nó de unidade de escala.</span><span class="sxs-lookup"><span data-stu-id="b52a2-125">Scale unit node resource ID.</span></span>

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

### <span data-ttu-id="b52a2-126">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b52a2-126">-Confirm</span></span>
<span data-ttu-id="b52a2-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b52a2-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b52a2-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b52a2-128">-WhatIf</span></span>
<span data-ttu-id="b52a2-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b52a2-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b52a2-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b52a2-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b52a2-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b52a2-131">CommonParameters</span></span>
<span data-ttu-id="b52a2-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b52a2-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b52a2-133">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b52a2-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b52a2-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b52a2-134">INPUTS</span></span>

## <span data-ttu-id="b52a2-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b52a2-135">OUTPUTS</span></span>

## <span data-ttu-id="b52a2-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b52a2-136">NOTES</span></span>

## <span data-ttu-id="b52a2-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b52a2-137">RELATED LINKS</span></span>

