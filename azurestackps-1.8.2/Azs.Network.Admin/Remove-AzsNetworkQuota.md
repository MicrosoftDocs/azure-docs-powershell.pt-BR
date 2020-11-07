---
external help file: Azs.Network.Admin-help.xml
Module Name: Azs.Network.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 94609250696a99a337153e9e0d3a1d092e380c40
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/08/2020
ms.locfileid: "93947170"
---
# <span data-ttu-id="2c09e-101">Remove-AzsNetworkQuota</span><span class="sxs-lookup"><span data-stu-id="2c09e-101">Remove-AzsNetworkQuota</span></span>

## <span data-ttu-id="2c09e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2c09e-102">SYNOPSIS</span></span>
<span data-ttu-id="2c09e-103">Excluir uma cota por nome.</span><span class="sxs-lookup"><span data-stu-id="2c09e-103">Delete a quota by name.</span></span>

## <span data-ttu-id="2c09e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2c09e-104">SYNTAX</span></span>

### <span data-ttu-id="2c09e-105">Excluir (padrão)</span><span class="sxs-lookup"><span data-stu-id="2c09e-105">Delete (Default)</span></span>
```
Remove-AzsNetworkQuota -Name <String> [-Location <String>] [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2c09e-106">Identificação</span><span class="sxs-lookup"><span data-stu-id="2c09e-106">ResourceId</span></span>
```
Remove-AzsNetworkQuota -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2c09e-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2c09e-107">DESCRIPTION</span></span>
<span data-ttu-id="2c09e-108">Excluir uma cota por nome.</span><span class="sxs-lookup"><span data-stu-id="2c09e-108">Delete a quota by name.</span></span>

## <span data-ttu-id="2c09e-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2c09e-109">EXAMPLES</span></span>

### <span data-ttu-id="2c09e-110">EXEMPLO 1</span><span class="sxs-lookup"><span data-stu-id="2c09e-110">EXAMPLE 1</span></span>
```
Remove-AzsNetworkQuota -Name NetworkQuota1
```

<span data-ttu-id="2c09e-111">Remova uma cota de rede por nome.</span><span class="sxs-lookup"><span data-stu-id="2c09e-111">Remove a network quota by name.</span></span>

### <span data-ttu-id="2c09e-112">EXEMPLO 2</span><span class="sxs-lookup"><span data-stu-id="2c09e-112">EXAMPLE 2</span></span>
```
Get-AzsNetworkQuota -Name NetworkQuota1 | Remove-AzsNetworkQuota
```

<span data-ttu-id="2c09e-113">Remova uma cota de rede usando um pipe.</span><span class="sxs-lookup"><span data-stu-id="2c09e-113">Remove a network quota using a pipe.</span></span>

### <span data-ttu-id="2c09e-114">EXEMPLO 3</span><span class="sxs-lookup"><span data-stu-id="2c09e-114">EXAMPLE 3</span></span>
```
Remove-AzsNetworkQuota -Name NetworkQuota1
```

<span data-ttu-id="2c09e-115">Remover uma cota de rede.</span><span class="sxs-lookup"><span data-stu-id="2c09e-115">Remove a network quota.</span></span>

## <span data-ttu-id="2c09e-116">OS</span><span class="sxs-lookup"><span data-stu-id="2c09e-116">PARAMETERS</span></span>

### <span data-ttu-id="2c09e-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="2c09e-117">-Name</span></span>
<span data-ttu-id="2c09e-118">Nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="2c09e-118">Name of the resource.</span></span>

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

### <span data-ttu-id="2c09e-119">-Local</span><span class="sxs-lookup"><span data-stu-id="2c09e-119">-Location</span></span>
<span data-ttu-id="2c09e-120">Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="2c09e-120">Location of the resource.</span></span>

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

### <span data-ttu-id="2c09e-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2c09e-121">-ResourceId</span></span>
<span data-ttu-id="2c09e-122">A ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="2c09e-122">The resource id.</span></span>

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

### <span data-ttu-id="2c09e-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2c09e-123">-AsJob</span></span>
<span data-ttu-id="2c09e-124">Executar assíncrono como um trabalho e retornar o objeto de trabalho.</span><span class="sxs-lookup"><span data-stu-id="2c09e-124">Run asynchronous as a job and return the job object.</span></span>


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

### <span data-ttu-id="2c09e-125">-Force</span><span class="sxs-lookup"><span data-stu-id="2c09e-125">-Force</span></span>
<span data-ttu-id="2c09e-126">Parâmetro de opção para não pedir confirmação.</span><span class="sxs-lookup"><span data-stu-id="2c09e-126">Switch parameter for not asking confirmation.</span></span>

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

### <span data-ttu-id="2c09e-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2c09e-127">-WhatIf</span></span>
<span data-ttu-id="2c09e-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="2c09e-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2c09e-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2c09e-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2c09e-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="2c09e-130">-Confirm</span></span>
<span data-ttu-id="2c09e-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2c09e-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2c09e-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c09e-132">CommonParameters</span></span>
<span data-ttu-id="2c09e-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c09e-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c09e-134">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2c09e-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c09e-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2c09e-135">INPUTS</span></span>

## <span data-ttu-id="2c09e-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2c09e-136">OUTPUTS</span></span>

## <span data-ttu-id="2c09e-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2c09e-137">NOTES</span></span>

## <span data-ttu-id="2c09e-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2c09e-138">RELATED LINKS</span></span>
