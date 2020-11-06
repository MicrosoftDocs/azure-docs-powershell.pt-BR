---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: A8FDC5A3-F309-49B3-B417-8E0A1535BAF4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/stop-azurermrecoveryservicesbackupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Stop-AzureRmRecoveryServicesBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Stop-AzureRmRecoveryServicesBackupJob.md
ms.openlocfilehash: ba6f0ad6caee1ae5bac2e67855ef6ed5e9435068
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427479"
---
# <span data-ttu-id="491d7-101">Stop-AzureRmRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="491d7-101">Stop-AzureRmRecoveryServicesBackupJob</span></span>

## <span data-ttu-id="491d7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="491d7-102">SYNOPSIS</span></span>
<span data-ttu-id="491d7-103">Cancela um trabalho em execução.</span><span class="sxs-lookup"><span data-stu-id="491d7-103">Cancels a running job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="491d7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="491d7-104">SYNTAX</span></span>

### <span data-ttu-id="491d7-105">JobFilterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="491d7-105">JobFilterSet (Default)</span></span>
```
Stop-AzureRmRecoveryServicesBackupJob [-Job] <JobBase> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="491d7-106">IdFilterSet</span><span class="sxs-lookup"><span data-stu-id="491d7-106">IdFilterSet</span></span>
```
Stop-AzureRmRecoveryServicesBackupJob [-JobId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="491d7-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="491d7-107">DESCRIPTION</span></span>
<span data-ttu-id="491d7-108">O cmdlet **Stop-AzureRmRecoveryServicesBackupJob** cancela um trabalho de backup do Azure existente.</span><span class="sxs-lookup"><span data-stu-id="491d7-108">The **Stop-AzureRmRecoveryServicesBackupJob** cmdlet cancels an existing Azure Backup job.</span></span>
<span data-ttu-id="491d7-109">Use esse cmdlet para interromper um trabalho que leve muito tempo e bloqueie outras atividades.</span><span class="sxs-lookup"><span data-stu-id="491d7-109">Use this cmdlet to stop a job that takes too long and blocks other activities.</span></span>

<span data-ttu-id="491d7-110">Você pode cancelar somente os tipos de trabalho de backup e restauração.</span><span class="sxs-lookup"><span data-stu-id="491d7-110">You can cancel only Backup and Restore job types.</span></span>

<span data-ttu-id="491d7-111">Defina o contexto do cofre usando o cmdlet Set-AzureRmRecoveryServicesVaultContext antes de usar o cmdlet atual.</span><span class="sxs-lookup"><span data-stu-id="491d7-111">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="491d7-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="491d7-112">EXAMPLES</span></span>

### <span data-ttu-id="491d7-113">Exemplo 1: parar um trabalho de backup</span><span class="sxs-lookup"><span data-stu-id="491d7-113">Example 1: Stop a backup job</span></span>
```
PS C:\>$Job = Get-AzureRmRecoveryServicesBackupJob -Operation Backup
PS C:\> Stop-AzureRmRecoveryServicesBackupJob -JobID $Job.InstanceId
```

<span data-ttu-id="491d7-114">O primeiro comando obtém um trabalho de backup e armazena o trabalho na variável $Job.</span><span class="sxs-lookup"><span data-stu-id="491d7-114">The first command gets a backup job, and then stores the job in the $Job variable.</span></span>

<span data-ttu-id="491d7-115">O último comando interrompe o trabalho especificando a ID da instância do trabalho de backup em $Job.</span><span class="sxs-lookup"><span data-stu-id="491d7-115">The last command stops the job by specifying the Instance ID of the backup job in $Job.</span></span>

## <span data-ttu-id="491d7-116">OS</span><span class="sxs-lookup"><span data-stu-id="491d7-116">PARAMETERS</span></span>

### <span data-ttu-id="491d7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="491d7-117">-DefaultProfile</span></span>
<span data-ttu-id="491d7-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="491d7-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="491d7-119">-Trabalho</span><span class="sxs-lookup"><span data-stu-id="491d7-119">-Job</span></span>
<span data-ttu-id="491d7-120">Especifica um trabalho cancelado por esse cmdlet.</span><span class="sxs-lookup"><span data-stu-id="491d7-120">Specifies a job that this cmdlet cancels.</span></span>
<span data-ttu-id="491d7-121">Para obter um objeto **BackupJob** , use o cmdlet Get-AzureRmRecoveryServicesBackupJob.</span><span class="sxs-lookup"><span data-stu-id="491d7-121">To obtain a **BackupJob** object, use the Get-AzureRmRecoveryServicesBackupJob cmdlet.</span></span>

```yaml
Type: JobBase
Parameter Sets: JobFilterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="491d7-122">-JobId</span><span class="sxs-lookup"><span data-stu-id="491d7-122">-JobId</span></span>
<span data-ttu-id="491d7-123">Especifica a ID do trabalho a ser cancelado.</span><span class="sxs-lookup"><span data-stu-id="491d7-123">Specifies the ID of the job to cancel.</span></span>
<span data-ttu-id="491d7-124">A ID é a propriedade InstanceId de um objeto **BackupJob** .</span><span class="sxs-lookup"><span data-stu-id="491d7-124">The ID is the InstanceId property of a **BackupJob** object.</span></span>
<span data-ttu-id="491d7-125">Para obter um objeto **BackupJob** , use Get-AzureRmRecoveryServicesBackupJob.</span><span class="sxs-lookup"><span data-stu-id="491d7-125">To obtain an **BackupJob** object, use Get-AzureRmRecoveryServicesBackupJob.</span></span>

```yaml
Type: String
Parameter Sets: IdFilterSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="491d7-126">-Confirme</span><span class="sxs-lookup"><span data-stu-id="491d7-126">-Confirm</span></span>
<span data-ttu-id="491d7-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="491d7-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="491d7-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="491d7-128">-WhatIf</span></span>
<span data-ttu-id="491d7-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="491d7-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="491d7-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="491d7-130">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="491d7-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="491d7-131">CommonParameters</span></span>
<span data-ttu-id="491d7-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="491d7-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="491d7-133">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="491d7-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="491d7-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="491d7-134">INPUTS</span></span>

### <span data-ttu-id="491d7-135">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="491d7-135">None</span></span>
<span data-ttu-id="491d7-136">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="491d7-136">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="491d7-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="491d7-137">OUTPUTS</span></span>

### <span data-ttu-id="491d7-138">Microsoft. Azure. Commands. Recoveryservices. backup. cmdlets. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="491d7-138">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="491d7-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="491d7-139">NOTES</span></span>

## <span data-ttu-id="491d7-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="491d7-140">RELATED LINKS</span></span>

[<span data-ttu-id="491d7-141">Get-AzureRmRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="491d7-141">Get-AzureRmRecoveryServicesBackupJob</span></span>](./Get-AzureRmRecoveryServicesBackupJob.md)

[<span data-ttu-id="491d7-142">Wait-AzureRmRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="491d7-142">Wait-AzureRmRecoveryServicesBackupJob</span></span>](./Wait-AzureRmRecoveryServicesBackupJob.md)


