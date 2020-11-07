---
external help file: ''
Module Name: Azs.Backup.Admin
online version: https://docs.microsoft.com/powershell/module/azs.backup.admin/set-azsbackupconfiguration
schema: 2.0.0
ms.openlocfilehash: c99e2c549cc865a5f7f9ad0d7c3252cbf6651e98
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/24/2020
ms.locfileid: "93945351"
---
# <span data-ttu-id="7c6b7-101">Set-AzsBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="7c6b7-101">Set-AzsBackupConfiguration</span></span>

## <span data-ttu-id="7c6b7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7c6b7-102">SYNOPSIS</span></span>
<span data-ttu-id="7c6b7-103">Atualize um local de backup.</span><span class="sxs-lookup"><span data-stu-id="7c6b7-103">Update a backup location.</span></span>

## <span data-ttu-id="7c6b7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7c6b7-104">SYNTAX</span></span>

### <span data-ttu-id="7c6b7-105">UpdateExpanded (padrão)</span><span class="sxs-lookup"><span data-stu-id="7c6b7-105">UpdateExpanded (Default)</span></span>
```
Set-AzsBackupConfiguration [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String>]
 [-BackupFrequencyInHours <Int32>] [-BackupRetentionPeriodInDays <Int32>] [-EncryptionCertPath <String>]
 [-IsBackupSchedulerEnabled] [-Password <SecureString>] [-Path <String>] [-Tag <Hashtable>]
 [-UserName <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="7c6b7-106">Atualização</span><span class="sxs-lookup"><span data-stu-id="7c6b7-106">Update</span></span>
```
Set-AzsBackupConfiguration -Backup <IBackupLocation> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="7c6b7-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7c6b7-107">DESCRIPTION</span></span>
<span data-ttu-id="7c6b7-108">Atualize um local de backup.</span><span class="sxs-lookup"><span data-stu-id="7c6b7-108">Update a backup location.</span></span>

## <span data-ttu-id="7c6b7-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7c6b7-109">EXAMPLES</span></span>

### <span data-ttu-id="7c6b7-110">Exemplo 1: definir configuração de backup</span><span class="sxs-lookup"><span data-stu-id="7c6b7-110">Example 1: Set backup configuration</span></span>
```powershell
PS C:\> Set-AzsBackupConfiguration -Path "\\***.***.***.***\Share" -Username "asdomain1\azurestackadmin" -Password $password  -EncryptionCertPath $encryptionCertPath

```

<span data-ttu-id="7c6b7-111">Defina a configuração de backup do Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="7c6b7-111">Set Azure Stack backup configuration.</span></span>

## <span data-ttu-id="7c6b7-112">OS</span><span class="sxs-lookup"><span data-stu-id="7c6b7-112">PARAMETERS</span></span>

### <span data-ttu-id="7c6b7-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7c6b7-113">-AsJob</span></span>
<span data-ttu-id="7c6b7-114">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="7c6b7-114">Run the command as a job</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="7c6b7-115">-Backup</span><span class="sxs-lookup"><span data-stu-id="7c6b7-115">-Backup</span></span>
<span data-ttu-id="7c6b7-116">Informações sobre o local do backup.</span><span class="sxs-lookup"><span data-stu-id="7c6b7-116">Information about the backup location.</span></span>
<span data-ttu-id="7c6b7-117">Para construir, consulte a seção de notas para propriedades de BACKUP e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="7c6b7-117">To construct, see NOTES section for BACKUP properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.BackupAdmin.Models.Api20180901.IBackupLocation
Parameter Sets: Update
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="7c6b7-118">-BackupFrequencyInHours</span><span class="sxs-lookup"><span data-stu-id="7c6b7-118">-BackupFrequencyInHours</span></span>
<span data-ttu-id="7c6b7-119">O intervalo, em horas, para a frequência com que o Agendador faz um backup.</span><span class="sxs-lookup"><span data-stu-id="7c6b7-119">The interval, in hours, for the frequency that the scheduler takes a backup.</span></span>

```yaml
Type: System.Int32
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="7c6b7-120">-BackupRetentionPeriodInDays</span><span class="sxs-lookup"><span data-stu-id="7c6b7-120">-BackupRetentionPeriodInDays</span></span>
<span data-ttu-id="7c6b7-121">O período de retenção, em dias, para fins de backup no local de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="7c6b7-121">The retention period, in days, for backs in the storage location.</span></span>

```yaml
Type: System.Int32
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="7c6b7-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c6b7-122">-DefaultProfile</span></span>
<span data-ttu-id="7c6b7-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7c6b7-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="7c6b7-124">-EncryptionCertPath</span><span class="sxs-lookup"><span data-stu-id="7c6b7-124">-EncryptionCertPath</span></span>
<span data-ttu-id="7c6b7-125">Caminho para o arquivo de certificado de criptografia com chave pública (. cer).</span><span class="sxs-lookup"><span data-stu-id="7c6b7-125">Path to the encryption cert file with public key (.cer).</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="7c6b7-126">-IsBackupSchedulerEnabled</span><span class="sxs-lookup"><span data-stu-id="7c6b7-126">-IsBackupSchedulerEnabled</span></span>
<span data-ttu-id="7c6b7-127">Verdadeiro se o Agendador de backup estiver habilitado.</span><span class="sxs-lookup"><span data-stu-id="7c6b7-127">True if the backup scheduler is enabled.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="7c6b7-128">-Local</span><span class="sxs-lookup"><span data-stu-id="7c6b7-128">-Location</span></span>
<span data-ttu-id="7c6b7-129">Nome do local de backup.</span><span class="sxs-lookup"><span data-stu-id="7c6b7-129">Name of the backup location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="7c6b7-130">-Nowait</span><span class="sxs-lookup"><span data-stu-id="7c6b7-130">-NoWait</span></span>
<span data-ttu-id="7c6b7-131">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="7c6b7-131">Run the command asynchronously</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="7c6b7-132">-Senha</span><span class="sxs-lookup"><span data-stu-id="7c6b7-132">-Password</span></span>
<span data-ttu-id="7c6b7-133">Senha para acessar o local.</span><span class="sxs-lookup"><span data-stu-id="7c6b7-133">Password to access the location.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="7c6b7-134">-Caminho</span><span class="sxs-lookup"><span data-stu-id="7c6b7-134">-Path</span></span>
<span data-ttu-id="7c6b7-135">Caminho para o local de atualização</span><span class="sxs-lookup"><span data-stu-id="7c6b7-135">Path to the update location</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="7c6b7-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c6b7-136">-ResourceGroupName</span></span>
<span data-ttu-id="7c6b7-137">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="7c6b7-137">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: "system.$((Get-AzLocation)[0].Location)"
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="7c6b7-138">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7c6b7-138">-SubscriptionId</span></span>
<span data-ttu-id="7c6b7-139">Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="7c6b7-139">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="7c6b7-140">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="7c6b7-140">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="7c6b7-141">-Marca</span><span class="sxs-lookup"><span data-stu-id="7c6b7-141">-Tag</span></span>
<span data-ttu-id="7c6b7-142">Lista de pares de valores chave.</span><span class="sxs-lookup"><span data-stu-id="7c6b7-142">List of key value pairs.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="7c6b7-143">-UserName</span><span class="sxs-lookup"><span data-stu-id="7c6b7-143">-UserName</span></span>
<span data-ttu-id="7c6b7-144">Nome de usuário para acessar o local.</span><span class="sxs-lookup"><span data-stu-id="7c6b7-144">Username to access the location.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="7c6b7-145">-Confirme</span><span class="sxs-lookup"><span data-stu-id="7c6b7-145">-Confirm</span></span>
<span data-ttu-id="7c6b7-146">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7c6b7-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7c6b7-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7c6b7-147">-WhatIf</span></span>
<span data-ttu-id="7c6b7-148">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="7c6b7-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7c6b7-149">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7c6b7-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7c6b7-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c6b7-150">CommonParameters</span></span>
<span data-ttu-id="7c6b7-151">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7c6b7-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c6b7-152">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7c6b7-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c6b7-153">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7c6b7-153">INPUTS</span></span>

### <span data-ttu-id="7c6b7-154">Microsoft. Azure. PowerShell. cmdlets. BackupAdmin. Models. Api20180901. IBackupLocation</span><span class="sxs-lookup"><span data-stu-id="7c6b7-154">Microsoft.Azure.PowerShell.Cmdlets.BackupAdmin.Models.Api20180901.IBackupLocation</span></span>

## <span data-ttu-id="7c6b7-155">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7c6b7-155">OUTPUTS</span></span>

### <span data-ttu-id="7c6b7-156">Microsoft. Azure. PowerShell. cmdlets. BackupAdmin. Models. Api20180901. IBackupLocation</span><span class="sxs-lookup"><span data-stu-id="7c6b7-156">Microsoft.Azure.PowerShell.Cmdlets.BackupAdmin.Models.Api20180901.IBackupLocation</span></span>



## <span data-ttu-id="7c6b7-157">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7c6b7-157">NOTES</span></span>

<span data-ttu-id="7c6b7-158">Propriedades de parâmetros complexas para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="7c6b7-158">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="7c6b7-159">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="7c6b7-159">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="7c6b7-160">BACKUP <IBackupLocation> : informações sobre o local do backup.</span><span class="sxs-lookup"><span data-stu-id="7c6b7-160">BACKUP <IBackupLocation>: Information about the backup location.</span></span>
  - <span data-ttu-id="7c6b7-161">`[Location <String>]`: Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="7c6b7-161">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="7c6b7-162">`[Tag <IResourceTags>]`: Lista de pares de valores chave.</span><span class="sxs-lookup"><span data-stu-id="7c6b7-162">`[Tag <IResourceTags>]`: List of key value pairs.</span></span>
    - <span data-ttu-id="7c6b7-163">`[(Any) <String>]`: Isso indica que qualquer propriedade pode ser adicionada a esse objeto.</span><span class="sxs-lookup"><span data-stu-id="7c6b7-163">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="7c6b7-164">`[BackupFrequencyInHours <Int32?>]`: O intervalo, em horas, para a frequência com que o Agendador faz um backup.</span><span class="sxs-lookup"><span data-stu-id="7c6b7-164">`[BackupFrequencyInHours <Int32?>]`: The interval, in hours, for the frequency that the scheduler takes a backup.</span></span>
  - <span data-ttu-id="7c6b7-165">`[BackupRetentionPeriodInDays <Int32?>]`: O período de retenção, em dias, para backups no local de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="7c6b7-165">`[BackupRetentionPeriodInDays <Int32?>]`: The retention period, in days, for backs in the storage location.</span></span>
  - <span data-ttu-id="7c6b7-166">`[EncryptionCertBase64 <String>]`: Os dados brutos da base64 do certificado de criptografia de backup.</span><span class="sxs-lookup"><span data-stu-id="7c6b7-166">`[EncryptionCertBase64 <String>]`: The base64 raw data for the backup encryption certificate.</span></span>
  - <span data-ttu-id="7c6b7-167">`[IsBackupSchedulerEnabled <Boolean?>]`: Verdadeiro se o Agendador de backup estiver habilitado.</span><span class="sxs-lookup"><span data-stu-id="7c6b7-167">`[IsBackupSchedulerEnabled <Boolean?>]`: True if the backup scheduler is enabled.</span></span>
  - <span data-ttu-id="7c6b7-168">`[Password <String>]`: Senha para acessar o local.</span><span class="sxs-lookup"><span data-stu-id="7c6b7-168">`[Password <String>]`: Password to access the location.</span></span>
  - <span data-ttu-id="7c6b7-169">`[Path <String>]`: Caminho para o local de atualização</span><span class="sxs-lookup"><span data-stu-id="7c6b7-169">`[Path <String>]`: Path to the update location</span></span>
  - <span data-ttu-id="7c6b7-170">`[UserName <String>]`: Nome de usuário para acessar o local.</span><span class="sxs-lookup"><span data-stu-id="7c6b7-170">`[UserName <String>]`: Username to access the location.</span></span>

## <span data-ttu-id="7c6b7-171">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7c6b7-171">RELATED LINKS</span></span>

