---
external help file: Azs.InfrastructureInsights.Admin-help.xml
Module Name: Azs.InfrastructureInsights.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: b04ce97fe1fc7e21f166b1bb86db52bc8ad6e29e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93774448"
---
# <span data-ttu-id="1e1ba-101">Close-AzsAlert</span><span class="sxs-lookup"><span data-stu-id="1e1ba-101">Close-AzsAlert</span></span>

## <span data-ttu-id="1e1ba-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1e1ba-102">SYNOPSIS</span></span>
<span data-ttu-id="1e1ba-103">Fecha o alerta fornecido.</span><span class="sxs-lookup"><span data-stu-id="1e1ba-103">Closes the given alert.</span></span>

## <span data-ttu-id="1e1ba-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1e1ba-104">SYNTAX</span></span>

### <span data-ttu-id="1e1ba-105">Fechar (padrão)</span><span class="sxs-lookup"><span data-stu-id="1e1ba-105">Close (Default)</span></span>
```
Close-AzsAlert -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1e1ba-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="1e1ba-106">InputObject</span></span>
```
Close-AzsAlert -InputObject <Alert> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1e1ba-107">Identificação</span><span class="sxs-lookup"><span data-stu-id="1e1ba-107">ResourceId</span></span>
```
Close-AzsAlert -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1e1ba-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1e1ba-108">DESCRIPTION</span></span>
<span data-ttu-id="1e1ba-109">Fecha o alerta fornecido.</span><span class="sxs-lookup"><span data-stu-id="1e1ba-109">Closes the given alert.</span></span>

## <span data-ttu-id="1e1ba-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1e1ba-110">EXAMPLES</span></span>

### <span data-ttu-id="1e1ba-111">--------------------------EXEMPLO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="1e1ba-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Close-AzsAlert -Name f2147f3d-42ac-4316-8cbc-f0f9c18888b0
```

<span data-ttu-id="1e1ba-112">Fechar um alerta por nome.</span><span class="sxs-lookup"><span data-stu-id="1e1ba-112">Close an alert by Name.</span></span>

### <span data-ttu-id="1e1ba-113">--------------------------EXEMPLO 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="1e1ba-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsAlert -Name f2147f3d-42ac-4316-8cbc-f0f9c18888b0 | Close-AzsAlert
```

<span data-ttu-id="1e1ba-114">Fechar um alerta por meio do encanamento.</span><span class="sxs-lookup"><span data-stu-id="1e1ba-114">Close an alert through piping.</span></span>

## <span data-ttu-id="1e1ba-115">OS</span><span class="sxs-lookup"><span data-stu-id="1e1ba-115">PARAMETERS</span></span>

### <span data-ttu-id="1e1ba-116">-Force</span><span class="sxs-lookup"><span data-stu-id="1e1ba-116">-Force</span></span>
<span data-ttu-id="1e1ba-117">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="1e1ba-117">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="1e1ba-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1e1ba-118">-InputObject</span></span>
<span data-ttu-id="1e1ba-119">Um alerta retornado do Get-AzsAlert.</span><span class="sxs-lookup"><span data-stu-id="1e1ba-119">An alert returned from Get-AzsAlert.</span></span>

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

### <span data-ttu-id="1e1ba-120">-Local</span><span class="sxs-lookup"><span data-stu-id="1e1ba-120">-Location</span></span>
<span data-ttu-id="1e1ba-121">Nome do local.</span><span class="sxs-lookup"><span data-stu-id="1e1ba-121">Name of the location.</span></span>

```yaml
Type: String
Parameter Sets: Close
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e1ba-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="1e1ba-122">-Name</span></span>
<span data-ttu-id="1e1ba-123">O identificador do alerta.</span><span class="sxs-lookup"><span data-stu-id="1e1ba-123">The alert identifier.</span></span>

```yaml
Type: String
Parameter Sets: Close
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e1ba-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e1ba-124">-ResourceGroupName</span></span>
<span data-ttu-id="1e1ba-125">Nome do grupo de recursos do qual o recurso reside.</span><span class="sxs-lookup"><span data-stu-id="1e1ba-125">Resource group name which the resource resides.</span></span>

```yaml
Type: String
Parameter Sets: Close
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e1ba-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1e1ba-126">-ResourceId</span></span>
<span data-ttu-id="1e1ba-127">A ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="1e1ba-127">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e1ba-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="1e1ba-128">-Confirm</span></span>
<span data-ttu-id="1e1ba-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1e1ba-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1e1ba-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1e1ba-130">-WhatIf</span></span>
<span data-ttu-id="1e1ba-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="1e1ba-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1e1ba-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1e1ba-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1e1ba-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e1ba-133">CommonParameters</span></span>
<span data-ttu-id="1e1ba-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1e1ba-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e1ba-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1e1ba-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e1ba-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1e1ba-136">INPUTS</span></span>

## <span data-ttu-id="1e1ba-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1e1ba-137">OUTPUTS</span></span>

### <span data-ttu-id="1e1ba-138">Microsoft. AzureStack. Management. InfrastructureInsights. admin. Models. Alert</span><span class="sxs-lookup"><span data-stu-id="1e1ba-138">Microsoft.AzureStack.Management.InfrastructureInsights.Admin.Models.Alert</span></span>

## <span data-ttu-id="1e1ba-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1e1ba-139">NOTES</span></span>

## <span data-ttu-id="1e1ba-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1e1ba-140">RELATED LINKS</span></span>

