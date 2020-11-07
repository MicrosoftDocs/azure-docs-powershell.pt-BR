---
external help file: Azs.Backup.Admin-help.xml
Module Name: Azs.Backup.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 460d24e091a702cfee32b8c5b7d9c3a8016e73b3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93774501"
---
# <span data-ttu-id="ced58-101">Start-AzsBackup</span><span class="sxs-lookup"><span data-stu-id="ced58-101">Start-AzsBackup</span></span>

## <span data-ttu-id="ced58-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ced58-102">SYNOPSIS</span></span>
<span data-ttu-id="ced58-103">Fazer backup de um local específico.</span><span class="sxs-lookup"><span data-stu-id="ced58-103">Back up a specific location.</span></span>

## <span data-ttu-id="ced58-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ced58-104">SYNTAX</span></span>

### <span data-ttu-id="ced58-105">CreateBackup (padrão)</span><span class="sxs-lookup"><span data-stu-id="ced58-105">CreateBackup (Default)</span></span>
```
Start-AzsBackup [-ResourceGroupName <String>] [-Location <String>] [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ced58-106">CreateBackup_FromResourceId</span><span class="sxs-lookup"><span data-stu-id="ced58-106">CreateBackup_FromResourceId</span></span>
```
Start-AzsBackup -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ced58-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ced58-107">DESCRIPTION</span></span>
<span data-ttu-id="ced58-108">Fazer backup de um local específico.</span><span class="sxs-lookup"><span data-stu-id="ced58-108">Back up a specific location.</span></span>

## <span data-ttu-id="ced58-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ced58-109">EXAMPLES</span></span>

### <span data-ttu-id="ced58-110">EXEMPLO 1</span><span class="sxs-lookup"><span data-stu-id="ced58-110">EXAMPLE 1</span></span>
```
Start-AzsBackup
```

<span data-ttu-id="ced58-111">Inicie um backup do Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="ced58-111">Start an Azure Stack backup.</span></span>

## <span data-ttu-id="ced58-112">OS</span><span class="sxs-lookup"><span data-stu-id="ced58-112">PARAMETERS</span></span>

### <span data-ttu-id="ced58-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ced58-113">-AsJob</span></span>
<span data-ttu-id="ced58-114">Executar assíncrono como um trabalho e retornar o objeto de trabalho.</span><span class="sxs-lookup"><span data-stu-id="ced58-114">Run asynchronous as a job and return the job object.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ced58-115">-Force</span><span class="sxs-lookup"><span data-stu-id="ced58-115">-Force</span></span>
<span data-ttu-id="ced58-116">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="ced58-116">Don't ask for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ced58-117">-Local</span><span class="sxs-lookup"><span data-stu-id="ced58-117">-Location</span></span>
<span data-ttu-id="ced58-118">Nome do local de backup.</span><span class="sxs-lookup"><span data-stu-id="ced58-118">Name of the backup location.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateBackup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ced58-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ced58-119">-ResourceGroupName</span></span>
<span data-ttu-id="ced58-120">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ced58-120">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateBackup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ced58-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ced58-121">-ResourceId</span></span>
<span data-ttu-id="ced58-122">A ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="ced58-122">The resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateBackup_FromResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ced58-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="ced58-123">-Confirm</span></span>
<span data-ttu-id="ced58-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ced58-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ced58-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ced58-125">-WhatIf</span></span>
<span data-ttu-id="ced58-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ced58-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ced58-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ced58-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ced58-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ced58-128">CommonParameters</span></span>
<span data-ttu-id="ced58-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ced58-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ced58-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ced58-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ced58-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ced58-131">INPUTS</span></span>

## <span data-ttu-id="ced58-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ced58-132">OUTPUTS</span></span>

### <span data-ttu-id="ced58-133">Microsoft. AzureStack. Management. backup. admin. Models. LongRunningOperationStatus</span><span class="sxs-lookup"><span data-stu-id="ced58-133">Microsoft.AzureStack.Management.Backup.Admin.Models.LongRunningOperationStatus</span></span>

## <span data-ttu-id="ced58-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ced58-134">NOTES</span></span>

## <span data-ttu-id="ced58-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ced58-135">RELATED LINKS</span></span>
