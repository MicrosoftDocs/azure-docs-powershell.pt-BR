---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 48f7fd6280596e70810d330f3fe69b37059e15cd
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2020
ms.locfileid: "93774606"
---
# <span data-ttu-id="eb6e1-101">Start-AzsInfrastructureRoleInstance</span><span class="sxs-lookup"><span data-stu-id="eb6e1-101">Start-AzsInfrastructureRoleInstance</span></span>

## <span data-ttu-id="eb6e1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="eb6e1-102">SYNOPSIS</span></span>
<span data-ttu-id="eb6e1-103">Ative uma instância de função de infraestrutura.</span><span class="sxs-lookup"><span data-stu-id="eb6e1-103">Power on an infrastructure role instance.</span></span>

## <span data-ttu-id="eb6e1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="eb6e1-104">SYNTAX</span></span>

### <span data-ttu-id="eb6e1-105">Power-out (padrão)</span><span class="sxs-lookup"><span data-stu-id="eb6e1-105">PowerOn (Default)</span></span>
```
Start-AzsInfrastructureRoleInstance -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-AsJob]
 [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eb6e1-106">Identificação</span><span class="sxs-lookup"><span data-stu-id="eb6e1-106">ResourceId</span></span>
```
Start-AzsInfrastructureRoleInstance -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="eb6e1-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="eb6e1-107">DESCRIPTION</span></span>
<span data-ttu-id="eb6e1-108">Ative uma instância de função de infraestrutura.</span><span class="sxs-lookup"><span data-stu-id="eb6e1-108">Power on an infrastructure role instance.</span></span>

## <span data-ttu-id="eb6e1-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="eb6e1-109">EXAMPLES</span></span>

### <span data-ttu-id="eb6e1-110">EXEMPLO 1</span><span class="sxs-lookup"><span data-stu-id="eb6e1-110">EXAMPLE 1</span></span>
```
Start-AzsInfrastructureRoleInstance -Name "AzS-ACS01"
```

<span data-ttu-id="eb6e1-111">Ative uma instância de função de infraestrutura.</span><span class="sxs-lookup"><span data-stu-id="eb6e1-111">Power on an infrastructure role instance.</span></span>

## <span data-ttu-id="eb6e1-112">OS</span><span class="sxs-lookup"><span data-stu-id="eb6e1-112">PARAMETERS</span></span>

### <span data-ttu-id="eb6e1-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="eb6e1-113">-Name</span></span>
<span data-ttu-id="eb6e1-114">Nome da instância da função de infraestrutura.</span><span class="sxs-lookup"><span data-stu-id="eb6e1-114">Name of the infrastructure role instance.</span></span>

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

### <span data-ttu-id="eb6e1-115">-Local</span><span class="sxs-lookup"><span data-stu-id="eb6e1-115">-Location</span></span>
<span data-ttu-id="eb6e1-116">Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="eb6e1-116">Location of the resource.</span></span>

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

### <span data-ttu-id="eb6e1-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb6e1-117">-ResourceGroupName</span></span>
<span data-ttu-id="eb6e1-118">Grupo de recursos no qual o provedor de recursos foi registrado.</span><span class="sxs-lookup"><span data-stu-id="eb6e1-118">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="eb6e1-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="eb6e1-119">-ResourceId</span></span>
<span data-ttu-id="eb6e1-120">ID do recurso de instância da infraestrutura.</span><span class="sxs-lookup"><span data-stu-id="eb6e1-120">Infrastructure role instance resource ID.</span></span>

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

### <span data-ttu-id="eb6e1-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="eb6e1-121">-AsJob</span></span>
<span data-ttu-id="eb6e1-122">Executar assíncrono como um trabalho e retornar o objeto de trabalho.</span><span class="sxs-lookup"><span data-stu-id="eb6e1-122">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="eb6e1-123">-Force</span><span class="sxs-lookup"><span data-stu-id="eb6e1-123">-Force</span></span>
<span data-ttu-id="eb6e1-124">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="eb6e1-124">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="eb6e1-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eb6e1-125">-WhatIf</span></span>
<span data-ttu-id="eb6e1-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="eb6e1-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eb6e1-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="eb6e1-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eb6e1-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="eb6e1-128">-Confirm</span></span>
<span data-ttu-id="eb6e1-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eb6e1-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eb6e1-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb6e1-130">CommonParameters</span></span>
<span data-ttu-id="eb6e1-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eb6e1-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb6e1-132">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eb6e1-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb6e1-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="eb6e1-133">INPUTS</span></span>

## <span data-ttu-id="eb6e1-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="eb6e1-134">OUTPUTS</span></span>

## <span data-ttu-id="eb6e1-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="eb6e1-135">NOTES</span></span>

## <span data-ttu-id="eb6e1-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="eb6e1-136">RELATED LINKS</span></span>
