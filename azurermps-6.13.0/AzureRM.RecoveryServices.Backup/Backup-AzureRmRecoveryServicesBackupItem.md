---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: 04D7317E-2089-4197-909D-89F0CEC4851A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/backup-azurermrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Backup-AzureRmRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Backup-AzureRmRecoveryServicesBackupItem.md
ms.openlocfilehash: 9838db99fa1126f3948bb16f9ee16180cb652904
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429395"
---
# <span data-ttu-id="ea3cf-101">Backup-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="ea3cf-101">Backup-AzureRmRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="ea3cf-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ea3cf-102">SYNOPSIS</span></span>
<span data-ttu-id="ea3cf-103">Inicia um backup para um item de backup.</span><span class="sxs-lookup"><span data-stu-id="ea3cf-103">Starts a backup for a Backup item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ea3cf-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ea3cf-104">SYNTAX</span></span>

```
Backup-AzureRmRecoveryServicesBackupItem -Item <ItemBase> [-ExpiryDateTimeUTC <DateTime>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ea3cf-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ea3cf-105">DESCRIPTION</span></span>
<span data-ttu-id="ea3cf-106">O cmdlet **backup-AzureRmRecoveryServicesBackupItem** inicia um backup para um item do Azure backup protegido que não está vinculado ao agendamento de backup.</span><span class="sxs-lookup"><span data-stu-id="ea3cf-106">The **Backup-AzureRmRecoveryServicesBackupItem** cmdlet starts a backup for a protected Azure Backup item that is not tied to the backup schedule.</span></span>
<span data-ttu-id="ea3cf-107">Você pode fazer um backup inicial imediatamente após habilitar a proteção ou iniciar um backup após a falha de um backup agendado.</span><span class="sxs-lookup"><span data-stu-id="ea3cf-107">You can do an initial backup immediately after you enable protection or start a backup after a scheduled backup fails.</span></span>
<span data-ttu-id="ea3cf-108">Defina o contexto do cofre usando o cmdlet Set-AzureRmRecoveryServicesVaultContext antes de usar o cmdlet atual.</span><span class="sxs-lookup"><span data-stu-id="ea3cf-108">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="ea3cf-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ea3cf-109">EXAMPLES</span></span>

### <span data-ttu-id="ea3cf-110">Exemplo 1: iniciar um backup para um item de backup</span><span class="sxs-lookup"><span data-stu-id="ea3cf-110">Example 1: Start a backup for a Backup item</span></span>
```
PS C:\> $NamedContainer = Get-AzureRmRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -Name "pstestv2vm1" 
PS C:\> $Item = Get-AzureRmRecoveryServicesBackupItem -Container $NamedContainer -WorkloadType AzureVM 
PS C:\> $Job = Backup-AzureRmRecoveryServicesItem -Item $Item
Operation        Status               StartTime            EndTime                   JOBID                           
------------     ---------            ------               ---------                 -------                                         
pstestv2vm1      Backup               InProgress           4/23/2016 5:00:30 PM      cf4b3ef5-2fac-4c8e-a215-d2eba4124f27
```

<span data-ttu-id="ea3cf-111">O primeiro comando obtém o contêiner de backup do tipo AzureVM chamado pstestv2vm1 e, em seguida, armazena-o na variável $NamedContainer.</span><span class="sxs-lookup"><span data-stu-id="ea3cf-111">The first command gets the Backup container of type AzureVM named pstestv2vm1, and then stores it in the $NamedContainer variable.</span></span>
<span data-ttu-id="ea3cf-112">O segundo comando obtém o item de backup correspondente ao contêiner no $NamedContainer e, em seguida, armazena-o na variável $Item.</span><span class="sxs-lookup"><span data-stu-id="ea3cf-112">The second command gets the Backup item corresponding to the container in $NamedContainer, and then stores it in the $Item variable.</span></span>
<span data-ttu-id="ea3cf-113">O último comando dispara o trabalho de backup para o item de backup em $Item.</span><span class="sxs-lookup"><span data-stu-id="ea3cf-113">The last command triggers the backup job for the Backup item in $Item.</span></span>

## <span data-ttu-id="ea3cf-114">OS</span><span class="sxs-lookup"><span data-stu-id="ea3cf-114">PARAMETERS</span></span>

### <span data-ttu-id="ea3cf-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea3cf-115">-DefaultProfile</span></span>
<span data-ttu-id="ea3cf-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ea3cf-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea3cf-117">-ExpiryDateTimeUTC</span><span class="sxs-lookup"><span data-stu-id="ea3cf-117">-ExpiryDateTimeUTC</span></span>
<span data-ttu-id="ea3cf-118">Especifica um tempo de expiração como um objeto **DateTime** .</span><span class="sxs-lookup"><span data-stu-id="ea3cf-118">Specifies an expiry time as a **DateTime** object.</span></span>

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

### <span data-ttu-id="ea3cf-119">-Item</span><span class="sxs-lookup"><span data-stu-id="ea3cf-119">-Item</span></span>
<span data-ttu-id="ea3cf-120">Especifica um item de backup para o qual esse cmdlet inicia uma operação de backup.</span><span class="sxs-lookup"><span data-stu-id="ea3cf-120">Specifies a Backup item for which this cmdlet starts a backup operation.</span></span>

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

### <span data-ttu-id="ea3cf-121">-Cofreid</span><span class="sxs-lookup"><span data-stu-id="ea3cf-121">-VaultId</span></span>
<span data-ttu-id="ea3cf-122">ID do braço do cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="ea3cf-122">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="ea3cf-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="ea3cf-123">-Confirm</span></span>
<span data-ttu-id="ea3cf-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ea3cf-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ea3cf-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea3cf-125">-WhatIf</span></span>
<span data-ttu-id="ea3cf-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ea3cf-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ea3cf-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ea3cf-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ea3cf-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea3cf-128">CommonParameters</span></span>
<span data-ttu-id="ea3cf-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea3cf-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea3cf-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea3cf-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea3cf-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ea3cf-131">INPUTS</span></span>

### <span data-ttu-id="ea3cf-132">Microsoft. Azure. Commands. Recoveryservices. backup. cmdlets. Models. dobase</span><span class="sxs-lookup"><span data-stu-id="ea3cf-132">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>
<span data-ttu-id="ea3cf-133">Parâmetros: Item (ByValue)</span><span class="sxs-lookup"><span data-stu-id="ea3cf-133">Parameters: Item (ByValue)</span></span>

### <span data-ttu-id="ea3cf-134">System. Nullable ' 1 [[System. DateTime, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="ea3cf-134">System.Nullable\`1[[System.DateTime, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="ea3cf-135">System. String</span><span class="sxs-lookup"><span data-stu-id="ea3cf-135">System.String</span></span>
<span data-ttu-id="ea3cf-136">Parâmetros: Vaultid (ByValue)</span><span class="sxs-lookup"><span data-stu-id="ea3cf-136">Parameters: VaultId (ByValue)</span></span>

## <span data-ttu-id="ea3cf-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ea3cf-137">OUTPUTS</span></span>

### <span data-ttu-id="ea3cf-138">Microsoft. Azure. Commands. Recoveryservices. backup. cmdlets. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="ea3cf-138">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="ea3cf-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ea3cf-139">NOTES</span></span>

## <span data-ttu-id="ea3cf-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ea3cf-140">RELATED LINKS</span></span>

[<span data-ttu-id="ea3cf-141">Get-AzureRmRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="ea3cf-141">Get-AzureRmRecoveryServicesBackupContainer</span></span>](./Get-AzureRmRecoveryServicesBackupContainer.md)

[<span data-ttu-id="ea3cf-142">Get-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="ea3cf-142">Get-AzureRmRecoveryServicesBackupItem</span></span>](./Get-AzureRmRecoveryServicesBackupItem.md)

[<span data-ttu-id="ea3cf-143">Restore-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="ea3cf-143">Restore-AzureRmRecoveryServicesBackupItem</span></span>](./Restore-AzureRmRecoveryServicesBackupItem.md)


