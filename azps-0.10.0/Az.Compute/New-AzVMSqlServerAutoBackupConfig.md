---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 0AC17275-17A9-47DE-BF04-C1A51DF057DC
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmsqlserverautobackupconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzVMSqlServerAutoBackupConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzVMSqlServerAutoBackupConfig.md
ms.openlocfilehash: ecff02643dd6d0e017d56af01792a06dc7b8d998
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100398267"
---
# <span data-ttu-id="f57ed-101">New-AzVMSqlServerAutoBackupConfig</span><span class="sxs-lookup"><span data-stu-id="f57ed-101">New-AzVMSqlServerAutoBackupConfig</span></span>

## <span data-ttu-id="f57ed-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f57ed-102">SYNOPSIS</span></span>
<span data-ttu-id="f57ed-103">Cria um objeto de configuração para backup automático do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="f57ed-103">Creates a configuration object for SQL Server automatic backup.</span></span>

## <span data-ttu-id="f57ed-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f57ed-104">SYNTAX</span></span>

### <span data-ttu-id="f57ed-105">StorageUriSqlServerAutoBackup (Padrão)</span><span class="sxs-lookup"><span data-stu-id="f57ed-105">StorageUriSqlServerAutoBackup (Default)</span></span>
```
New-AzVMSqlServerAutoBackupConfig [-ResourceGroupName] <String> [-Enable]
 [[-RetentionPeriodInDays] <Int32>] [-EnableEncryption] [[-CertificatePassword] <SecureString>]
 [[-StorageUri] <Uri>] [[-StorageKey] <SecureString>] [-BackupSystemDbs] [-BackupScheduleType <String>]
 [-FullBackupFrequency <String>] [-FullBackupStartHour <Int32>] [-FullBackupWindowInHours <Int32>]
 [-LogBackupFrequencyInMinutes <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f57ed-106">StorageContextSqlServerAutoBackup</span><span class="sxs-lookup"><span data-stu-id="f57ed-106">StorageContextSqlServerAutoBackup</span></span>
```
New-AzVMSqlServerAutoBackupConfig [-ResourceGroupName] <String> [-Enable]
 [[-RetentionPeriodInDays] <Int32>] [-EnableEncryption] [[-CertificatePassword] <SecureString>]
 [[-StorageContext] <IStorageContext>] [[-StorageUri] <Uri>] [[-StorageKey] <SecureString>] [-BackupSystemDbs]
 [-BackupScheduleType <String>] [-FullBackupFrequency <String>] [-FullBackupStartHour <Int32>]
 [-FullBackupWindowInHours <Int32>] [-LogBackupFrequencyInMinutes <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f57ed-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="f57ed-107">DESCRIPTION</span></span>
<span data-ttu-id="f57ed-108">O **cmdlet New-AzVMSqlServerAutoBackupConfig** cria um objeto de configuração para o backup automático do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="f57ed-108">The **New-AzVMSqlServerAutoBackupConfig** cmdlet creates a configuration object for SQL Server automatic backup.</span></span>

## <span data-ttu-id="f57ed-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f57ed-109">EXAMPLES</span></span>

### <span data-ttu-id="f57ed-110">Exemplo 1: Criar uma configuração de backup automática usando o URI de armazenamento e a chave da conta</span><span class="sxs-lookup"><span data-stu-id="f57ed-110">Example 1: Create an automatic backup configuration using storage URI and account key</span></span>
```
PS C:\> $AutoBackupConfig = New-AzVMSqlServerAutoBackupConfig -Enable -RetentionPeriod 10 -StorageUri "\\contoso\StorageGeneral" -StorageKey "< Storage Key for ContosoGeneral >"
Enable                : True
EnableEncryption      : False
RetentionPeriodInDays : 10
```

<span data-ttu-id="f57ed-111">Esse comando cria um objeto de configuração de backup automático especificando o URI de armazenamento e a chave da conta.</span><span class="sxs-lookup"><span data-stu-id="f57ed-111">This command creates an automatic backup configuration object by specifying storage URI and account key.</span></span>
<span data-ttu-id="f57ed-112">O backup automático é habilitado e os backups automáticos são mantidos por 10 dias.</span><span class="sxs-lookup"><span data-stu-id="f57ed-112">Automatic backup is enabled and automatic backups are kept for 10 days.</span></span>
<span data-ttu-id="f57ed-113">O comando armazena o resultado na variável $AutoBackupConfig dados.</span><span class="sxs-lookup"><span data-stu-id="f57ed-113">The command stores the result in the $AutoBackupConfig variable.</span></span>
<span data-ttu-id="f57ed-114">Você pode especificar esse item de configuração para outros cmdlets, como o Set-AzVMSqlServerExtension cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f57ed-114">You can specify this configuration item for other cmdlets, such as the Set-AzVMSqlServerExtension cmdlet.</span></span>

### <span data-ttu-id="f57ed-115">Exemplo 2: Criar uma configuração de backup automática usando o contexto de armazenamento</span><span class="sxs-lookup"><span data-stu-id="f57ed-115">Example 2: Create an automatic backup configuration using storage context</span></span>
```
PS C:\> $StorageContext = New-AzureStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral >"
PS C:\> $AutoBackupConfig = New-AzVMSqlServerAutoBackupConfig -StorageContext $StorageContext -Enable -RetentionPeriod 10
Enable                : True
EnableEncryption      : False
RetentionPeriodInDays : 10
```

<span data-ttu-id="f57ed-116">O primeiro comando cria um contexto de armazenamento e o armazena na $StorageContext variável.</span><span class="sxs-lookup"><span data-stu-id="f57ed-116">The first command creates a storage context, and then stores it in the $StorageContext variable.</span></span>
<span data-ttu-id="f57ed-117">Para obter mais informações, consulte New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="f57ed-117">For more information, see New-AzureStorageContext.</span></span>

<span data-ttu-id="f57ed-118">O segundo comando cria um objeto de configuração de backup automático especificando o contexto de armazenamento no $StorageContext.</span><span class="sxs-lookup"><span data-stu-id="f57ed-118">The second command creates an automatic backup configuration object by specifying the storage context in $StorageContext.</span></span>
<span data-ttu-id="f57ed-119">O backup automático está habilitado e os backups automáticos são mantidos por 10 dias.</span><span class="sxs-lookup"><span data-stu-id="f57ed-119">Automatic backup is enabled and automatic backups are kept for 10 days.</span></span>

### <span data-ttu-id="f57ed-120">Exemplo 3: Criar uma configuração de backup automática usando contexto de armazenamento com criptografia e senha</span><span class="sxs-lookup"><span data-stu-id="f57ed-120">Example 3: Create an automatic backup configuration using storage context with encryption and password</span></span>
```
PS C:\> $StorageContext = New-AzVMSqlServerAutoBackupConfig -StorageContext $StorageContext -Enable -RetentionPeriod 10 -EnableEncryption -CertificatePassword $CertificatePassword
Enable                : True
EnableEncryption      : True
RetentionPeriodInDays : 10
```

<span data-ttu-id="f57ed-121">Esse comando cria e armazena um objeto de configuração de backup automático.</span><span class="sxs-lookup"><span data-stu-id="f57ed-121">This command creates and stores an automatic backup configuration object.</span></span>
<span data-ttu-id="f57ed-122">O comando especifica o contexto de armazenamento criado em um exemplo anterior.</span><span class="sxs-lookup"><span data-stu-id="f57ed-122">The command specifies the storage context created in a previous example.</span></span>
<span data-ttu-id="f57ed-123">O comando habilita a criptografia com senha.</span><span class="sxs-lookup"><span data-stu-id="f57ed-123">The command enables encryption with password.</span></span>
<span data-ttu-id="f57ed-124">A senha foi armazenada anteriormente como uma cadeia de caracteres segura na variável $CertificatePassword dados.</span><span class="sxs-lookup"><span data-stu-id="f57ed-124">The password was previously stored as a secure string in the $CertificatePassword variable.</span></span>
<span data-ttu-id="f57ed-125">Para criar uma cadeia de caracteres segura, use ConvertTo-SecureString cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f57ed-125">To create a secure string, use the ConvertTo-SecureString cmdlet.</span></span>

## <span data-ttu-id="f57ed-126">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f57ed-126">PARAMETERS</span></span>

### <span data-ttu-id="f57ed-127">-BackupScheduleType</span><span class="sxs-lookup"><span data-stu-id="f57ed-127">-BackupScheduleType</span></span>
<span data-ttu-id="f57ed-128">Tipo de agendamento de backup, manual ou automatizado</span><span class="sxs-lookup"><span data-stu-id="f57ed-128">Backup schedule type, manual or automated</span></span>

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

### <span data-ttu-id="f57ed-129">-BackupSystemDbs</span><span class="sxs-lookup"><span data-stu-id="f57ed-129">-BackupSystemDbs</span></span>
<span data-ttu-id="f57ed-130">Backup de bancos de dados do sistema</span><span class="sxs-lookup"><span data-stu-id="f57ed-130">Backup system databases</span></span>

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

### <span data-ttu-id="f57ed-131">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="f57ed-131">-CertificatePassword</span></span>
<span data-ttu-id="f57ed-132">Especifica uma senha para criptografar o certificado usado para executar backups criptografados do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="f57ed-132">Specifies a password to encrypt the certificate that is used to perform SQL Server encrypted backups.</span></span>

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

### <span data-ttu-id="f57ed-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f57ed-133">-DefaultProfile</span></span>
<span data-ttu-id="f57ed-134">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="f57ed-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f57ed-135">-Habilitar</span><span class="sxs-lookup"><span data-stu-id="f57ed-135">-Enable</span></span>
<span data-ttu-id="f57ed-136">Indica que o backup automatizado para a máquina virtual DO SQL Server está habilitado.</span><span class="sxs-lookup"><span data-stu-id="f57ed-136">Indicates that automated backup for the SQL Server virtual machine is enabled.</span></span>
<span data-ttu-id="f57ed-137">Se você especificar esse parâmetro, o backup automatizado definirá um cronograma de backup para todos os bancos de dados atuais e novos.</span><span class="sxs-lookup"><span data-stu-id="f57ed-137">If you specify this parameter, automated backup sets a backup schedule for all current and new databases.</span></span>
<span data-ttu-id="f57ed-138">Isso atualiza as configurações de Backup Gerenciado para seguir este cronograma.</span><span class="sxs-lookup"><span data-stu-id="f57ed-138">This updates your Managed Backup settings to follow this schedule.</span></span>

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

### <span data-ttu-id="f57ed-139">-EnableEncryption</span><span class="sxs-lookup"><span data-stu-id="f57ed-139">-EnableEncryption</span></span>
<span data-ttu-id="f57ed-140">Indica que esse cmdlet habilita a criptografia.</span><span class="sxs-lookup"><span data-stu-id="f57ed-140">Indicates that this cmdlet enables encryption.</span></span>

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

### <span data-ttu-id="f57ed-141">-FullBackupFrequency</span><span class="sxs-lookup"><span data-stu-id="f57ed-141">-FullBackupFrequency</span></span>
<span data-ttu-id="f57ed-142">Frequência de Backup Total do Sql Server, diariamente ou semanalmente</span><span class="sxs-lookup"><span data-stu-id="f57ed-142">Sql Server Full Backup frequency, daily or weekly</span></span>

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

### <span data-ttu-id="f57ed-143">-FullBackupStartHour</span><span class="sxs-lookup"><span data-stu-id="f57ed-143">-FullBackupStartHour</span></span>
<span data-ttu-id="f57ed-144">Hora do dia (0 a 23) quando o Backup Completo do Sql Server deve começar</span><span class="sxs-lookup"><span data-stu-id="f57ed-144">Hour of the day (0-23) when the Sql Server Full Backup should start</span></span>

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

### <span data-ttu-id="f57ed-145">-FullBackupWindowInHours</span><span class="sxs-lookup"><span data-stu-id="f57ed-145">-FullBackupWindowInHours</span></span>
<span data-ttu-id="f57ed-146">Janela backup completo do Sql Server em horas</span><span class="sxs-lookup"><span data-stu-id="f57ed-146">Sql Server Full Backup window in hours</span></span>

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

### <span data-ttu-id="f57ed-147">-LogBackupFrequencyInMinutes</span><span class="sxs-lookup"><span data-stu-id="f57ed-147">-LogBackupFrequencyInMinutes</span></span>
<span data-ttu-id="f57ed-148">Frequência de backup de log do Sql Server, uma vez a cada 1 a 60 minutos</span><span class="sxs-lookup"><span data-stu-id="f57ed-148">Sql Server Log Backup frequency, once every 1-60 minutes</span></span>

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

### <span data-ttu-id="f57ed-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f57ed-149">-ResourceGroupName</span></span>
<span data-ttu-id="f57ed-150">Especifica o nome do grupo de recursos da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="f57ed-150">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="f57ed-151">-RetentionPeriodInDays</span><span class="sxs-lookup"><span data-stu-id="f57ed-151">-RetentionPeriodInDays</span></span>
<span data-ttu-id="f57ed-152">Especifica o número de dias para reter um backup.</span><span class="sxs-lookup"><span data-stu-id="f57ed-152">Specifies the number of days to retain a backup.</span></span>

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

### <span data-ttu-id="f57ed-153">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="f57ed-153">-StorageContext</span></span>
<span data-ttu-id="f57ed-154">Especifica a conta de armazenamento que será usada para armazenar backups.</span><span class="sxs-lookup"><span data-stu-id="f57ed-154">Specifies the storage account that will be used to store backups.</span></span>
<span data-ttu-id="f57ed-155">Para obter um **objeto AzureStorageContext,** use New-AzureStorageContext cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f57ed-155">To obtain an **AzureStorageContext** object, use the New-AzureStorageContext cmdlet.</span></span>
<span data-ttu-id="f57ed-156">O padrão é a conta de armazenamento associada à máquina virtual do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="f57ed-156">The default is the storage account that is associated with the SQL Server virtual machine.</span></span>

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

### <span data-ttu-id="f57ed-157">-StorageKey</span><span class="sxs-lookup"><span data-stu-id="f57ed-157">-StorageKey</span></span>
<span data-ttu-id="f57ed-158">Especifica a chave de armazenamento da conta de armazenamento de blob.</span><span class="sxs-lookup"><span data-stu-id="f57ed-158">Specifies the storage key of the blob storage account.</span></span>

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

### <span data-ttu-id="f57ed-159">-StorageUri</span><span class="sxs-lookup"><span data-stu-id="f57ed-159">-StorageUri</span></span>
<span data-ttu-id="f57ed-160">Especifica o URI (Uniform Resource Identifier) da conta de armazenamento de blob.</span><span class="sxs-lookup"><span data-stu-id="f57ed-160">Specifies the Uniform Resource Identifier (URI) of the blob storage account.</span></span>

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

### <span data-ttu-id="f57ed-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f57ed-161">CommonParameters</span></span>
<span data-ttu-id="f57ed-162">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f57ed-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f57ed-163">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f57ed-163">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f57ed-164">Entradas</span><span class="sxs-lookup"><span data-stu-id="f57ed-164">INPUTS</span></span>

### <span data-ttu-id="f57ed-165">Nenhum</span><span class="sxs-lookup"><span data-stu-id="f57ed-165">None</span></span>
<span data-ttu-id="f57ed-166">Este cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="f57ed-166">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f57ed-167">Saídas</span><span class="sxs-lookup"><span data-stu-id="f57ed-167">OUTPUTS</span></span>

### <span data-ttu-id="f57ed-168">Microsoft.Azure.Commands.Compute.AutoBackupSettings</span><span class="sxs-lookup"><span data-stu-id="f57ed-168">Microsoft.Azure.Commands.Compute.AutoBackupSettings</span></span>

## <span data-ttu-id="f57ed-169">Notas</span><span class="sxs-lookup"><span data-stu-id="f57ed-169">NOTES</span></span>

## <span data-ttu-id="f57ed-170">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f57ed-170">RELATED LINKS</span></span>

[<span data-ttu-id="f57ed-171">New-AzureVMSqlServerAutoPatchingConfig</span><span class="sxs-lookup"><span data-stu-id="f57ed-171">New-AzureVMSqlServerAutoPatchingConfig</span></span>](./New-AzVMSqlServerAutoPatchingConfig.md)

[<span data-ttu-id="f57ed-172">Set-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="f57ed-172">Set-AzVMSqlServerExtension</span></span>](./Set-AzVMSqlServerExtension.md)


