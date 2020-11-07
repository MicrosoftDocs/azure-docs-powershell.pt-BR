---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 348582b008d50371bc937961cd76edbf1ba13762
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93774458"
---
# <span data-ttu-id="f1fcf-101">Suspend-AzsInfrastructureRoleInstance</span><span class="sxs-lookup"><span data-stu-id="f1fcf-101">Suspend-AzsInfrastructureRoleInstance</span></span>

## <span data-ttu-id="f1fcf-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f1fcf-102">SYNOPSIS</span></span>
<span data-ttu-id="f1fcf-103">Desligar uma instância de função de infraestrutura.</span><span class="sxs-lookup"><span data-stu-id="f1fcf-103">Shut down an infrastructure role instance.</span></span>

## <span data-ttu-id="f1fcf-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f1fcf-104">SYNTAX</span></span>

### <span data-ttu-id="f1fcf-105">Shutdown (padrão)</span><span class="sxs-lookup"><span data-stu-id="f1fcf-105">Shutdown (Default)</span></span>
```
Suspend-AzsInfrastructureRoleInstance -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f1fcf-106">Identificação</span><span class="sxs-lookup"><span data-stu-id="f1fcf-106">ResourceId</span></span>
```
Suspend-AzsInfrastructureRoleInstance -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f1fcf-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f1fcf-107">DESCRIPTION</span></span>
<span data-ttu-id="f1fcf-108">Desligar uma instância de função de infraestrutura.</span><span class="sxs-lookup"><span data-stu-id="f1fcf-108">Shut down an infrastructure role instance.</span></span>

## <span data-ttu-id="f1fcf-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f1fcf-109">EXAMPLES</span></span>

### <span data-ttu-id="f1fcf-110">--------------------------EXEMPLO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="f1fcf-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Suspend-AzsInfrastructureRoleInstance -Name "AzS-ACS01"
```

<span data-ttu-id="f1fcf-111">Desligar uma instância de função de infraestrutura.</span><span class="sxs-lookup"><span data-stu-id="f1fcf-111">Shut down an infrastructure role instance.</span></span>
<span data-ttu-id="f1fcf-112">Na falha, uma exceção é lançada.</span><span class="sxs-lookup"><span data-stu-id="f1fcf-112">On failure an exception is thrown.</span></span>

## <span data-ttu-id="f1fcf-113">OS</span><span class="sxs-lookup"><span data-stu-id="f1fcf-113">PARAMETERS</span></span>

### <span data-ttu-id="f1fcf-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f1fcf-114">-AsJob</span></span>
<span data-ttu-id="f1fcf-115">Executar assíncrono como um trabalho e retornar o objeto de trabalho.</span><span class="sxs-lookup"><span data-stu-id="f1fcf-115">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="f1fcf-116">-Force</span><span class="sxs-lookup"><span data-stu-id="f1fcf-116">-Force</span></span>
<span data-ttu-id="f1fcf-117">Não pedir confirmação</span><span class="sxs-lookup"><span data-stu-id="f1fcf-117">Don't ask for confirmation</span></span>

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

### <span data-ttu-id="f1fcf-118">-Local</span><span class="sxs-lookup"><span data-stu-id="f1fcf-118">-Location</span></span>
<span data-ttu-id="f1fcf-119">Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="f1fcf-119">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: Shutdown
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1fcf-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="f1fcf-120">-Name</span></span>
<span data-ttu-id="f1fcf-121">Nome de uma instância de função de infraestrutura.</span><span class="sxs-lookup"><span data-stu-id="f1fcf-121">Name of an infrastructure role instance.</span></span>

```yaml
Type: String
Parameter Sets: Shutdown
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1fcf-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1fcf-122">-ResourceGroupName</span></span>
<span data-ttu-id="f1fcf-123">Grupo de recursos no qual o provedor de recursos foi registrado.</span><span class="sxs-lookup"><span data-stu-id="f1fcf-123">Resource group in which the resource provider has been registered.</span></span>

```yaml
Type: String
Parameter Sets: Shutdown
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1fcf-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f1fcf-124">-ResourceId</span></span>
<span data-ttu-id="f1fcf-125">ID do recurso de instância da infraestrutura.</span><span class="sxs-lookup"><span data-stu-id="f1fcf-125">Infrastructure role instance resource ID.</span></span>

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

### <span data-ttu-id="f1fcf-126">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f1fcf-126">-Confirm</span></span>
<span data-ttu-id="f1fcf-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f1fcf-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f1fcf-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f1fcf-128">-WhatIf</span></span>
<span data-ttu-id="f1fcf-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f1fcf-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f1fcf-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f1fcf-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f1fcf-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1fcf-131">CommonParameters</span></span>
<span data-ttu-id="f1fcf-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1fcf-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1fcf-133">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f1fcf-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1fcf-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f1fcf-134">INPUTS</span></span>

## <span data-ttu-id="f1fcf-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f1fcf-135">OUTPUTS</span></span>

## <span data-ttu-id="f1fcf-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f1fcf-136">NOTES</span></span>

## <span data-ttu-id="f1fcf-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f1fcf-137">RELATED LINKS</span></span>

