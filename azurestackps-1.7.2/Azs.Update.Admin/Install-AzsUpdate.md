---
external help file: Azs.Update.Admin-help.xml
Module Name: Azs.Update.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4406dc4cadecd1945e82b8a90e9937df2183b4da
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93595630"
---
# <span data-ttu-id="9a5c7-101">Install-AzsUpdate</span><span class="sxs-lookup"><span data-stu-id="9a5c7-101">Install-AzsUpdate</span></span>

## <span data-ttu-id="9a5c7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9a5c7-102">SYNOPSIS</span></span>
<span data-ttu-id="9a5c7-103">Aplicar uma atualização específica em um local de atualização.</span><span class="sxs-lookup"><span data-stu-id="9a5c7-103">Apply a specific update at an update location.</span></span>

## <span data-ttu-id="9a5c7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9a5c7-104">SYNTAX</span></span>

### <span data-ttu-id="9a5c7-105">Aplicar (padrão)</span><span class="sxs-lookup"><span data-stu-id="9a5c7-105">Apply (Default)</span></span>
```
Install-AzsUpdate -Name <String> [-ResourceGroupName <String>] [-Location <String>] [-AsJob] [-Force] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9a5c7-106">Identificação</span><span class="sxs-lookup"><span data-stu-id="9a5c7-106">ResourceId</span></span>
```
Install-AzsUpdate [-AsJob] -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9a5c7-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9a5c7-107">DESCRIPTION</span></span>
<span data-ttu-id="9a5c7-108">Aplicar uma atualização específica em um local de atualização.</span><span class="sxs-lookup"><span data-stu-id="9a5c7-108">Apply a specific update at an update location.</span></span> <span data-ttu-id="9a5c7-109">Após a chamada, Get-AzsUpdateRun pode ser usado para modificar o progresso da atualização.</span><span class="sxs-lookup"><span data-stu-id="9a5c7-109">After invoked, Get-AzsUpdateRun may be used to modify the progress of the update.</span></span>

## <span data-ttu-id="9a5c7-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9a5c7-110">EXAMPLES</span></span>

### <span data-ttu-id="9a5c7-111">--------------------------EXEMPLO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="9a5c7-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsUpdate -Name Microsoft1.0.180305.1 | Install-AzsUpdate
```

<span data-ttu-id="9a5c7-112">Aplicar uma atualização específica em um local de atualização.</span><span class="sxs-lookup"><span data-stu-id="9a5c7-112">Apply a specific update at an update location.</span></span>

## <span data-ttu-id="9a5c7-113">OS</span><span class="sxs-lookup"><span data-stu-id="9a5c7-113">PARAMETERS</span></span>

### <span data-ttu-id="9a5c7-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9a5c7-114">-AsJob</span></span>
<span data-ttu-id="9a5c7-115">Executar assíncrono como um trabalho e retornar o objeto de trabalho.</span><span class="sxs-lookup"><span data-stu-id="9a5c7-115">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="9a5c7-116">-Force</span><span class="sxs-lookup"><span data-stu-id="9a5c7-116">-Force</span></span>
<span data-ttu-id="9a5c7-117">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="9a5c7-117">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="9a5c7-118">-Local</span><span class="sxs-lookup"><span data-stu-id="9a5c7-118">-Location</span></span>
<span data-ttu-id="9a5c7-119">O nome do local de atualização.</span><span class="sxs-lookup"><span data-stu-id="9a5c7-119">The name of the update location.</span></span>

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

### <span data-ttu-id="9a5c7-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="9a5c7-120">-Name</span></span>
<span data-ttu-id="9a5c7-121">Nome da atualização.</span><span class="sxs-lookup"><span data-stu-id="9a5c7-121">Name of the update.</span></span>

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

### <span data-ttu-id="9a5c7-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9a5c7-122">-ResourceGroupName</span></span>
<span data-ttu-id="9a5c7-123">O grupo de recursos no qual o recurso está localizado.</span><span class="sxs-lookup"><span data-stu-id="9a5c7-123">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="9a5c7-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9a5c7-124">-ResourceId</span></span>
<span data-ttu-id="9a5c7-125">A ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="9a5c7-125">The resource id.</span></span>

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

### <span data-ttu-id="9a5c7-126">-Confirme</span><span class="sxs-lookup"><span data-stu-id="9a5c7-126">-Confirm</span></span>
<span data-ttu-id="9a5c7-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9a5c7-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9a5c7-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9a5c7-128">-WhatIf</span></span>
<span data-ttu-id="9a5c7-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="9a5c7-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9a5c7-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9a5c7-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9a5c7-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a5c7-131">CommonParameters</span></span>
<span data-ttu-id="9a5c7-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9a5c7-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a5c7-133">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9a5c7-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a5c7-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9a5c7-134">INPUTS</span></span>

## <span data-ttu-id="9a5c7-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9a5c7-135">OUTPUTS</span></span>

### <span data-ttu-id="9a5c7-136">Microsoft. AzureStack. Management. Update. admin. Models. Update</span><span class="sxs-lookup"><span data-stu-id="9a5c7-136">Microsoft.AzureStack.Management.Update.Admin.Models.Update</span></span>

## <span data-ttu-id="9a5c7-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9a5c7-137">NOTES</span></span>

## <span data-ttu-id="9a5c7-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9a5c7-138">RELATED LINKS</span></span>

