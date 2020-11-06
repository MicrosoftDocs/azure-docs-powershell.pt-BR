---
external help file: Azs.Backup.Admin-help.xml
Module Name: Azs.Backup.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 271426278c561ede4778e0ad69cf9ee4e6c0607e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93426105"
---
# <span data-ttu-id="daaf3-101">Set-AzsBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="daaf3-101">Set-AzsBackupConfiguration</span></span>

## <span data-ttu-id="daaf3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="daaf3-102">SYNOPSIS</span></span>
<span data-ttu-id="daaf3-103">Defina a configuração de backup no local especificado.</span><span class="sxs-lookup"><span data-stu-id="daaf3-103">Set the backup configuration at the specified location.</span></span>

## <span data-ttu-id="daaf3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="daaf3-104">SYNTAX</span></span>

### <span data-ttu-id="daaf3-105">Atualização (padrão)</span><span class="sxs-lookup"><span data-stu-id="daaf3-105">Update (Default)</span></span>
```
Set-AzsBackupConfiguration [-ResourceGroupName <String>] [-Location <String>] [-Path <String>]
 [-Username <String>] [-Password <SecureString>] [-EncryptionKey <SecureString>]
 [-IsBackupSchedulerEnabled <Boolean>] [-BackupFrequencyInHours <Int32>] [-BackupRetentionPeriodInDays <Int32>]
 [-AsJob] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="daaf3-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="daaf3-106">InputObject</span></span>
```
Set-AzsBackupConfiguration -InputObject <BackupLocation> [-Path <String>] [-Username <String>]
 [-Password <SecureString>] [-EncryptionKey <SecureString>] [-IsBackupSchedulerEnabled <Boolean>]
 [-BackupFrequencyInHours <Int32>] [-BackupRetentionPeriodInDays <Int32>] [-AsJob] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="daaf3-107">Identificação</span><span class="sxs-lookup"><span data-stu-id="daaf3-107">ResourceId</span></span>
```
Set-AzsBackupConfiguration -ResourceId <String> [-Path <String>] [-Username <String>]
 [-Password <SecureString>] [-EncryptionKey <SecureString>] [-IsBackupSchedulerEnabled <Boolean>]
 [-BackupFrequencyInHours <Int32>] [-BackupRetentionPeriodInDays <Int32>] [-AsJob] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="daaf3-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="daaf3-108">DESCRIPTION</span></span>
<span data-ttu-id="daaf3-109">Defina a configuração de backup no local especificado.</span><span class="sxs-lookup"><span data-stu-id="daaf3-109">Set the backup configuration at the specified location.</span></span>

## <span data-ttu-id="daaf3-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="daaf3-110">EXAMPLES</span></span>

### <span data-ttu-id="daaf3-111">--------------------------EXEMPLO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="daaf3-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Set-AzsBackupConfiguration -Path "\\***.***.***.***\Share" -Username "asdomain1\azurestackadmin" -Password $password  -EncryptionKey $encryptionKey
```

<span data-ttu-id="daaf3-112">Defina a configuração de backup do Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="daaf3-112">Set Azure Stack backup configuration.</span></span>

## <span data-ttu-id="daaf3-113">OS</span><span class="sxs-lookup"><span data-stu-id="daaf3-113">PARAMETERS</span></span>

### <span data-ttu-id="daaf3-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="daaf3-114">-AsJob</span></span>
<span data-ttu-id="daaf3-115">Executar assíncrono como um trabalho e retornar o objeto de trabalho.</span><span class="sxs-lookup"><span data-stu-id="daaf3-115">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="daaf3-116">-BackupFrequencyInHours</span><span class="sxs-lookup"><span data-stu-id="daaf3-116">-BackupFrequencyInHours</span></span>
<span data-ttu-id="daaf3-117">O intervalo, em horas, para a frequência com que o Agendador faz um backup.</span><span class="sxs-lookup"><span data-stu-id="daaf3-117">The interval, in hours, for the frequency that the scheduler takes a backup.</span></span>

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

### <span data-ttu-id="daaf3-118">-BackupRetentionPeriodInDays</span><span class="sxs-lookup"><span data-stu-id="daaf3-118">-BackupRetentionPeriodInDays</span></span>
<span data-ttu-id="daaf3-119">O período de retenção, em dias, para backups no local de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="daaf3-119">The retention period, in days, for backups in the storage location.</span></span>

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

### <span data-ttu-id="daaf3-120">-EncryptionKey</span><span class="sxs-lookup"><span data-stu-id="daaf3-120">-EncryptionKey</span></span>
<span data-ttu-id="daaf3-121">Chave de criptografia usada para criptografar backups.</span><span class="sxs-lookup"><span data-stu-id="daaf3-121">Encryption key used to encrypt backups.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="daaf3-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="daaf3-122">-InputObject</span></span>
<span data-ttu-id="daaf3-123">Configuração de local de backup retornada por Get-AzsBackupConfiguration.</span><span class="sxs-lookup"><span data-stu-id="daaf3-123">Backup location configuration returned by Get-AzsBackupConfiguration.</span></span>

```yaml
Type: BackupLocation
Parameter Sets: InputObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="daaf3-124">-IsBackupSchedulerEnabled</span><span class="sxs-lookup"><span data-stu-id="daaf3-124">-IsBackupSchedulerEnabled</span></span>
<span data-ttu-id="daaf3-125">Se o Agendador de backup deve ser habilitado.</span><span class="sxs-lookup"><span data-stu-id="daaf3-125">Whether the backup scheduler should be enabled.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="daaf3-126">-Local</span><span class="sxs-lookup"><span data-stu-id="daaf3-126">-Location</span></span>
<span data-ttu-id="daaf3-127">Local para configurar.</span><span class="sxs-lookup"><span data-stu-id="daaf3-127">Location to configure.</span></span>

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

### <span data-ttu-id="daaf3-128">-Senha</span><span class="sxs-lookup"><span data-stu-id="daaf3-128">-Password</span></span>
<span data-ttu-id="daaf3-129">Senha necessária para acessar o local do backup.</span><span class="sxs-lookup"><span data-stu-id="daaf3-129">Password required to access backup location.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="daaf3-130">-Caminho</span><span class="sxs-lookup"><span data-stu-id="daaf3-130">-Path</span></span>
<span data-ttu-id="daaf3-131">Local onde os backups serão armazenados.</span><span class="sxs-lookup"><span data-stu-id="daaf3-131">Location where backups will be stored.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: BackupShare

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="daaf3-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="daaf3-132">-ResourceGroupName</span></span>
<span data-ttu-id="daaf3-133">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="daaf3-133">Name of the resource group.</span></span>

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

### <span data-ttu-id="daaf3-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="daaf3-134">-ResourceId</span></span>
<span data-ttu-id="daaf3-135">A ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="daaf3-135">The resource id.</span></span>

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

### <span data-ttu-id="daaf3-136">-Username</span><span class="sxs-lookup"><span data-stu-id="daaf3-136">-Username</span></span>
<span data-ttu-id="daaf3-137">Nome de usuário necessário para acessar o local do backup.</span><span class="sxs-lookup"><span data-stu-id="daaf3-137">Username required to access backup location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="daaf3-138">-Confirme</span><span class="sxs-lookup"><span data-stu-id="daaf3-138">-Confirm</span></span>
<span data-ttu-id="daaf3-139">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="daaf3-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="daaf3-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="daaf3-140">-WhatIf</span></span>
<span data-ttu-id="daaf3-141">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="daaf3-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="daaf3-142">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="daaf3-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="daaf3-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="daaf3-143">CommonParameters</span></span>
<span data-ttu-id="daaf3-144">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="daaf3-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="daaf3-145">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="daaf3-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="daaf3-146">SENSORES</span><span class="sxs-lookup"><span data-stu-id="daaf3-146">INPUTS</span></span>

## <span data-ttu-id="daaf3-147">EXIBE</span><span class="sxs-lookup"><span data-stu-id="daaf3-147">OUTPUTS</span></span>

### <span data-ttu-id="daaf3-148">Microsoft. AzureStack. Management. backup. admin. Models. BackupLocation</span><span class="sxs-lookup"><span data-stu-id="daaf3-148">Microsoft.AzureStack.Management.Backup.Admin.Models.BackupLocation</span></span>

## <span data-ttu-id="daaf3-149">INFORMA</span><span class="sxs-lookup"><span data-stu-id="daaf3-149">NOTES</span></span>

## <span data-ttu-id="daaf3-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="daaf3-150">RELATED LINKS</span></span>

