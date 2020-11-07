---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 769567562199d33116911f1f1f5e258ae2decbbe
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2020
ms.locfileid: "93775139"
---
# <span data-ttu-id="d6f31-101">Restore-AzsStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d6f31-101">Restore-AzsStorageAccount</span></span>

## <span data-ttu-id="d6f31-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d6f31-102">SYNOPSIS</span></span>
<span data-ttu-id="d6f31-103">Desexcluir uma conta de armazenamento excluída.</span><span class="sxs-lookup"><span data-stu-id="d6f31-103">Undelete a deleted storage account.</span></span>

## <span data-ttu-id="d6f31-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d6f31-104">SYNTAX</span></span>

### <span data-ttu-id="d6f31-105">Reexcluir (padrão)</span><span class="sxs-lookup"><span data-stu-id="d6f31-105">Undelete (Default)</span></span>
```
Restore-AzsStorageAccount -FarmName <String> -Name <String> [-ResourceGroupName <String>] [-Force] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d6f31-106">Identificação</span><span class="sxs-lookup"><span data-stu-id="d6f31-106">ResourceId</span></span>
```
Restore-AzsStorageAccount -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d6f31-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d6f31-107">DESCRIPTION</span></span>
<span data-ttu-id="d6f31-108">Desexcluir uma conta de armazenamento excluída.</span><span class="sxs-lookup"><span data-stu-id="d6f31-108">Undelete a deleted storage account.</span></span>

## <span data-ttu-id="d6f31-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d6f31-109">EXAMPLES</span></span>

### <span data-ttu-id="d6f31-110">EXEMPLO 1</span><span class="sxs-lookup"><span data-stu-id="d6f31-110">EXAMPLE 1</span></span>
```
Restore-AzsStorageAccount -FarmName "90987d65-eb60-42ae-b735-18bcd7ff69da" -Name "83fe9ac0-f1e7-433e-b04c-c61ae0712093"
```

<span data-ttu-id="d6f31-111">Desexcluir uma conta de armazenamento excluída.</span><span class="sxs-lookup"><span data-stu-id="d6f31-111">Undelete a deleted storage account.</span></span>

## <span data-ttu-id="d6f31-112">OS</span><span class="sxs-lookup"><span data-stu-id="d6f31-112">PARAMETERS</span></span>

### <span data-ttu-id="d6f31-113">-Farmname</span><span class="sxs-lookup"><span data-stu-id="d6f31-113">-FarmName</span></span>
<span data-ttu-id="d6f31-114">ID do farm.</span><span class="sxs-lookup"><span data-stu-id="d6f31-114">Farm Id.</span></span>

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

### <span data-ttu-id="d6f31-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="d6f31-115">-Name</span></span>
<span data-ttu-id="d6f31-116">ID da conta de armazenamento interna, que não está visível para Tenant.</span><span class="sxs-lookup"><span data-stu-id="d6f31-116">Internal storage account ID, which is not visible to tenant.</span></span>

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

### <span data-ttu-id="d6f31-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6f31-117">-ResourceGroupName</span></span>
<span data-ttu-id="d6f31-118">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d6f31-118">Resource group name.</span></span>

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

### <span data-ttu-id="d6f31-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d6f31-119">-ResourceId</span></span>
<span data-ttu-id="d6f31-120">A ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="d6f31-120">The resource id.</span></span>

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

### <span data-ttu-id="d6f31-121">-Force</span><span class="sxs-lookup"><span data-stu-id="d6f31-121">-Force</span></span>
<span data-ttu-id="d6f31-122">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="d6f31-122">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="d6f31-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d6f31-123">-WhatIf</span></span>
<span data-ttu-id="d6f31-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d6f31-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d6f31-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d6f31-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d6f31-126">-Confirme</span><span class="sxs-lookup"><span data-stu-id="d6f31-126">-Confirm</span></span>
<span data-ttu-id="d6f31-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d6f31-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d6f31-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6f31-128">CommonParameters</span></span>
<span data-ttu-id="d6f31-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d6f31-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6f31-130">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d6f31-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6f31-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d6f31-131">INPUTS</span></span>

## <span data-ttu-id="d6f31-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d6f31-132">OUTPUTS</span></span>

## <span data-ttu-id="d6f31-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d6f31-133">NOTES</span></span>

## <span data-ttu-id="d6f31-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d6f31-134">RELATED LINKS</span></span>
