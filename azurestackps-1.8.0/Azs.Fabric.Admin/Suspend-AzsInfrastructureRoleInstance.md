---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 04b011279d88f294e1caf95519e29a8368b08546
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2020
ms.locfileid: "93774716"
---
# <span data-ttu-id="2a2d7-101">Suspend-AzsInfrastructureRoleInstance</span><span class="sxs-lookup"><span data-stu-id="2a2d7-101">Suspend-AzsInfrastructureRoleInstance</span></span>

## <span data-ttu-id="2a2d7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2a2d7-102">SYNOPSIS</span></span>
<span data-ttu-id="2a2d7-103">Desligar uma instância de função de infraestrutura.</span><span class="sxs-lookup"><span data-stu-id="2a2d7-103">Shut down an infrastructure role instance.</span></span>

## <span data-ttu-id="2a2d7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2a2d7-104">SYNTAX</span></span>

### <span data-ttu-id="2a2d7-105">Shutdown (padrão)</span><span class="sxs-lookup"><span data-stu-id="2a2d7-105">Shutdown (Default)</span></span>
```
Suspend-AzsInfrastructureRoleInstance -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2a2d7-106">Identificação</span><span class="sxs-lookup"><span data-stu-id="2a2d7-106">ResourceId</span></span>
```
Suspend-AzsInfrastructureRoleInstance -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2a2d7-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2a2d7-107">DESCRIPTION</span></span>
<span data-ttu-id="2a2d7-108">Desligar uma instância de função de infraestrutura.</span><span class="sxs-lookup"><span data-stu-id="2a2d7-108">Shut down an infrastructure role instance.</span></span>

## <span data-ttu-id="2a2d7-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2a2d7-109">EXAMPLES</span></span>

### <span data-ttu-id="2a2d7-110">EXEMPLO 1</span><span class="sxs-lookup"><span data-stu-id="2a2d7-110">EXAMPLE 1</span></span>
```
Suspend-AzsInfrastructureRoleInstance -Name "AzS-ACS01"
```

<span data-ttu-id="2a2d7-111">Desligar uma instância de função de infraestrutura.</span><span class="sxs-lookup"><span data-stu-id="2a2d7-111">Shut down an infrastructure role instance.</span></span>
<span data-ttu-id="2a2d7-112">Na falha, uma exceção é lançada.</span><span class="sxs-lookup"><span data-stu-id="2a2d7-112">On failure an exception is thrown.</span></span>

## <span data-ttu-id="2a2d7-113">OS</span><span class="sxs-lookup"><span data-stu-id="2a2d7-113">PARAMETERS</span></span>

### <span data-ttu-id="2a2d7-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="2a2d7-114">-Name</span></span>
<span data-ttu-id="2a2d7-115">Nome de uma instância de função de infraestrutura.</span><span class="sxs-lookup"><span data-stu-id="2a2d7-115">Name of an infrastructure role instance.</span></span>

```yaml
Type: String
Parameter Sets: Shutdown
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a2d7-116">-Local</span><span class="sxs-lookup"><span data-stu-id="2a2d7-116">-Location</span></span>
<span data-ttu-id="2a2d7-117">Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="2a2d7-117">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: Shutdown
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a2d7-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2a2d7-118">-ResourceGroupName</span></span>
<span data-ttu-id="2a2d7-119">Grupo de recursos no qual o provedor de recursos foi registrado.</span><span class="sxs-lookup"><span data-stu-id="2a2d7-119">Resource group in which the resource provider has been registered.</span></span>

```yaml
Type: String
Parameter Sets: Shutdown
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a2d7-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2a2d7-120">-ResourceId</span></span>
<span data-ttu-id="2a2d7-121">ID do recurso de instância da infraestrutura.</span><span class="sxs-lookup"><span data-stu-id="2a2d7-121">Infrastructure role instance resource ID.</span></span>

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

### <span data-ttu-id="2a2d7-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2a2d7-122">-AsJob</span></span>
<span data-ttu-id="2a2d7-123">Executar assíncrono como um trabalho e retornar o objeto de trabalho.</span><span class="sxs-lookup"><span data-stu-id="2a2d7-123">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="2a2d7-124">-Force</span><span class="sxs-lookup"><span data-stu-id="2a2d7-124">-Force</span></span>
<span data-ttu-id="2a2d7-125">Não pedir confirmação</span><span class="sxs-lookup"><span data-stu-id="2a2d7-125">Don't ask for confirmation</span></span>

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

### <span data-ttu-id="2a2d7-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2a2d7-126">-WhatIf</span></span>
<span data-ttu-id="2a2d7-127">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="2a2d7-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2a2d7-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2a2d7-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2a2d7-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="2a2d7-129">-Confirm</span></span>
<span data-ttu-id="2a2d7-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2a2d7-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2a2d7-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a2d7-131">CommonParameters</span></span>
<span data-ttu-id="2a2d7-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2a2d7-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a2d7-133">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2a2d7-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a2d7-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2a2d7-134">INPUTS</span></span>

## <span data-ttu-id="2a2d7-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2a2d7-135">OUTPUTS</span></span>

## <span data-ttu-id="2a2d7-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2a2d7-136">NOTES</span></span>

## <span data-ttu-id="2a2d7-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2a2d7-137">RELATED LINKS</span></span>
