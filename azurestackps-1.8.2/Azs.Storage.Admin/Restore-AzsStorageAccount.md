---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 769567562199d33116911f1f1f5e258ae2decbbe
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/08/2020
ms.locfileid: "93946907"
---
# <span data-ttu-id="cf1c1-101">Restore-AzsStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cf1c1-101">Restore-AzsStorageAccount</span></span>

## <span data-ttu-id="cf1c1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cf1c1-102">SYNOPSIS</span></span>
<span data-ttu-id="cf1c1-103">Desexcluir uma conta de armazenamento excluída.</span><span class="sxs-lookup"><span data-stu-id="cf1c1-103">Undelete a deleted storage account.</span></span>

## <span data-ttu-id="cf1c1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cf1c1-104">SYNTAX</span></span>

### <span data-ttu-id="cf1c1-105">Reexcluir (padrão)</span><span class="sxs-lookup"><span data-stu-id="cf1c1-105">Undelete (Default)</span></span>
```
Restore-AzsStorageAccount -FarmName <String> -Name <String> [-ResourceGroupName <String>] [-Force] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cf1c1-106">Identificação</span><span class="sxs-lookup"><span data-stu-id="cf1c1-106">ResourceId</span></span>
```
Restore-AzsStorageAccount -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cf1c1-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="cf1c1-107">DESCRIPTION</span></span>
<span data-ttu-id="cf1c1-108">Desexcluir uma conta de armazenamento excluída.</span><span class="sxs-lookup"><span data-stu-id="cf1c1-108">Undelete a deleted storage account.</span></span>

## <span data-ttu-id="cf1c1-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cf1c1-109">EXAMPLES</span></span>

### <span data-ttu-id="cf1c1-110">EXEMPLO 1</span><span class="sxs-lookup"><span data-stu-id="cf1c1-110">EXAMPLE 1</span></span>
```
Restore-AzsStorageAccount -FarmName "90987d65-eb60-42ae-b735-18bcd7ff69da" -Name "83fe9ac0-f1e7-433e-b04c-c61ae0712093"
```

<span data-ttu-id="cf1c1-111">Desexcluir uma conta de armazenamento excluída.</span><span class="sxs-lookup"><span data-stu-id="cf1c1-111">Undelete a deleted storage account.</span></span>

## <span data-ttu-id="cf1c1-112">OS</span><span class="sxs-lookup"><span data-stu-id="cf1c1-112">PARAMETERS</span></span>

### <span data-ttu-id="cf1c1-113">-Farmname</span><span class="sxs-lookup"><span data-stu-id="cf1c1-113">-FarmName</span></span>
<span data-ttu-id="cf1c1-114">ID do farm.</span><span class="sxs-lookup"><span data-stu-id="cf1c1-114">Farm Id.</span></span>

```yaml
Type: String
Parameter Sets: Undelete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf1c1-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="cf1c1-115">-Name</span></span>
<span data-ttu-id="cf1c1-116">ID da conta de armazenamento interna, que não está visível para Tenant.</span><span class="sxs-lookup"><span data-stu-id="cf1c1-116">Internal storage account ID, which is not visible to tenant.</span></span>

```yaml
Type: String
Parameter Sets: Undelete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf1c1-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf1c1-117">-ResourceGroupName</span></span>
<span data-ttu-id="cf1c1-118">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="cf1c1-118">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: Undelete
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf1c1-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cf1c1-119">-ResourceId</span></span>
<span data-ttu-id="cf1c1-120">A ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="cf1c1-120">The resource id.</span></span>

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

### <span data-ttu-id="cf1c1-121">-Force</span><span class="sxs-lookup"><span data-stu-id="cf1c1-121">-Force</span></span>
<span data-ttu-id="cf1c1-122">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="cf1c1-122">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="cf1c1-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cf1c1-123">-WhatIf</span></span>
<span data-ttu-id="cf1c1-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="cf1c1-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cf1c1-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="cf1c1-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cf1c1-126">-Confirme</span><span class="sxs-lookup"><span data-stu-id="cf1c1-126">-Confirm</span></span>
<span data-ttu-id="cf1c1-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cf1c1-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cf1c1-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf1c1-128">CommonParameters</span></span>
<span data-ttu-id="cf1c1-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cf1c1-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf1c1-130">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cf1c1-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf1c1-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="cf1c1-131">INPUTS</span></span>

## <span data-ttu-id="cf1c1-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="cf1c1-132">OUTPUTS</span></span>

## <span data-ttu-id="cf1c1-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="cf1c1-133">NOTES</span></span>

## <span data-ttu-id="cf1c1-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cf1c1-134">RELATED LINKS</span></span>
