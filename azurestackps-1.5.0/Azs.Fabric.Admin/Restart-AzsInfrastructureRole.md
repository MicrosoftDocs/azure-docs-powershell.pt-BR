---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: da781ee77cb94e7bc442b72ad0655041cf23b546
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93425705"
---
# <span data-ttu-id="c38de-101">Restart-AzsInfrastructureRole</span><span class="sxs-lookup"><span data-stu-id="c38de-101">Restart-AzsInfrastructureRole</span></span>

## <span data-ttu-id="c38de-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c38de-102">SYNOPSIS</span></span>
<span data-ttu-id="c38de-103">Reinicia a função de infraestrutura solicitada.</span><span class="sxs-lookup"><span data-stu-id="c38de-103">Restarts the requested infrastructure role.</span></span>

## <span data-ttu-id="c38de-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c38de-104">SYNTAX</span></span>

### <span data-ttu-id="c38de-105">Reiniciar (padrão)</span><span class="sxs-lookup"><span data-stu-id="c38de-105">Restart (Default)</span></span>
```
Restart-AzsInfrastructureRole -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-AsJob]
 [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c38de-106">Identificação</span><span class="sxs-lookup"><span data-stu-id="c38de-106">ResourceId</span></span>
```
Restart-AzsInfrastructureRole -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c38de-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c38de-107">DESCRIPTION</span></span>
<span data-ttu-id="c38de-108">Reinicia a função de infraestrutura solicitada.</span><span class="sxs-lookup"><span data-stu-id="c38de-108">Restarts the requested infrastructure role.</span></span>

## <span data-ttu-id="c38de-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c38de-109">EXAMPLES</span></span>

### <span data-ttu-id="c38de-110">--------------------------EXEMPLO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="c38de-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Restart-AzsInfrastructureRole -Name "Compute Controller"
```

<span data-ttu-id="c38de-111">Reinicie uma função de infraestrutura que tenha falhado.</span><span class="sxs-lookup"><span data-stu-id="c38de-111">Restart an infrastructure role which has crashed.</span></span>

## <span data-ttu-id="c38de-112">OS</span><span class="sxs-lookup"><span data-stu-id="c38de-112">PARAMETERS</span></span>

### <span data-ttu-id="c38de-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c38de-113">-AsJob</span></span>
<span data-ttu-id="c38de-114">Executar assíncrono como um trabalho e retornar o objeto de trabalho.</span><span class="sxs-lookup"><span data-stu-id="c38de-114">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="c38de-115">-Force</span><span class="sxs-lookup"><span data-stu-id="c38de-115">-Force</span></span>
<span data-ttu-id="c38de-116">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="c38de-116">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="c38de-117">-Local</span><span class="sxs-lookup"><span data-stu-id="c38de-117">-Location</span></span>
<span data-ttu-id="c38de-118">Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="c38de-118">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: Restart
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c38de-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="c38de-119">-Name</span></span>
<span data-ttu-id="c38de-120">Nome da função de infraestrutura.</span><span class="sxs-lookup"><span data-stu-id="c38de-120">Infrastructure role name.</span></span>

```yaml
Type: String
Parameter Sets: Restart
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c38de-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c38de-121">-ResourceGroupName</span></span>
<span data-ttu-id="c38de-122">Grupo de recursos no qual o provedor de recursos foi registrado.</span><span class="sxs-lookup"><span data-stu-id="c38de-122">Resource group in which the resource provider has been registered.</span></span>

```yaml
Type: String
Parameter Sets: Restart
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c38de-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c38de-123">-ResourceId</span></span>
<span data-ttu-id="c38de-124">ID do recurso da função de infraestrutura.</span><span class="sxs-lookup"><span data-stu-id="c38de-124">Infrastructure role resource ID.</span></span>

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

### <span data-ttu-id="c38de-125">-Confirme</span><span class="sxs-lookup"><span data-stu-id="c38de-125">-Confirm</span></span>
<span data-ttu-id="c38de-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c38de-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c38de-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c38de-127">-WhatIf</span></span>
<span data-ttu-id="c38de-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c38de-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c38de-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c38de-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c38de-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c38de-130">CommonParameters</span></span>
<span data-ttu-id="c38de-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c38de-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c38de-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c38de-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c38de-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c38de-133">INPUTS</span></span>

## <span data-ttu-id="c38de-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c38de-134">OUTPUTS</span></span>

## <span data-ttu-id="c38de-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c38de-135">NOTES</span></span>

## <span data-ttu-id="c38de-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c38de-136">RELATED LINKS</span></span>

