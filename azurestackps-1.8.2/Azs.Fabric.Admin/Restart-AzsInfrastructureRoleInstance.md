---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 03dfddb3ec666df5096184c5e00692862e091626
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/08/2020
ms.locfileid: "93946680"
---
# <span data-ttu-id="8b81b-101">Restart-AzsInfrastructureRoleInstance</span><span class="sxs-lookup"><span data-stu-id="8b81b-101">Restart-AzsInfrastructureRoleInstance</span></span>

## <span data-ttu-id="8b81b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8b81b-102">SYNOPSIS</span></span>
<span data-ttu-id="8b81b-103">Reinicie uma instância de função de infraestrutura.</span><span class="sxs-lookup"><span data-stu-id="8b81b-103">Reboot an infrastructure role instance.</span></span>

## <span data-ttu-id="8b81b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8b81b-104">SYNTAX</span></span>

### <span data-ttu-id="8b81b-105">Reiniciar (padrão)</span><span class="sxs-lookup"><span data-stu-id="8b81b-105">Restart (Default)</span></span>
```
Restart-AzsInfrastructureRoleInstance -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8b81b-106">Identificação</span><span class="sxs-lookup"><span data-stu-id="8b81b-106">ResourceId</span></span>
```
Restart-AzsInfrastructureRoleInstance -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8b81b-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8b81b-107">DESCRIPTION</span></span>
<span data-ttu-id="8b81b-108">Reinicie uma instância de função de infraestrutura.</span><span class="sxs-lookup"><span data-stu-id="8b81b-108">Reboot an infrastructure role instance.</span></span>

## <span data-ttu-id="8b81b-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8b81b-109">EXAMPLES</span></span>

### <span data-ttu-id="8b81b-110">EXEMPLO 1</span><span class="sxs-lookup"><span data-stu-id="8b81b-110">EXAMPLE 1</span></span>
```
Restart-AzsInfrastructureRoleInstance -Name "AzS-ACS01"
```

<span data-ttu-id="8b81b-111">Reinicie uma instância de função de infraestrutura.</span><span class="sxs-lookup"><span data-stu-id="8b81b-111">Reboot an infrastructure role instance.</span></span>

## <span data-ttu-id="8b81b-112">OS</span><span class="sxs-lookup"><span data-stu-id="8b81b-112">PARAMETERS</span></span>

### <span data-ttu-id="8b81b-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="8b81b-113">-Name</span></span>
<span data-ttu-id="8b81b-114">Nome de uma instância de função de infraestrutura.</span><span class="sxs-lookup"><span data-stu-id="8b81b-114">Name of an infrastructure role instance.</span></span>

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

### <span data-ttu-id="8b81b-115">-Local</span><span class="sxs-lookup"><span data-stu-id="8b81b-115">-Location</span></span>
<span data-ttu-id="8b81b-116">Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="8b81b-116">Location of the resource.</span></span>

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

### <span data-ttu-id="8b81b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b81b-117">-ResourceGroupName</span></span>
<span data-ttu-id="8b81b-118">Grupo de recursos no qual o provedor de recursos foi registrado.</span><span class="sxs-lookup"><span data-stu-id="8b81b-118">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="8b81b-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8b81b-119">-ResourceId</span></span>
<span data-ttu-id="8b81b-120">ID do recurso de instância da infraestrutura.</span><span class="sxs-lookup"><span data-stu-id="8b81b-120">Infrastructure role instance resource ID.</span></span>

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

### <span data-ttu-id="8b81b-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8b81b-121">-AsJob</span></span>
<span data-ttu-id="8b81b-122">Executar assíncrono como um trabalho e retornar o objeto de trabalho.</span><span class="sxs-lookup"><span data-stu-id="8b81b-122">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="8b81b-123">-Force</span><span class="sxs-lookup"><span data-stu-id="8b81b-123">-Force</span></span>
<span data-ttu-id="8b81b-124">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="8b81b-124">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="8b81b-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8b81b-125">-WhatIf</span></span>
<span data-ttu-id="8b81b-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="8b81b-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8b81b-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8b81b-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8b81b-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="8b81b-128">-Confirm</span></span>
<span data-ttu-id="8b81b-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8b81b-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8b81b-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b81b-130">CommonParameters</span></span>
<span data-ttu-id="8b81b-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b81b-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b81b-132">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8b81b-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b81b-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8b81b-133">INPUTS</span></span>

## <span data-ttu-id="8b81b-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8b81b-134">OUTPUTS</span></span>

## <span data-ttu-id="8b81b-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8b81b-135">NOTES</span></span>

## <span data-ttu-id="8b81b-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8b81b-136">RELATED LINKS</span></span>
