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
ms.locfileid: "93426005"
---
# <span data-ttu-id="d8e36-101">Set-AzsBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="d8e36-101">Set-AzsBackupConfiguration</span></span>

## <span data-ttu-id="d8e36-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d8e36-102">SYNOPSIS</span></span>
<span data-ttu-id="d8e36-103">Defina a configuração de backup no local especificado.</span><span class="sxs-lookup"><span data-stu-id="d8e36-103">Set the backup configuration at the specified location.</span></span>

## <span data-ttu-id="d8e36-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d8e36-104">SYNTAX</span></span>

### <span data-ttu-id="d8e36-105">Atualização (padrão)</span><span class="sxs-lookup"><span data-stu-id="d8e36-105">Update (Default)</span></span>
```
Set-AzsBackupConfiguration [-ResourceGroupName <String>] [-Location <String>] [-Path <String>]
 [-Username <String>] [-Password <SecureString>] [-EncryptionKey <SecureString>]
 [-IsBackupSchedulerEnabled <Boolean>] [-BackupFrequencyInHours <Int32>] [-BackupRetentionPeriodInDays <Int32>]
 [-AsJob] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d8e36-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="d8e36-106">InputObject</span></span>
```
Set-AzsBackupConfiguration -InputObject <BackupLocation> [-Path <String>] [-Username <String>]
 [-Password <SecureString>] [-EncryptionKey <SecureString>] [-IsBackupSchedulerEnabled <Boolean>]
 [-BackupFrequencyInHours <Int32>] [-BackupRetentionPeriodInDays <Int32>] [-AsJob] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d8e36-107">Identificação</span><span class="sxs-lookup"><span data-stu-id="d8e36-107">ResourceId</span></span>
```
Set-AzsBackupConfiguration -ResourceId <String> [-Path <String>] [-Username <String>]
 [-Password <SecureString>] [-EncryptionKey <SecureString>] [-IsBackupSchedulerEnabled <Boolean>]
 [-BackupFrequencyInHours <Int32>] [-BackupRetentionPeriodInDays <Int32>] [-AsJob] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d8e36-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d8e36-108">DESCRIPTION</span></span>
<span data-ttu-id="d8e36-109">Defina a configuração de backup no local especificado.</span><span class="sxs-lookup"><span data-stu-id="d8e36-109">Set the backup configuration at the specified location.</span></span>

## <span data-ttu-id="d8e36-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d8e36-110">EXAMPLES</span></span>

### <span data-ttu-id="d8e36-111">--------------------------EXEMPLO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="d8e36-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Set-AzsBackupConfiguration -Path "\\***.***.***.***\Share" -Username "asdomain1\azurestackadmin" -Password $password  -EncryptionKey $encryptionKey
```

<span data-ttu-id="d8e36-112">Defina a configuração de backup do Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="d8e36-112">Set Azure Stack backup configuration.</span></span>

## <span data-ttu-id="d8e36-113">OS</span><span class="sxs-lookup"><span data-stu-id="d8e36-113">PARAMETERS</span></span>

### <span data-ttu-id="d8e36-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d8e36-114">-AsJob</span></span>
<span data-ttu-id="d8e36-115">Executar assíncrono como um trabalho e retornar o objeto de trabalho.</span><span class="sxs-lookup"><span data-stu-id="d8e36-115">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="d8e36-116">-BackupFrequencyInHours</span><span class="sxs-lookup"><span data-stu-id="d8e36-116">-BackupFrequencyInHours</span></span>
<span data-ttu-id="d8e36-117">O intervalo, em horas, para a frequência com que o Agendador faz um backup.</span><span class="sxs-lookup"><span data-stu-id="d8e36-117">The interval, in hours, for the frequency that the scheduler takes a backup.</span></span>

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

### <span data-ttu-id="d8e36-118">-BackupRetentionPeriodInDays</span><span class="sxs-lookup"><span data-stu-id="d8e36-118">-BackupRetentionPeriodInDays</span></span>
<span data-ttu-id="d8e36-119">O período de retenção, em dias, para backups no local de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="d8e36-119">The retention period, in days, for backups in the storage location.</span></span>

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

### <span data-ttu-id="d8e36-120">-EncryptionKey</span><span class="sxs-lookup"><span data-stu-id="d8e36-120">-EncryptionKey</span></span>
<span data-ttu-id="d8e36-121">Chave de criptografia usada para criptografar backups.</span><span class="sxs-lookup"><span data-stu-id="d8e36-121">Encryption key used to encrypt backups.</span></span>

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

### <span data-ttu-id="d8e36-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d8e36-122">-InputObject</span></span>
<span data-ttu-id="d8e36-123">Configuração de local de backup retornada por Get-AzsBackupConfiguration.</span><span class="sxs-lookup"><span data-stu-id="d8e36-123">Backup location configuration returned by Get-AzsBackupConfiguration.</span></span>

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

### <span data-ttu-id="d8e36-124">-IsBackupSchedulerEnabled</span><span class="sxs-lookup"><span data-stu-id="d8e36-124">-IsBackupSchedulerEnabled</span></span>
<span data-ttu-id="d8e36-125">Se o Agendador de backup deve ser habilitado.</span><span class="sxs-lookup"><span data-stu-id="d8e36-125">Whether the backup scheduler should be enabled.</span></span>

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

### <span data-ttu-id="d8e36-126">-Local</span><span class="sxs-lookup"><span data-stu-id="d8e36-126">-Location</span></span>
<span data-ttu-id="d8e36-127">Local para configurar.</span><span class="sxs-lookup"><span data-stu-id="d8e36-127">Location to configure.</span></span>

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

### <span data-ttu-id="d8e36-128">-Senha</span><span class="sxs-lookup"><span data-stu-id="d8e36-128">-Password</span></span>
<span data-ttu-id="d8e36-129">Senha necessária para acessar o local do backup.</span><span class="sxs-lookup"><span data-stu-id="d8e36-129">Password required to access backup location.</span></span>

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

### <span data-ttu-id="d8e36-130">-Caminho</span><span class="sxs-lookup"><span data-stu-id="d8e36-130">-Path</span></span>
<span data-ttu-id="d8e36-131">Local onde os backups serão armazenados.</span><span class="sxs-lookup"><span data-stu-id="d8e36-131">Location where backups will be stored.</span></span>

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

### <span data-ttu-id="d8e36-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8e36-132">-ResourceGroupName</span></span>
<span data-ttu-id="d8e36-133">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d8e36-133">Name of the resource group.</span></span>

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

### <span data-ttu-id="d8e36-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d8e36-134">-ResourceId</span></span>
<span data-ttu-id="d8e36-135">A ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="d8e36-135">The resource id.</span></span>

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

### <span data-ttu-id="d8e36-136">-Username</span><span class="sxs-lookup"><span data-stu-id="d8e36-136">-Username</span></span>
<span data-ttu-id="d8e36-137">Nome de usuário necessário para acessar o local do backup.</span><span class="sxs-lookup"><span data-stu-id="d8e36-137">Username required to access backup location.</span></span>

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

### <span data-ttu-id="d8e36-138">-Confirme</span><span class="sxs-lookup"><span data-stu-id="d8e36-138">-Confirm</span></span>
<span data-ttu-id="d8e36-139">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d8e36-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d8e36-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8e36-140">-WhatIf</span></span>
<span data-ttu-id="d8e36-141">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d8e36-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d8e36-142">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d8e36-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d8e36-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8e36-143">CommonParameters</span></span>
<span data-ttu-id="d8e36-144">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8e36-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8e36-145">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8e36-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8e36-146">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d8e36-146">INPUTS</span></span>

## <span data-ttu-id="d8e36-147">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d8e36-147">OUTPUTS</span></span>

### <span data-ttu-id="d8e36-148">Microsoft. AzureStack. Management. backup. admin. Models. BackupLocation</span><span class="sxs-lookup"><span data-stu-id="d8e36-148">Microsoft.AzureStack.Management.Backup.Admin.Models.BackupLocation</span></span>

## <span data-ttu-id="d8e36-149">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d8e36-149">NOTES</span></span>

## <span data-ttu-id="d8e36-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d8e36-150">RELATED LINKS</span></span>

