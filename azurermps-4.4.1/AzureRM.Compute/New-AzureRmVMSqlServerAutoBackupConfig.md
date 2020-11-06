---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
Module Name: Azure
ms.assetid: 0AC17275-17A9-47DE-BF04-C1A51DF057DC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVMSqlServerAutoBackupConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVMSqlServerAutoBackupConfig.md
ms.openlocfilehash: 2617ca54050f6a37fcc5714fe80e2f2d50e33e40
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610840"
---
# <span data-ttu-id="8e5e6-101">New-AzureVMSqlServerAutoBackupConfig</span><span class="sxs-lookup"><span data-stu-id="8e5e6-101">New-AzureVMSqlServerAutoBackupConfig</span></span>

## <span data-ttu-id="8e5e6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8e5e6-102">SYNOPSIS</span></span>
<span data-ttu-id="8e5e6-103">Cria um objeto de configuração para o backup automático do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="8e5e6-103">Creates a configuration object for SQL Server automatic backup.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8e5e6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8e5e6-104">SYNTAX</span></span>

### <span data-ttu-id="8e5e6-105">StorageUriSqlServerAutoBackup (padrão)</span><span class="sxs-lookup"><span data-stu-id="8e5e6-105">StorageUriSqlServerAutoBackup (Default)</span></span>
```
New-AzureVMSqlServerAutoBackupConfig [-Enable] [[-RetentionPeriodInDays] <Int32>] [-EnableEncryption]
 [[-CertificatePassword] <SecureString>] [[-StorageUri] <Uri>] [[-StorageKey] <SecureString>]
 [-BackupSystemDbs] [-BackupScheduleType <String>] [-FullBackupFrequency <String>]
 [-FullBackupStartHour <Int32>] [-FullBackupWindowInHours <Int32>] [-LogBackupFrequencyInMinutes <Int32>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="8e5e6-106">StorageContextSqlServerAutoBackup</span><span class="sxs-lookup"><span data-stu-id="8e5e6-106">StorageContextSqlServerAutoBackup</span></span>
```
New-AzureVMSqlServerAutoBackupConfig [-Enable] [[-RetentionPeriodInDays] <Int32>] [-EnableEncryption]
 [[-CertificatePassword] <SecureString>] [[-StorageContext] <IStorageContext>] [[-StorageUri] <Uri>]
 [[-StorageKey] <SecureString>] [-BackupSystemDbs] [-BackupScheduleType <String>]
 [-FullBackupFrequency <String>] [-FullBackupStartHour <Int32>] [-FullBackupWindowInHours <Int32>]
 [-LogBackupFrequencyInMinutes <Int32>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="8e5e6-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8e5e6-107">DESCRIPTION</span></span>
<span data-ttu-id="8e5e6-108">O cmdlet **New-AzureVMSqlServerAutoBackupConfig** cria um objeto de configuração para o backup automático do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="8e5e6-108">The **New-AzureVMSqlServerAutoBackupConfig** cmdlet creates a configuration object for SQL Server automatic backup.</span></span>

## <span data-ttu-id="8e5e6-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8e5e6-109">EXAMPLES</span></span>

### <span data-ttu-id="8e5e6-110">Exemplo 1: criar uma configuração de backup automática usando o URI de armazenamento e a chave de conta</span><span class="sxs-lookup"><span data-stu-id="8e5e6-110">Example 1: Create an automatic backup configuration using storage URI and account key</span></span>
```
PS C:\> $AutoBackupConfig = New-AzureVMSqlServerAutoBackupConfig -Enable -RetentionPeriod 10 -StorageUri "\\contoso\StorageGeneral" -StorageKey "< Storage Key for ContosoGeneral >"
Enable                : True
EnableEncryption      : False
RetentionPeriodInDays : 10
```

<span data-ttu-id="8e5e6-111">Esse comando cria um objeto de configuração de backup automático especificando a chave da conta e o URI de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="8e5e6-111">This command creates an automatic backup configuration object by specifying storage URI and account key.</span></span>
<span data-ttu-id="8e5e6-112">O backup automático é ativado e os backups automáticos são mantidos por 10 dias.</span><span class="sxs-lookup"><span data-stu-id="8e5e6-112">Automatic backup is enabled and automatic backups are kept for 10 days.</span></span>
<span data-ttu-id="8e5e6-113">O comando armazena o resultado na variável $AutoBackupConfig.</span><span class="sxs-lookup"><span data-stu-id="8e5e6-113">The command stores the result in the $AutoBackupConfig variable.</span></span>
<span data-ttu-id="8e5e6-114">Você pode especificar esse item de configuração para outros cmdlets, como o cmdlet Set-AzureRmVMSqlServerExtension.</span><span class="sxs-lookup"><span data-stu-id="8e5e6-114">You can specify this configuration item for other cmdlets, such as the Set-AzureRmVMSqlServerExtension cmdlet.</span></span>

### <span data-ttu-id="8e5e6-115">Exemplo 2: criar uma configuração de backup automática usando contexto de armazenamento</span><span class="sxs-lookup"><span data-stu-id="8e5e6-115">Example 2: Create an automatic backup configuration using storage context</span></span>
```
PS C:\> $StorageContext = New-AzureStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral >"
PS C:\> $AutoBackupConfig = New-AzureVMSqlServerAutoBackupConfig -StorageContext $StorageContext -Enable -RetentionPeriod 10
Enable                : True
EnableEncryption      : False
RetentionPeriodInDays : 10
```

<span data-ttu-id="8e5e6-116">O primeiro comando cria um contexto de armazenamento e, em seguida, armazena-o na variável $StorageContext.</span><span class="sxs-lookup"><span data-stu-id="8e5e6-116">The first command creates a storage context, and then stores it in the $StorageContext variable.</span></span>
<span data-ttu-id="8e5e6-117">Para obter mais informações, consulte New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="8e5e6-117">For more information, see New-AzureStorageContext.</span></span>

<span data-ttu-id="8e5e6-118">O segundo comando cria um objeto de configuração de backup automático especificando o contexto de armazenamento em $StorageContext.</span><span class="sxs-lookup"><span data-stu-id="8e5e6-118">The second command creates an automatic backup configuration object by specifying the storage context in $StorageContext.</span></span>
<span data-ttu-id="8e5e6-119">O backup automático é ativado e os backups automáticos são mantidos por 10 dias.</span><span class="sxs-lookup"><span data-stu-id="8e5e6-119">Automatic backup is enabled and automatic backups are kept for 10 days.</span></span>

### <span data-ttu-id="8e5e6-120">Exemplo 3: criar uma configuração de backup automática usando contexto de armazenamento com criptografia e senha</span><span class="sxs-lookup"><span data-stu-id="8e5e6-120">Example 3: Create an automatic backup configuration using storage context with encryption and password</span></span>
```
PS C:\> $StorageContext = New-AzureVMSqlServerAutoBackupConfig -StorageContext $StorageContext -Enable -RetentionPeriod 10 -EnableEncryption -CertificatePassword $CertificatePassword
Enable                : True
EnableEncryption      : True
RetentionPeriodInDays : 10
```

<span data-ttu-id="8e5e6-121">Esse comando cria e armazena um objeto de configuração de backup automático.</span><span class="sxs-lookup"><span data-stu-id="8e5e6-121">This command creates and stores an automatic backup configuration object.</span></span>
<span data-ttu-id="8e5e6-122">O comando especifica o contexto de armazenamento criado em um exemplo anterior.</span><span class="sxs-lookup"><span data-stu-id="8e5e6-122">The command specifies the storage context created in a previous example.</span></span>
<span data-ttu-id="8e5e6-123">O comando habilita a criptografia com senha.</span><span class="sxs-lookup"><span data-stu-id="8e5e6-123">The command enables encryption with password.</span></span>
<span data-ttu-id="8e5e6-124">A senha foi armazenada anteriormente como uma cadeia de caracteres segura na variável $CertificatePassword.</span><span class="sxs-lookup"><span data-stu-id="8e5e6-124">The password was previously stored as a secure string in the $CertificatePassword variable.</span></span>
<span data-ttu-id="8e5e6-125">Para criar uma cadeia de caracteres segura, use o cmdlet ConvertTo-SecureString.</span><span class="sxs-lookup"><span data-stu-id="8e5e6-125">To create a secure string, use the ConvertTo-SecureString cmdlet.</span></span>

## <span data-ttu-id="8e5e6-126">OS</span><span class="sxs-lookup"><span data-stu-id="8e5e6-126">PARAMETERS</span></span>

### <span data-ttu-id="8e5e6-127">-Habilitar</span><span class="sxs-lookup"><span data-stu-id="8e5e6-127">-Enable</span></span>
<span data-ttu-id="8e5e6-128">Indica que o backup automatizado para a máquina virtual do SQL Server está habilitado.</span><span class="sxs-lookup"><span data-stu-id="8e5e6-128">Indicates that automated backup for the SQL Server virtual machine is enabled.</span></span>
<span data-ttu-id="8e5e6-129">Se você especificar esse parâmetro, o backup automatizado definirá um agendamento de backup para todos os bancos de dados novos e atuais.</span><span class="sxs-lookup"><span data-stu-id="8e5e6-129">If you specify this parameter, automated backup sets a backup schedule for all current and new databases.</span></span>
<span data-ttu-id="8e5e6-130">Isso atualiza as configurações de backup gerenciado para acompanhar este cronograma.</span><span class="sxs-lookup"><span data-stu-id="8e5e6-130">This updates your Managed Backup settings to follow this schedule.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e5e6-131">-RetentionPeriodInDays</span><span class="sxs-lookup"><span data-stu-id="8e5e6-131">-RetentionPeriodInDays</span></span>
<span data-ttu-id="8e5e6-132">Especifica o número de dias para manter um backup.</span><span class="sxs-lookup"><span data-stu-id="8e5e6-132">Specifies the number of days to retain a backup.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e5e6-133">-EnableEncryption</span><span class="sxs-lookup"><span data-stu-id="8e5e6-133">-EnableEncryption</span></span>
<span data-ttu-id="8e5e6-134">Indica que esse cmdlet habilita a criptografia.</span><span class="sxs-lookup"><span data-stu-id="8e5e6-134">Indicates that this cmdlet enables encryption.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e5e6-135">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="8e5e6-135">-CertificatePassword</span></span>
<span data-ttu-id="8e5e6-136">Especifica uma senha para criptografar o certificado que é usado para executar backups criptografados do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="8e5e6-136">Specifies a password to encrypt the certificate that is used to perform SQL Server encrypted backups.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e5e6-137">-StorageUri</span><span class="sxs-lookup"><span data-stu-id="8e5e6-137">-StorageUri</span></span>
<span data-ttu-id="8e5e6-138">Especifica o URI (Uniform Resource Identifier) da conta de armazenamento BLOB.</span><span class="sxs-lookup"><span data-stu-id="8e5e6-138">Specifies the Uniform Resource Identifier (URI) of the blob storage account.</span></span>

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e5e6-139">-StorageKey</span><span class="sxs-lookup"><span data-stu-id="8e5e6-139">-StorageKey</span></span>
<span data-ttu-id="8e5e6-140">Especifica a chave de armazenamento da conta de armazenamento BLOB.</span><span class="sxs-lookup"><span data-stu-id="8e5e6-140">Specifies the storage key of the blob storage account.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e5e6-141">-Perfil</span><span class="sxs-lookup"><span data-stu-id="8e5e6-141">-Profile</span></span>
<span data-ttu-id="8e5e6-142">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="8e5e6-142">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="8e5e6-143">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="8e5e6-143">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Commands.Utilities.Common.AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e5e6-144">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="8e5e6-144">-InformationAction</span></span>
<span data-ttu-id="8e5e6-145">@ {Text =}</span><span class="sxs-lookup"><span data-stu-id="8e5e6-145">@{Text=}</span></span>

```yaml
Type: System.Management.Automation.ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e5e6-146">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="8e5e6-146">-InformationVariable</span></span>
<span data-ttu-id="8e5e6-147">@ {Text =}</span><span class="sxs-lookup"><span data-stu-id="8e5e6-147">@{Text=}</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e5e6-148">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="8e5e6-148">-StorageContext</span></span>
<span data-ttu-id="8e5e6-149">Especifica a conta de armazenamento que será usada para armazenar backups.</span><span class="sxs-lookup"><span data-stu-id="8e5e6-149">Specifies the storage account that will be used to store backups.</span></span>
<span data-ttu-id="8e5e6-150">Para obter um objeto **AzureStorageContext** , use o cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="8e5e6-150">To obtain an **AzureStorageContext** object, use the New-AzureStorageContext cmdlet.</span></span>
<span data-ttu-id="8e5e6-151">O padrão é a conta de armazenamento associada à máquina virtual do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="8e5e6-151">The default is the storage account that is associated with the SQL Server virtual machine.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: StorageContextSqlServerAutoBackup
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e5e6-152">-BackupScheduleType</span><span class="sxs-lookup"><span data-stu-id="8e5e6-152">-BackupScheduleType</span></span>
<span data-ttu-id="8e5e6-153">Tipo de agendamento de backup, manual ou automatizado</span><span class="sxs-lookup"><span data-stu-id="8e5e6-153">Backup schedule type, manual or automated</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e5e6-154">-BackupSystemDbs</span><span class="sxs-lookup"><span data-stu-id="8e5e6-154">-BackupSystemDbs</span></span>
<span data-ttu-id="8e5e6-155">Bancos de dados do sistema de backup</span><span class="sxs-lookup"><span data-stu-id="8e5e6-155">Backup system databases</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e5e6-156">-FullBackupFrequency</span><span class="sxs-lookup"><span data-stu-id="8e5e6-156">-FullBackupFrequency</span></span>
<span data-ttu-id="8e5e6-157">Frequência de backup total do SQL Server, diária ou semanal</span><span class="sxs-lookup"><span data-stu-id="8e5e6-157">Sql Server Full Backup frequency, daily or week</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e5e6-158">-FullBackupStartHour</span><span class="sxs-lookup"><span data-stu-id="8e5e6-158">-FullBackupStartHour</span></span>
<span data-ttu-id="8e5e6-159">Hora do dia (0-23) quando o backup completo do SQL Server deve começar</span><span class="sxs-lookup"><span data-stu-id="8e5e6-159">Hour of the day (0-23) when the Sql Server Full Backup should start</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e5e6-160">-FullBackupWindowInHours</span><span class="sxs-lookup"><span data-stu-id="8e5e6-160">-FullBackupWindowInHours</span></span>
<span data-ttu-id="8e5e6-161">Janela de backup completo do SQL Server em horas</span><span class="sxs-lookup"><span data-stu-id="8e5e6-161">Sql Server Full Backup window in hours</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e5e6-162">-LogBackupFrequencyInMinutes</span><span class="sxs-lookup"><span data-stu-id="8e5e6-162">-LogBackupFrequencyInMinutes</span></span>
<span data-ttu-id="8e5e6-163">Frequência de backup de log do SQL Server, a cada 1-60 minutos</span><span class="sxs-lookup"><span data-stu-id="8e5e6-163">Sql Server Log Backup frequency, once every 1-60 minutes</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e5e6-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e5e6-164">CommonParameters</span></span>
<span data-ttu-id="8e5e6-165">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e5e6-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e5e6-166">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8e5e6-166">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e5e6-167">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8e5e6-167">INPUTS</span></span>

## <span data-ttu-id="8e5e6-168">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8e5e6-168">OUTPUTS</span></span>

## <span data-ttu-id="8e5e6-169">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8e5e6-169">NOTES</span></span>

## <span data-ttu-id="8e5e6-170">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8e5e6-170">RELATED LINKS</span></span>

[<span data-ttu-id="8e5e6-171">New-AzureVMSqlServerAutoPatchingConfig</span><span class="sxs-lookup"><span data-stu-id="8e5e6-171">New-AzureVMSqlServerAutoPatchingConfig</span></span>](./New-AzureVMSqlServerAutoPatchingConfig.md)

[<span data-ttu-id="8e5e6-172">Set-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="8e5e6-172">Set-AzureRmVMSqlServerExtension</span></span>](./Set-AzureRMVMSqlServerExtension.md)


