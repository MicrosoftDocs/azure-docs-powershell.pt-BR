---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: f6e7801a2188fe80577bc6cef9315069b0207f91
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93425959"
---
# <span data-ttu-id="402a7-101">Restart-AzsInfrastructureRoleInstance</span><span class="sxs-lookup"><span data-stu-id="402a7-101">Restart-AzsInfrastructureRoleInstance</span></span>

## <span data-ttu-id="402a7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="402a7-102">SYNOPSIS</span></span>
<span data-ttu-id="402a7-103">Reinicie uma instância de função de infraestrutura.</span><span class="sxs-lookup"><span data-stu-id="402a7-103">Reboot an infrastructure role instance.</span></span>

## <span data-ttu-id="402a7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="402a7-104">SYNTAX</span></span>

### <span data-ttu-id="402a7-105">Reiniciar (padrão)</span><span class="sxs-lookup"><span data-stu-id="402a7-105">Restart (Default)</span></span>
```
Restart-AzsInfrastructureRoleInstance -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="402a7-106">Identificação</span><span class="sxs-lookup"><span data-stu-id="402a7-106">ResourceId</span></span>
```
Restart-AzsInfrastructureRoleInstance -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="402a7-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="402a7-107">DESCRIPTION</span></span>
<span data-ttu-id="402a7-108">Reinicie uma instância de função de infraestrutura.</span><span class="sxs-lookup"><span data-stu-id="402a7-108">Reboot an infrastructure role instance.</span></span>

## <span data-ttu-id="402a7-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="402a7-109">EXAMPLES</span></span>

### <span data-ttu-id="402a7-110">--------------------------EXEMPLO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="402a7-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Restart-AzsInfrastructureRoleInstance -Name "AzS-ACS01"
```

<span data-ttu-id="402a7-111">Reinicie uma instância de função de infraestrutura.</span><span class="sxs-lookup"><span data-stu-id="402a7-111">Reboot an infrastructure role instance.</span></span>

## <span data-ttu-id="402a7-112">OS</span><span class="sxs-lookup"><span data-stu-id="402a7-112">PARAMETERS</span></span>

### <span data-ttu-id="402a7-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="402a7-113">-AsJob</span></span>
<span data-ttu-id="402a7-114">Executar assíncrono como um trabalho e retornar o objeto de trabalho.</span><span class="sxs-lookup"><span data-stu-id="402a7-114">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="402a7-115">-Force</span><span class="sxs-lookup"><span data-stu-id="402a7-115">-Force</span></span>
<span data-ttu-id="402a7-116">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="402a7-116">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="402a7-117">-Local</span><span class="sxs-lookup"><span data-stu-id="402a7-117">-Location</span></span>
<span data-ttu-id="402a7-118">Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="402a7-118">Location of the resource.</span></span>

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

### <span data-ttu-id="402a7-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="402a7-119">-Name</span></span>
<span data-ttu-id="402a7-120">Nome de uma instância de função de infraestrutura.</span><span class="sxs-lookup"><span data-stu-id="402a7-120">Name of an infrastructure role instance.</span></span>

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

### <span data-ttu-id="402a7-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="402a7-121">-ResourceGroupName</span></span>
<span data-ttu-id="402a7-122">Grupo de recursos no qual o provedor de recursos foi registrado.</span><span class="sxs-lookup"><span data-stu-id="402a7-122">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="402a7-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="402a7-123">-ResourceId</span></span>
<span data-ttu-id="402a7-124">ID do recurso de instância da infraestrutura.</span><span class="sxs-lookup"><span data-stu-id="402a7-124">Infrastructure role instance resource ID.</span></span>

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

### <span data-ttu-id="402a7-125">-Confirme</span><span class="sxs-lookup"><span data-stu-id="402a7-125">-Confirm</span></span>
<span data-ttu-id="402a7-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="402a7-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="402a7-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="402a7-127">-WhatIf</span></span>
<span data-ttu-id="402a7-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="402a7-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="402a7-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="402a7-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="402a7-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="402a7-130">CommonParameters</span></span>
<span data-ttu-id="402a7-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="402a7-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="402a7-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="402a7-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="402a7-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="402a7-133">INPUTS</span></span>

## <span data-ttu-id="402a7-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="402a7-134">OUTPUTS</span></span>

## <span data-ttu-id="402a7-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="402a7-135">NOTES</span></span>

## <span data-ttu-id="402a7-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="402a7-136">RELATED LINKS</span></span>

