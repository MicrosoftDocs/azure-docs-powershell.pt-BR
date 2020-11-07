---
external help file: Azs.Backup.Admin-help.xml
Module Name: Azs.Backup.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 35b937b810da65cc3cc2ed330198011ec108f9d6
ms.sourcegitcommit: 10ec909100a70acec94d42f6084e7bf0342c6854
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/19/2020
ms.locfileid: "93784954"
---
# <span data-ttu-id="3e1ac-101">Restore-AzsBackup</span><span class="sxs-lookup"><span data-stu-id="3e1ac-101">Restore-AzsBackup</span></span>

## <span data-ttu-id="3e1ac-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3e1ac-102">SYNOPSIS</span></span>
<span data-ttu-id="3e1ac-103">Restaurar um backup.</span><span class="sxs-lookup"><span data-stu-id="3e1ac-103">Restore a backup.</span></span>

## <span data-ttu-id="3e1ac-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3e1ac-104">SYNTAX</span></span>

### <span data-ttu-id="3e1ac-105">Backups_Restore (padrão)</span><span class="sxs-lookup"><span data-stu-id="3e1ac-105">Backups_Restore (Default)</span></span>
```
Restore-AzsBackup [-ResourceGroupName <String>] -Name <String> [-Location <String>]
 -DecryptionCertPath <String> -DecryptionCertPassword <SecureString> [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3e1ac-106">Identificação</span><span class="sxs-lookup"><span data-stu-id="3e1ac-106">ResourceId</span></span>
```
Restore-AzsBackup -DecryptionCertPath <String> -DecryptionCertPassword <SecureString> -ResourceId <String>
 [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3e1ac-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3e1ac-107">DESCRIPTION</span></span>
<span data-ttu-id="3e1ac-108">Restaurar um backup.</span><span class="sxs-lookup"><span data-stu-id="3e1ac-108">Restore a backup.</span></span>

## <span data-ttu-id="3e1ac-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3e1ac-109">EXAMPLES</span></span>

### <span data-ttu-id="3e1ac-110">EXEMPLO 1</span><span class="sxs-lookup"><span data-stu-id="3e1ac-110">EXAMPLE 1</span></span>
```
Restore-AzsBackup -Name 4e90bd2f-c7ab-47a3-a3c7-908cddd1ad0e -DecryptionCertPath $decryptionCertPath -DecryptionCertPassword $decryptionCertPassword
```

<span data-ttu-id="3e1ac-111">Restaure a partir de um backup de pilha do Azure.</span><span class="sxs-lookup"><span data-stu-id="3e1ac-111">Restore from an Azure Stack backup.</span></span>

## <span data-ttu-id="3e1ac-112">OS</span><span class="sxs-lookup"><span data-stu-id="3e1ac-112">PARAMETERS</span></span>

### <span data-ttu-id="3e1ac-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3e1ac-113">-AsJob</span></span>
<span data-ttu-id="3e1ac-114">Executar assíncrono como um trabalho e retornar o objeto de trabalho.</span><span class="sxs-lookup"><span data-stu-id="3e1ac-114">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="3e1ac-115">-DecryptionCertPassword</span><span class="sxs-lookup"><span data-stu-id="3e1ac-115">-DecryptionCertPassword</span></span>
<span data-ttu-id="3e1ac-116">Senha do certificado de descriptografia.</span><span class="sxs-lookup"><span data-stu-id="3e1ac-116">Password of the decryption cert.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e1ac-117">-DecryptionCertPath</span><span class="sxs-lookup"><span data-stu-id="3e1ac-117">-DecryptionCertPath</span></span>
<span data-ttu-id="3e1ac-118">Caminho para o arquivo de certificado de descriptografia com chave privada (. pfx).</span><span class="sxs-lookup"><span data-stu-id="3e1ac-118">Path to the decryption cert file with private key (.pfx).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e1ac-119">-Force</span><span class="sxs-lookup"><span data-stu-id="3e1ac-119">-Force</span></span>
<span data-ttu-id="3e1ac-120">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="3e1ac-120">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="3e1ac-121">-Local</span><span class="sxs-lookup"><span data-stu-id="3e1ac-121">-Location</span></span>
<span data-ttu-id="3e1ac-122">Nome do local para o backup.</span><span class="sxs-lookup"><span data-stu-id="3e1ac-122">Name of location to backup.</span></span>

```yaml
Type: System.String
Parameter Sets: Backups_Restore
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e1ac-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="3e1ac-123">-Name</span></span>
<span data-ttu-id="3e1ac-124">Nome do backup.</span><span class="sxs-lookup"><span data-stu-id="3e1ac-124">Name of the backup.</span></span>

```yaml
Type: System.String
Parameter Sets: Backups_Restore
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e1ac-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e1ac-125">-ResourceGroupName</span></span>
<span data-ttu-id="3e1ac-126">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="3e1ac-126">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Backups_Restore
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e1ac-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3e1ac-127">-ResourceId</span></span>
<span data-ttu-id="3e1ac-128">A ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="3e1ac-128">The resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e1ac-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="3e1ac-129">-Confirm</span></span>
<span data-ttu-id="3e1ac-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3e1ac-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3e1ac-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3e1ac-131">-WhatIf</span></span>
<span data-ttu-id="3e1ac-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="3e1ac-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3e1ac-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3e1ac-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3e1ac-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e1ac-134">CommonParameters</span></span>
<span data-ttu-id="3e1ac-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e1ac-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e1ac-136">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3e1ac-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e1ac-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3e1ac-137">INPUTS</span></span>

## <span data-ttu-id="3e1ac-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3e1ac-138">OUTPUTS</span></span>

## <span data-ttu-id="3e1ac-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3e1ac-139">NOTES</span></span>

## <span data-ttu-id="3e1ac-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3e1ac-140">RELATED LINKS</span></span>
