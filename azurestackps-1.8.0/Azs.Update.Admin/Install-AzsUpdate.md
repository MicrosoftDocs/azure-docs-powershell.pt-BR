---
external help file: Azs.Update.Admin-help.xml
Module Name: Azs.Update.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: ab432625ab6af4a8fbd23895cb82e1d9f83954c8
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2020
ms.locfileid: "93774559"
---
# <span data-ttu-id="3fef3-101">Install-AzsUpdate</span><span class="sxs-lookup"><span data-stu-id="3fef3-101">Install-AzsUpdate</span></span>

## <span data-ttu-id="3fef3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3fef3-102">SYNOPSIS</span></span>
<span data-ttu-id="3fef3-103">Aplicar uma atualização específica em um local de atualização.</span><span class="sxs-lookup"><span data-stu-id="3fef3-103">Apply a specific update at an update location.</span></span>

## <span data-ttu-id="3fef3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3fef3-104">SYNTAX</span></span>

### <span data-ttu-id="3fef3-105">Aplicar (padrão)</span><span class="sxs-lookup"><span data-stu-id="3fef3-105">Apply (Default)</span></span>
```
Install-AzsUpdate -Name <String> [-ResourceGroupName <String>] [-Location <String>] [-AsJob] [-Force] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3fef3-106">Identificação</span><span class="sxs-lookup"><span data-stu-id="3fef3-106">ResourceId</span></span>
```
Install-AzsUpdate [-AsJob] -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3fef3-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3fef3-107">DESCRIPTION</span></span>
<span data-ttu-id="3fef3-108">Aplicar uma atualização específica em um local de atualização.</span><span class="sxs-lookup"><span data-stu-id="3fef3-108">Apply a specific update at an update location.</span></span> <span data-ttu-id="3fef3-109">Após a chamada, Get-AzsUpdateRun pode ser usado para modificar o progresso da atualização.</span><span class="sxs-lookup"><span data-stu-id="3fef3-109">After invoked, Get-AzsUpdateRun may be used to modify the progress of the update.</span></span>

## <span data-ttu-id="3fef3-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3fef3-110">EXAMPLES</span></span>

### <span data-ttu-id="3fef3-111">EXEMPLO 1</span><span class="sxs-lookup"><span data-stu-id="3fef3-111">EXAMPLE 1</span></span>
```
Get-AzsUpdate -Name Microsoft1.0.180305.1 | Install-AzsUpdate
```

<span data-ttu-id="3fef3-112">Aplicar uma atualização específica em um local de atualização.</span><span class="sxs-lookup"><span data-stu-id="3fef3-112">Apply a specific update at an update location.</span></span>

## <span data-ttu-id="3fef3-113">OS</span><span class="sxs-lookup"><span data-stu-id="3fef3-113">PARAMETERS</span></span>

### <span data-ttu-id="3fef3-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="3fef3-114">-Name</span></span>
<span data-ttu-id="3fef3-115">Nome da atualização.</span><span class="sxs-lookup"><span data-stu-id="3fef3-115">Name of the update.</span></span>

```yaml
Type: String
Parameter Sets: Apply
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fef3-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3fef3-116">-ResourceGroupName</span></span>
<span data-ttu-id="3fef3-117">O grupo de recursos no qual o recurso está localizado.</span><span class="sxs-lookup"><span data-stu-id="3fef3-117">The resource group the resource is located under.</span></span>

```yaml
Type: String
Parameter Sets: Apply
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fef3-118">-Local</span><span class="sxs-lookup"><span data-stu-id="3fef3-118">-Location</span></span>
<span data-ttu-id="3fef3-119">O nome do local de atualização.</span><span class="sxs-lookup"><span data-stu-id="3fef3-119">The name of the update location.</span></span>

```yaml
Type: String
Parameter Sets: Apply
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fef3-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3fef3-120">-AsJob</span></span>
<span data-ttu-id="3fef3-121">Executar assíncrono como um trabalho e retornar o objeto de trabalho.</span><span class="sxs-lookup"><span data-stu-id="3fef3-121">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="3fef3-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3fef3-122">-ResourceId</span></span>
<span data-ttu-id="3fef3-123">A ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="3fef3-123">The resource id.</span></span>

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

### <span data-ttu-id="3fef3-124">-Force</span><span class="sxs-lookup"><span data-stu-id="3fef3-124">-Force</span></span>
<span data-ttu-id="3fef3-125">Sinalizador para remover o item sem confirmação.</span><span class="sxs-lookup"><span data-stu-id="3fef3-125">Flag to remove the item without confirmation.</span></span>

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

### <span data-ttu-id="3fef3-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3fef3-126">-WhatIf</span></span>
<span data-ttu-id="3fef3-127">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="3fef3-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3fef3-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3fef3-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3fef3-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="3fef3-129">-Confirm</span></span>
<span data-ttu-id="3fef3-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3fef3-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3fef3-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3fef3-131">CommonParameters</span></span>
<span data-ttu-id="3fef3-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3fef3-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3fef3-133">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3fef3-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3fef3-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3fef3-134">INPUTS</span></span>

## <span data-ttu-id="3fef3-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3fef3-135">OUTPUTS</span></span>

### <span data-ttu-id="3fef3-136">Microsoft. AzureStack. Management. Update. admin. Models. Update</span><span class="sxs-lookup"><span data-stu-id="3fef3-136">Microsoft.AzureStack.Management.Update.Admin.Models.Update</span></span>

## <span data-ttu-id="3fef3-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3fef3-137">NOTES</span></span>

## <span data-ttu-id="3fef3-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3fef3-138">RELATED LINKS</span></span>
