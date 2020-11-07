---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4cc08220a92dce5a49544cf958db79d7243b9ebb
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/08/2020
ms.locfileid: "93947057"
---
# <span data-ttu-id="997bf-101">New-AzsStorageQuota</span><span class="sxs-lookup"><span data-stu-id="997bf-101">New-AzsStorageQuota</span></span>

## <span data-ttu-id="997bf-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="997bf-102">SYNOPSIS</span></span>
<span data-ttu-id="997bf-103">Criar uma nova cota de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="997bf-103">Create a new storage quota.</span></span>

## <span data-ttu-id="997bf-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="997bf-104">SYNTAX</span></span>

```
New-AzsStorageQuota [-Name] <String> [[-CapacityInGb] <Int32>] [[-NumberOfStorageAccounts] <Int32>]
 [[-Location] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="997bf-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="997bf-105">DESCRIPTION</span></span>
<span data-ttu-id="997bf-106">Criar uma nova cota de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="997bf-106">Create a new storage quota.</span></span>

## <span data-ttu-id="997bf-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="997bf-107">EXAMPLES</span></span>

### <span data-ttu-id="997bf-108">EXEMPLO 1</span><span class="sxs-lookup"><span data-stu-id="997bf-108">EXAMPLE 1</span></span>
```
New-AzsStorageQuota -CapacityInGb 1000 -NumberOfStorageAccounts 100 -Name 'TestCreateStorageQuota'
```

<span data-ttu-id="997bf-109">Criar uma nova cota de armazenamento com valores especificados.</span><span class="sxs-lookup"><span data-stu-id="997bf-109">Create a new storage quota with specified values.</span></span>

## <span data-ttu-id="997bf-110">OS</span><span class="sxs-lookup"><span data-stu-id="997bf-110">PARAMETERS</span></span>

### <span data-ttu-id="997bf-111">-Nome</span><span class="sxs-lookup"><span data-stu-id="997bf-111">-Name</span></span>
<span data-ttu-id="997bf-112">O nome da cota de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="997bf-112">The name of the storage quota.</span></span>

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

### <span data-ttu-id="997bf-113">-CapacityInGb</span><span class="sxs-lookup"><span data-stu-id="997bf-113">-CapacityInGb</span></span>
<span data-ttu-id="997bf-114">Capacidade de máximo (GB).</span><span class="sxs-lookup"><span data-stu-id="997bf-114">Maxium capacity (GB).</span></span>

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

### <span data-ttu-id="997bf-115">-NumberOfStorageAccounts</span><span class="sxs-lookup"><span data-stu-id="997bf-115">-NumberOfStorageAccounts</span></span>
<span data-ttu-id="997bf-116">Número total de contas de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="997bf-116">Total number of storage accounts.</span></span>

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

### <span data-ttu-id="997bf-117">-Local</span><span class="sxs-lookup"><span data-stu-id="997bf-117">-Location</span></span>
<span data-ttu-id="997bf-118">Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="997bf-118">Resource location.</span></span>

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

### <span data-ttu-id="997bf-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="997bf-119">-WhatIf</span></span>
<span data-ttu-id="997bf-120">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="997bf-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="997bf-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="997bf-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="997bf-122">-Confirme</span><span class="sxs-lookup"><span data-stu-id="997bf-122">-Confirm</span></span>
<span data-ttu-id="997bf-123">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="997bf-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="997bf-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="997bf-124">CommonParameters</span></span>
<span data-ttu-id="997bf-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="997bf-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="997bf-126">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="997bf-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="997bf-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="997bf-127">INPUTS</span></span>

## <span data-ttu-id="997bf-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="997bf-128">OUTPUTS</span></span>

### <span data-ttu-id="997bf-129">Microsoft. AzureStack. Management. Storage. admin. Models. StorageQuota</span><span class="sxs-lookup"><span data-stu-id="997bf-129">Microsoft.AzureStack.Management.Storage.Admin.Models.StorageQuota</span></span>

## <span data-ttu-id="997bf-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="997bf-130">NOTES</span></span>

## <span data-ttu-id="997bf-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="997bf-131">RELATED LINKS</span></span>
