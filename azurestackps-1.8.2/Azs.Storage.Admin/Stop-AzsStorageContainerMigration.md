---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8c9a27b1722c1c7f08d9daeab0205dd20d9ba8b9
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/08/2020
ms.locfileid: "93946603"
---
# <span data-ttu-id="6740c-101">Stop-AzsStorageContainerMigration</span><span class="sxs-lookup"><span data-stu-id="6740c-101">Stop-AzsStorageContainerMigration</span></span>

## <span data-ttu-id="6740c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6740c-102">SYNOPSIS</span></span>
<span data-ttu-id="6740c-103">Cancelar um trabalho de migração de contêineres.</span><span class="sxs-lookup"><span data-stu-id="6740c-103">Cancel a container migration job.</span></span>

## <span data-ttu-id="6740c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6740c-104">SYNTAX</span></span>

```
Stop-AzsStorageContainerMigration [-JobId] <String> [[-ResourceGroupName] <String>] [-FarmName] <String>
 [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6740c-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6740c-105">DESCRIPTION</span></span>
<span data-ttu-id="6740c-106">Cancelar um trabalho de migração de contêineres.</span><span class="sxs-lookup"><span data-stu-id="6740c-106">Cancel a container migration job.</span></span>

## <span data-ttu-id="6740c-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6740c-107">EXAMPLES</span></span>

### <span data-ttu-id="6740c-108">EXEMPLO 1</span><span class="sxs-lookup"><span data-stu-id="6740c-108">EXAMPLE 1</span></span>
```
Stop-AzsStorageContainerMigration -FarmName "342fccbe-e8c0-468d-a90e-cfca5fa8877c" -JobId "ac8cde1b-804f-4ace-b39b-5322106703bf"
```

<span data-ttu-id="6740c-109">Cancele a migração do contêiner.</span><span class="sxs-lookup"><span data-stu-id="6740c-109">Cancel container migration.</span></span>

## <span data-ttu-id="6740c-110">OS</span><span class="sxs-lookup"><span data-stu-id="6740c-110">PARAMETERS</span></span>

### <span data-ttu-id="6740c-111">-JobId</span><span class="sxs-lookup"><span data-stu-id="6740c-111">-JobId</span></span>
<span data-ttu-id="6740c-112">ID da operação.</span><span class="sxs-lookup"><span data-stu-id="6740c-112">Operation Id.</span></span>

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

### <span data-ttu-id="6740c-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6740c-113">-ResourceGroupName</span></span>
<span data-ttu-id="6740c-114">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="6740c-114">Resource group name.</span></span>

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

### <span data-ttu-id="6740c-115">-Farmname</span><span class="sxs-lookup"><span data-stu-id="6740c-115">-FarmName</span></span>
<span data-ttu-id="6740c-116">ID do farm.</span><span class="sxs-lookup"><span data-stu-id="6740c-116">Farm Id.</span></span>

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

### <span data-ttu-id="6740c-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6740c-117">-AsJob</span></span>
<span data-ttu-id="6740c-118">Executar assíncrono como um trabalho e retornar o objeto de trabalho.</span><span class="sxs-lookup"><span data-stu-id="6740c-118">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="6740c-119">-Force</span><span class="sxs-lookup"><span data-stu-id="6740c-119">-Force</span></span>
<span data-ttu-id="6740c-120">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="6740c-120">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="6740c-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6740c-121">-WhatIf</span></span>
<span data-ttu-id="6740c-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="6740c-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6740c-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6740c-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6740c-124">-Confirme</span><span class="sxs-lookup"><span data-stu-id="6740c-124">-Confirm</span></span>
<span data-ttu-id="6740c-125">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6740c-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6740c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6740c-126">CommonParameters</span></span>
<span data-ttu-id="6740c-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6740c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6740c-128">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6740c-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6740c-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6740c-129">INPUTS</span></span>

## <span data-ttu-id="6740c-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6740c-130">OUTPUTS</span></span>

## <span data-ttu-id="6740c-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6740c-131">NOTES</span></span>

## <span data-ttu-id="6740c-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6740c-132">RELATED LINKS</span></span>
