---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 04D7317E-2089-4197-909D-89F0CEC4851A
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/backup-azrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Backup-AzRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Backup-AzRecoveryServicesBackupItem.md
ms.openlocfilehash: 3ce18989f737a28cc0949027cb4ea827116b89a1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886866"
---
# <span data-ttu-id="37596-101">Backup-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="37596-101">Backup-AzRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="37596-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="37596-102">SYNOPSIS</span></span>

<span data-ttu-id="37596-103">Inicia um backup para um item backup.</span><span class="sxs-lookup"><span data-stu-id="37596-103">Starts a backup for a Backup item.</span></span>

## <span data-ttu-id="37596-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="37596-104">SYNTAX</span></span>

```
Backup-AzRecoveryServicesBackupItem -Item <ItemBase> [-ExpiryDateTimeUTC <DateTime>] [-BackupType <BackupType>]
 [-EnableCompression] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="37596-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="37596-105">DESCRIPTION</span></span>

<span data-ttu-id="37596-106">O cmdlet **Backup-AzRecoveryServicesBackupItem** recebe um backup de adhoc do item de backup protegido do Azure.</span><span class="sxs-lookup"><span data-stu-id="37596-106">The **Backup-AzRecoveryServicesBackupItem** cmdlet takes an adhoc backup of protected Azure backup item.</span></span> <span data-ttu-id="37596-107">Usando esse cmdlet, você pode fazer um backup inicial imediatamente após habilitar a proteção ou iniciar um backup se um backup agendado falhar.</span><span class="sxs-lookup"><span data-stu-id="37596-107">Using this cmdlet you can do an initial backup immediately after you enable protection or start a backup if a scheduled backup fails.</span></span> <span data-ttu-id="37596-108">Esse cmdlet também pode ser usado para retenção personalizada com ou sem data de expiração - os parâmetros de referência ajudam a obter mais detalhes.</span><span class="sxs-lookup"><span data-stu-id="37596-108">This cmdlet can also be used for custom retention with or without expiry date - refer parameters help text for more details.</span></span> 

## <span data-ttu-id="37596-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="37596-109">EXAMPLES</span></span>

### <span data-ttu-id="37596-110">Exemplo 1: Iniciar um backup de um item de backup</span><span class="sxs-lookup"><span data-stu-id="37596-110">Example 1: Start a backup for a Backup item</span></span>

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

<span data-ttu-id="37596-111">O primeiro comando obtém o contêiner backup do tipo AzureVM chamado pstestv2vm1 e o armazena na variável $NamedContainer.</span><span class="sxs-lookup"><span data-stu-id="37596-111">The first command gets the Backup container of type AzureVM named pstestv2vm1, and then stores it in the $NamedContainer variable.</span></span>
<span data-ttu-id="37596-112">O segundo comando obtém o item backup correspondente ao contêiner no $NamedContainer e o armazena na variável $Item.</span><span class="sxs-lookup"><span data-stu-id="37596-112">The second command gets the Backup item corresponding to the container in $NamedContainer, and then stores it in the $Item variable.</span></span>
<span data-ttu-id="37596-113">O último comando aciona o trabalho de backup para o item backup no $Item.</span><span class="sxs-lookup"><span data-stu-id="37596-113">The last command triggers the backup job for the Backup item in $Item.</span></span>

### <span data-ttu-id="37596-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="37596-114">Example 2</span></span>

<span data-ttu-id="37596-115">Inicia um backup para um item backup.</span><span class="sxs-lookup"><span data-stu-id="37596-115">Starts a backup for a Backup item.</span></span> <span data-ttu-id="37596-116">(gerado automaticamente)</span><span class="sxs-lookup"><span data-stu-id="37596-116">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Backup-AzRecoveryServicesBackupItem -ExpiryDateTimeUTC <DateTime> -Item $Item -VaultId $vault.ID
```

## <span data-ttu-id="37596-117">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="37596-117">PARAMETERS</span></span>

### <span data-ttu-id="37596-118">-BackupType</span><span class="sxs-lookup"><span data-stu-id="37596-118">-BackupType</span></span>

<span data-ttu-id="37596-119">Tipo de backup a ser executado</span><span class="sxs-lookup"><span data-stu-id="37596-119">Type of backup to be performed</span></span>

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

### <span data-ttu-id="37596-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37596-120">-DefaultProfile</span></span>

<span data-ttu-id="37596-121">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="37596-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="37596-122">-EnableCompression</span><span class="sxs-lookup"><span data-stu-id="37596-122">-EnableCompression</span></span>

<span data-ttu-id="37596-123">Se a habilitação da compactação for necessária</span><span class="sxs-lookup"><span data-stu-id="37596-123">If enabling compression is required</span></span>

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

### <span data-ttu-id="37596-124">-ExpiryDateTimeUTC</span><span class="sxs-lookup"><span data-stu-id="37596-124">-ExpiryDateTimeUTC</span></span>

<span data-ttu-id="37596-125">Especifica um tempo de expiração para o ponto de recuperação como um objeto DateTime, se nada for dado, ele leva o valor padrão de 30 dias.</span><span class="sxs-lookup"><span data-stu-id="37596-125">Specifies an expiry time for the Recovery point as a DateTime object, if nothing is given it takes the default value of  30 days.</span></span> <span data-ttu-id="37596-126">Aplicável à VM, SQL (somente para o tipo de backup completo somente cópia), itens de backup AFS.</span><span class="sxs-lookup"><span data-stu-id="37596-126">Applicable to VM, SQL (for only Copy-only-full backup type), AFS backup items.</span></span>

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

### <span data-ttu-id="37596-127">-Item</span><span class="sxs-lookup"><span data-stu-id="37596-127">-Item</span></span>

<span data-ttu-id="37596-128">Especifica um item backup para o qual este cmdlet inicia uma operação de backup.</span><span class="sxs-lookup"><span data-stu-id="37596-128">Specifies a Backup item for which this cmdlet starts a backup operation.</span></span>

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

### <span data-ttu-id="37596-129">-VaultId</span><span class="sxs-lookup"><span data-stu-id="37596-129">-VaultId</span></span>

<span data-ttu-id="37596-130">ARM ID do Cofre de Serviços de Recuperação.</span><span class="sxs-lookup"><span data-stu-id="37596-130">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="37596-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="37596-131">-Confirm</span></span>

<span data-ttu-id="37596-132">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="37596-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="37596-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="37596-133">-WhatIf</span></span>

<span data-ttu-id="37596-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="37596-134">Shows what would happen if the cmdlet runs.</span></span>

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

### <span data-ttu-id="37596-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37596-135">CommonParameters</span></span>
<span data-ttu-id="37596-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37596-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37596-137">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="37596-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37596-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="37596-138">INPUTS</span></span>

### <span data-ttu-id="37596-139">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span><span class="sxs-lookup"><span data-stu-id="37596-139">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

### <span data-ttu-id="37596-140">System.Nullable'1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="37596-140">System.Nullable\`1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="37596-141">System.String</span><span class="sxs-lookup"><span data-stu-id="37596-141">System.String</span></span>

## <span data-ttu-id="37596-142">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="37596-142">OUTPUTS</span></span>

### <span data-ttu-id="37596-143">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span><span class="sxs-lookup"><span data-stu-id="37596-143">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="37596-144">NOTES</span><span class="sxs-lookup"><span data-stu-id="37596-144">NOTES</span></span>

## <span data-ttu-id="37596-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="37596-145">RELATED LINKS</span></span>

[<span data-ttu-id="37596-146">Get-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="37596-146">Get-AzRecoveryServicesBackupContainer</span></span>](./Get-AzRecoveryServicesBackupContainer.md)

[<span data-ttu-id="37596-147">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="37596-147">Get-AzRecoveryServicesBackupItem</span></span>](./Get-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="37596-148">Restore-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="37596-148">Restore-AzRecoveryServicesBackupItem</span></span>](./Restore-AzRecoveryServicesBackupItem.md)
