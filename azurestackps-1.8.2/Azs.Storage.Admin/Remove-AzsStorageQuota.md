---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0983e05a36de72148571ccbbc7f1454343ad393a
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/08/2020
ms.locfileid: "93946634"
---
# <span data-ttu-id="34a02-101">Remove-AzsStorageQuota</span><span class="sxs-lookup"><span data-stu-id="34a02-101">Remove-AzsStorageQuota</span></span>

## <span data-ttu-id="34a02-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="34a02-102">SYNOPSIS</span></span>
<span data-ttu-id="34a02-103">Excluir uma cota existente</span><span class="sxs-lookup"><span data-stu-id="34a02-103">Delete an existing quota</span></span>

## <span data-ttu-id="34a02-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="34a02-104">SYNTAX</span></span>

### <span data-ttu-id="34a02-105">Excluir (padrão)</span><span class="sxs-lookup"><span data-stu-id="34a02-105">Delete (Default)</span></span>
```
Remove-AzsStorageQuota -Name <String> [-Location <String>] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="34a02-106">Identificação</span><span class="sxs-lookup"><span data-stu-id="34a02-106">ResourceId</span></span>
```
Remove-AzsStorageQuota -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="34a02-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="34a02-107">DESCRIPTION</span></span>
<span data-ttu-id="34a02-108">Excluir uma cota existente</span><span class="sxs-lookup"><span data-stu-id="34a02-108">Delete an existing quota</span></span>

## <span data-ttu-id="34a02-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="34a02-109">EXAMPLES</span></span>

### <span data-ttu-id="34a02-110">EXEMPLO 1</span><span class="sxs-lookup"><span data-stu-id="34a02-110">EXAMPLE 1</span></span>
```
Remove-AzsStorageQuota -Name 'TestDeleteStorageQuota'
```

<span data-ttu-id="34a02-111">Remova uma cota de armazenamento por nome.</span><span class="sxs-lookup"><span data-stu-id="34a02-111">Remove a storage quota by name.</span></span>

### <span data-ttu-id="34a02-112">EXEMPLO 2</span><span class="sxs-lookup"><span data-stu-id="34a02-112">EXAMPLE 2</span></span>
```
Get-AzsStorageQuota -Name 'testquota' | Remove-AzsStorageQuota
```

<span data-ttu-id="34a02-113">Remova uma cota de armazenamento por tubulação.</span><span class="sxs-lookup"><span data-stu-id="34a02-113">Remove a storage quota by piping.</span></span>

## <span data-ttu-id="34a02-114">OS</span><span class="sxs-lookup"><span data-stu-id="34a02-114">PARAMETERS</span></span>

### <span data-ttu-id="34a02-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="34a02-115">-Name</span></span>
<span data-ttu-id="34a02-116">O nome da cota de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="34a02-116">The name of the storage quota.</span></span>

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

### <span data-ttu-id="34a02-117">-Local</span><span class="sxs-lookup"><span data-stu-id="34a02-117">-Location</span></span>
<span data-ttu-id="34a02-118">Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="34a02-118">Resource location.</span></span>

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

### <span data-ttu-id="34a02-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="34a02-119">-ResourceId</span></span>
<span data-ttu-id="34a02-120">A ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="34a02-120">The resource id.</span></span>

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

### <span data-ttu-id="34a02-121">-Force</span><span class="sxs-lookup"><span data-stu-id="34a02-121">-Force</span></span>
<span data-ttu-id="34a02-122">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="34a02-122">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="34a02-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="34a02-123">-WhatIf</span></span>
<span data-ttu-id="34a02-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="34a02-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="34a02-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="34a02-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="34a02-126">-Confirme</span><span class="sxs-lookup"><span data-stu-id="34a02-126">-Confirm</span></span>
<span data-ttu-id="34a02-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="34a02-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="34a02-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34a02-128">CommonParameters</span></span>
<span data-ttu-id="34a02-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34a02-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34a02-130">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34a02-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34a02-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="34a02-131">INPUTS</span></span>

## <span data-ttu-id="34a02-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="34a02-132">OUTPUTS</span></span>

## <span data-ttu-id="34a02-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="34a02-133">NOTES</span></span>

## <span data-ttu-id="34a02-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="34a02-134">RELATED LINKS</span></span>
