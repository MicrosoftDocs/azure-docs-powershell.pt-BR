---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 81bdb6a75e10af30b6febe9bbbf0989933818aec
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93425614"
---
# <span data-ttu-id="450d7-101">Stop-AzsStorageContainerMigration</span><span class="sxs-lookup"><span data-stu-id="450d7-101">Stop-AzsStorageContainerMigration</span></span>

## <span data-ttu-id="450d7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="450d7-102">SYNOPSIS</span></span>
<span data-ttu-id="450d7-103">Cancelar um trabalho de migração de contêineres.</span><span class="sxs-lookup"><span data-stu-id="450d7-103">Cancel a container migration job.</span></span>

## <span data-ttu-id="450d7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="450d7-104">SYNTAX</span></span>

```
Stop-AzsStorageContainerMigration [-JobId] <String> [[-ResourceGroupName] <String>] [-FarmName] <String>
 [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="450d7-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="450d7-105">DESCRIPTION</span></span>
<span data-ttu-id="450d7-106">Cancelar um trabalho de migração de contêineres.</span><span class="sxs-lookup"><span data-stu-id="450d7-106">Cancel a container migration job.</span></span>

## <span data-ttu-id="450d7-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="450d7-107">EXAMPLES</span></span>

### <span data-ttu-id="450d7-108">--------------------------EXEMPLO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="450d7-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Stop-AzsStorageContainerMigration -FarmName "342fccbe-e8c0-468d-a90e-cfca5fa8877c" -JobId "ac8cde1b-804f-4ace-b39b-5322106703bf"
```

<span data-ttu-id="450d7-109">Cancele a migração do contêiner.</span><span class="sxs-lookup"><span data-stu-id="450d7-109">Cancel container migration.</span></span>

## <span data-ttu-id="450d7-110">OS</span><span class="sxs-lookup"><span data-stu-id="450d7-110">PARAMETERS</span></span>

### <span data-ttu-id="450d7-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="450d7-111">-AsJob</span></span>
<span data-ttu-id="450d7-112">Executar assíncrono como um trabalho e retornar o objeto de trabalho.</span><span class="sxs-lookup"><span data-stu-id="450d7-112">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="450d7-113">-Farmname</span><span class="sxs-lookup"><span data-stu-id="450d7-113">-FarmName</span></span>
<span data-ttu-id="450d7-114">ID do farm.</span><span class="sxs-lookup"><span data-stu-id="450d7-114">Farm Id.</span></span>

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

### <span data-ttu-id="450d7-115">-Force</span><span class="sxs-lookup"><span data-stu-id="450d7-115">-Force</span></span>
<span data-ttu-id="450d7-116">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="450d7-116">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="450d7-117">-JobId</span><span class="sxs-lookup"><span data-stu-id="450d7-117">-JobId</span></span>
<span data-ttu-id="450d7-118">ID da operação.</span><span class="sxs-lookup"><span data-stu-id="450d7-118">Operation Id.</span></span>

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

### <span data-ttu-id="450d7-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="450d7-119">-ResourceGroupName</span></span>
<span data-ttu-id="450d7-120">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="450d7-120">Resource group name.</span></span>

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

### <span data-ttu-id="450d7-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="450d7-121">-Confirm</span></span>
<span data-ttu-id="450d7-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="450d7-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="450d7-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="450d7-123">-WhatIf</span></span>
<span data-ttu-id="450d7-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="450d7-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="450d7-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="450d7-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="450d7-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="450d7-126">CommonParameters</span></span>
<span data-ttu-id="450d7-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="450d7-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="450d7-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="450d7-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="450d7-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="450d7-129">INPUTS</span></span>

## <span data-ttu-id="450d7-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="450d7-130">OUTPUTS</span></span>

## <span data-ttu-id="450d7-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="450d7-131">NOTES</span></span>

## <span data-ttu-id="450d7-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="450d7-132">RELATED LINKS</span></span>

