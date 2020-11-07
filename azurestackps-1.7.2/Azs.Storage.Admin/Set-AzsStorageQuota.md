---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2eec56d9fc157da994521a5b258cd28132344c52
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93774159"
---
# <span data-ttu-id="3ff8f-101">Set-AzsStorageQuota</span><span class="sxs-lookup"><span data-stu-id="3ff8f-101">Set-AzsStorageQuota</span></span>

## <span data-ttu-id="3ff8f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3ff8f-102">SYNOPSIS</span></span>
<span data-ttu-id="3ff8f-103">Criar ou atualizar uma cota de armazenamento existente.</span><span class="sxs-lookup"><span data-stu-id="3ff8f-103">Create or update an existing storage quota.</span></span>

## <span data-ttu-id="3ff8f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3ff8f-104">SYNTAX</span></span>

### <span data-ttu-id="3ff8f-105">Atualização (padrão)</span><span class="sxs-lookup"><span data-stu-id="3ff8f-105">Update (Default)</span></span>
```
Set-AzsStorageQuota -Name <String> [-CapacityInGb <Int32>] [-NumberOfStorageAccounts <Int32>]
 [-Location <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3ff8f-106">Identificação</span><span class="sxs-lookup"><span data-stu-id="3ff8f-106">ResourceId</span></span>
```
Set-AzsStorageQuota [-CapacityInGb <Int32>] [-NumberOfStorageAccounts <Int32>] -ResourceId <String> [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3ff8f-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="3ff8f-107">InputObject</span></span>
```
Set-AzsStorageQuota [-CapacityInGb <Int32>] [-NumberOfStorageAccounts <Int32>] -InputObject <StorageQuota>
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3ff8f-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3ff8f-108">DESCRIPTION</span></span>
<span data-ttu-id="3ff8f-109">Criar ou atualizar uma cota de armazenamento existente.</span><span class="sxs-lookup"><span data-stu-id="3ff8f-109">Create or update an existing storage quota.</span></span>

## <span data-ttu-id="3ff8f-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3ff8f-110">EXAMPLES</span></span>

### <span data-ttu-id="3ff8f-111">--------------------------EXEMPLO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="3ff8f-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Set-AzsStorageQuota -Name 'TestUpdateStorageQuota' -CapacityInGb 123 -NumberOfStorageAccounts 10
```

<span data-ttu-id="3ff8f-112">Atualizar uma cota de armazenamento existente.</span><span class="sxs-lookup"><span data-stu-id="3ff8f-112">Update an existing storage quota.</span></span>

## <span data-ttu-id="3ff8f-113">OS</span><span class="sxs-lookup"><span data-stu-id="3ff8f-113">PARAMETERS</span></span>

### <span data-ttu-id="3ff8f-114">-CapacityInGb</span><span class="sxs-lookup"><span data-stu-id="3ff8f-114">-CapacityInGb</span></span>
<span data-ttu-id="3ff8f-115">Capacidade de máximo (GB).</span><span class="sxs-lookup"><span data-stu-id="3ff8f-115">Maxium capacity (GB).</span></span>

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

### <span data-ttu-id="3ff8f-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3ff8f-116">-InputObject</span></span>
<span data-ttu-id="3ff8f-117">Posbbily cota de armazenamento modificada retornada por Get-AzsStorageQuota.</span><span class="sxs-lookup"><span data-stu-id="3ff8f-117">Posbbily modified storage quota returned by Get-AzsStorageQuota.</span></span>

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

### <span data-ttu-id="3ff8f-118">-Local</span><span class="sxs-lookup"><span data-stu-id="3ff8f-118">-Location</span></span>
<span data-ttu-id="3ff8f-119">Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="3ff8f-119">Resource location.</span></span>

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

### <span data-ttu-id="3ff8f-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="3ff8f-120">-Name</span></span>
<span data-ttu-id="3ff8f-121">O nome da cota de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="3ff8f-121">The name of the storage quota.</span></span>

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

### <span data-ttu-id="3ff8f-122">-NumberOfStorageAccounts</span><span class="sxs-lookup"><span data-stu-id="3ff8f-122">-NumberOfStorageAccounts</span></span>
<span data-ttu-id="3ff8f-123">Número total de contas de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="3ff8f-123">Total number of storage accounts.</span></span>

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

### <span data-ttu-id="3ff8f-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3ff8f-124">-ResourceId</span></span>
<span data-ttu-id="3ff8f-125">A ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="3ff8f-125">The resource id.</span></span>

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

### <span data-ttu-id="3ff8f-126">-Confirme</span><span class="sxs-lookup"><span data-stu-id="3ff8f-126">-Confirm</span></span>
<span data-ttu-id="3ff8f-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3ff8f-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3ff8f-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3ff8f-128">-WhatIf</span></span>
<span data-ttu-id="3ff8f-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="3ff8f-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3ff8f-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3ff8f-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3ff8f-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ff8f-131">CommonParameters</span></span>
<span data-ttu-id="3ff8f-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3ff8f-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ff8f-133">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ff8f-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ff8f-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3ff8f-134">INPUTS</span></span>

## <span data-ttu-id="3ff8f-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3ff8f-135">OUTPUTS</span></span>

### <span data-ttu-id="3ff8f-136">Microsoft. AzureStack. Management. Storage. admin. Models. StorageQuota</span><span class="sxs-lookup"><span data-stu-id="3ff8f-136">Microsoft.AzureStack.Management.Storage.Admin.Models.StorageQuota</span></span>

## <span data-ttu-id="3ff8f-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3ff8f-137">NOTES</span></span>

## <span data-ttu-id="3ff8f-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3ff8f-138">RELATED LINKS</span></span>

