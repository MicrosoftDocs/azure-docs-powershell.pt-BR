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
ms.locfileid: "93774315"
---
# <span data-ttu-id="35c4e-101">Resume-AzsUpdateRun</span><span class="sxs-lookup"><span data-stu-id="35c4e-101">Resume-AzsUpdateRun</span></span>

## <span data-ttu-id="35c4e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="35c4e-102">SYNOPSIS</span></span>
<span data-ttu-id="35c4e-103">Retoma uma execução de atualização iniciada anteriormente que falhou.</span><span class="sxs-lookup"><span data-stu-id="35c4e-103">Resumes a previously started update run that failed.</span></span>

## <span data-ttu-id="35c4e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="35c4e-104">SYNTAX</span></span>

### <span data-ttu-id="35c4e-105">UpdateRuns_Rerun (padrão)</span><span class="sxs-lookup"><span data-stu-id="35c4e-105">UpdateRuns_Rerun (Default)</span></span>
```
Resume-AzsUpdateRun -Name <String> [-Location <String>] [-ResourceGroupName <String>] -UpdateName <String>
 [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="35c4e-106">Identificação</span><span class="sxs-lookup"><span data-stu-id="35c4e-106">ResourceId</span></span>
```
Resume-AzsUpdateRun [-AsJob] -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="35c4e-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="35c4e-107">DESCRIPTION</span></span>
<span data-ttu-id="35c4e-108">Retoma uma execução de atualização iniciada anteriormente que falhou.</span><span class="sxs-lookup"><span data-stu-id="35c4e-108">Resumes a previously started update run that failed.</span></span> <span data-ttu-id="35c4e-109">Execuções de atualização retomadas serão retomadas no ponto em que houve falha na última vez.</span><span class="sxs-lookup"><span data-stu-id="35c4e-109">Resumeed update runs will resume at the point they last failed.</span></span>

## <span data-ttu-id="35c4e-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="35c4e-110">EXAMPLES</span></span>

### <span data-ttu-id="35c4e-111">--------------------------EXEMPLO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="35c4e-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsUpdateRun -Name 5173e9f4-3040-494f-b7a7-738a6331d55c -UpdateName Microsoft1.0.180305.1 | Resume-AzsUpdateRun
```

<span data-ttu-id="35c4e-112">Retoma uma execução de atualização iniciada anteriormente que falhou.</span><span class="sxs-lookup"><span data-stu-id="35c4e-112">Resumes a previously started update run that failed.</span></span>

## <span data-ttu-id="35c4e-113">OS</span><span class="sxs-lookup"><span data-stu-id="35c4e-113">PARAMETERS</span></span>

### <span data-ttu-id="35c4e-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="35c4e-114">-AsJob</span></span>
<span data-ttu-id="35c4e-115">Executar assíncrono como um trabalho e retornar o objeto de trabalho.</span><span class="sxs-lookup"><span data-stu-id="35c4e-115">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="35c4e-116">-Force</span><span class="sxs-lookup"><span data-stu-id="35c4e-116">-Force</span></span>
<span data-ttu-id="35c4e-117">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="35c4e-117">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="35c4e-118">-Local</span><span class="sxs-lookup"><span data-stu-id="35c4e-118">-Location</span></span>
<span data-ttu-id="35c4e-119">O nome do local de atualização.</span><span class="sxs-lookup"><span data-stu-id="35c4e-119">The name of the update location.</span></span>

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

### <span data-ttu-id="35c4e-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="35c4e-120">-Name</span></span>
<span data-ttu-id="35c4e-121">Identificador de execução de atualização.</span><span class="sxs-lookup"><span data-stu-id="35c4e-121">Update run identifier.</span></span>

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

### <span data-ttu-id="35c4e-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35c4e-122">-ResourceGroupName</span></span>
<span data-ttu-id="35c4e-123">O grupo de recursos no qual o recurso está localizado.</span><span class="sxs-lookup"><span data-stu-id="35c4e-123">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="35c4e-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="35c4e-124">-ResourceId</span></span>
<span data-ttu-id="35c4e-125">A ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="35c4e-125">The resource id.</span></span>

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

### <span data-ttu-id="35c4e-126">-Updatename</span><span class="sxs-lookup"><span data-stu-id="35c4e-126">-UpdateName</span></span>
<span data-ttu-id="35c4e-127">Nome para exibição da atualização.</span><span class="sxs-lookup"><span data-stu-id="35c4e-127">Display name of the update.</span></span>

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

### <span data-ttu-id="35c4e-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="35c4e-128">-Confirm</span></span>
<span data-ttu-id="35c4e-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="35c4e-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="35c4e-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="35c4e-130">-WhatIf</span></span>
<span data-ttu-id="35c4e-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="35c4e-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="35c4e-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="35c4e-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="35c4e-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35c4e-133">CommonParameters</span></span>
<span data-ttu-id="35c4e-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35c4e-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35c4e-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="35c4e-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35c4e-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="35c4e-136">INPUTS</span></span>

## <span data-ttu-id="35c4e-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="35c4e-137">OUTPUTS</span></span>

## <span data-ttu-id="35c4e-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="35c4e-138">NOTES</span></span>

## <span data-ttu-id="35c4e-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="35c4e-139">RELATED LINKS</span></span>

