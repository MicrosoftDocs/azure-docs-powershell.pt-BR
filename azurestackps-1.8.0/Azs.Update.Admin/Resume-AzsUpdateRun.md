---
external help file: Azs.Update.Admin-help.xml
Module Name: Azs.Update.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: fb3b784d079d1de3cec1d4fe3ec50a2853a4b054
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2020
ms.locfileid: "93774552"
---
# <span data-ttu-id="d94e7-101">Resume-AzsUpdateRun</span><span class="sxs-lookup"><span data-stu-id="d94e7-101">Resume-AzsUpdateRun</span></span>

## <span data-ttu-id="d94e7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d94e7-102">SYNOPSIS</span></span>
<span data-ttu-id="d94e7-103">Retoma uma execução de atualização iniciada anteriormente que falhou.</span><span class="sxs-lookup"><span data-stu-id="d94e7-103">Resumes a previously started update run that failed.</span></span>

## <span data-ttu-id="d94e7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d94e7-104">SYNTAX</span></span>

### <span data-ttu-id="d94e7-105">UpdateRuns_Rerun (padrão)</span><span class="sxs-lookup"><span data-stu-id="d94e7-105">UpdateRuns_Rerun (Default)</span></span>
```
Resume-AzsUpdateRun -Name <String> [-Location <String>] [-ResourceGroupName <String>] -UpdateName <String>
 [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d94e7-106">Identificação</span><span class="sxs-lookup"><span data-stu-id="d94e7-106">ResourceId</span></span>
```
Resume-AzsUpdateRun [-AsJob] -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d94e7-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d94e7-107">DESCRIPTION</span></span>
<span data-ttu-id="d94e7-108">Retoma uma execução de atualização iniciada anteriormente que falhou.</span><span class="sxs-lookup"><span data-stu-id="d94e7-108">Resumes a previously started update run that failed.</span></span> <span data-ttu-id="d94e7-109">Execuções de atualização retomadas serão retomadas no ponto em que houve falha na última vez.</span><span class="sxs-lookup"><span data-stu-id="d94e7-109">Resumeed update runs will resume at the point they last failed.</span></span>

## <span data-ttu-id="d94e7-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d94e7-110">EXAMPLES</span></span>

### <span data-ttu-id="d94e7-111">EXEMPLO 1</span><span class="sxs-lookup"><span data-stu-id="d94e7-111">EXAMPLE 1</span></span>
```
Get-AzsUpdateRun -Name 5173e9f4-3040-494f-b7a7-738a6331d55c -UpdateName Microsoft1.0.180305.1 | Resume-AzsUpdateRun
```

<span data-ttu-id="d94e7-112">Retoma uma execução de atualização iniciada anteriormente que falhou.</span><span class="sxs-lookup"><span data-stu-id="d94e7-112">Resumes a previously started update run that failed.</span></span>

## <span data-ttu-id="d94e7-113">OS</span><span class="sxs-lookup"><span data-stu-id="d94e7-113">PARAMETERS</span></span>

### <span data-ttu-id="d94e7-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="d94e7-114">-Name</span></span>
<span data-ttu-id="d94e7-115">Identificador de execução de atualização.</span><span class="sxs-lookup"><span data-stu-id="d94e7-115">Update run identifier.</span></span>

```yaml
Type: String
Parameter Sets: UpdateRuns_Rerun
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d94e7-116">-Local</span><span class="sxs-lookup"><span data-stu-id="d94e7-116">-Location</span></span>
<span data-ttu-id="d94e7-117">O nome do local de atualização.</span><span class="sxs-lookup"><span data-stu-id="d94e7-117">The name of the update location.</span></span>

```yaml
Type: String
Parameter Sets: UpdateRuns_Rerun
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d94e7-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d94e7-118">-ResourceGroupName</span></span>
<span data-ttu-id="d94e7-119">O grupo de recursos no qual o recurso está localizado.</span><span class="sxs-lookup"><span data-stu-id="d94e7-119">The resource group the resource is located under.</span></span>

```yaml
Type: String
Parameter Sets: UpdateRuns_Rerun
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d94e7-120">-Updatename</span><span class="sxs-lookup"><span data-stu-id="d94e7-120">-UpdateName</span></span>
<span data-ttu-id="d94e7-121">Nome para exibição da atualização.</span><span class="sxs-lookup"><span data-stu-id="d94e7-121">Display name of the update.</span></span>

```yaml
Type: String
Parameter Sets: UpdateRuns_Rerun
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d94e7-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d94e7-122">-AsJob</span></span>
<span data-ttu-id="d94e7-123">Executar assíncrono como um trabalho e retornar o objeto de trabalho.</span><span class="sxs-lookup"><span data-stu-id="d94e7-123">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="d94e7-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d94e7-124">-ResourceId</span></span>
<span data-ttu-id="d94e7-125">A ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="d94e7-125">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d94e7-126">-Force</span><span class="sxs-lookup"><span data-stu-id="d94e7-126">-Force</span></span>
<span data-ttu-id="d94e7-127">Sinalizador para remover o item sem confirmação.</span><span class="sxs-lookup"><span data-stu-id="d94e7-127">Flag to remove the item without confirmation.</span></span>

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

### <span data-ttu-id="d94e7-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d94e7-128">-WhatIf</span></span>
<span data-ttu-id="d94e7-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d94e7-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d94e7-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d94e7-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d94e7-131">-Confirme</span><span class="sxs-lookup"><span data-stu-id="d94e7-131">-Confirm</span></span>
<span data-ttu-id="d94e7-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d94e7-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d94e7-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d94e7-133">CommonParameters</span></span>
<span data-ttu-id="d94e7-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d94e7-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d94e7-135">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d94e7-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d94e7-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d94e7-136">INPUTS</span></span>

## <span data-ttu-id="d94e7-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d94e7-137">OUTPUTS</span></span>

## <span data-ttu-id="d94e7-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d94e7-138">NOTES</span></span>

## <span data-ttu-id="d94e7-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d94e7-139">RELATED LINKS</span></span>
