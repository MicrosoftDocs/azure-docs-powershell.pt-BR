---
external help file: Azs.Backup.Admin-help.xml
Module Name: Azs.Backup.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 573a47b3684020817130e1d41c764abef717de0a
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/08/2020
ms.locfileid: "93946805"
---
# <span data-ttu-id="c4d65-101">Restore-AzsBackup</span><span class="sxs-lookup"><span data-stu-id="c4d65-101">Restore-AzsBackup</span></span>

## <span data-ttu-id="c4d65-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c4d65-102">SYNOPSIS</span></span>
<span data-ttu-id="c4d65-103">Restaurar um backup.</span><span class="sxs-lookup"><span data-stu-id="c4d65-103">Restore a backup.</span></span>

## <span data-ttu-id="c4d65-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c4d65-104">SYNTAX</span></span>

### <span data-ttu-id="c4d65-105">Backups_Restore (padrão)</span><span class="sxs-lookup"><span data-stu-id="c4d65-105">Backups_Restore (Default)</span></span>
```
Restore-AzsBackup [-ResourceGroupName <String>] -Name <String> [-Location <String>] [-AsJob] [-Force] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c4d65-106">Identificação</span><span class="sxs-lookup"><span data-stu-id="c4d65-106">ResourceId</span></span>
```
Restore-AzsBackup -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c4d65-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c4d65-107">DESCRIPTION</span></span>
<span data-ttu-id="c4d65-108">Restaurar um backup.</span><span class="sxs-lookup"><span data-stu-id="c4d65-108">Restore a backup.</span></span>

## <span data-ttu-id="c4d65-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c4d65-109">EXAMPLES</span></span>

### <span data-ttu-id="c4d65-110">--------------------------EXEMPLO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="c4d65-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Restore-AzsBackup -Backup 4e90bd2f-c7ab-47a3-a3c7-908cddd1ad0e
```

<span data-ttu-id="c4d65-111">Restaure a partir de um backup de pilha do Azure.</span><span class="sxs-lookup"><span data-stu-id="c4d65-111">Restore from an Azure Stack backup.</span></span>

## <span data-ttu-id="c4d65-112">OS</span><span class="sxs-lookup"><span data-stu-id="c4d65-112">PARAMETERS</span></span>

### <span data-ttu-id="c4d65-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c4d65-113">-AsJob</span></span>
<span data-ttu-id="c4d65-114">Executar assíncrono como um trabalho e retornar o objeto de trabalho.</span><span class="sxs-lookup"><span data-stu-id="c4d65-114">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="c4d65-115">-Force</span><span class="sxs-lookup"><span data-stu-id="c4d65-115">-Force</span></span>
<span data-ttu-id="c4d65-116">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="c4d65-116">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="c4d65-117">-Local</span><span class="sxs-lookup"><span data-stu-id="c4d65-117">-Location</span></span>
<span data-ttu-id="c4d65-118">Nome do local para o backup.</span><span class="sxs-lookup"><span data-stu-id="c4d65-118">Name of location to backup.</span></span>

```yaml
Type: String
Parameter Sets: Backups_Restore
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4d65-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="c4d65-119">-Name</span></span>
<span data-ttu-id="c4d65-120">Nome do backup.</span><span class="sxs-lookup"><span data-stu-id="c4d65-120">Name of the backup.</span></span>

```yaml
Type: String
Parameter Sets: Backups_Restore
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4d65-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4d65-121">-ResourceGroupName</span></span>
<span data-ttu-id="c4d65-122">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c4d65-122">Name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: Backups_Restore
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4d65-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c4d65-123">-ResourceId</span></span>
<span data-ttu-id="c4d65-124">{{Descrição do ResourceId}}</span><span class="sxs-lookup"><span data-stu-id="c4d65-124">{{Fill ResourceId Description}}</span></span>

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

### <span data-ttu-id="c4d65-125">-Confirme</span><span class="sxs-lookup"><span data-stu-id="c4d65-125">-Confirm</span></span>
<span data-ttu-id="c4d65-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c4d65-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c4d65-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c4d65-127">-WhatIf</span></span>
<span data-ttu-id="c4d65-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c4d65-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c4d65-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c4d65-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c4d65-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4d65-130">CommonParameters</span></span>
<span data-ttu-id="c4d65-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4d65-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4d65-132">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c4d65-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4d65-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c4d65-133">INPUTS</span></span>

## <span data-ttu-id="c4d65-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c4d65-134">OUTPUTS</span></span>

## <span data-ttu-id="c4d65-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c4d65-135">NOTES</span></span>

## <span data-ttu-id="c4d65-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c4d65-136">RELATED LINKS</span></span>

