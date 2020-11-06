---
external help file: Azs.InfrastructureInsights.Admin-help.xml
Module Name: Azs.InfrastructureInsights.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7b06ae4189b427686f4237c1a6eae841fcaba5c1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93425940"
---
# <span data-ttu-id="dffdf-101">Repair-AzsAlert</span><span class="sxs-lookup"><span data-stu-id="dffdf-101">Repair-AzsAlert</span></span>

## <span data-ttu-id="dffdf-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="dffdf-102">SYNOPSIS</span></span>
<span data-ttu-id="dffdf-103">Repara o alerta fornecido.</span><span class="sxs-lookup"><span data-stu-id="dffdf-103">Repairs the given alert.</span></span>

## <span data-ttu-id="dffdf-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="dffdf-104">SYNTAX</span></span>

### <span data-ttu-id="dffdf-105">Reparar (padrão)</span><span class="sxs-lookup"><span data-stu-id="dffdf-105">Repair (Default)</span></span>
```
Repair-AzsAlert -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="dffdf-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="dffdf-106">InputObject</span></span>
```
Repair-AzsAlert -InputObject <Alert> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dffdf-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="dffdf-107">DESCRIPTION</span></span>
<span data-ttu-id="dffdf-108">Repara o alerta fornecido.</span><span class="sxs-lookup"><span data-stu-id="dffdf-108">Repairs the given alert.</span></span>

## <span data-ttu-id="dffdf-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="dffdf-109">EXAMPLES</span></span>

### <span data-ttu-id="dffdf-110">--------------------------EXEMPLO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="dffdf-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Repair-AzsAlert -Name f2147f3d-42ac-4316-8cbc-f0f9c18888b0
```

<span data-ttu-id="dffdf-111">Repara um alerta por nome.</span><span class="sxs-lookup"><span data-stu-id="dffdf-111">Repairs an alert by Name.</span></span>

### <span data-ttu-id="dffdf-112">--------------------------EXEMPLO 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="dffdf-112">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsAlert -Name f2147f3d-42ac-4316-8cbc-f0f9c18888b0 | Repair-AzsAlert
```

<span data-ttu-id="dffdf-113">Repara um alerta por meio do encanamento.</span><span class="sxs-lookup"><span data-stu-id="dffdf-113">Repairs an alert through piping.</span></span>

## <span data-ttu-id="dffdf-114">OS</span><span class="sxs-lookup"><span data-stu-id="dffdf-114">PARAMETERS</span></span>

### <span data-ttu-id="dffdf-115">-Force</span><span class="sxs-lookup"><span data-stu-id="dffdf-115">-Force</span></span>
<span data-ttu-id="dffdf-116">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="dffdf-116">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="dffdf-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dffdf-117">-InputObject</span></span>
<span data-ttu-id="dffdf-118">Um alerta retornado do Get-AzsAlert.</span><span class="sxs-lookup"><span data-stu-id="dffdf-118">An alert returned from Get-AzsAlert.</span></span>

```yaml
Type: Alert
Parameter Sets: InputObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dffdf-119">-Local</span><span class="sxs-lookup"><span data-stu-id="dffdf-119">-Location</span></span>
<span data-ttu-id="dffdf-120">Nome do local.</span><span class="sxs-lookup"><span data-stu-id="dffdf-120">Name of the location.</span></span>

```yaml
Type: String
Parameter Sets: Repair
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dffdf-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="dffdf-121">-Name</span></span>
<span data-ttu-id="dffdf-122">O identificador do alerta.</span><span class="sxs-lookup"><span data-stu-id="dffdf-122">The alert identifier.</span></span>

```yaml
Type: String
Parameter Sets: Repair
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dffdf-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dffdf-123">-ResourceGroupName</span></span>
<span data-ttu-id="dffdf-124">Nome do grupo de recursos do qual o recurso reside.</span><span class="sxs-lookup"><span data-stu-id="dffdf-124">Resource group name which the resource resides.</span></span>

```yaml
Type: String
Parameter Sets: Repair
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dffdf-125">-Confirme</span><span class="sxs-lookup"><span data-stu-id="dffdf-125">-Confirm</span></span>
<span data-ttu-id="dffdf-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dffdf-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dffdf-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dffdf-127">-WhatIf</span></span>
<span data-ttu-id="dffdf-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="dffdf-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dffdf-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="dffdf-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dffdf-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dffdf-130">CommonParameters</span></span>
<span data-ttu-id="dffdf-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dffdf-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dffdf-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dffdf-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dffdf-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="dffdf-133">INPUTS</span></span>

## <span data-ttu-id="dffdf-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="dffdf-134">OUTPUTS</span></span>

## <span data-ttu-id="dffdf-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="dffdf-135">NOTES</span></span>

## <span data-ttu-id="dffdf-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="dffdf-136">RELATED LINKS</span></span>

