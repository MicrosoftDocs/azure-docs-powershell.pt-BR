---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: f5a52ebfe2d59a200add1c8f763f7a3cafa59c18
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93774099"
---
# <span data-ttu-id="1ccdb-101">Start-AzsInfrastructureRoleInstance</span><span class="sxs-lookup"><span data-stu-id="1ccdb-101">Start-AzsInfrastructureRoleInstance</span></span>

## <span data-ttu-id="1ccdb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1ccdb-102">SYNOPSIS</span></span>
<span data-ttu-id="1ccdb-103">Ative uma instância de função de infraestrutura.</span><span class="sxs-lookup"><span data-stu-id="1ccdb-103">Power on an infrastructure role instance.</span></span>

## <span data-ttu-id="1ccdb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1ccdb-104">SYNTAX</span></span>

### <span data-ttu-id="1ccdb-105">Power-out (padrão)</span><span class="sxs-lookup"><span data-stu-id="1ccdb-105">PowerOn (Default)</span></span>
```
Start-AzsInfrastructureRoleInstance -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-AsJob]
 [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1ccdb-106">Identificação</span><span class="sxs-lookup"><span data-stu-id="1ccdb-106">ResourceId</span></span>
```
Start-AzsInfrastructureRoleInstance -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1ccdb-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1ccdb-107">DESCRIPTION</span></span>
<span data-ttu-id="1ccdb-108">Ative uma instância de função de infraestrutura.</span><span class="sxs-lookup"><span data-stu-id="1ccdb-108">Power on an infrastructure role instance.</span></span>

## <span data-ttu-id="1ccdb-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1ccdb-109">EXAMPLES</span></span>

### <span data-ttu-id="1ccdb-110">--------------------------EXEMPLO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="1ccdb-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Start-AzsInfrastructureRoleInstance -Name "AzS-ACS01"
```

<span data-ttu-id="1ccdb-111">Ative uma instância de função de infraestrutura.</span><span class="sxs-lookup"><span data-stu-id="1ccdb-111">Power on an infrastructure role instance.</span></span>

## <span data-ttu-id="1ccdb-112">OS</span><span class="sxs-lookup"><span data-stu-id="1ccdb-112">PARAMETERS</span></span>

### <span data-ttu-id="1ccdb-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1ccdb-113">-AsJob</span></span>
<span data-ttu-id="1ccdb-114">Executar assíncrono como um trabalho e retornar o objeto de trabalho.</span><span class="sxs-lookup"><span data-stu-id="1ccdb-114">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="1ccdb-115">-Force</span><span class="sxs-lookup"><span data-stu-id="1ccdb-115">-Force</span></span>
<span data-ttu-id="1ccdb-116">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="1ccdb-116">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="1ccdb-117">-Local</span><span class="sxs-lookup"><span data-stu-id="1ccdb-117">-Location</span></span>
<span data-ttu-id="1ccdb-118">Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="1ccdb-118">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: PowerOn
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ccdb-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="1ccdb-119">-Name</span></span>
<span data-ttu-id="1ccdb-120">Nome de uma instância de função de infraestrutura.</span><span class="sxs-lookup"><span data-stu-id="1ccdb-120">Name of an infrastructure role instance.</span></span>

```yaml
Type: String
Parameter Sets: PowerOn
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ccdb-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ccdb-121">-ResourceGroupName</span></span>
<span data-ttu-id="1ccdb-122">Grupo de recursos no qual o provedor de recursos foi registrado.</span><span class="sxs-lookup"><span data-stu-id="1ccdb-122">Resource group in which the resource provider has been registered.</span></span>

```yaml
Type: String
Parameter Sets: PowerOn
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ccdb-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1ccdb-123">-ResourceId</span></span>
<span data-ttu-id="1ccdb-124">ID do recurso de instância da infraestrutura.</span><span class="sxs-lookup"><span data-stu-id="1ccdb-124">Infrastructure role instance resource ID.</span></span>

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

### <span data-ttu-id="1ccdb-125">-Confirme</span><span class="sxs-lookup"><span data-stu-id="1ccdb-125">-Confirm</span></span>
<span data-ttu-id="1ccdb-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1ccdb-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1ccdb-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1ccdb-127">-WhatIf</span></span>
<span data-ttu-id="1ccdb-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="1ccdb-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1ccdb-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1ccdb-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1ccdb-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ccdb-130">CommonParameters</span></span>
<span data-ttu-id="1ccdb-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ccdb-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ccdb-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ccdb-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ccdb-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1ccdb-133">INPUTS</span></span>

## <span data-ttu-id="1ccdb-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1ccdb-134">OUTPUTS</span></span>

## <span data-ttu-id="1ccdb-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1ccdb-135">NOTES</span></span>

## <span data-ttu-id="1ccdb-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1ccdb-136">RELATED LINKS</span></span>
