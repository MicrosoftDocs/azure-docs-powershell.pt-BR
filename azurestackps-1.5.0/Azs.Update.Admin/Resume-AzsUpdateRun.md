---
external help file: Azs.Update.Admin-help.xml
Module Name: Azs.Update.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 19c8f8fce7c3711c5002f9588900e6bdf8efcbb0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93601702"
---
# <span data-ttu-id="eed0c-101">Resume-AzsUpdateRun</span><span class="sxs-lookup"><span data-stu-id="eed0c-101">Resume-AzsUpdateRun</span></span>

## <span data-ttu-id="eed0c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="eed0c-102">SYNOPSIS</span></span>
<span data-ttu-id="eed0c-103">Retoma uma execução de atualização iniciada anteriormente que falhou.</span><span class="sxs-lookup"><span data-stu-id="eed0c-103">Resumes a previously started update run that failed.</span></span>

## <span data-ttu-id="eed0c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="eed0c-104">SYNTAX</span></span>

### <span data-ttu-id="eed0c-105">UpdateRuns_Rerun (padrão)</span><span class="sxs-lookup"><span data-stu-id="eed0c-105">UpdateRuns_Rerun (Default)</span></span>
```
Resume-AzsUpdateRun -Name <String> [-Location <String>] [-ResourceGroupName <String>] -UpdateName <String>
 [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eed0c-106">Identificação</span><span class="sxs-lookup"><span data-stu-id="eed0c-106">ResourceId</span></span>
```
Resume-AzsUpdateRun [-AsJob] -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eed0c-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="eed0c-107">DESCRIPTION</span></span>
<span data-ttu-id="eed0c-108">Retoma uma execução de atualização iniciada anteriormente que falhou.</span><span class="sxs-lookup"><span data-stu-id="eed0c-108">Resumes a previously started update run that failed.</span></span> <span data-ttu-id="eed0c-109">Execuções de atualização retomadas serão retomadas no ponto em que houve falha na última vez.</span><span class="sxs-lookup"><span data-stu-id="eed0c-109">Resumeed update runs will resume at the point they last failed.</span></span>

## <span data-ttu-id="eed0c-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="eed0c-110">EXAMPLES</span></span>

### <span data-ttu-id="eed0c-111">--------------------------EXEMPLO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="eed0c-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsUpdateRun -Name 5173e9f4-3040-494f-b7a7-738a6331d55c -UpdateName Microsoft1.0.180305.1 | Resume-AzsUpdateRun
```

<span data-ttu-id="eed0c-112">Retoma uma execução de atualização iniciada anteriormente que falhou.</span><span class="sxs-lookup"><span data-stu-id="eed0c-112">Resumes a previously started update run that failed.</span></span>

## <span data-ttu-id="eed0c-113">OS</span><span class="sxs-lookup"><span data-stu-id="eed0c-113">PARAMETERS</span></span>

### <span data-ttu-id="eed0c-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="eed0c-114">-AsJob</span></span>
<span data-ttu-id="eed0c-115">Executar assíncrono como um trabalho e retornar o objeto de trabalho.</span><span class="sxs-lookup"><span data-stu-id="eed0c-115">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="eed0c-116">-Force</span><span class="sxs-lookup"><span data-stu-id="eed0c-116">-Force</span></span>
<span data-ttu-id="eed0c-117">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="eed0c-117">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="eed0c-118">-Local</span><span class="sxs-lookup"><span data-stu-id="eed0c-118">-Location</span></span>
<span data-ttu-id="eed0c-119">O nome do local de atualização.</span><span class="sxs-lookup"><span data-stu-id="eed0c-119">The name of the update location.</span></span>

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

### <span data-ttu-id="eed0c-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="eed0c-120">-Name</span></span>
<span data-ttu-id="eed0c-121">Identificador de execução de atualização.</span><span class="sxs-lookup"><span data-stu-id="eed0c-121">Update run identifier.</span></span>

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

### <span data-ttu-id="eed0c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eed0c-122">-ResourceGroupName</span></span>
<span data-ttu-id="eed0c-123">O grupo de recursos no qual o recurso está localizado.</span><span class="sxs-lookup"><span data-stu-id="eed0c-123">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="eed0c-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="eed0c-124">-ResourceId</span></span>
<span data-ttu-id="eed0c-125">A ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="eed0c-125">The resource id.</span></span>

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

### <span data-ttu-id="eed0c-126">-Updatename</span><span class="sxs-lookup"><span data-stu-id="eed0c-126">-UpdateName</span></span>
<span data-ttu-id="eed0c-127">Nome para exibição da atualização.</span><span class="sxs-lookup"><span data-stu-id="eed0c-127">Display name of the update.</span></span>

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

### <span data-ttu-id="eed0c-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="eed0c-128">-Confirm</span></span>
<span data-ttu-id="eed0c-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eed0c-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eed0c-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eed0c-130">-WhatIf</span></span>
<span data-ttu-id="eed0c-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="eed0c-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eed0c-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="eed0c-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eed0c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eed0c-133">CommonParameters</span></span>
<span data-ttu-id="eed0c-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eed0c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eed0c-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eed0c-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eed0c-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="eed0c-136">INPUTS</span></span>

## <span data-ttu-id="eed0c-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="eed0c-137">OUTPUTS</span></span>

## <span data-ttu-id="eed0c-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="eed0c-138">NOTES</span></span>

## <span data-ttu-id="eed0c-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="eed0c-139">RELATED LINKS</span></span>

