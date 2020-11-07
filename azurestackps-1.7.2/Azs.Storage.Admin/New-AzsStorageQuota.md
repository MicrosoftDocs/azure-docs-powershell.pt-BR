---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 143f368b73aac490242e42f21ed76ee76ab012dc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93774163"
---
# <span data-ttu-id="12aa4-101">New-AzsStorageQuota</span><span class="sxs-lookup"><span data-stu-id="12aa4-101">New-AzsStorageQuota</span></span>

## <span data-ttu-id="12aa4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="12aa4-102">SYNOPSIS</span></span>
<span data-ttu-id="12aa4-103">Criar uma nova cota de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="12aa4-103">Create a new storage quota.</span></span>

## <span data-ttu-id="12aa4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="12aa4-104">SYNTAX</span></span>

```
New-AzsStorageQuota [-Name] <String> [[-CapacityInGb] <Int32>] [[-NumberOfStorageAccounts] <Int32>]
 [[-Location] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="12aa4-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="12aa4-105">DESCRIPTION</span></span>
<span data-ttu-id="12aa4-106">Criar uma nova cota de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="12aa4-106">Create a new storage quota.</span></span>

## <span data-ttu-id="12aa4-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="12aa4-107">EXAMPLES</span></span>

### <span data-ttu-id="12aa4-108">--------------------------EXEMPLO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="12aa4-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AzsStorageQuota -CapacityInGb 1000 -NumberOfStorageAccounts 100 -Name 'TestCreateStorageQuota'
```

<span data-ttu-id="12aa4-109">Criar uma nova cota de armazenamento com valores especificados.</span><span class="sxs-lookup"><span data-stu-id="12aa4-109">Create a new storage quota with specified values.</span></span>

## <span data-ttu-id="12aa4-110">OS</span><span class="sxs-lookup"><span data-stu-id="12aa4-110">PARAMETERS</span></span>

### <span data-ttu-id="12aa4-111">-CapacityInGb</span><span class="sxs-lookup"><span data-stu-id="12aa4-111">-CapacityInGb</span></span>
<span data-ttu-id="12aa4-112">Capacidade de máximo (GB).</span><span class="sxs-lookup"><span data-stu-id="12aa4-112">Maxium capacity (GB).</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: 500
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12aa4-113">-Local</span><span class="sxs-lookup"><span data-stu-id="12aa4-113">-Location</span></span>
<span data-ttu-id="12aa4-114">Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="12aa4-114">Resource location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12aa4-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="12aa4-115">-Name</span></span>
<span data-ttu-id="12aa4-116">O nome da cota de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="12aa4-116">The name of the storage quota.</span></span>

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

### <span data-ttu-id="12aa4-117">-NumberOfStorageAccounts</span><span class="sxs-lookup"><span data-stu-id="12aa4-117">-NumberOfStorageAccounts</span></span>
<span data-ttu-id="12aa4-118">Número total de contas de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="12aa4-118">Total number of storage accounts.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: 20
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12aa4-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="12aa4-119">-Confirm</span></span>
<span data-ttu-id="12aa4-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="12aa4-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="12aa4-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="12aa4-121">-WhatIf</span></span>
<span data-ttu-id="12aa4-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="12aa4-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="12aa4-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="12aa4-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="12aa4-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12aa4-124">CommonParameters</span></span>
<span data-ttu-id="12aa4-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12aa4-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12aa4-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12aa4-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12aa4-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="12aa4-127">INPUTS</span></span>

## <span data-ttu-id="12aa4-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="12aa4-128">OUTPUTS</span></span>

### <span data-ttu-id="12aa4-129">Microsoft. AzureStack. Management. Storage. admin. Models. StorageQuota</span><span class="sxs-lookup"><span data-stu-id="12aa4-129">Microsoft.AzureStack.Management.Storage.Admin.Models.StorageQuota</span></span>

## <span data-ttu-id="12aa4-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="12aa4-130">NOTES</span></span>

## <span data-ttu-id="12aa4-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="12aa4-131">RELATED LINKS</span></span>

