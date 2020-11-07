---
external help file: Azs.Backup.Admin-help.xml
Module Name: Azs.Backup.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: fd5f27a942a33082b9488f74cac2779107f7371f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93774502"
---
# <span data-ttu-id="8be74-101">Set-AzsBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="8be74-101">Set-AzsBackupConfiguration</span></span>

## <span data-ttu-id="8be74-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8be74-102">SYNOPSIS</span></span>
<span data-ttu-id="8be74-103">Defina a configuração de backup no local especificado.</span><span class="sxs-lookup"><span data-stu-id="8be74-103">Set the backup configuration at the specified location.</span></span>

## <span data-ttu-id="8be74-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8be74-104">SYNTAX</span></span>

### <span data-ttu-id="8be74-105">Atualização (padrão)</span><span class="sxs-lookup"><span data-stu-id="8be74-105">Update (Default)</span></span>
```
Set-AzsBackupConfiguration [-ResourceGroupName <String>] [-Location <String>] [-Path <String>]
 [-Username <String>] [-Password <SecureString>] [-EncryptionCertPath <String>]
 [-IsBackupSchedulerEnabled <Boolean>] [-BackupFrequencyInHours <Int32>] [-BackupRetentionPeriodInDays <Int32>]
 [-AsJob] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8be74-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="8be74-106">InputObject</span></span>
```
Set-AzsBackupConfiguration -InputObject <BackupLocation> [-Path <String>] [-Username <String>]
 [-Password <SecureString>] [-EncryptionCertPath <String>] [-IsBackupSchedulerEnabled <Boolean>]
 [-BackupFrequencyInHours <Int32>] [-BackupRetentionPeriodInDays <Int32>] [-AsJob] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8be74-107">Identificação</span><span class="sxs-lookup"><span data-stu-id="8be74-107">ResourceId</span></span>
```
Set-AzsBackupConfiguration -ResourceId <String> [-Path <String>] [-Username <String>]
 [-Password <SecureString>] [-EncryptionCertPath <String>] [-IsBackupSchedulerEnabled <Boolean>]
 [-BackupFrequencyInHours <Int32>] [-BackupRetentionPeriodInDays <Int32>] [-AsJob] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8be74-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8be74-108">DESCRIPTION</span></span>
<span data-ttu-id="8be74-109">Defina a configuração de backup no local especificado.</span><span class="sxs-lookup"><span data-stu-id="8be74-109">Set the backup configuration at the specified location.</span></span>

## <span data-ttu-id="8be74-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8be74-110">EXAMPLES</span></span>

### <span data-ttu-id="8be74-111">EXEMPLO 1</span><span class="sxs-lookup"><span data-stu-id="8be74-111">EXAMPLE 1</span></span>
```
Set-AzsBackupConfiguration -Path "\\***.***.***.***\Share" -Username "asdomain1\azurestackadmin" -Password $password  -EncryptionCertPath $encryptionCertPath
```

<span data-ttu-id="8be74-112">Defina a configuração de backup do Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="8be74-112">Set Azure Stack backup configuration.</span></span>

## <span data-ttu-id="8be74-113">OS</span><span class="sxs-lookup"><span data-stu-id="8be74-113">PARAMETERS</span></span>

### <span data-ttu-id="8be74-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8be74-114">-AsJob</span></span>
<span data-ttu-id="8be74-115">Executar assíncrono como um trabalho e retornar o objeto de trabalho.</span><span class="sxs-lookup"><span data-stu-id="8be74-115">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="8be74-116">-BackupFrequencyInHours</span><span class="sxs-lookup"><span data-stu-id="8be74-116">-BackupFrequencyInHours</span></span>
<span data-ttu-id="8be74-117">O intervalo, em horas, para a frequência com que o Agendador faz um backup.</span><span class="sxs-lookup"><span data-stu-id="8be74-117">The interval, in hours, for the frequency that the scheduler takes a backup.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8be74-118">-BackupRetentionPeriodInDays</span><span class="sxs-lookup"><span data-stu-id="8be74-118">-BackupRetentionPeriodInDays</span></span>
<span data-ttu-id="8be74-119">O período de retenção, em dias, para backups no local de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="8be74-119">The retention period, in days, for backups in the storage location.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8be74-120">-EncryptionCertPath</span><span class="sxs-lookup"><span data-stu-id="8be74-120">-EncryptionCertPath</span></span>
<span data-ttu-id="8be74-121">Caminho para o arquivo de certificado de criptografia com chave pública (. cer).</span><span class="sxs-lookup"><span data-stu-id="8be74-121">Path to the encryption cert file with public key (.cer).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8be74-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8be74-122">-InputObject</span></span>
<span data-ttu-id="8be74-123">Configuração de local de backup retornada por Get-AzsBackupConfiguration.</span><span class="sxs-lookup"><span data-stu-id="8be74-123">Backup location configuration returned by Get-AzsBackupConfiguration.</span></span>

```yaml
Type: Microsoft.AzureStack.Management.Backup.Admin.Models.BackupLocation
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8be74-124">-IsBackupSchedulerEnabled</span><span class="sxs-lookup"><span data-stu-id="8be74-124">-IsBackupSchedulerEnabled</span></span>
<span data-ttu-id="8be74-125">Se o Agendador de backup deve ser habilitado.</span><span class="sxs-lookup"><span data-stu-id="8be74-125">Whether the backup scheduler should be enabled.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8be74-126">-Local</span><span class="sxs-lookup"><span data-stu-id="8be74-126">-Location</span></span>
<span data-ttu-id="8be74-127">Local para configurar.</span><span class="sxs-lookup"><span data-stu-id="8be74-127">Location to configure.</span></span>

```yaml
Type: System.String
Parameter Sets: Update
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8be74-128">-Senha</span><span class="sxs-lookup"><span data-stu-id="8be74-128">-Password</span></span>
<span data-ttu-id="8be74-129">Senha necessária para acessar o local do backup.</span><span class="sxs-lookup"><span data-stu-id="8be74-129">Password required to access backup location.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8be74-130">-Caminho</span><span class="sxs-lookup"><span data-stu-id="8be74-130">-Path</span></span>
<span data-ttu-id="8be74-131">Local onde os backups serão armazenados.</span><span class="sxs-lookup"><span data-stu-id="8be74-131">Location where backups will be stored.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: BackupShare

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8be74-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8be74-132">-ResourceGroupName</span></span>
<span data-ttu-id="8be74-133">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="8be74-133">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Update
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8be74-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8be74-134">-ResourceId</span></span>
<span data-ttu-id="8be74-135">A ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="8be74-135">The resource id.</span></span>

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

### <span data-ttu-id="8be74-136">-Username</span><span class="sxs-lookup"><span data-stu-id="8be74-136">-Username</span></span>
<span data-ttu-id="8be74-137">Nome de usuário necessário para acessar o local do backup.</span><span class="sxs-lookup"><span data-stu-id="8be74-137">Username required to access backup location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8be74-138">-Confirme</span><span class="sxs-lookup"><span data-stu-id="8be74-138">-Confirm</span></span>
<span data-ttu-id="8be74-139">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8be74-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8be74-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8be74-140">-WhatIf</span></span>
<span data-ttu-id="8be74-141">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="8be74-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8be74-142">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8be74-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8be74-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8be74-143">CommonParameters</span></span>
<span data-ttu-id="8be74-144">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8be74-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8be74-145">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8be74-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8be74-146">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8be74-146">INPUTS</span></span>

## <span data-ttu-id="8be74-147">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8be74-147">OUTPUTS</span></span>

### <span data-ttu-id="8be74-148">Microsoft. AzureStack. Management. backup. admin. Models. BackupLocation</span><span class="sxs-lookup"><span data-stu-id="8be74-148">Microsoft.AzureStack.Management.Backup.Admin.Models.BackupLocation</span></span>

## <span data-ttu-id="8be74-149">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8be74-149">NOTES</span></span>

## <span data-ttu-id="8be74-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8be74-150">RELATED LINKS</span></span>
