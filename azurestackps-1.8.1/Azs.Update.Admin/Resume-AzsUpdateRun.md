---
external help file: Azs.Update.Admin-help.xml
Module Name: Azs.Update.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: fb3b784d079d1de3cec1d4fe3ec50a2853a4b054
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2020
ms.locfileid: "93775027"
---
# <span data-ttu-id="febae-101">Resume-AzsUpdateRun</span><span class="sxs-lookup"><span data-stu-id="febae-101">Resume-AzsUpdateRun</span></span>

## <span data-ttu-id="febae-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="febae-102">SYNOPSIS</span></span>
<span data-ttu-id="febae-103">Retoma uma execução de atualização iniciada anteriormente que falhou.</span><span class="sxs-lookup"><span data-stu-id="febae-103">Resumes a previously started update run that failed.</span></span>

## <span data-ttu-id="febae-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="febae-104">SYNTAX</span></span>

### <span data-ttu-id="febae-105">UpdateRuns_Rerun (padrão)</span><span class="sxs-lookup"><span data-stu-id="febae-105">UpdateRuns_Rerun (Default)</span></span>
```
Resume-AzsUpdateRun -Name <String> [-Location <String>] [-ResourceGroupName <String>] -UpdateName <String>
 [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="febae-106">Identificação</span><span class="sxs-lookup"><span data-stu-id="febae-106">ResourceId</span></span>
```
Resume-AzsUpdateRun [-AsJob] -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="febae-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="febae-107">DESCRIPTION</span></span>
<span data-ttu-id="febae-108">Retoma uma execução de atualização iniciada anteriormente que falhou.</span><span class="sxs-lookup"><span data-stu-id="febae-108">Resumes a previously started update run that failed.</span></span> <span data-ttu-id="febae-109">Execuções de atualização retomadas serão retomadas no ponto em que houve falha na última vez.</span><span class="sxs-lookup"><span data-stu-id="febae-109">Resumeed update runs will resume at the point they last failed.</span></span>

## <span data-ttu-id="febae-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="febae-110">EXAMPLES</span></span>

### <span data-ttu-id="febae-111">EXEMPLO 1</span><span class="sxs-lookup"><span data-stu-id="febae-111">EXAMPLE 1</span></span>
```
Get-AzsUpdateRun -Name 5173e9f4-3040-494f-b7a7-738a6331d55c -UpdateName Microsoft1.0.180305.1 | Resume-AzsUpdateRun
```

<span data-ttu-id="febae-112">Retoma uma execução de atualização iniciada anteriormente que falhou.</span><span class="sxs-lookup"><span data-stu-id="febae-112">Resumes a previously started update run that failed.</span></span>

## <span data-ttu-id="febae-113">OS</span><span class="sxs-lookup"><span data-stu-id="febae-113">PARAMETERS</span></span>

### <span data-ttu-id="febae-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="febae-114">-Name</span></span>
<span data-ttu-id="febae-115">Identificador de execução de atualização.</span><span class="sxs-lookup"><span data-stu-id="febae-115">Update run identifier.</span></span>

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

### <span data-ttu-id="febae-116">-Local</span><span class="sxs-lookup"><span data-stu-id="febae-116">-Location</span></span>
<span data-ttu-id="febae-117">O nome do local de atualização.</span><span class="sxs-lookup"><span data-stu-id="febae-117">The name of the update location.</span></span>

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

### <span data-ttu-id="febae-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="febae-118">-ResourceGroupName</span></span>
<span data-ttu-id="febae-119">O grupo de recursos no qual o recurso está localizado.</span><span class="sxs-lookup"><span data-stu-id="febae-119">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="febae-120">-Updatename</span><span class="sxs-lookup"><span data-stu-id="febae-120">-UpdateName</span></span>
<span data-ttu-id="febae-121">Nome para exibição da atualização.</span><span class="sxs-lookup"><span data-stu-id="febae-121">Display name of the update.</span></span>

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

### <span data-ttu-id="febae-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="febae-122">-AsJob</span></span>
<span data-ttu-id="febae-123">Executar assíncrono como um trabalho e retornar o objeto de trabalho.</span><span class="sxs-lookup"><span data-stu-id="febae-123">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="febae-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="febae-124">-ResourceId</span></span>
<span data-ttu-id="febae-125">A ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="febae-125">The resource id.</span></span>

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

### <span data-ttu-id="febae-126">-Force</span><span class="sxs-lookup"><span data-stu-id="febae-126">-Force</span></span>
<span data-ttu-id="febae-127">Sinalizador para remover o item sem confirmação.</span><span class="sxs-lookup"><span data-stu-id="febae-127">Flag to remove the item without confirmation.</span></span>

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

### <span data-ttu-id="febae-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="febae-128">-WhatIf</span></span>
<span data-ttu-id="febae-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="febae-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="febae-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="febae-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="febae-131">-Confirme</span><span class="sxs-lookup"><span data-stu-id="febae-131">-Confirm</span></span>
<span data-ttu-id="febae-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="febae-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="febae-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="febae-133">CommonParameters</span></span>
<span data-ttu-id="febae-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="febae-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="febae-135">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="febae-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="febae-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="febae-136">INPUTS</span></span>

## <span data-ttu-id="febae-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="febae-137">OUTPUTS</span></span>

## <span data-ttu-id="febae-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="febae-138">NOTES</span></span>

## <span data-ttu-id="febae-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="febae-139">RELATED LINKS</span></span>
