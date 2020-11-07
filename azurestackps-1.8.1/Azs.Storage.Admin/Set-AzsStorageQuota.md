---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 641017c75243a253a6b9eb0054df7737a674f671
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2020
ms.locfileid: "93775125"
---
# <span data-ttu-id="d5177-101">Set-AzsStorageQuota</span><span class="sxs-lookup"><span data-stu-id="d5177-101">Set-AzsStorageQuota</span></span>

## <span data-ttu-id="d5177-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d5177-102">SYNOPSIS</span></span>
<span data-ttu-id="d5177-103">Criar ou atualizar uma cota de armazenamento existente.</span><span class="sxs-lookup"><span data-stu-id="d5177-103">Create or update an existing storage quota.</span></span>

## <span data-ttu-id="d5177-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d5177-104">SYNTAX</span></span>

### <span data-ttu-id="d5177-105">Atualização (padrão)</span><span class="sxs-lookup"><span data-stu-id="d5177-105">Update (Default)</span></span>
```
Set-AzsStorageQuota -Name <String> [-CapacityInGb <Int32>] [-NumberOfStorageAccounts <Int32>]
 [-Location <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d5177-106">Identificação</span><span class="sxs-lookup"><span data-stu-id="d5177-106">ResourceId</span></span>
```
Set-AzsStorageQuota [-CapacityInGb <Int32>] [-NumberOfStorageAccounts <Int32>] -ResourceId <String> [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d5177-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="d5177-107">InputObject</span></span>
```
Set-AzsStorageQuota [-CapacityInGb <Int32>] [-NumberOfStorageAccounts <Int32>] -InputObject <StorageQuota>
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d5177-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d5177-108">DESCRIPTION</span></span>
<span data-ttu-id="d5177-109">Criar ou atualizar uma cota de armazenamento existente.</span><span class="sxs-lookup"><span data-stu-id="d5177-109">Create or update an existing storage quota.</span></span>

## <span data-ttu-id="d5177-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d5177-110">EXAMPLES</span></span>

### <span data-ttu-id="d5177-111">EXEMPLO 1</span><span class="sxs-lookup"><span data-stu-id="d5177-111">EXAMPLE 1</span></span>
```
Set-AzsStorageQuota -Name 'TestUpdateStorageQuota' -CapacityInGb 123 -NumberOfStorageAccounts 10
```

<span data-ttu-id="d5177-112">Atualizar uma cota de armazenamento existente.</span><span class="sxs-lookup"><span data-stu-id="d5177-112">Update an existing storage quota.</span></span>

## <span data-ttu-id="d5177-113">OS</span><span class="sxs-lookup"><span data-stu-id="d5177-113">PARAMETERS</span></span>

### <span data-ttu-id="d5177-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="d5177-114">-Name</span></span>
<span data-ttu-id="d5177-115">O nome da cota de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="d5177-115">The name of the storage quota.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5177-116">-CapacityInGb</span><span class="sxs-lookup"><span data-stu-id="d5177-116">-CapacityInGb</span></span>
<span data-ttu-id="d5177-117">Capacidade de máximo (GB).</span><span class="sxs-lookup"><span data-stu-id="d5177-117">Maxium capacity (GB).</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5177-118">-NumberOfStorageAccounts</span><span class="sxs-lookup"><span data-stu-id="d5177-118">-NumberOfStorageAccounts</span></span>
<span data-ttu-id="d5177-119">Número total de contas de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="d5177-119">Total number of storage accounts.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5177-120">-Local</span><span class="sxs-lookup"><span data-stu-id="d5177-120">-Location</span></span>
<span data-ttu-id="d5177-121">Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="d5177-121">Resource location.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5177-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d5177-122">-ResourceId</span></span>
<span data-ttu-id="d5177-123">A ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="d5177-123">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5177-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d5177-124">-InputObject</span></span>
<span data-ttu-id="d5177-125">Posbbily cota de armazenamento modificada retornada por Get-AzsStorageQuota.</span><span class="sxs-lookup"><span data-stu-id="d5177-125">Posbbily modified storage quota returned by Get-AzsStorageQuota.</span></span>

```yaml
Type: StorageQuota
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d5177-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d5177-126">-WhatIf</span></span>
<span data-ttu-id="d5177-127">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d5177-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d5177-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d5177-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d5177-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="d5177-129">-Confirm</span></span>
<span data-ttu-id="d5177-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d5177-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d5177-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5177-131">CommonParameters</span></span>
<span data-ttu-id="d5177-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d5177-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5177-133">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d5177-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5177-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d5177-134">INPUTS</span></span>

## <span data-ttu-id="d5177-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d5177-135">OUTPUTS</span></span>

### <span data-ttu-id="d5177-136">Microsoft. AzureStack. Management. Storage. admin. Models. StorageQuota</span><span class="sxs-lookup"><span data-stu-id="d5177-136">Microsoft.AzureStack.Management.Storage.Admin.Models.StorageQuota</span></span>

## <span data-ttu-id="d5177-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d5177-137">NOTES</span></span>

## <span data-ttu-id="d5177-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d5177-138">RELATED LINKS</span></span>