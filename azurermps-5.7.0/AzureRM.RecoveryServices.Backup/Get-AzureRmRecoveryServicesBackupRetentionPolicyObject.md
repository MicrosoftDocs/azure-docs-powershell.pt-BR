---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: 476094CC-A320-4B2D-B53D-6BFFE30C76CC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/get-azurermrecoveryservicesbackupretentionpolicyobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupRetentionPolicyObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupRetentionPolicyObject.md
ms.openlocfilehash: 83ed9062c5ad4beb0dff9c9c89b79a443cc68a52
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427490"
---
# <span data-ttu-id="3f665-101">Get-AzureRmRecoveryServicesBackupRetentionPolicyObject</span><span class="sxs-lookup"><span data-stu-id="3f665-101">Get-AzureRmRecoveryServicesBackupRetentionPolicyObject</span></span>

## <span data-ttu-id="3f665-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3f665-102">SYNOPSIS</span></span>
<span data-ttu-id="3f665-103">Obtém um objeto de política de retenção base.</span><span class="sxs-lookup"><span data-stu-id="3f665-103">Gets a base retention policy object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3f665-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3f665-104">SYNTAX</span></span>

```
Get-AzureRmRecoveryServicesBackupRetentionPolicyObject [-WorkloadType] <WorkloadType>
 [[-BackupManagementType] <BackupManagementType>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3f665-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3f665-105">DESCRIPTION</span></span>
<span data-ttu-id="3f665-106">O cmdlet **Get-AzureRmRecoveryServicesBackupRetentionPolicyObject** tem um **AzureRMRecoveryServicesRetentionPolicyObject** base.</span><span class="sxs-lookup"><span data-stu-id="3f665-106">The **Get-AzureRmRecoveryServicesBackupRetentionPolicyObject** cmdlet gets a base **AzureRMRecoveryServicesRetentionPolicyObject**.</span></span>
<span data-ttu-id="3f665-107">Esse objeto não é mantido no sistema.</span><span class="sxs-lookup"><span data-stu-id="3f665-107">This object is not persisted in the system.</span></span>
<span data-ttu-id="3f665-108">É um objeto temporário que você pode manipular e usar com o cmdlet New-AzureRmRecoveryServicesBackupProtectionPolicy para criar uma nova política de backup.</span><span class="sxs-lookup"><span data-stu-id="3f665-108">It is a temporary object that you can manipulate and use with the New-AzureRmRecoveryServicesBackupProtectionPolicy cmdlet to create a new backup policy.</span></span>

## <span data-ttu-id="3f665-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3f665-109">EXAMPLES</span></span>

### <span data-ttu-id="3f665-110">Exemplo 1: criar uma política de proteção de backup</span><span class="sxs-lookup"><span data-stu-id="3f665-110">Example 1: Create a backup protection policy</span></span>
```
PS C:\>$RetPol = Get-AzureRmRecoveryServicesBackupRetentionPolicyObject -WorkloadType AzureVM 
PS C:\> $RetPol.DailySchedule.DurationCountInDays = 365
PS C:\> $SchPol = Get-AzureRmRecoveryServicesBackupSchedulePolicyObject -WorkloadType AzureVM 
PS C:\> New-AzureRmRecoveryServicesBackupProtectionPolicy -Name "NewPolicy" -WorkloadType AzureVM -RetentionPolicy $RetPol -SchedulePolicy $SchPol
```

<span data-ttu-id="3f665-111">O primeiro comando obtém o objeto da política de retenção e, em seguida, armazena-o na variável $RetPol.</span><span class="sxs-lookup"><span data-stu-id="3f665-111">The first command gets the retention policy object, and then stores it in the $RetPol variable.</span></span>

<span data-ttu-id="3f665-112">O segundo comando define a duração do objeto da política de retenção como 365 dias.</span><span class="sxs-lookup"><span data-stu-id="3f665-112">The second command sets the duration for the retention policy object to 365 days.</span></span>

<span data-ttu-id="3f665-113">O terceiro comando obtém o objeto de política de agendamento e, em seguida, armazena-o na variável $SchPol.</span><span class="sxs-lookup"><span data-stu-id="3f665-113">The third command gets the schedule policy object, and then stores it in the $SchPol variable.</span></span>

<span data-ttu-id="3f665-114">O último comando cria uma política de proteção de backup usando a política de retenção e a política de agendamento criadas com os comandos anteriores.</span><span class="sxs-lookup"><span data-stu-id="3f665-114">The last command creates a backup protection policy using the retention policy and schedule policy created with the previous commands.</span></span>

## <span data-ttu-id="3f665-115">OS</span><span class="sxs-lookup"><span data-stu-id="3f665-115">PARAMETERS</span></span>

### <span data-ttu-id="3f665-116">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="3f665-116">-BackupManagementType</span></span>
<span data-ttu-id="3f665-117">Especifica o tipo de gerenciamento de backup.</span><span class="sxs-lookup"><span data-stu-id="3f665-117">Specifies the Backup management type.</span></span>
<span data-ttu-id="3f665-118">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="3f665-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3f665-119">AzureVM</span><span class="sxs-lookup"><span data-stu-id="3f665-119">AzureVM</span></span> 
- <span data-ttu-id="3f665-120">AzureSQLDatabase</span><span class="sxs-lookup"><span data-stu-id="3f665-120">AzureSQLDatabase</span></span>

```yaml
Type: BackupManagementType
Parameter Sets: (All)
Aliases: 
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f665-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f665-121">-DefaultProfile</span></span>
<span data-ttu-id="3f665-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3f665-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3f665-123">-Workloadtype</span><span class="sxs-lookup"><span data-stu-id="3f665-123">-WorkloadType</span></span>
<span data-ttu-id="3f665-124">Especifica o tipo de carga de trabalho.</span><span class="sxs-lookup"><span data-stu-id="3f665-124">Specifies the workload type.</span></span>
<span data-ttu-id="3f665-125">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="3f665-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3f665-126">AzureVM</span><span class="sxs-lookup"><span data-stu-id="3f665-126">AzureVM</span></span> 
- <span data-ttu-id="3f665-127">AzureSQLDatabase</span><span class="sxs-lookup"><span data-stu-id="3f665-127">AzureSQLDatabase</span></span>

```yaml
Type: WorkloadType
Parameter Sets: (All)
Aliases: 
Accepted values: AzureVM, AzureSQLDatabase

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f665-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f665-128">CommonParameters</span></span>
<span data-ttu-id="3f665-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f665-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f665-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3f665-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f665-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3f665-131">INPUTS</span></span>

### <span data-ttu-id="3f665-132">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="3f665-132">None</span></span>
<span data-ttu-id="3f665-133">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="3f665-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3f665-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3f665-134">OUTPUTS</span></span>

### <span data-ttu-id="3f665-135">Microsoft. Azure. Commands. Recoveryservices. backup. cmdlets. Models. RetentionPolicyBase</span><span class="sxs-lookup"><span data-stu-id="3f665-135">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RetentionPolicyBase</span></span>

## <span data-ttu-id="3f665-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3f665-136">NOTES</span></span>

## <span data-ttu-id="3f665-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3f665-137">RELATED LINKS</span></span>

[<span data-ttu-id="3f665-138">Get-AzureRmRecoveryServicesBackupSchedulePolicyObject</span><span class="sxs-lookup"><span data-stu-id="3f665-138">Get-AzureRmRecoveryServicesBackupSchedulePolicyObject</span></span>](./Get-AzureRmRecoveryServicesBackupSchedulePolicyObject.md)

[<span data-ttu-id="3f665-139">New-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="3f665-139">New-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzureRmRecoveryServicesBackupProtectionPolicy.md)


