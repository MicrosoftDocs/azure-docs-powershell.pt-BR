---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 81bdb6a75e10af30b6febe9bbbf0989933818aec
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2020
ms.locfileid: "93774824"
---
# <span data-ttu-id="f2d6c-101">Stop-AzsStorageContainerMigration</span><span class="sxs-lookup"><span data-stu-id="f2d6c-101">Stop-AzsStorageContainerMigration</span></span>

## <span data-ttu-id="f2d6c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f2d6c-102">SYNOPSIS</span></span>
<span data-ttu-id="f2d6c-103">Cancelar um trabalho de migração de contêineres.</span><span class="sxs-lookup"><span data-stu-id="f2d6c-103">Cancel a container migration job.</span></span>

## <span data-ttu-id="f2d6c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f2d6c-104">SYNTAX</span></span>

```
Stop-AzsStorageContainerMigration [-JobId] <String> [[-ResourceGroupName] <String>] [-FarmName] <String>
 [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f2d6c-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f2d6c-105">DESCRIPTION</span></span>
<span data-ttu-id="f2d6c-106">Cancelar um trabalho de migração de contêineres.</span><span class="sxs-lookup"><span data-stu-id="f2d6c-106">Cancel a container migration job.</span></span>

## <span data-ttu-id="f2d6c-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f2d6c-107">EXAMPLES</span></span>

### <span data-ttu-id="f2d6c-108">--------------------------EXEMPLO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="f2d6c-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Stop-AzsStorageContainerMigration -FarmName "342fccbe-e8c0-468d-a90e-cfca5fa8877c" -JobId "ac8cde1b-804f-4ace-b39b-5322106703bf"
```

<span data-ttu-id="f2d6c-109">Cancele a migração do contêiner.</span><span class="sxs-lookup"><span data-stu-id="f2d6c-109">Cancel container migration.</span></span>

## <span data-ttu-id="f2d6c-110">OS</span><span class="sxs-lookup"><span data-stu-id="f2d6c-110">PARAMETERS</span></span>

### <span data-ttu-id="f2d6c-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f2d6c-111">-AsJob</span></span>
<span data-ttu-id="f2d6c-112">Executar assíncrono como um trabalho e retornar o objeto de trabalho.</span><span class="sxs-lookup"><span data-stu-id="f2d6c-112">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="f2d6c-113">-Farmname</span><span class="sxs-lookup"><span data-stu-id="f2d6c-113">-FarmName</span></span>
<span data-ttu-id="f2d6c-114">ID do farm.</span><span class="sxs-lookup"><span data-stu-id="f2d6c-114">Farm Id.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2d6c-115">-Force</span><span class="sxs-lookup"><span data-stu-id="f2d6c-115">-Force</span></span>
<span data-ttu-id="f2d6c-116">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="f2d6c-116">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="f2d6c-117">-JobId</span><span class="sxs-lookup"><span data-stu-id="f2d6c-117">-JobId</span></span>
<span data-ttu-id="f2d6c-118">ID da operação.</span><span class="sxs-lookup"><span data-stu-id="f2d6c-118">Operation Id.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2d6c-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2d6c-119">-ResourceGroupName</span></span>
<span data-ttu-id="f2d6c-120">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f2d6c-120">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2d6c-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f2d6c-121">-Confirm</span></span>
<span data-ttu-id="f2d6c-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f2d6c-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f2d6c-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f2d6c-123">-WhatIf</span></span>
<span data-ttu-id="f2d6c-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f2d6c-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f2d6c-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f2d6c-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f2d6c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2d6c-126">CommonParameters</span></span>
<span data-ttu-id="f2d6c-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2d6c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2d6c-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f2d6c-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2d6c-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f2d6c-129">INPUTS</span></span>

## <span data-ttu-id="f2d6c-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f2d6c-130">OUTPUTS</span></span>

## <span data-ttu-id="f2d6c-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f2d6c-131">NOTES</span></span>

## <span data-ttu-id="f2d6c-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f2d6c-132">RELATED LINKS</span></span>

