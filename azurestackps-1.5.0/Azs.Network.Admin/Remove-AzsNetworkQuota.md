---
external help file: Azs.Network.Admin-help.xml
Module Name: Azs.Network.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3f7f40982a4c7d24e02e7e365163cc6250ff8791
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93425757"
---
# <span data-ttu-id="179c1-101">Remove-AzsNetworkQuota</span><span class="sxs-lookup"><span data-stu-id="179c1-101">Remove-AzsNetworkQuota</span></span>

## <span data-ttu-id="179c1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="179c1-102">SYNOPSIS</span></span>
<span data-ttu-id="179c1-103">Excluir uma cota por nome.</span><span class="sxs-lookup"><span data-stu-id="179c1-103">Delete a quota by name.</span></span>

## <span data-ttu-id="179c1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="179c1-104">SYNTAX</span></span>

### <span data-ttu-id="179c1-105">Excluir (padrão)</span><span class="sxs-lookup"><span data-stu-id="179c1-105">Delete (Default)</span></span>
```
Remove-AzsNetworkQuota -Name <String> [-Location <String>] [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="179c1-106">Identificação</span><span class="sxs-lookup"><span data-stu-id="179c1-106">ResourceId</span></span>
```
Remove-AzsNetworkQuota -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="179c1-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="179c1-107">DESCRIPTION</span></span>
<span data-ttu-id="179c1-108">Excluir uma cota por nome.</span><span class="sxs-lookup"><span data-stu-id="179c1-108">Delete a quota by name.</span></span>

## <span data-ttu-id="179c1-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="179c1-109">EXAMPLES</span></span>

### <span data-ttu-id="179c1-110">--------------------------EXEMPLO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="179c1-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsNetworkQuota -Name NetworkQuota1
```

<span data-ttu-id="179c1-111">Remova uma cota de rede por nome.</span><span class="sxs-lookup"><span data-stu-id="179c1-111">Remove a network quota by name.</span></span>

### <span data-ttu-id="179c1-112">--------------------------EXEMPLO 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="179c1-112">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsNetworkQuota -Name NetworkQuota1 | Remove-AzsNetworkQuota
```

<span data-ttu-id="179c1-113">Remova uma cota de rede usando um pipe.</span><span class="sxs-lookup"><span data-stu-id="179c1-113">Remove a network quota using a pipe.</span></span>

### <span data-ttu-id="179c1-114">--------------------------EXEMPLO 3--------------------------</span><span class="sxs-lookup"><span data-stu-id="179c1-114">-------------------------- EXAMPLE 3 --------------------------</span></span>
```
Remove-AzsNetworkQuota -Name NetworkQuota1
```

<span data-ttu-id="179c1-115">Remover uma cota de rede.</span><span class="sxs-lookup"><span data-stu-id="179c1-115">Remove a network quota.</span></span>

## <span data-ttu-id="179c1-116">OS</span><span class="sxs-lookup"><span data-stu-id="179c1-116">PARAMETERS</span></span>

### <span data-ttu-id="179c1-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="179c1-117">-AsJob</span></span>
<span data-ttu-id="179c1-118">Executar assíncrono como um trabalho e retornar o objeto de trabalho.</span><span class="sxs-lookup"><span data-stu-id="179c1-118">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="179c1-119">-Force</span><span class="sxs-lookup"><span data-stu-id="179c1-119">-Force</span></span>
<span data-ttu-id="179c1-120">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="179c1-120">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="179c1-121">-Local</span><span class="sxs-lookup"><span data-stu-id="179c1-121">-Location</span></span>
<span data-ttu-id="179c1-122">Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="179c1-122">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: Delete
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="179c1-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="179c1-123">-Name</span></span>
<span data-ttu-id="179c1-124">Nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="179c1-124">Name of the resource.</span></span>

```yaml
Type: String
Parameter Sets: Delete
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="179c1-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="179c1-125">-ResourceId</span></span>
<span data-ttu-id="179c1-126">A ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="179c1-126">The resource id.</span></span>

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

### <span data-ttu-id="179c1-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="179c1-127">-Confirm</span></span>
<span data-ttu-id="179c1-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="179c1-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="179c1-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="179c1-129">-WhatIf</span></span>
<span data-ttu-id="179c1-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="179c1-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="179c1-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="179c1-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="179c1-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="179c1-132">CommonParameters</span></span>
<span data-ttu-id="179c1-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="179c1-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="179c1-134">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="179c1-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="179c1-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="179c1-135">INPUTS</span></span>

## <span data-ttu-id="179c1-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="179c1-136">OUTPUTS</span></span>

## <span data-ttu-id="179c1-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="179c1-137">NOTES</span></span>

## <span data-ttu-id="179c1-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="179c1-138">RELATED LINKS</span></span>

