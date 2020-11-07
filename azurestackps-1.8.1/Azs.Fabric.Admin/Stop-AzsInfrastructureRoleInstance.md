---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 47e4c38d3ccd98350721d358cb98eec55341ba97
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2020
ms.locfileid: "93775117"
---
# <span data-ttu-id="5cdd4-101">Stop-AzsInfrastructureRoleInstance</span><span class="sxs-lookup"><span data-stu-id="5cdd4-101">Stop-AzsInfrastructureRoleInstance</span></span>

## <span data-ttu-id="5cdd4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5cdd4-102">SYNOPSIS</span></span>
<span data-ttu-id="5cdd4-103">Desligue uma instância de função de infraestrutura.</span><span class="sxs-lookup"><span data-stu-id="5cdd4-103">Power off an infrastructure role instance.</span></span>

## <span data-ttu-id="5cdd4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5cdd4-104">SYNTAX</span></span>

### <span data-ttu-id="5cdd4-105">PowerOff (padrão)</span><span class="sxs-lookup"><span data-stu-id="5cdd4-105">PowerOff (Default)</span></span>
```
Stop-AzsInfrastructureRoleInstance -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-AsJob]
 [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5cdd4-106">Identificação</span><span class="sxs-lookup"><span data-stu-id="5cdd4-106">ResourceId</span></span>
```
Stop-AzsInfrastructureRoleInstance -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5cdd4-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5cdd4-107">DESCRIPTION</span></span>
<span data-ttu-id="5cdd4-108">Desligue uma instância de função de infraestrutura.</span><span class="sxs-lookup"><span data-stu-id="5cdd4-108">Power off an infrastructure role instance.</span></span>

## <span data-ttu-id="5cdd4-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5cdd4-109">EXAMPLES</span></span>

### <span data-ttu-id="5cdd4-110">EXEMPLO 1</span><span class="sxs-lookup"><span data-stu-id="5cdd4-110">EXAMPLE 1</span></span>
```
Stop-AzsInfrastructureRoleInstancef -Name "AzS-ACS01"
```

<span data-ttu-id="5cdd4-111">Desligue uma instância de função de infraestrutura.</span><span class="sxs-lookup"><span data-stu-id="5cdd4-111">Power off a infrastructure role instance.</span></span>

## <span data-ttu-id="5cdd4-112">OS</span><span class="sxs-lookup"><span data-stu-id="5cdd4-112">PARAMETERS</span></span>

### <span data-ttu-id="5cdd4-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="5cdd4-113">-Name</span></span>
<span data-ttu-id="5cdd4-114">Nome de uma instância de função de infraestrutura.</span><span class="sxs-lookup"><span data-stu-id="5cdd4-114">Name of an infrastructure role instance.</span></span>

```yaml
Type: String
Parameter Sets: PowerOff
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5cdd4-115">-Local</span><span class="sxs-lookup"><span data-stu-id="5cdd4-115">-Location</span></span>
<span data-ttu-id="5cdd4-116">Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="5cdd4-116">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: PowerOff
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5cdd4-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5cdd4-117">-ResourceGroupName</span></span>
<span data-ttu-id="5cdd4-118">Grupo de recursos no qual o provedor de recursos foi registrado.</span><span class="sxs-lookup"><span data-stu-id="5cdd4-118">Resource group in which the resource provider has been registered.</span></span>

```yaml
Type: String
Parameter Sets: PowerOff
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5cdd4-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5cdd4-119">-ResourceId</span></span>
<span data-ttu-id="5cdd4-120">ID do recurso de instância da infraestrutura.</span><span class="sxs-lookup"><span data-stu-id="5cdd4-120">Infrastructure role instance resource ID.</span></span>

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

### <span data-ttu-id="5cdd4-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5cdd4-121">-AsJob</span></span>
<span data-ttu-id="5cdd4-122">Executar assíncrono como um trabalho e retornar o objeto de trabalho.</span><span class="sxs-lookup"><span data-stu-id="5cdd4-122">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="5cdd4-123">-Force</span><span class="sxs-lookup"><span data-stu-id="5cdd4-123">-Force</span></span>
<span data-ttu-id="5cdd4-124">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="5cdd4-124">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="5cdd4-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5cdd4-125">-WhatIf</span></span>
<span data-ttu-id="5cdd4-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="5cdd4-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5cdd4-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5cdd4-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5cdd4-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="5cdd4-128">-Confirm</span></span>
<span data-ttu-id="5cdd4-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5cdd4-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5cdd4-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5cdd4-130">CommonParameters</span></span>
<span data-ttu-id="5cdd4-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5cdd4-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5cdd4-132">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5cdd4-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5cdd4-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5cdd4-133">INPUTS</span></span>

## <span data-ttu-id="5cdd4-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5cdd4-134">OUTPUTS</span></span>

## <span data-ttu-id="5cdd4-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5cdd4-135">NOTES</span></span>

## <span data-ttu-id="5cdd4-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5cdd4-136">RELATED LINKS</span></span>
