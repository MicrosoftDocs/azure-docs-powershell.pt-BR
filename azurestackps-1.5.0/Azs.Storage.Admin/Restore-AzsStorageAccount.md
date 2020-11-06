---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: b4e3e69a0c55188514a31dbe7377f8336784b114
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93426221"
---
# <span data-ttu-id="6494a-101">Restore-AzsStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6494a-101">Restore-AzsStorageAccount</span></span>

## <span data-ttu-id="6494a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6494a-102">SYNOPSIS</span></span>
<span data-ttu-id="6494a-103">Desexcluir uma conta de armazenamento excluída.</span><span class="sxs-lookup"><span data-stu-id="6494a-103">Undelete a deleted storage account.</span></span>

## <span data-ttu-id="6494a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6494a-104">SYNTAX</span></span>

### <span data-ttu-id="6494a-105">Reexcluir (padrão)</span><span class="sxs-lookup"><span data-stu-id="6494a-105">Undelete (Default)</span></span>
```
Restore-AzsStorageAccount -FarmName <String> -Name <String> [-ResourceGroupName <String>] [-Force] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6494a-106">Identificação</span><span class="sxs-lookup"><span data-stu-id="6494a-106">ResourceId</span></span>
```
Restore-AzsStorageAccount -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6494a-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6494a-107">DESCRIPTION</span></span>
<span data-ttu-id="6494a-108">Desexcluir uma conta de armazenamento excluída.</span><span class="sxs-lookup"><span data-stu-id="6494a-108">Undelete a deleted storage account.</span></span>

## <span data-ttu-id="6494a-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6494a-109">EXAMPLES</span></span>

### <span data-ttu-id="6494a-110">--------------------------EXEMPLO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="6494a-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Restore-AzsStorageAccount -FarmName "90987d65-eb60-42ae-b735-18bcd7ff69da" -Name "83fe9ac0-f1e7-433e-b04c-c61ae0712093"
```

<span data-ttu-id="6494a-111">Desexcluir uma conta de armazenamento excluída.</span><span class="sxs-lookup"><span data-stu-id="6494a-111">Undelete a deleted storage account.</span></span>

## <span data-ttu-id="6494a-112">OS</span><span class="sxs-lookup"><span data-stu-id="6494a-112">PARAMETERS</span></span>

### <span data-ttu-id="6494a-113">-Farmname</span><span class="sxs-lookup"><span data-stu-id="6494a-113">-FarmName</span></span>
<span data-ttu-id="6494a-114">ID do farm.</span><span class="sxs-lookup"><span data-stu-id="6494a-114">Farm Id.</span></span>

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

### <span data-ttu-id="6494a-115">-Force</span><span class="sxs-lookup"><span data-stu-id="6494a-115">-Force</span></span>
<span data-ttu-id="6494a-116">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="6494a-116">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="6494a-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="6494a-117">-Name</span></span>
<span data-ttu-id="6494a-118">ID da conta de armazenamento interna, que não está visível para Tenant.</span><span class="sxs-lookup"><span data-stu-id="6494a-118">Internal storage account ID, which is not visible to tenant.</span></span>

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

### <span data-ttu-id="6494a-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6494a-119">-ResourceGroupName</span></span>
<span data-ttu-id="6494a-120">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="6494a-120">Resource group name.</span></span>

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

### <span data-ttu-id="6494a-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6494a-121">-ResourceId</span></span>
<span data-ttu-id="6494a-122">A ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="6494a-122">The resource id.</span></span>

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

### <span data-ttu-id="6494a-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="6494a-123">-Confirm</span></span>
<span data-ttu-id="6494a-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6494a-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6494a-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6494a-125">-WhatIf</span></span>
<span data-ttu-id="6494a-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="6494a-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6494a-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6494a-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6494a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6494a-128">CommonParameters</span></span>
<span data-ttu-id="6494a-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6494a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6494a-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6494a-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6494a-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6494a-131">INPUTS</span></span>

## <span data-ttu-id="6494a-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6494a-132">OUTPUTS</span></span>

## <span data-ttu-id="6494a-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6494a-133">NOTES</span></span>

## <span data-ttu-id="6494a-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6494a-134">RELATED LINKS</span></span>

