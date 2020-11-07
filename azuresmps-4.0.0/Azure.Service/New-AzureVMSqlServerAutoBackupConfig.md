---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 55E097F4-1F49-4196-9A8B-949FD5D9108A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4035487fa0363e6a7802966d9bc6422429723d94
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946199"
---
# <span data-ttu-id="bda1e-101">New-AzureVMSqlServerAutoBackupConfig</span><span class="sxs-lookup"><span data-stu-id="bda1e-101">New-AzureVMSqlServerAutoBackupConfig</span></span>

## <span data-ttu-id="bda1e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bda1e-102">SYNOPSIS</span></span>
<span data-ttu-id="bda1e-103">Cria um objeto de configuração para o backup automático do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="bda1e-103">Creates a configuration object for SQL Server automatic backup.</span></span>

## <span data-ttu-id="bda1e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bda1e-104">SYNTAX</span></span>

### <span data-ttu-id="bda1e-105">StorageUriSqlServerAutoBackup (padrão)</span><span class="sxs-lookup"><span data-stu-id="bda1e-105">StorageUriSqlServerAutoBackup (Default)</span></span>
```
New-AzureVMSqlServerAutoBackupConfig [-Enable] [[-RetentionPeriodInDays] <Int32>] [-EnableEncryption]
 [[-CertificatePassword] <SecureString>] [[-StorageUri] <Uri>] [[-StorageKey] <SecureString>]
 [-BackupSystemDbs] [-BackupScheduleType <String>] [-FullBackupFrequency <String>]
 [-FullBackupStartHour <Int32>] [-FullBackupWindowInHours <Int32>] [-LogBackupFrequencyInMinutes <Int32>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="bda1e-106">StorageContextSqlServerAutoBackup</span><span class="sxs-lookup"><span data-stu-id="bda1e-106">StorageContextSqlServerAutoBackup</span></span>
```
New-AzureVMSqlServerAutoBackupConfig [-Enable] [[-RetentionPeriodInDays] <Int32>] [-EnableEncryption]
 [[-CertificatePassword] <SecureString>] [[-StorageContext] <AzureStorageContext>] [[-StorageUri] <Uri>]
 [[-StorageKey] <SecureString>] [-BackupSystemDbs] [-BackupScheduleType <String>]
 [-FullBackupFrequency <String>] [-FullBackupStartHour <Int32>] [-FullBackupWindowInHours <Int32>]
 [-LogBackupFrequencyInMinutes <Int32>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="bda1e-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="bda1e-107">DESCRIPTION</span></span>
<span data-ttu-id="bda1e-108">O cmdlet **New-AzureVMSqlServerAutoBackupConfig** cria um objeto de configuração para o backup automático do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="bda1e-108">The **New-AzureVMSqlServerAutoBackupConfig** cmdlet creates a configuration object for SQL Server automatic backup.</span></span>

## <span data-ttu-id="bda1e-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bda1e-109">EXAMPLES</span></span>

### <span data-ttu-id="bda1e-110">Exemplo 1: criar uma configuração de backup automático usando o URI de armazenamento e a chave de conta</span><span class="sxs-lookup"><span data-stu-id="bda1e-110">Example 1: Create an auto-backup configuration using storage URI and account key</span></span>
```
PS C:\> $ABS = New-AzureVMSqlServerAutoBackupConfig -Enable -RetentionPeriod 10 -StorageUri $StorageUrl -StorageKey $StorageAccountKeySecure
Enable                : True
EnableEncryption      : False
RetentionPeriodInDays : 10
```

<span data-ttu-id="bda1e-111">Esse comando cria um objeto de configuração de backup automático especificando a URL de armazenamento e a chave de conta.</span><span class="sxs-lookup"><span data-stu-id="bda1e-111">This command creates an auto-backup configuration object by specifying storage URL and account key.</span></span>

### <span data-ttu-id="bda1e-112">Exemplo 2: criar uma configuração de backup automático usando contexto de armazenamento</span><span class="sxs-lookup"><span data-stu-id="bda1e-112">Example 2: Create an auto-backup configuration using storage context</span></span>
```
PS C:\> $ABS = New-AzureVMSqlServerAutoBackupConfig -StorageContext $StorageContext -Enable -RetentionPeriod 10
Enable                : True
EnableEncryption      : False
RetentionPeriodInDays : 10
```

<span data-ttu-id="bda1e-113">Esse comando cria um objeto de configuração de backup automático especificando o contexto de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="bda1e-113">This command creates an auto-backup configuration object by specifying storage context.</span></span>

### <span data-ttu-id="bda1e-114">Exemplo 3: criar uma configuração de backup automático usando contexto de armazenamento com criptografia e senha</span><span class="sxs-lookup"><span data-stu-id="bda1e-114">Example 3: Create an auto-backup configuration using storage context with encryption and password</span></span>
```
PS C:\> $ABS = New-AzureVMSqlServerAutoBackupConfig -StorageContext $StorageContext -Enable -RetentionPeriod 10 -EnableEncryption -CertificatePassword $CertPasswd
Enable                : True
EnableEncryption      : True
RetentionPeriodInDays : 10
```

<span data-ttu-id="bda1e-115">Esse comando cria um objeto de configuração de backup automático especificando o contexto de armazenamento e habilitando a opção de criptografia com senha.</span><span class="sxs-lookup"><span data-stu-id="bda1e-115">This command creates an auto-backup configuration object by specifying Storage context and enabling encryption option with password.</span></span>
<span data-ttu-id="bda1e-116">O ist certificatepassword armazenado na variável chamada $CertPasswd.</span><span class="sxs-lookup"><span data-stu-id="bda1e-116">The certificatepassword ist stored in the variable named $CertPasswd.</span></span>

## <span data-ttu-id="bda1e-117">OS</span><span class="sxs-lookup"><span data-stu-id="bda1e-117">PARAMETERS</span></span>

### <span data-ttu-id="bda1e-118">-BackupScheduleType</span><span class="sxs-lookup"><span data-stu-id="bda1e-118">-BackupScheduleType</span></span>
<span data-ttu-id="bda1e-119">Tipo de agendamento de backup, manual ou automatizado</span><span class="sxs-lookup"><span data-stu-id="bda1e-119">Backup schedule type, manual or automated</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bda1e-120">-BackupSystemDbs</span><span class="sxs-lookup"><span data-stu-id="bda1e-120">-BackupSystemDbs</span></span>
<span data-ttu-id="bda1e-121">Bancos de dados do sistema de backup</span><span class="sxs-lookup"><span data-stu-id="bda1e-121">Backup system databases</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bda1e-122">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="bda1e-122">-CertificatePassword</span></span>
<span data-ttu-id="bda1e-123">Especifica uma senha para criptografar o certificado que é usado para executar backups criptografados do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="bda1e-123">Specifies a password to encrypt the certificate that is used to perform SQL Server encrypted backups.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bda1e-124">-Habilitar</span><span class="sxs-lookup"><span data-stu-id="bda1e-124">-Enable</span></span>
<span data-ttu-id="bda1e-125">Indica que o backup automatizado para a máquina virtual do SQL Server está habilitado.</span><span class="sxs-lookup"><span data-stu-id="bda1e-125">Indicates that automated backup for the SQL Server virtual machine is enabled.</span></span>
<span data-ttu-id="bda1e-126">Se você usar esse parâmetro, o backup automatizado definirá um agendamento de backup para todos os bancos de dados novos e atuais.</span><span class="sxs-lookup"><span data-stu-id="bda1e-126">If you use this parameter, automated backup sets a backup schedule for all current and new databases.</span></span>
<span data-ttu-id="bda1e-127">Isso atualiza as configurações de backup gerenciado para acompanhar este cronograma.</span><span class="sxs-lookup"><span data-stu-id="bda1e-127">This updates your Managed Backup settings to follow this schedule.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bda1e-128">-EnableEncryption</span><span class="sxs-lookup"><span data-stu-id="bda1e-128">-EnableEncryption</span></span>
<span data-ttu-id="bda1e-129">Indica que a criptografia está habilitada.</span><span class="sxs-lookup"><span data-stu-id="bda1e-129">Indicates that encryption is enabled.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bda1e-130">-FullBackupFrequency</span><span class="sxs-lookup"><span data-stu-id="bda1e-130">-FullBackupFrequency</span></span>
<span data-ttu-id="bda1e-131">Frequência de backup total do SQL Server, diária ou semanal</span><span class="sxs-lookup"><span data-stu-id="bda1e-131">Sql Server Full Backup frequency, daily or week</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bda1e-132">-FullBackupStartHour</span><span class="sxs-lookup"><span data-stu-id="bda1e-132">-FullBackupStartHour</span></span>
<span data-ttu-id="bda1e-133">Hora do dia (0-23) quando o backup completo do SQL Server deve começar</span><span class="sxs-lookup"><span data-stu-id="bda1e-133">Hour of the day (0-23) when the Sql Server Full Backup should start</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bda1e-134">-FullBackupWindowInHours</span><span class="sxs-lookup"><span data-stu-id="bda1e-134">-FullBackupWindowInHours</span></span>
<span data-ttu-id="bda1e-135">Janela de backup completo do SQL Server em horas</span><span class="sxs-lookup"><span data-stu-id="bda1e-135">Sql Server Full Backup window in hours</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bda1e-136">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="bda1e-136">-InformationAction</span></span>
<span data-ttu-id="bda1e-137">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="bda1e-137">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="bda1e-138">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="bda1e-138">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="bda1e-139">Contínuo</span><span class="sxs-lookup"><span data-stu-id="bda1e-139">Continue</span></span>
- <span data-ttu-id="bda1e-140">Ignorar</span><span class="sxs-lookup"><span data-stu-id="bda1e-140">Ignore</span></span>
- <span data-ttu-id="bda1e-141">Inquire</span><span class="sxs-lookup"><span data-stu-id="bda1e-141">Inquire</span></span>
- <span data-ttu-id="bda1e-142">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="bda1e-142">SilentlyContinue</span></span>
- <span data-ttu-id="bda1e-143">Finaliza</span><span class="sxs-lookup"><span data-stu-id="bda1e-143">Stop</span></span>
- <span data-ttu-id="bda1e-144">Suspensão</span><span class="sxs-lookup"><span data-stu-id="bda1e-144">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bda1e-145">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="bda1e-145">-InformationVariable</span></span>
<span data-ttu-id="bda1e-146">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="bda1e-146">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bda1e-147">-LogBackupFrequencyInMinutes</span><span class="sxs-lookup"><span data-stu-id="bda1e-147">-LogBackupFrequencyInMinutes</span></span>
<span data-ttu-id="bda1e-148">Frequência de backup de log do SQL Server, a cada 1-60 minutos</span><span class="sxs-lookup"><span data-stu-id="bda1e-148">Sql Server Log Backup frequency, once every 1-60 minutes</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bda1e-149">-Perfil</span><span class="sxs-lookup"><span data-stu-id="bda1e-149">-Profile</span></span>
<span data-ttu-id="bda1e-150">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="bda1e-150">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="bda1e-151">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="bda1e-151">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bda1e-152">-RetentionPeriodInDays</span><span class="sxs-lookup"><span data-stu-id="bda1e-152">-RetentionPeriodInDays</span></span>
<span data-ttu-id="bda1e-153">Especifica a duração do período de retenção em dias.</span><span class="sxs-lookup"><span data-stu-id="bda1e-153">Specifies the length of the retention period in days.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bda1e-154">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="bda1e-154">-StorageContext</span></span>
<span data-ttu-id="bda1e-155">Especifica a conta de armazenamento a ser usada para armazenar backups.</span><span class="sxs-lookup"><span data-stu-id="bda1e-155">Specifies the storage account to be used to store backups.</span></span>
<span data-ttu-id="bda1e-156">Padrão é a conta de armazenamento associada à máquina virtual do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="bda1e-156">Default is the storage account associated with the SQL Server virtual machine.</span></span>

```yaml
Type: AzureStorageContext
Parameter Sets: StorageContextSqlServerAutoBackup
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bda1e-157">-StorageKey</span><span class="sxs-lookup"><span data-stu-id="bda1e-157">-StorageKey</span></span>
<span data-ttu-id="bda1e-158">Especifica a chave de armazenamento da conta de armazenamento BLOB.</span><span class="sxs-lookup"><span data-stu-id="bda1e-158">Specifies the storage key of the blob storage account.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bda1e-159">-StorageUri</span><span class="sxs-lookup"><span data-stu-id="bda1e-159">-StorageUri</span></span>
<span data-ttu-id="bda1e-160">Especifica um URI para a conta de armazenamento BLOB.</span><span class="sxs-lookup"><span data-stu-id="bda1e-160">Specifies a URI to the blob storage account.</span></span>

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bda1e-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bda1e-161">CommonParameters</span></span>
<span data-ttu-id="bda1e-162">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bda1e-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bda1e-163">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bda1e-163">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bda1e-164">SENSORES</span><span class="sxs-lookup"><span data-stu-id="bda1e-164">INPUTS</span></span>

## <span data-ttu-id="bda1e-165">EXIBE</span><span class="sxs-lookup"><span data-stu-id="bda1e-165">OUTPUTS</span></span>

## <span data-ttu-id="bda1e-166">INFORMA</span><span class="sxs-lookup"><span data-stu-id="bda1e-166">NOTES</span></span>

## <span data-ttu-id="bda1e-167">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bda1e-167">RELATED LINKS</span></span>

[<span data-ttu-id="bda1e-168">New-AzureVMSqlServerAutoPatchingConfig</span><span class="sxs-lookup"><span data-stu-id="bda1e-168">New-AzureVMSqlServerAutoPatchingConfig</span></span>](./New-AzureVMSqlServerAutoPatchingConfig.md)


