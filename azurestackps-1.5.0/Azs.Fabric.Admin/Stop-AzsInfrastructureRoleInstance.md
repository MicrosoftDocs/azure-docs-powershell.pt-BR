---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5a63ccb6706f4d43e890b8805af0d00aff350bc4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93426194"
---
# <span data-ttu-id="c5c55-101">Stop-AzsInfrastructureRoleInstance</span><span class="sxs-lookup"><span data-stu-id="c5c55-101">Stop-AzsInfrastructureRoleInstance</span></span>

## <span data-ttu-id="c5c55-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c5c55-102">SYNOPSIS</span></span>
<span data-ttu-id="c5c55-103">Desligue uma instância de função de infraestrutura.</span><span class="sxs-lookup"><span data-stu-id="c5c55-103">Power off an infrastructure role instance.</span></span>

## <span data-ttu-id="c5c55-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c5c55-104">SYNTAX</span></span>

### <span data-ttu-id="c5c55-105">PowerOff (padrão)</span><span class="sxs-lookup"><span data-stu-id="c5c55-105">PowerOff (Default)</span></span>
```
Stop-AzsInfrastructureRoleInstance -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-AsJob]
 [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c5c55-106">Identificação</span><span class="sxs-lookup"><span data-stu-id="c5c55-106">ResourceId</span></span>
```
Stop-AzsInfrastructureRoleInstance -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c5c55-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c5c55-107">DESCRIPTION</span></span>
<span data-ttu-id="c5c55-108">Desligue uma instância de função de infraestrutura.</span><span class="sxs-lookup"><span data-stu-id="c5c55-108">Power off an infrastructure role instance.</span></span>

## <span data-ttu-id="c5c55-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c5c55-109">EXAMPLES</span></span>

### <span data-ttu-id="c5c55-110">--------------------------EXEMPLO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="c5c55-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Stop-AzsInfrastructureRoleInstancef -Name "AzS-ACS01"
```

<span data-ttu-id="c5c55-111">Desligue uma instância de função de infraestrutura.</span><span class="sxs-lookup"><span data-stu-id="c5c55-111">Power off a infrastructure role instance.</span></span>

## <span data-ttu-id="c5c55-112">OS</span><span class="sxs-lookup"><span data-stu-id="c5c55-112">PARAMETERS</span></span>

### <span data-ttu-id="c5c55-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c5c55-113">-AsJob</span></span>
<span data-ttu-id="c5c55-114">Executar assíncrono como um trabalho e retornar o objeto de trabalho.</span><span class="sxs-lookup"><span data-stu-id="c5c55-114">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="c5c55-115">-Force</span><span class="sxs-lookup"><span data-stu-id="c5c55-115">-Force</span></span>
<span data-ttu-id="c5c55-116">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="c5c55-116">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="c5c55-117">-Local</span><span class="sxs-lookup"><span data-stu-id="c5c55-117">-Location</span></span>
<span data-ttu-id="c5c55-118">Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="c5c55-118">Location of the resource.</span></span>

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

### <span data-ttu-id="c5c55-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="c5c55-119">-Name</span></span>
<span data-ttu-id="c5c55-120">Nome de uma instância de função de infraestrutura.</span><span class="sxs-lookup"><span data-stu-id="c5c55-120">Name of an infrastructure role instance.</span></span>

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

### <span data-ttu-id="c5c55-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5c55-121">-ResourceGroupName</span></span>
<span data-ttu-id="c5c55-122">Grupo de recursos no qual o provedor de recursos foi registrado.</span><span class="sxs-lookup"><span data-stu-id="c5c55-122">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="c5c55-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c5c55-123">-ResourceId</span></span>
<span data-ttu-id="c5c55-124">ID do recurso de instância da infraestrutura.</span><span class="sxs-lookup"><span data-stu-id="c5c55-124">Infrastructure role instance resource ID.</span></span>

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

### <span data-ttu-id="c5c55-125">-Confirme</span><span class="sxs-lookup"><span data-stu-id="c5c55-125">-Confirm</span></span>
<span data-ttu-id="c5c55-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c5c55-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c5c55-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c5c55-127">-WhatIf</span></span>
<span data-ttu-id="c5c55-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c5c55-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c5c55-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c5c55-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c5c55-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5c55-130">CommonParameters</span></span>
<span data-ttu-id="c5c55-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c5c55-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5c55-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c5c55-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5c55-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c5c55-133">INPUTS</span></span>

## <span data-ttu-id="c5c55-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c5c55-134">OUTPUTS</span></span>

## <span data-ttu-id="c5c55-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c5c55-135">NOTES</span></span>

## <span data-ttu-id="c5c55-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c5c55-136">RELATED LINKS</span></span>

