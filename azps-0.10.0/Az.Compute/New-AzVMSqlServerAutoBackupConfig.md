---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 0AC17275-17A9-47DE-BF04-C1A51DF057DC
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmsqlserverautobackupconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzVMSqlServerAutoBackupConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzVMSqlServerAutoBackupConfig.md
ms.openlocfilehash: 1ff53a29fa26ebe7ac78cac5140a9105b43bb27d
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776955"
---
# <span data-ttu-id="b9525-101">New-AzVMSqlServerAutoBackupConfig</span><span class="sxs-lookup"><span data-stu-id="b9525-101">New-AzVMSqlServerAutoBackupConfig</span></span>

## <span data-ttu-id="b9525-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b9525-102">SYNOPSIS</span></span>
<span data-ttu-id="b9525-103">Cria um objeto de configuração para o backup automático do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="b9525-103">Creates a configuration object for SQL Server automatic backup.</span></span>

## <span data-ttu-id="b9525-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b9525-104">SYNTAX</span></span>

### <span data-ttu-id="b9525-105">StorageUriSqlServerAutoBackup (padrão)</span><span class="sxs-lookup"><span data-stu-id="b9525-105">StorageUriSqlServerAutoBackup (Default)</span></span>
```
New-AzVMSqlServerAutoBackupConfig [-ResourceGroupName] <String> [-Enable]
 [[-RetentionPeriodInDays] <Int32>] [-EnableEncryption] [[-CertificatePassword] <SecureString>]
 [[-StorageUri] <Uri>] [[-StorageKey] <SecureString>] [-BackupSystemDbs] [-BackupScheduleType <String>]
 [-FullBackupFrequency <String>] [-FullBackupStartHour <Int32>] [-FullBackupWindowInHours <Int32>]
 [-LogBackupFrequencyInMinutes <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b9525-106">StorageContextSqlServerAutoBackup</span><span class="sxs-lookup"><span data-stu-id="b9525-106">StorageContextSqlServerAutoBackup</span></span>
```
New-AzVMSqlServerAutoBackupConfig [-ResourceGroupName] <String> [-Enable]
 [[-RetentionPeriodInDays] <Int32>] [-EnableEncryption] [[-CertificatePassword] <SecureString>]
 [[-StorageContext] <IStorageContext>] [[-StorageUri] <Uri>] [[-StorageKey] <SecureString>] [-BackupSystemDbs]
 [-BackupScheduleType <String>] [-FullBackupFrequency <String>] [-FullBackupStartHour <Int32>]
 [-FullBackupWindowInHours <Int32>] [-LogBackupFrequencyInMinutes <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b9525-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b9525-107">DESCRIPTION</span></span>
<span data-ttu-id="b9525-108">O cmdlet **New-AzVMSqlServerAutoBackupConfig** cria um objeto de configuração para o backup automático do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="b9525-108">The **New-AzVMSqlServerAutoBackupConfig** cmdlet creates a configuration object for SQL Server automatic backup.</span></span>

## <span data-ttu-id="b9525-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b9525-109">EXAMPLES</span></span>

### <span data-ttu-id="b9525-110">Exemplo 1: criar uma configuração de backup automática usando o URI de armazenamento e a chave de conta</span><span class="sxs-lookup"><span data-stu-id="b9525-110">Example 1: Create an automatic backup configuration using storage URI and account key</span></span>
```
PS C:\> $AutoBackupConfig = New-AzVMSqlServerAutoBackupConfig -Enable -RetentionPeriod 10 -StorageUri "\\contoso\StorageGeneral" -StorageKey "< Storage Key for ContosoGeneral >"
Enable                : True
EnableEncryption      : False
RetentionPeriodInDays : 10
```

<span data-ttu-id="b9525-111">Esse comando cria um objeto de configuração de backup automático especificando a chave da conta e o URI de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="b9525-111">This command creates an automatic backup configuration object by specifying storage URI and account key.</span></span>
<span data-ttu-id="b9525-112">O backup automático é ativado e os backups automáticos são mantidos por 10 dias.</span><span class="sxs-lookup"><span data-stu-id="b9525-112">Automatic backup is enabled and automatic backups are kept for 10 days.</span></span>
<span data-ttu-id="b9525-113">O comando armazena o resultado na variável $AutoBackupConfig.</span><span class="sxs-lookup"><span data-stu-id="b9525-113">The command stores the result in the $AutoBackupConfig variable.</span></span>
<span data-ttu-id="b9525-114">Você pode especificar esse item de configuração para outros cmdlets, como o cmdlet Set-AzVMSqlServerExtension.</span><span class="sxs-lookup"><span data-stu-id="b9525-114">You can specify this configuration item for other cmdlets, such as the Set-AzVMSqlServerExtension cmdlet.</span></span>

### <span data-ttu-id="b9525-115">Exemplo 2: criar uma configuração de backup automática usando contexto de armazenamento</span><span class="sxs-lookup"><span data-stu-id="b9525-115">Example 2: Create an automatic backup configuration using storage context</span></span>
```
PS C:\> $StorageContext = New-AzureStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral >"
PS C:\> $AutoBackupConfig = New-AzVMSqlServerAutoBackupConfig -StorageContext $StorageContext -Enable -RetentionPeriod 10
Enable                : True
EnableEncryption      : False
RetentionPeriodInDays : 10
```

<span data-ttu-id="b9525-116">O primeiro comando cria um contexto de armazenamento e, em seguida, armazena-o na variável $StorageContext.</span><span class="sxs-lookup"><span data-stu-id="b9525-116">The first command creates a storage context, and then stores it in the $StorageContext variable.</span></span>
<span data-ttu-id="b9525-117">Para obter mais informações, consulte New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="b9525-117">For more information, see New-AzureStorageContext.</span></span>

<span data-ttu-id="b9525-118">O segundo comando cria um objeto de configuração de backup automático especificando o contexto de armazenamento em $StorageContext.</span><span class="sxs-lookup"><span data-stu-id="b9525-118">The second command creates an automatic backup configuration object by specifying the storage context in $StorageContext.</span></span>
<span data-ttu-id="b9525-119">O backup automático é ativado e os backups automáticos são mantidos por 10 dias.</span><span class="sxs-lookup"><span data-stu-id="b9525-119">Automatic backup is enabled and automatic backups are kept for 10 days.</span></span>

### <span data-ttu-id="b9525-120">Exemplo 3: criar uma configuração de backup automática usando contexto de armazenamento com criptografia e senha</span><span class="sxs-lookup"><span data-stu-id="b9525-120">Example 3: Create an automatic backup configuration using storage context with encryption and password</span></span>
```
PS C:\> $StorageContext = New-AzVMSqlServerAutoBackupConfig -StorageContext $StorageContext -Enable -RetentionPeriod 10 -EnableEncryption -CertificatePassword $CertificatePassword
Enable                : True
EnableEncryption      : True
RetentionPeriodInDays : 10
```

<span data-ttu-id="b9525-121">Esse comando cria e armazena um objeto de configuração de backup automático.</span><span class="sxs-lookup"><span data-stu-id="b9525-121">This command creates and stores an automatic backup configuration object.</span></span>
<span data-ttu-id="b9525-122">O comando especifica o contexto de armazenamento criado em um exemplo anterior.</span><span class="sxs-lookup"><span data-stu-id="b9525-122">The command specifies the storage context created in a previous example.</span></span>
<span data-ttu-id="b9525-123">O comando habilita a criptografia com senha.</span><span class="sxs-lookup"><span data-stu-id="b9525-123">The command enables encryption with password.</span></span>
<span data-ttu-id="b9525-124">A senha foi armazenada anteriormente como uma cadeia de caracteres segura na variável $CertificatePassword.</span><span class="sxs-lookup"><span data-stu-id="b9525-124">The password was previously stored as a secure string in the $CertificatePassword variable.</span></span>
<span data-ttu-id="b9525-125">Para criar uma cadeia de caracteres segura, use o cmdlet ConvertTo-SecureString.</span><span class="sxs-lookup"><span data-stu-id="b9525-125">To create a secure string, use the ConvertTo-SecureString cmdlet.</span></span>

## <span data-ttu-id="b9525-126">OS</span><span class="sxs-lookup"><span data-stu-id="b9525-126">PARAMETERS</span></span>

### <span data-ttu-id="b9525-127">-BackupScheduleType</span><span class="sxs-lookup"><span data-stu-id="b9525-127">-BackupScheduleType</span></span>
<span data-ttu-id="b9525-128">Tipo de agendamento de backup, manual ou automatizado</span><span class="sxs-lookup"><span data-stu-id="b9525-128">Backup schedule type, manual or automated</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Manual, Automated

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9525-129">-BackupSystemDbs</span><span class="sxs-lookup"><span data-stu-id="b9525-129">-BackupSystemDbs</span></span>
<span data-ttu-id="b9525-130">Bancos de dados do sistema de backup</span><span class="sxs-lookup"><span data-stu-id="b9525-130">Backup system databases</span></span>

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

### <span data-ttu-id="b9525-131">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="b9525-131">-CertificatePassword</span></span>
<span data-ttu-id="b9525-132">Especifica uma senha para criptografar o certificado que é usado para executar backups criptografados do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="b9525-132">Specifies a password to encrypt the certificate that is used to perform SQL Server encrypted backups.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9525-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9525-133">-DefaultProfile</span></span>
<span data-ttu-id="b9525-134">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b9525-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9525-135">-Habilitar</span><span class="sxs-lookup"><span data-stu-id="b9525-135">-Enable</span></span>
<span data-ttu-id="b9525-136">Indica que o backup automatizado para a máquina virtual do SQL Server está habilitado.</span><span class="sxs-lookup"><span data-stu-id="b9525-136">Indicates that automated backup for the SQL Server virtual machine is enabled.</span></span>
<span data-ttu-id="b9525-137">Se você especificar esse parâmetro, o backup automatizado definirá um agendamento de backup para todos os bancos de dados novos e atuais.</span><span class="sxs-lookup"><span data-stu-id="b9525-137">If you specify this parameter, automated backup sets a backup schedule for all current and new databases.</span></span>
<span data-ttu-id="b9525-138">Isso atualiza as configurações de backup gerenciado para acompanhar este cronograma.</span><span class="sxs-lookup"><span data-stu-id="b9525-138">This updates your Managed Backup settings to follow this schedule.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9525-139">-EnableEncryption</span><span class="sxs-lookup"><span data-stu-id="b9525-139">-EnableEncryption</span></span>
<span data-ttu-id="b9525-140">Indica que esse cmdlet habilita a criptografia.</span><span class="sxs-lookup"><span data-stu-id="b9525-140">Indicates that this cmdlet enables encryption.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9525-141">-FullBackupFrequency</span><span class="sxs-lookup"><span data-stu-id="b9525-141">-FullBackupFrequency</span></span>
<span data-ttu-id="b9525-142">Frequência de backup total do SQL Server, diária ou semanal</span><span class="sxs-lookup"><span data-stu-id="b9525-142">Sql Server Full Backup frequency, daily or weekly</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Daily, Weekly

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9525-143">-FullBackupStartHour</span><span class="sxs-lookup"><span data-stu-id="b9525-143">-FullBackupStartHour</span></span>
<span data-ttu-id="b9525-144">Hora do dia (0-23) quando o backup completo do SQL Server deve começar</span><span class="sxs-lookup"><span data-stu-id="b9525-144">Hour of the day (0-23) when the Sql Server Full Backup should start</span></span>

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

### <span data-ttu-id="b9525-145">-FullBackupWindowInHours</span><span class="sxs-lookup"><span data-stu-id="b9525-145">-FullBackupWindowInHours</span></span>
<span data-ttu-id="b9525-146">Janela de backup completo do SQL Server em horas</span><span class="sxs-lookup"><span data-stu-id="b9525-146">Sql Server Full Backup window in hours</span></span>

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

### <span data-ttu-id="b9525-147">-LogBackupFrequencyInMinutes</span><span class="sxs-lookup"><span data-stu-id="b9525-147">-LogBackupFrequencyInMinutes</span></span>
<span data-ttu-id="b9525-148">Frequência de backup de log do SQL Server, a cada 1-60 minutos</span><span class="sxs-lookup"><span data-stu-id="b9525-148">Sql Server Log Backup frequency, once every 1-60 minutes</span></span>

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

### <span data-ttu-id="b9525-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b9525-149">-ResourceGroupName</span></span>
<span data-ttu-id="b9525-150">Especifica o nome do grupo de recursos da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="b9525-150">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9525-151">-RetentionPeriodInDays</span><span class="sxs-lookup"><span data-stu-id="b9525-151">-RetentionPeriodInDays</span></span>
<span data-ttu-id="b9525-152">Especifica o número de dias para manter um backup.</span><span class="sxs-lookup"><span data-stu-id="b9525-152">Specifies the number of days to retain a backup.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9525-153">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="b9525-153">-StorageContext</span></span>
<span data-ttu-id="b9525-154">Especifica a conta de armazenamento que será usada para armazenar backups.</span><span class="sxs-lookup"><span data-stu-id="b9525-154">Specifies the storage account that will be used to store backups.</span></span>
<span data-ttu-id="b9525-155">Para obter um objeto **AzureStorageContext** , use o cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="b9525-155">To obtain an **AzureStorageContext** object, use the New-AzureStorageContext cmdlet.</span></span>
<span data-ttu-id="b9525-156">O padrão é a conta de armazenamento associada à máquina virtual do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="b9525-156">The default is the storage account that is associated with the SQL Server virtual machine.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: StorageContextSqlServerAutoBackup
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9525-157">-StorageKey</span><span class="sxs-lookup"><span data-stu-id="b9525-157">-StorageKey</span></span>
<span data-ttu-id="b9525-158">Especifica a chave de armazenamento da conta de armazenamento BLOB.</span><span class="sxs-lookup"><span data-stu-id="b9525-158">Specifies the storage key of the blob storage account.</span></span>

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

### <span data-ttu-id="b9525-159">-StorageUri</span><span class="sxs-lookup"><span data-stu-id="b9525-159">-StorageUri</span></span>
<span data-ttu-id="b9525-160">Especifica o URI (Uniform Resource Identifier) da conta de armazenamento BLOB.</span><span class="sxs-lookup"><span data-stu-id="b9525-160">Specifies the Uniform Resource Identifier (URI) of the blob storage account.</span></span>

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

### <span data-ttu-id="b9525-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9525-161">CommonParameters</span></span>
<span data-ttu-id="b9525-162">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9525-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9525-163">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b9525-163">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9525-164">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b9525-164">INPUTS</span></span>

### <span data-ttu-id="b9525-165">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="b9525-165">None</span></span>
<span data-ttu-id="b9525-166">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="b9525-166">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b9525-167">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b9525-167">OUTPUTS</span></span>

### <span data-ttu-id="b9525-168">Microsoft. Azure. Commands. COMPUTE. AutoBackupSettings</span><span class="sxs-lookup"><span data-stu-id="b9525-168">Microsoft.Azure.Commands.Compute.AutoBackupSettings</span></span>

## <span data-ttu-id="b9525-169">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b9525-169">NOTES</span></span>

## <span data-ttu-id="b9525-170">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b9525-170">RELATED LINKS</span></span>

[<span data-ttu-id="b9525-171">New-AzureVMSqlServerAutoPatchingConfig</span><span class="sxs-lookup"><span data-stu-id="b9525-171">New-AzureVMSqlServerAutoPatchingConfig</span></span>](./New-AzureVMSqlServerAutoPatchingConfig.md)

[<span data-ttu-id="b9525-172">Set-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="b9525-172">Set-AzVMSqlServerExtension</span></span>](./Set-AzVMSqlServerExtension.md)


