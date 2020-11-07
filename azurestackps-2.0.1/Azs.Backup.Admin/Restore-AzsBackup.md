---
external help file: ''
Module Name: Azs.Backup.Admin
online version: https://docs.microsoft.com/powershell/module/azs.backup.admin/restore-azsbackup
schema: 2.0.0
ms.openlocfilehash: d441c74817ccaf1b32b7caf6fe811f6a5a4789da
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/24/2020
ms.locfileid: "93945353"
---
# <span data-ttu-id="8dfb1-101">Restore-AzsBackup</span><span class="sxs-lookup"><span data-stu-id="8dfb1-101">Restore-AzsBackup</span></span>

## <span data-ttu-id="8dfb1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8dfb1-102">SYNOPSIS</span></span>
<span data-ttu-id="8dfb1-103">Restaurar um backup.</span><span class="sxs-lookup"><span data-stu-id="8dfb1-103">Restore a backup.</span></span>

## <span data-ttu-id="8dfb1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8dfb1-104">SYNTAX</span></span>

### <span data-ttu-id="8dfb1-105">RestoreExpanded (padrão)</span><span class="sxs-lookup"><span data-stu-id="8dfb1-105">RestoreExpanded (Default)</span></span>
```
Restore-AzsBackup -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String>]
 [-DecryptionCertPassword <SecureString>] [-DecryptionCertPath <String>] [-RoleName <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-Force] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="8dfb1-106">Restaurar</span><span class="sxs-lookup"><span data-stu-id="8dfb1-106">Restore</span></span>
```
Restore-AzsBackup -Name <String> -RestoreOption <IRestoreOptions> [-Location <String>]
 [-ResourceGroupName <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-Force]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="8dfb1-107">RestoreViaIdentity</span><span class="sxs-lookup"><span data-stu-id="8dfb1-107">RestoreViaIdentity</span></span>
```
Restore-AzsBackup -InputObject <IBackupAdminIdentity> -RestoreOption <IRestoreOptions>
 [-DefaultProfile <PSObject>] [-AsJob] [-Force] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="8dfb1-108">RestoreViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="8dfb1-108">RestoreViaIdentityExpanded</span></span>
```
Restore-AzsBackup -InputObject <IBackupAdminIdentity> [-DecryptionCertPassword <SecureString>]
 [-DecryptionCertPath <String>] [-RoleName <String>] [-DefaultProfile <PSObject>] [-AsJob] [-Force] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="8dfb1-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8dfb1-109">DESCRIPTION</span></span>
<span data-ttu-id="8dfb1-110">Restaurar um backup.</span><span class="sxs-lookup"><span data-stu-id="8dfb1-110">Restore a backup.</span></span>

## <span data-ttu-id="8dfb1-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8dfb1-111">EXAMPLES</span></span>

### <span data-ttu-id="8dfb1-112">Exemplo 1: restaurar backup</span><span class="sxs-lookup"><span data-stu-id="8dfb1-112">Example 1: Restore Backup</span></span>
```powershell
PS C:\> Restore-AzsBackup -Name $backupResourceName -DecryptionCertPath $decryptionCertPath -DecryptionCertPassword $decryptionCertPassword

```

<span data-ttu-id="8dfb1-113">Restaure a partir de um backup de pilha do Azure.</span><span class="sxs-lookup"><span data-stu-id="8dfb1-113">Restore from an Azure Stack backup.</span></span>

## <span data-ttu-id="8dfb1-114">OS</span><span class="sxs-lookup"><span data-stu-id="8dfb1-114">PARAMETERS</span></span>

### <span data-ttu-id="8dfb1-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8dfb1-115">-AsJob</span></span>
<span data-ttu-id="8dfb1-116">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="8dfb1-116">Run the command as a job</span></span>

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

### <span data-ttu-id="8dfb1-117">-DecryptionCertPassword</span><span class="sxs-lookup"><span data-stu-id="8dfb1-117">-DecryptionCertPassword</span></span>
<span data-ttu-id="8dfb1-118">A senha do certificado de descriptografia.</span><span class="sxs-lookup"><span data-stu-id="8dfb1-118">The password for the decryption certificate.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: RestoreExpanded, RestoreViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="8dfb1-119">-DecryptionCertPath</span><span class="sxs-lookup"><span data-stu-id="8dfb1-119">-DecryptionCertPath</span></span>
<span data-ttu-id="8dfb1-120">Caminho para o arquivo de certificado de descriptografia com chave privada (. pfx).</span><span class="sxs-lookup"><span data-stu-id="8dfb1-120">Path to the decryption cert file with private key (.pfx).</span></span>

```yaml
Type: System.String
Parameter Sets: RestoreExpanded, RestoreViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="8dfb1-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8dfb1-121">-DefaultProfile</span></span>
<span data-ttu-id="8dfb1-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8dfb1-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8dfb1-123">-Force</span><span class="sxs-lookup"><span data-stu-id="8dfb1-123">-Force</span></span>
<span data-ttu-id="8dfb1-124">Não pedir confirmação</span><span class="sxs-lookup"><span data-stu-id="8dfb1-124">Don't ask for confirmation</span></span>

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

### <span data-ttu-id="8dfb1-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8dfb1-125">-InputObject</span></span>
<span data-ttu-id="8dfb1-126">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="8dfb1-126">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.BackupAdmin.Models.IBackupAdminIdentity
Parameter Sets: RestoreViaIdentity, RestoreViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="8dfb1-127">-Local</span><span class="sxs-lookup"><span data-stu-id="8dfb1-127">-Location</span></span>
<span data-ttu-id="8dfb1-128">Nome do local de backup.</span><span class="sxs-lookup"><span data-stu-id="8dfb1-128">Name of the backup location.</span></span>

```yaml
Type: System.String
Parameter Sets: Restore, RestoreExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="8dfb1-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="8dfb1-129">-Name</span></span>
<span data-ttu-id="8dfb1-130">Nome do backup.</span><span class="sxs-lookup"><span data-stu-id="8dfb1-130">Name of the backup.</span></span>

```yaml
Type: System.String
Parameter Sets: Restore, RestoreExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="8dfb1-131">-Nowait</span><span class="sxs-lookup"><span data-stu-id="8dfb1-131">-NoWait</span></span>
<span data-ttu-id="8dfb1-132">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="8dfb1-132">Run the command asynchronously</span></span>

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

### <span data-ttu-id="8dfb1-133">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8dfb1-133">-PassThru</span></span>
<span data-ttu-id="8dfb1-134">Retorna verdadeiro quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="8dfb1-134">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="8dfb1-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8dfb1-135">-ResourceGroupName</span></span>
<span data-ttu-id="8dfb1-136">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="8dfb1-136">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Restore, RestoreExpanded
Aliases:

Required: False
Position: Named
Default value: "system.$((Get-AzLocation)[0].Location)"
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="8dfb1-137">-RestoreOption</span><span class="sxs-lookup"><span data-stu-id="8dfb1-137">-RestoreOption</span></span>
<span data-ttu-id="8dfb1-138">Propriedades para opções de restauração.</span><span class="sxs-lookup"><span data-stu-id="8dfb1-138">Properties for restore options.</span></span>
<span data-ttu-id="8dfb1-139">Para construir, consulte a seção notas para propriedades RESTOREOPTION e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="8dfb1-139">To construct, see NOTES section for RESTOREOPTION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.BackupAdmin.Models.Api20180901.IRestoreOptions
Parameter Sets: Restore, RestoreViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="8dfb1-140">-RoleName</span><span class="sxs-lookup"><span data-stu-id="8dfb1-140">-RoleName</span></span>
<span data-ttu-id="8dfb1-141">O nome da função de pilha do Azure para restauração, defina-o como Empty para toda a função de infraestrutura</span><span class="sxs-lookup"><span data-stu-id="8dfb1-141">The Azure Stack role name for restore, set it to empty for all infrastructure role</span></span>

```yaml
Type: System.String
Parameter Sets: RestoreExpanded, RestoreViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="8dfb1-142">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8dfb1-142">-SubscriptionId</span></span>
<span data-ttu-id="8dfb1-143">Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="8dfb1-143">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="8dfb1-144">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="8dfb1-144">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Restore, RestoreExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="8dfb1-145">-Confirme</span><span class="sxs-lookup"><span data-stu-id="8dfb1-145">-Confirm</span></span>
<span data-ttu-id="8dfb1-146">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8dfb1-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8dfb1-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8dfb1-147">-WhatIf</span></span>
<span data-ttu-id="8dfb1-148">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="8dfb1-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8dfb1-149">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8dfb1-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8dfb1-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8dfb1-150">CommonParameters</span></span>
<span data-ttu-id="8dfb1-151">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8dfb1-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8dfb1-152">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8dfb1-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8dfb1-153">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8dfb1-153">INPUTS</span></span>

### <span data-ttu-id="8dfb1-154">Microsoft. Azure. PowerShell. cmdlets. BackupAdmin. Models. IBackupAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="8dfb1-154">Microsoft.Azure.PowerShell.Cmdlets.BackupAdmin.Models.IBackupAdminIdentity</span></span>

## <span data-ttu-id="8dfb1-155">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8dfb1-155">OUTPUTS</span></span>

### <span data-ttu-id="8dfb1-156">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8dfb1-156">System.Boolean</span></span>



## <span data-ttu-id="8dfb1-157">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8dfb1-157">NOTES</span></span>

<span data-ttu-id="8dfb1-158">Propriedades de parâmetros complexas para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="8dfb1-158">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8dfb1-159">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="8dfb1-159">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="8dfb1-160">INPUTobject <IBackupAdminIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="8dfb1-160">INPUTOBJECT <IBackupAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="8dfb1-161">`[Backup <String>]`: Nome do backup.</span><span class="sxs-lookup"><span data-stu-id="8dfb1-161">`[Backup <String>]`: Name of the backup.</span></span>
  - <span data-ttu-id="8dfb1-162">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="8dfb1-162">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="8dfb1-163">`[Location <String>]`: Nome do local de backup.</span><span class="sxs-lookup"><span data-stu-id="8dfb1-163">`[Location <String>]`: Name of the backup location.</span></span>
  - <span data-ttu-id="8dfb1-164">`[ResourceGroupName <String>]`: Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="8dfb1-164">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="8dfb1-165">`[SubscriptionId <String>]`: Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="8dfb1-165">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="8dfb1-166">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="8dfb1-166">The subscription ID forms part of the URI for every service call.</span></span>

<span data-ttu-id="8dfb1-167">RESTOREOPTION <IRestoreOptions> : propriedades para opções de restauração.</span><span class="sxs-lookup"><span data-stu-id="8dfb1-167">RESTOREOPTION <IRestoreOptions>: Properties for restore options.</span></span>
  - <span data-ttu-id="8dfb1-168">`[DecryptionCertBase64 <String>]`: Os dados brutos do arquivo de certificado na cadeia de caracteres base64.</span><span class="sxs-lookup"><span data-stu-id="8dfb1-168">`[DecryptionCertBase64 <String>]`: The certificate file raw data in Base64 string.</span></span> <span data-ttu-id="8dfb1-169">Deve ser o arquivo. pfx com a chave privada.</span><span class="sxs-lookup"><span data-stu-id="8dfb1-169">This should be the .pfx file with the private key.</span></span>
  - <span data-ttu-id="8dfb1-170">`[DecryptionCertPassword <String>]`: A senha do certificado de descriptografia.</span><span class="sxs-lookup"><span data-stu-id="8dfb1-170">`[DecryptionCertPassword <String>]`: The password for the decryption certificate.</span></span>
  - <span data-ttu-id="8dfb1-171">`[RoleName <String>]`: O nome da função de pilha do Azure para restauração, defina-o como Empty para toda a função de infraestrutura</span><span class="sxs-lookup"><span data-stu-id="8dfb1-171">`[RoleName <String>]`: The Azure Stack role name for restore, set it to empty for all infrastructure role</span></span>

## <span data-ttu-id="8dfb1-172">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8dfb1-172">RELATED LINKS</span></span>

