---
external help file: Azs.InfrastructureInsights.Admin-help.xml
Module Name: Azs.Infrastructureinsights.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 14885871139eaed1c901312b9540a90d385795e5
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/08/2020
ms.locfileid: "93946922"
---
# <span data-ttu-id="71555-101">Close-AzsAlert</span><span class="sxs-lookup"><span data-stu-id="71555-101">Close-AzsAlert</span></span>

## <span data-ttu-id="71555-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="71555-102">SYNOPSIS</span></span>
<span data-ttu-id="71555-103">Fecha o alerta fornecido.</span><span class="sxs-lookup"><span data-stu-id="71555-103">Closes the given alert.</span></span>

## <span data-ttu-id="71555-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="71555-104">SYNTAX</span></span>

### <span data-ttu-id="71555-105">Fechar (padrão)</span><span class="sxs-lookup"><span data-stu-id="71555-105">Close (Default)</span></span>
```
Close-AzsAlert -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="71555-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="71555-106">InputObject</span></span>
```
Close-AzsAlert -InputObject <Alert> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="71555-107">Identificação</span><span class="sxs-lookup"><span data-stu-id="71555-107">ResourceId</span></span>
```
Close-AzsAlert -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="71555-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="71555-108">DESCRIPTION</span></span>
<span data-ttu-id="71555-109">Fecha o alerta fornecido.</span><span class="sxs-lookup"><span data-stu-id="71555-109">Closes the given alert.</span></span>

## <span data-ttu-id="71555-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="71555-110">EXAMPLES</span></span>

### <span data-ttu-id="71555-111">EXEMPLO 1</span><span class="sxs-lookup"><span data-stu-id="71555-111">EXAMPLE 1</span></span>
```
Close-AzsAlert -Name f2147f3d-42ac-4316-8cbc-f0f9c18888b0
```

<span data-ttu-id="71555-112">Fechar um alerta por nome.</span><span class="sxs-lookup"><span data-stu-id="71555-112">Close an alert by Name.</span></span>

### <span data-ttu-id="71555-113">EXEMPLO 2</span><span class="sxs-lookup"><span data-stu-id="71555-113">EXAMPLE 2</span></span>
```
Get-AzsAlert -Name f2147f3d-42ac-4316-8cbc-f0f9c18888b0 | Close-AzsAlert
```

<span data-ttu-id="71555-114">Fechar um alerta por meio do encanamento.</span><span class="sxs-lookup"><span data-stu-id="71555-114">Close an alert through piping.</span></span>

## <span data-ttu-id="71555-115">OS</span><span class="sxs-lookup"><span data-stu-id="71555-115">PARAMETERS</span></span>

### <span data-ttu-id="71555-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="71555-116">-Name</span></span>
<span data-ttu-id="71555-117">O identificador do alerta.</span><span class="sxs-lookup"><span data-stu-id="71555-117">The alert identifier.</span></span>

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

### <span data-ttu-id="71555-118">-Local</span><span class="sxs-lookup"><span data-stu-id="71555-118">-Location</span></span>
<span data-ttu-id="71555-119">Nome do local.</span><span class="sxs-lookup"><span data-stu-id="71555-119">Name of the location.</span></span>

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

### <span data-ttu-id="71555-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71555-120">-ResourceGroupName</span></span>
<span data-ttu-id="71555-121">Nome do grupo de recursos do alerta.</span><span class="sxs-lookup"><span data-stu-id="71555-121">Resource group name of the alert.</span></span>

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

### <span data-ttu-id="71555-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="71555-122">-InputObject</span></span>
<span data-ttu-id="71555-123">Um alerta retornado do Get-AzsAlert.</span><span class="sxs-lookup"><span data-stu-id="71555-123">An alert returned from Get-AzsAlert.</span></span>

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

### <span data-ttu-id="71555-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="71555-124">-ResourceId</span></span>
<span data-ttu-id="71555-125">A ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="71555-125">The resource id.</span></span>

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

### <span data-ttu-id="71555-126">-Force</span><span class="sxs-lookup"><span data-stu-id="71555-126">-Force</span></span>
<span data-ttu-id="71555-127">Parâmetro de opção para não pedir confirmação.</span><span class="sxs-lookup"><span data-stu-id="71555-127">Switch parameter for not asking confirmation.</span></span>

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

### <span data-ttu-id="71555-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71555-128">-WhatIf</span></span>
<span data-ttu-id="71555-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="71555-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="71555-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="71555-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="71555-131">-Confirme</span><span class="sxs-lookup"><span data-stu-id="71555-131">-Confirm</span></span>
<span data-ttu-id="71555-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="71555-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="71555-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71555-133">CommonParameters</span></span>
<span data-ttu-id="71555-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71555-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71555-135">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71555-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71555-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="71555-136">INPUTS</span></span>

## <span data-ttu-id="71555-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="71555-137">OUTPUTS</span></span>

### <span data-ttu-id="71555-138">Microsoft. AzureStack. Management. InfrastructureInsights. admin. Models. Alert</span><span class="sxs-lookup"><span data-stu-id="71555-138">Microsoft.AzureStack.Management.InfrastructureInsights.Admin.Models.Alert</span></span>

## <span data-ttu-id="71555-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="71555-139">NOTES</span></span>

## <span data-ttu-id="71555-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="71555-140">RELATED LINKS</span></span>
