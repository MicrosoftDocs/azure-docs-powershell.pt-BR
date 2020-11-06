---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 04D7317E-2089-4197-909D-89F0CEC4851A
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/backup-azrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Backup-AzRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Backup-AzRecoveryServicesBackupItem.md
ms.openlocfilehash: 58a4ae793a221a693ffb91c03f024292d364666b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93599763"
---
# <span data-ttu-id="3d613-101">Backup-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="3d613-101">Backup-AzRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="3d613-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3d613-102">SYNOPSIS</span></span>
<span data-ttu-id="3d613-103">Inicia um backup para um item de backup.</span><span class="sxs-lookup"><span data-stu-id="3d613-103">Starts a backup for a Backup item.</span></span>

## <span data-ttu-id="3d613-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3d613-104">SYNTAX</span></span>

```
Backup-AzRecoveryServicesBackupItem -Item <ItemBase> [-ExpiryDateTimeUTC <DateTime>] [-BackupType <BackupType>]
 [-EnableCompression] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3d613-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3d613-105">DESCRIPTION</span></span>
<span data-ttu-id="3d613-106">O cmdlet **backup-AzRecoveryServicesBackupItem** inicia um backup para um item do Azure backup protegido que não está vinculado ao agendamento de backup.</span><span class="sxs-lookup"><span data-stu-id="3d613-106">The **Backup-AzRecoveryServicesBackupItem** cmdlet starts a backup for a protected Azure Backup item that is not tied to the backup schedule.</span></span>
<span data-ttu-id="3d613-107">Você pode fazer um backup inicial imediatamente após habilitar a proteção ou iniciar um backup após a falha de um backup agendado.</span><span class="sxs-lookup"><span data-stu-id="3d613-107">You can do an initial backup immediately after you enable protection or start a backup after a scheduled backup fails.</span></span>
<span data-ttu-id="3d613-108">Defina o contexto do cofre usando o cmdlet Set-AzRecoveryServicesVaultContext antes de usar o cmdlet atual.</span><span class="sxs-lookup"><span data-stu-id="3d613-108">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="3d613-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3d613-109">EXAMPLES</span></span>

### <span data-ttu-id="3d613-110">Exemplo 1: iniciar um backup para um item de backup</span><span class="sxs-lookup"><span data-stu-id="3d613-110">Example 1: Start a backup for a Backup item</span></span>
```
PS C:\> $NamedContainer = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -Name "pstestv2vm1" 
PS C:\> $Item = Get-AzRecoveryServicesBackupItem -Container $NamedContainer -WorkloadType AzureVM 
PS C:\> $Job = Backup-AzRecoveryServicesItem -Item $Item
Operation        Status               StartTime            EndTime                   JOBID                           
------------     ---------            ------               ---------                 -------                                         
pstestv2vm1      Backup               InProgress           4/23/2016 5:00:30 PM      cf4b3ef5-2fac-4c8e-a215-d2eba4124f27
```

<span data-ttu-id="3d613-111">O primeiro comando obtém o contêiner de backup do tipo AzureVM chamado pstestv2vm1 e, em seguida, armazena-o na variável $NamedContainer.</span><span class="sxs-lookup"><span data-stu-id="3d613-111">The first command gets the Backup container of type AzureVM named pstestv2vm1, and then stores it in the $NamedContainer variable.</span></span>
<span data-ttu-id="3d613-112">O segundo comando obtém o item de backup correspondente ao contêiner no $NamedContainer e, em seguida, armazena-o na variável $Item.</span><span class="sxs-lookup"><span data-stu-id="3d613-112">The second command gets the Backup item corresponding to the container in $NamedContainer, and then stores it in the $Item variable.</span></span>
<span data-ttu-id="3d613-113">O último comando dispara o trabalho de backup para o item de backup em $Item.</span><span class="sxs-lookup"><span data-stu-id="3d613-113">The last command triggers the backup job for the Backup item in $Item.</span></span>

## <span data-ttu-id="3d613-114">OS</span><span class="sxs-lookup"><span data-stu-id="3d613-114">PARAMETERS</span></span>

### <span data-ttu-id="3d613-115">-Backuptype</span><span class="sxs-lookup"><span data-stu-id="3d613-115">-BackupType</span></span>
<span data-ttu-id="3d613-116">Tipo de backup a ser realizado</span><span class="sxs-lookup"><span data-stu-id="3d613-116">Type of backup to be performed</span></span>

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

### <span data-ttu-id="3d613-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d613-117">-DefaultProfile</span></span>
<span data-ttu-id="3d613-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3d613-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3d613-119">-EnableCompression</span><span class="sxs-lookup"><span data-stu-id="3d613-119">-EnableCompression</span></span>
<span data-ttu-id="3d613-120">Se for necessário habilitar a compactação</span><span class="sxs-lookup"><span data-stu-id="3d613-120">If enabling compression is required</span></span>

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

### <span data-ttu-id="3d613-121">-ExpiryDateTimeUTC</span><span class="sxs-lookup"><span data-stu-id="3d613-121">-ExpiryDateTimeUTC</span></span>
<span data-ttu-id="3d613-122">Especifica um tempo de expiração como um objeto **DateTime** .</span><span class="sxs-lookup"><span data-stu-id="3d613-122">Specifies an expiry time as a **DateTime** object.</span></span>

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

### <span data-ttu-id="3d613-123">-Item</span><span class="sxs-lookup"><span data-stu-id="3d613-123">-Item</span></span>
<span data-ttu-id="3d613-124">Especifica um item de backup para o qual esse cmdlet inicia uma operação de backup.</span><span class="sxs-lookup"><span data-stu-id="3d613-124">Specifies a Backup item for which this cmdlet starts a backup operation.</span></span>

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

### <span data-ttu-id="3d613-125">-Cofreid</span><span class="sxs-lookup"><span data-stu-id="3d613-125">-VaultId</span></span>
<span data-ttu-id="3d613-126">ID do braço do cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="3d613-126">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="3d613-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="3d613-127">-Confirm</span></span>
<span data-ttu-id="3d613-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3d613-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3d613-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3d613-129">-WhatIf</span></span>
<span data-ttu-id="3d613-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="3d613-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3d613-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3d613-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3d613-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d613-132">CommonParameters</span></span>
<span data-ttu-id="3d613-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d613-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d613-134">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3d613-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d613-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3d613-135">INPUTS</span></span>

### <span data-ttu-id="3d613-136">Microsoft. Azure. Commands. Recoveryservices. backup. cmdlets. Models. dobase</span><span class="sxs-lookup"><span data-stu-id="3d613-136">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

### <span data-ttu-id="3d613-137">System. Nullable ' 1 [[System. DateTime, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="3d613-137">System.Nullable\`1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="3d613-138">System. String</span><span class="sxs-lookup"><span data-stu-id="3d613-138">System.String</span></span>

## <span data-ttu-id="3d613-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3d613-139">OUTPUTS</span></span>

### <span data-ttu-id="3d613-140">Microsoft. Azure. Commands. Recoveryservices. backup. cmdlets. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="3d613-140">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="3d613-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3d613-141">NOTES</span></span>

## <span data-ttu-id="3d613-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3d613-142">RELATED LINKS</span></span>

[<span data-ttu-id="3d613-143">Get-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="3d613-143">Get-AzRecoveryServicesBackupContainer</span></span>](./Get-AzRecoveryServicesBackupContainer.md)

[<span data-ttu-id="3d613-144">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="3d613-144">Get-AzRecoveryServicesBackupItem</span></span>](./Get-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="3d613-145">Restore-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="3d613-145">Restore-AzRecoveryServicesBackupItem</span></span>](./Restore-AzRecoveryServicesBackupItem.md)


