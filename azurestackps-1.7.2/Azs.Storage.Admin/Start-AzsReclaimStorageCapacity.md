---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: c3c7ec31ce2af23a4376f8b5f94deca302345e81
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93774347"
---
# <span data-ttu-id="9dbbc-101">Start-AzsReclaimStorageCapacity</span><span class="sxs-lookup"><span data-stu-id="9dbbc-101">Start-AzsReclaimStorageCapacity</span></span>

## <span data-ttu-id="9dbbc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9dbbc-102">SYNOPSIS</span></span>
<span data-ttu-id="9dbbc-103">Iniciar a coleta de lixo em objetos de armazenamento excluídos.</span><span class="sxs-lookup"><span data-stu-id="9dbbc-103">Start garbage collection on deleted storage objects.</span></span>

## <span data-ttu-id="9dbbc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9dbbc-104">SYNTAX</span></span>

```
Start-AzsReclaimStorageCapacity [[-ResourceGroupName] <String>] [-FarmName] <String> [-AsJob] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9dbbc-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9dbbc-105">DESCRIPTION</span></span>
<span data-ttu-id="9dbbc-106">Iniciar a coleta de lixo em objetos de armazenamento excluídos.</span><span class="sxs-lookup"><span data-stu-id="9dbbc-106">Start garbage collection on deleted storage objects.</span></span>

## <span data-ttu-id="9dbbc-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9dbbc-107">EXAMPLES</span></span>

### <span data-ttu-id="9dbbc-108">--------------------------EXEMPLO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="9dbbc-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Start-AzsReclaimStorageCapacity -FarmName "44263c10-13b2-4912-9b17-85c1e43b2a30"
```

<span data-ttu-id="9dbbc-109">Iniciar a coleta de lixo.</span><span class="sxs-lookup"><span data-stu-id="9dbbc-109">Start garbage collection.</span></span>

## <span data-ttu-id="9dbbc-110">OS</span><span class="sxs-lookup"><span data-stu-id="9dbbc-110">PARAMETERS</span></span>

### <span data-ttu-id="9dbbc-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9dbbc-111">-AsJob</span></span>
<span data-ttu-id="9dbbc-112">Executar assíncrono como um trabalho e retornar o objeto de trabalho.</span><span class="sxs-lookup"><span data-stu-id="9dbbc-112">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="9dbbc-113">-Farmname</span><span class="sxs-lookup"><span data-stu-id="9dbbc-113">-FarmName</span></span>
<span data-ttu-id="9dbbc-114">ID do farm.</span><span class="sxs-lookup"><span data-stu-id="9dbbc-114">Farm Id.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: name

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9dbbc-115">-Force</span><span class="sxs-lookup"><span data-stu-id="9dbbc-115">-Force</span></span>
<span data-ttu-id="9dbbc-116">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="9dbbc-116">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="9dbbc-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9dbbc-117">-ResourceGroupName</span></span>
<span data-ttu-id="9dbbc-118">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="9dbbc-118">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9dbbc-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="9dbbc-119">-Confirm</span></span>
<span data-ttu-id="9dbbc-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9dbbc-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9dbbc-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9dbbc-121">-WhatIf</span></span>
<span data-ttu-id="9dbbc-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="9dbbc-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9dbbc-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9dbbc-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9dbbc-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9dbbc-124">CommonParameters</span></span>
<span data-ttu-id="9dbbc-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9dbbc-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9dbbc-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9dbbc-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9dbbc-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9dbbc-127">INPUTS</span></span>

## <span data-ttu-id="9dbbc-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9dbbc-128">OUTPUTS</span></span>

## <span data-ttu-id="9dbbc-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9dbbc-129">NOTES</span></span>

## <span data-ttu-id="9dbbc-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9dbbc-130">RELATED LINKS</span></span>

