---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 0AC17275-17A9-47DE-BF04-C1A51DF057DC
online version: https://docs.microsoft.com/powershell/module/az.compute/new-azvmsqlserverautobackupconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMSqlServerAutoBackupConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMSqlServerAutoBackupConfig.md
ms.openlocfilehash: 6d9047679f4286e0e2212ca8e599237825326dd7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888376"
---
# <span data-ttu-id="24bb3-101">New-AzVMSqlServerAutoBackupConfig</span><span class="sxs-lookup"><span data-stu-id="24bb3-101">New-AzVMSqlServerAutoBackupConfig</span></span>

## <span data-ttu-id="24bb3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="24bb3-102">SYNOPSIS</span></span>
<span data-ttu-id="24bb3-103">Cria um objeto de configuração para SQL Server backup automático.</span><span class="sxs-lookup"><span data-stu-id="24bb3-103">Creates a configuration object for SQL Server automatic backup.</span></span>

## <span data-ttu-id="24bb3-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="24bb3-104">SYNTAX</span></span>

### <span data-ttu-id="24bb3-105">StorageUriSqlServerAutoBackup (Padrão)</span><span class="sxs-lookup"><span data-stu-id="24bb3-105">StorageUriSqlServerAutoBackup (Default)</span></span>
```
New-AzVMSqlServerAutoBackupConfig [-ResourceGroupName] <String> [-Enable] [[-RetentionPeriodInDays] <Int32>]
 [-EnableEncryption] [[-CertificatePassword] <SecureString>] [[-StorageUri] <Uri>]
 [[-StorageKey] <SecureString>] [-BackupSystemDbs] [-BackupScheduleType <String>]
 [-FullBackupFrequency <String>] [-FullBackupStartHour <Int32>] [-FullBackupWindowInHours <Int32>]
 [-LogBackupFrequencyInMinutes <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="24bb3-106">StorageContextSqlServerAutoBackup</span><span class="sxs-lookup"><span data-stu-id="24bb3-106">StorageContextSqlServerAutoBackup</span></span>
```
New-AzVMSqlServerAutoBackupConfig [-ResourceGroupName] <String> [-Enable] [[-RetentionPeriodInDays] <Int32>]
 [-EnableEncryption] [[-CertificatePassword] <SecureString>] [[-StorageContext] <IStorageContext>]
 [[-StorageUri] <Uri>] [[-StorageKey] <SecureString>] [-BackupSystemDbs] [-BackupScheduleType <String>]
 [-FullBackupFrequency <String>] [-FullBackupStartHour <Int32>] [-FullBackupWindowInHours <Int32>]
 [-LogBackupFrequencyInMinutes <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="24bb3-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="24bb3-107">DESCRIPTION</span></span>
<span data-ttu-id="24bb3-108">O cmdlet **New-AzVMSqlServerAutoBackupConfig** cria um objeto de configuração para SQL Server backup automático.</span><span class="sxs-lookup"><span data-stu-id="24bb3-108">The **New-AzVMSqlServerAutoBackupConfig** cmdlet creates a configuration object for SQL Server automatic backup.</span></span>

## <span data-ttu-id="24bb3-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="24bb3-109">EXAMPLES</span></span>

### <span data-ttu-id="24bb3-110">Exemplo 1: criar uma configuração de backup automática usando URI de armazenamento e chave de conta</span><span class="sxs-lookup"><span data-stu-id="24bb3-110">Example 1: Create an automatic backup configuration using storage URI and account key</span></span>
```
PS C:\> $AutoBackupConfig = New-AzVMSqlServerAutoBackupConfig -Enable -RetentionPeriod 10 -StorageUri "\\contoso\StorageGeneral" -StorageKey "< Storage Key for ContosoGeneral >"
Enable                : True
EnableEncryption      : False
RetentionPeriodInDays : 10
```

<span data-ttu-id="24bb3-111">Este comando cria um objeto de configuração de backup automático especificando URI de armazenamento e chave de conta.</span><span class="sxs-lookup"><span data-stu-id="24bb3-111">This command creates an automatic backup configuration object by specifying storage URI and account key.</span></span>
<span data-ttu-id="24bb3-112">O backup automático está habilitado e os backups automáticos são mantidos por 10 dias.</span><span class="sxs-lookup"><span data-stu-id="24bb3-112">Automatic backup is enabled and automatic backups are kept for 10 days.</span></span>
<span data-ttu-id="24bb3-113">O comando armazena o resultado na variável $AutoBackupConfig.</span><span class="sxs-lookup"><span data-stu-id="24bb3-113">The command stores the result in the $AutoBackupConfig variable.</span></span>
<span data-ttu-id="24bb3-114">Você pode especificar esse item de configuração para outros cmdlets, como o Set-AzVMSqlServerExtension cmdlet.</span><span class="sxs-lookup"><span data-stu-id="24bb3-114">You can specify this configuration item for other cmdlets, such as the Set-AzVMSqlServerExtension cmdlet.</span></span>

### <span data-ttu-id="24bb3-115">Exemplo 2: Criar uma configuração de backup automática usando o contexto de armazenamento</span><span class="sxs-lookup"><span data-stu-id="24bb3-115">Example 2: Create an automatic backup configuration using storage context</span></span>
```
PS C:\> $StorageContext = New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral >"
PS C:\> $AutoBackupConfig = New-AzVMSqlServerAutoBackupConfig -StorageContext $StorageContext -Enable -RetentionPeriod 10
Enable                : True
EnableEncryption      : False
RetentionPeriodInDays : 10
```

<span data-ttu-id="24bb3-116">O primeiro comando cria um contexto de armazenamento e o armazena na variável $StorageContext.</span><span class="sxs-lookup"><span data-stu-id="24bb3-116">The first command creates a storage context, and then stores it in the $StorageContext variable.</span></span>
<span data-ttu-id="24bb3-117">Para obter mais informações, consulte New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="24bb3-117">For more information, see New-AzStorageContext.</span></span>
<span data-ttu-id="24bb3-118">O segundo comando cria um objeto de configuração de backup automático especificando o contexto de armazenamento em $StorageContext.</span><span class="sxs-lookup"><span data-stu-id="24bb3-118">The second command creates an automatic backup configuration object by specifying the storage context in $StorageContext.</span></span>
<span data-ttu-id="24bb3-119">O backup automático está habilitado e os backups automáticos são mantidos por 10 dias.</span><span class="sxs-lookup"><span data-stu-id="24bb3-119">Automatic backup is enabled and automatic backups are kept for 10 days.</span></span>

### <span data-ttu-id="24bb3-120">Exemplo 3: criar uma configuração de backup automática usando o contexto de armazenamento com criptografia e senha</span><span class="sxs-lookup"><span data-stu-id="24bb3-120">Example 3: Create an automatic backup configuration using storage context with encryption and password</span></span>
```
PS C:\> $StorageContext = New-AzVMSqlServerAutoBackupConfig -StorageContext $StorageContext -Enable -RetentionPeriod 10 -EnableEncryption -CertificatePassword $CertificatePassword
Enable                : True
EnableEncryption      : True
RetentionPeriodInDays : 10
```

<span data-ttu-id="24bb3-121">Este comando cria e armazena um objeto de configuração de backup automático.</span><span class="sxs-lookup"><span data-stu-id="24bb3-121">This command creates and stores an automatic backup configuration object.</span></span>
<span data-ttu-id="24bb3-122">O comando especifica o contexto de armazenamento criado em um exemplo anterior.</span><span class="sxs-lookup"><span data-stu-id="24bb3-122">The command specifies the storage context created in a previous example.</span></span>
<span data-ttu-id="24bb3-123">O comando habilita a criptografia com senha.</span><span class="sxs-lookup"><span data-stu-id="24bb3-123">The command enables encryption with password.</span></span>
<span data-ttu-id="24bb3-124">A senha foi armazenada anteriormente como uma cadeia de caracteres segura na $CertificatePassword variável.</span><span class="sxs-lookup"><span data-stu-id="24bb3-124">The password was previously stored as a secure string in the $CertificatePassword variable.</span></span>
<span data-ttu-id="24bb3-125">Para criar uma cadeia de caracteres segura, use ConvertTo-SecureString cmdlet.</span><span class="sxs-lookup"><span data-stu-id="24bb3-125">To create a secure string, use the ConvertTo-SecureString cmdlet.</span></span>

## <span data-ttu-id="24bb3-126">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="24bb3-126">PARAMETERS</span></span>

### <span data-ttu-id="24bb3-127">-BackupScheduleType</span><span class="sxs-lookup"><span data-stu-id="24bb3-127">-BackupScheduleType</span></span>
<span data-ttu-id="24bb3-128">Tipo de agendamento de backup, manual ou automatizado</span><span class="sxs-lookup"><span data-stu-id="24bb3-128">Backup schedule type, manual or automated</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Manual, Automated

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24bb3-129">-BackupSystemDbs</span><span class="sxs-lookup"><span data-stu-id="24bb3-129">-BackupSystemDbs</span></span>
<span data-ttu-id="24bb3-130">Backup de bancos de dados do sistema</span><span class="sxs-lookup"><span data-stu-id="24bb3-130">Backup system databases</span></span>

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

### <span data-ttu-id="24bb3-131">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="24bb3-131">-CertificatePassword</span></span>
<span data-ttu-id="24bb3-132">Especifica uma senha para criptografar o certificado usado para executar SQL Server backups criptografados.</span><span class="sxs-lookup"><span data-stu-id="24bb3-132">Specifies a password to encrypt the certificate that is used to perform SQL Server encrypted backups.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24bb3-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24bb3-133">-DefaultProfile</span></span>
<span data-ttu-id="24bb3-134">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="24bb3-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24bb3-135">-Enable</span><span class="sxs-lookup"><span data-stu-id="24bb3-135">-Enable</span></span>
<span data-ttu-id="24bb3-136">Indica que o backup automatizado para a SQL Server virtual está habilitado.</span><span class="sxs-lookup"><span data-stu-id="24bb3-136">Indicates that automated backup for the SQL Server virtual machine is enabled.</span></span>
<span data-ttu-id="24bb3-137">Se você especificar esse parâmetro, o backup automatizado definirá um agendamento de backup para todos os bancos de dados atuais e novos.</span><span class="sxs-lookup"><span data-stu-id="24bb3-137">If you specify this parameter, automated backup sets a backup schedule for all current and new databases.</span></span>
<span data-ttu-id="24bb3-138">Isso atualiza suas configurações de Backup Gerenciado para seguir esse cronograma.</span><span class="sxs-lookup"><span data-stu-id="24bb3-138">This updates your Managed Backup settings to follow this schedule.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24bb3-139">-EnableEncryption</span><span class="sxs-lookup"><span data-stu-id="24bb3-139">-EnableEncryption</span></span>
<span data-ttu-id="24bb3-140">Indica que esse cmdlet habilita a criptografia.</span><span class="sxs-lookup"><span data-stu-id="24bb3-140">Indicates that this cmdlet enables encryption.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24bb3-141">-FullBackupFrequency</span><span class="sxs-lookup"><span data-stu-id="24bb3-141">-FullBackupFrequency</span></span>
<span data-ttu-id="24bb3-142">Frequência de Backup Completo do Sql Server, diariamente ou semanalmente</span><span class="sxs-lookup"><span data-stu-id="24bb3-142">Sql Server Full Backup frequency, daily or weekly</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Daily, Weekly

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24bb3-143">-FullBackupStartHour</span><span class="sxs-lookup"><span data-stu-id="24bb3-143">-FullBackupStartHour</span></span>
<span data-ttu-id="24bb3-144">Hora do dia (0-23) em que o Backup Completo do Sql Server deve começar</span><span class="sxs-lookup"><span data-stu-id="24bb3-144">Hour of the day (0-23) when the Sql Server Full Backup should start</span></span>

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

### <span data-ttu-id="24bb3-145">-FullBackupWindowInHours</span><span class="sxs-lookup"><span data-stu-id="24bb3-145">-FullBackupWindowInHours</span></span>
<span data-ttu-id="24bb3-146">Janela de Backup Completo do Sql Server em horas</span><span class="sxs-lookup"><span data-stu-id="24bb3-146">Sql Server Full Backup window in hours</span></span>

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

### <span data-ttu-id="24bb3-147">-LogBackupFrequencyInMinutes</span><span class="sxs-lookup"><span data-stu-id="24bb3-147">-LogBackupFrequencyInMinutes</span></span>
<span data-ttu-id="24bb3-148">Frequência de Backup de Log do Sql Server, uma vez a cada 1-60 minutos</span><span class="sxs-lookup"><span data-stu-id="24bb3-148">Sql Server Log Backup frequency, once every 1-60 minutes</span></span>

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

### <span data-ttu-id="24bb3-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24bb3-149">-ResourceGroupName</span></span>
<span data-ttu-id="24bb3-150">Especifica o nome do grupo de recursos da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="24bb3-150">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24bb3-151">-RetentionPeriodInDays</span><span class="sxs-lookup"><span data-stu-id="24bb3-151">-RetentionPeriodInDays</span></span>
<span data-ttu-id="24bb3-152">Especifica o número de dias para manter um backup.</span><span class="sxs-lookup"><span data-stu-id="24bb3-152">Specifies the number of days to retain a backup.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24bb3-153">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="24bb3-153">-StorageContext</span></span>
<span data-ttu-id="24bb3-154">Especifica a conta de armazenamento que será usada para armazenar backups.</span><span class="sxs-lookup"><span data-stu-id="24bb3-154">Specifies the storage account that will be used to store backups.</span></span>
<span data-ttu-id="24bb3-155">Para obter um **objeto AzureStorageContext,** use New-AzStorageContext cmdlet.</span><span class="sxs-lookup"><span data-stu-id="24bb3-155">To obtain an **AzureStorageContext** object, use the New-AzStorageContext cmdlet.</span></span>
<span data-ttu-id="24bb3-156">O padrão é a conta de armazenamento associada à máquina SQL Server virtual.</span><span class="sxs-lookup"><span data-stu-id="24bb3-156">The default is the storage account that is associated with the SQL Server virtual machine.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: StorageContextSqlServerAutoBackup
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24bb3-157">-StorageKey</span><span class="sxs-lookup"><span data-stu-id="24bb3-157">-StorageKey</span></span>
<span data-ttu-id="24bb3-158">Especifica a chave de armazenamento da conta de armazenamento de blob.</span><span class="sxs-lookup"><span data-stu-id="24bb3-158">Specifies the storage key of the blob storage account.</span></span>

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

### <span data-ttu-id="24bb3-159">-StorageUri</span><span class="sxs-lookup"><span data-stu-id="24bb3-159">-StorageUri</span></span>
<span data-ttu-id="24bb3-160">Especifica o URI (Uniform Resource Identifier) da conta de armazenamento de blob.</span><span class="sxs-lookup"><span data-stu-id="24bb3-160">Specifies the Uniform Resource Identifier (URI) of the blob storage account.</span></span>

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

### <span data-ttu-id="24bb3-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24bb3-161">CommonParameters</span></span>
<span data-ttu-id="24bb3-162">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24bb3-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24bb3-163">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="24bb3-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24bb3-164">INPUTS</span><span class="sxs-lookup"><span data-stu-id="24bb3-164">INPUTS</span></span>

### <span data-ttu-id="24bb3-165">System.String</span><span class="sxs-lookup"><span data-stu-id="24bb3-165">System.String</span></span>

### <span data-ttu-id="24bb3-166">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="24bb3-166">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="24bb3-167">System.Int32</span><span class="sxs-lookup"><span data-stu-id="24bb3-167">System.Int32</span></span>

### <span data-ttu-id="24bb3-168">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="24bb3-168">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

### <span data-ttu-id="24bb3-169">System.Uri</span><span class="sxs-lookup"><span data-stu-id="24bb3-169">System.Uri</span></span>

### <span data-ttu-id="24bb3-170">System.Security.SecureString</span><span class="sxs-lookup"><span data-stu-id="24bb3-170">System.Security.SecureString</span></span>

### <span data-ttu-id="24bb3-171">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="24bb3-171">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="24bb3-172">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="24bb3-172">OUTPUTS</span></span>

### <span data-ttu-id="24bb3-173">Microsoft.Azure.Commands.Compute.AutoBackupSettings</span><span class="sxs-lookup"><span data-stu-id="24bb3-173">Microsoft.Azure.Commands.Compute.AutoBackupSettings</span></span>

## <span data-ttu-id="24bb3-174">NOTES</span><span class="sxs-lookup"><span data-stu-id="24bb3-174">NOTES</span></span>

## <span data-ttu-id="24bb3-175">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="24bb3-175">RELATED LINKS</span></span>

[<span data-ttu-id="24bb3-176">New-AzVMSqlServerAutoPatchingConfig</span><span class="sxs-lookup"><span data-stu-id="24bb3-176">New-AzVMSqlServerAutoPatchingConfig</span></span>](./New-AzVMSqlServerAutoPatchingConfig.md)

[<span data-ttu-id="24bb3-177">Set-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="24bb3-177">Set-AzVMSqlServerExtension</span></span>](./Set-AzVMSqlServerExtension.md)


