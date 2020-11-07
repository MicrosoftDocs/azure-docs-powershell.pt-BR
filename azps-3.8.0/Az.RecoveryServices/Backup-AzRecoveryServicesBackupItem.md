---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 04D7317E-2089-4197-909D-89F0CEC4851A
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/backup-azrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Backup-AzRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Backup-AzRecoveryServicesBackupItem.md
ms.openlocfilehash: fb2b6c370ee7ce43c877bfac57b64a203e9238cb
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93777417"
---
# <span data-ttu-id="27041-101">Backup-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="27041-101">Backup-AzRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="27041-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="27041-102">SYNOPSIS</span></span>

<span data-ttu-id="27041-103">Inicia um backup para um item de backup.</span><span class="sxs-lookup"><span data-stu-id="27041-103">Starts a backup for a Backup item.</span></span>

## <span data-ttu-id="27041-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="27041-104">SYNTAX</span></span>

```
Backup-AzRecoveryServicesBackupItem -Item <ItemBase> [-ExpiryDateTimeUTC <DateTime>] [-BackupType <BackupType>]
 [-EnableCompression] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="27041-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="27041-105">DESCRIPTION</span></span>

<span data-ttu-id="27041-106">O cmdlet **backup-AzRecoveryServicesBackupItem** inicia um backup para um item do Azure backup protegido que não está vinculado ao agendamento de backup.</span><span class="sxs-lookup"><span data-stu-id="27041-106">The **Backup-AzRecoveryServicesBackupItem** cmdlet starts a backup for a protected Azure Backup item that is not tied to the backup schedule.</span></span>
<span data-ttu-id="27041-107">Você pode fazer um backup inicial imediatamente após habilitar a proteção ou iniciar um backup após a falha de um backup agendado.</span><span class="sxs-lookup"><span data-stu-id="27041-107">You can do an initial backup immediately after you enable protection or start a backup after a scheduled backup fails.</span></span>
<span data-ttu-id="27041-108">Defina o contexto do cofre usando o parâmetro-Cofreid.</span><span class="sxs-lookup"><span data-stu-id="27041-108">Set the vault context by using the -VaultId parameter.</span></span>

## <span data-ttu-id="27041-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="27041-109">EXAMPLES</span></span>

### <span data-ttu-id="27041-110">Exemplo 1: iniciar um backup para um item de backup</span><span class="sxs-lookup"><span data-stu-id="27041-110">Example 1: Start a backup for a Backup item</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $NamedContainer = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -FriendlyName "pstestv2vm1" -VaultId $vault.ID
PS C:\> $Item = Get-AzRecoveryServicesBackupItem -Container $NamedContainer -WorkloadType AzureVM -VaultId $vault.ID
PS C:\> $Job = Backup-AzRecoveryServicesBackupItem -Item $Item -VaultId $vault.ID
PS C:\> $Job
Operation        Status               StartTime            EndTime                   JOBID
------------     ---------            ------               ---------                 -------
pstestv2vm1      Backup               InProgress           4/23/2016 5:00:30 PM      cf4b3ef5-2fac-4c8e-a215-d2eba4124f27
```

<span data-ttu-id="27041-111">O primeiro comando obtém o contêiner de backup do tipo AzureVM chamado pstestv2vm1 e, em seguida, armazena-o na variável $NamedContainer.</span><span class="sxs-lookup"><span data-stu-id="27041-111">The first command gets the Backup container of type AzureVM named pstestv2vm1, and then stores it in the $NamedContainer variable.</span></span>
<span data-ttu-id="27041-112">O segundo comando obtém o item de backup correspondente ao contêiner no $NamedContainer e, em seguida, armazena-o na variável $Item.</span><span class="sxs-lookup"><span data-stu-id="27041-112">The second command gets the Backup item corresponding to the container in $NamedContainer, and then stores it in the $Item variable.</span></span>
<span data-ttu-id="27041-113">O último comando dispara o trabalho de backup para o item de backup em $Item.</span><span class="sxs-lookup"><span data-stu-id="27041-113">The last command triggers the backup job for the Backup item in $Item.</span></span>

## <span data-ttu-id="27041-114">OS</span><span class="sxs-lookup"><span data-stu-id="27041-114">PARAMETERS</span></span>

### <span data-ttu-id="27041-115">-Backuptype</span><span class="sxs-lookup"><span data-stu-id="27041-115">-BackupType</span></span>

<span data-ttu-id="27041-116">Tipo de backup a ser realizado</span><span class="sxs-lookup"><span data-stu-id="27041-116">Type of backup to be performed</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupType
Parameter Sets: (All)
Aliases:
Accepted values: Full, Differential, Log, CopyOnlyFull

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27041-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27041-117">-DefaultProfile</span></span>

<span data-ttu-id="27041-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="27041-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="27041-119">-EnableCompression</span><span class="sxs-lookup"><span data-stu-id="27041-119">-EnableCompression</span></span>

<span data-ttu-id="27041-120">Se for necessário habilitar a compactação</span><span class="sxs-lookup"><span data-stu-id="27041-120">If enabling compression is required</span></span>

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

### <span data-ttu-id="27041-121">-ExpiryDateTimeUTC</span><span class="sxs-lookup"><span data-stu-id="27041-121">-ExpiryDateTimeUTC</span></span>

<span data-ttu-id="27041-122">Especifica um tempo de expiração como um objeto **DateTime** .</span><span class="sxs-lookup"><span data-stu-id="27041-122">Specifies an expiry time as a **DateTime** object.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="27041-123">-Item</span><span class="sxs-lookup"><span data-stu-id="27041-123">-Item</span></span>

<span data-ttu-id="27041-124">Especifica um item de backup para o qual esse cmdlet inicia uma operação de backup.</span><span class="sxs-lookup"><span data-stu-id="27041-124">Specifies a Backup item for which this cmdlet starts a backup operation.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="27041-125">-Cofreid</span><span class="sxs-lookup"><span data-stu-id="27041-125">-VaultId</span></span>

<span data-ttu-id="27041-126">ID do braço do cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="27041-126">ARM ID of the Recovery Services Vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="27041-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="27041-127">-Confirm</span></span>

<span data-ttu-id="27041-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="27041-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="27041-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="27041-129">-WhatIf</span></span>

<span data-ttu-id="27041-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="27041-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="27041-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="27041-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="27041-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27041-132">CommonParameters</span></span>
<span data-ttu-id="27041-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="27041-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27041-134">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="27041-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27041-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="27041-135">INPUTS</span></span>

### <span data-ttu-id="27041-136">Microsoft. Azure. Commands. Recoveryservices. backup. cmdlets. Models. dobase</span><span class="sxs-lookup"><span data-stu-id="27041-136">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

### <span data-ttu-id="27041-137">System. Nullable ' 1 [[System. DateTime, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="27041-137">System.Nullable\`1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="27041-138">System. String</span><span class="sxs-lookup"><span data-stu-id="27041-138">System.String</span></span>

## <span data-ttu-id="27041-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="27041-139">OUTPUTS</span></span>

### <span data-ttu-id="27041-140">Microsoft. Azure. Commands. Recoveryservices. backup. cmdlets. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="27041-140">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="27041-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="27041-141">NOTES</span></span>

## <span data-ttu-id="27041-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="27041-142">RELATED LINKS</span></span>

[<span data-ttu-id="27041-143">Get-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="27041-143">Get-AzRecoveryServicesBackupContainer</span></span>](./Get-AzRecoveryServicesBackupContainer.md)

[<span data-ttu-id="27041-144">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="27041-144">Get-AzRecoveryServicesBackupItem</span></span>](./Get-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="27041-145">Restore-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="27041-145">Restore-AzRecoveryServicesBackupItem</span></span>](./Restore-AzRecoveryServicesBackupItem.md)
