---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 04b011279d88f294e1caf95519e29a8368b08546
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/08/2020
ms.locfileid: "93946880"
---
# <span data-ttu-id="ab407-101">Suspend-AzsInfrastructureRoleInstance</span><span class="sxs-lookup"><span data-stu-id="ab407-101">Suspend-AzsInfrastructureRoleInstance</span></span>

## <span data-ttu-id="ab407-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ab407-102">SYNOPSIS</span></span>
<span data-ttu-id="ab407-103">Desligar uma instância de função de infraestrutura.</span><span class="sxs-lookup"><span data-stu-id="ab407-103">Shut down an infrastructure role instance.</span></span>

## <span data-ttu-id="ab407-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ab407-104">SYNTAX</span></span>

### <span data-ttu-id="ab407-105">Shutdown (padrão)</span><span class="sxs-lookup"><span data-stu-id="ab407-105">Shutdown (Default)</span></span>
```
Suspend-AzsInfrastructureRoleInstance -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ab407-106">Identificação</span><span class="sxs-lookup"><span data-stu-id="ab407-106">ResourceId</span></span>
```
Suspend-AzsInfrastructureRoleInstance -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ab407-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ab407-107">DESCRIPTION</span></span>
<span data-ttu-id="ab407-108">Desligar uma instância de função de infraestrutura.</span><span class="sxs-lookup"><span data-stu-id="ab407-108">Shut down an infrastructure role instance.</span></span>

## <span data-ttu-id="ab407-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ab407-109">EXAMPLES</span></span>

### <span data-ttu-id="ab407-110">EXEMPLO 1</span><span class="sxs-lookup"><span data-stu-id="ab407-110">EXAMPLE 1</span></span>
```
Suspend-AzsInfrastructureRoleInstance -Name "AzS-ACS01"
```

<span data-ttu-id="ab407-111">Desligar uma instância de função de infraestrutura.</span><span class="sxs-lookup"><span data-stu-id="ab407-111">Shut down an infrastructure role instance.</span></span>
<span data-ttu-id="ab407-112">Na falha, uma exceção é lançada.</span><span class="sxs-lookup"><span data-stu-id="ab407-112">On failure an exception is thrown.</span></span>

## <span data-ttu-id="ab407-113">OS</span><span class="sxs-lookup"><span data-stu-id="ab407-113">PARAMETERS</span></span>

### <span data-ttu-id="ab407-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="ab407-114">-Name</span></span>
<span data-ttu-id="ab407-115">Nome de uma instância de função de infraestrutura.</span><span class="sxs-lookup"><span data-stu-id="ab407-115">Name of an infrastructure role instance.</span></span>

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

### <span data-ttu-id="ab407-116">-Local</span><span class="sxs-lookup"><span data-stu-id="ab407-116">-Location</span></span>
<span data-ttu-id="ab407-117">Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="ab407-117">Location of the resource.</span></span>

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

### <span data-ttu-id="ab407-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab407-118">-ResourceGroupName</span></span>
<span data-ttu-id="ab407-119">Grupo de recursos no qual o provedor de recursos foi registrado.</span><span class="sxs-lookup"><span data-stu-id="ab407-119">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="ab407-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ab407-120">-ResourceId</span></span>
<span data-ttu-id="ab407-121">ID do recurso de instância da infraestrutura.</span><span class="sxs-lookup"><span data-stu-id="ab407-121">Infrastructure role instance resource ID.</span></span>

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

### <span data-ttu-id="ab407-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ab407-122">-AsJob</span></span>
<span data-ttu-id="ab407-123">Executar assíncrono como um trabalho e retornar o objeto de trabalho.</span><span class="sxs-lookup"><span data-stu-id="ab407-123">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="ab407-124">-Force</span><span class="sxs-lookup"><span data-stu-id="ab407-124">-Force</span></span>
<span data-ttu-id="ab407-125">Não pedir confirmação</span><span class="sxs-lookup"><span data-stu-id="ab407-125">Don't ask for confirmation</span></span>

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

### <span data-ttu-id="ab407-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ab407-126">-WhatIf</span></span>
<span data-ttu-id="ab407-127">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ab407-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ab407-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ab407-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ab407-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="ab407-129">-Confirm</span></span>
<span data-ttu-id="ab407-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ab407-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ab407-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab407-131">CommonParameters</span></span>
<span data-ttu-id="ab407-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab407-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab407-133">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ab407-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab407-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ab407-134">INPUTS</span></span>

## <span data-ttu-id="ab407-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ab407-135">OUTPUTS</span></span>

## <span data-ttu-id="ab407-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ab407-136">NOTES</span></span>

## <span data-ttu-id="ab407-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ab407-137">RELATED LINKS</span></span>
