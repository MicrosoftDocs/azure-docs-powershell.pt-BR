---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 476094CC-A320-4B2D-B53D-6BFFE30C76CC
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupretentionpolicyobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRetentionPolicyObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRetentionPolicyObject.md
ms.openlocfilehash: fd86f92fb200fe6ce65281fb5997798c9ec8adde
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93944729"
---
# <span data-ttu-id="7bab9-101">Get-AzRecoveryServicesBackupRetentionPolicyObject</span><span class="sxs-lookup"><span data-stu-id="7bab9-101">Get-AzRecoveryServicesBackupRetentionPolicyObject</span></span>

## <span data-ttu-id="7bab9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7bab9-102">SYNOPSIS</span></span>
<span data-ttu-id="7bab9-103">Obtém um objeto de política de retenção base.</span><span class="sxs-lookup"><span data-stu-id="7bab9-103">Gets a base retention policy object.</span></span>

## <span data-ttu-id="7bab9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7bab9-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupRetentionPolicyObject [-WorkloadType] <WorkloadType>
 [[-BackupManagementType] <BackupManagementType>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7bab9-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7bab9-105">DESCRIPTION</span></span>
<span data-ttu-id="7bab9-106">O cmdlet **Get-AzRecoveryServicesBackupRetentionPolicyObject** tem um **AzureRMRecoveryServicesRetentionPolicyObject** base.</span><span class="sxs-lookup"><span data-stu-id="7bab9-106">The **Get-AzRecoveryServicesBackupRetentionPolicyObject** cmdlet gets a base **AzureRMRecoveryServicesRetentionPolicyObject**.</span></span>
<span data-ttu-id="7bab9-107">Esse objeto não é mantido no sistema.</span><span class="sxs-lookup"><span data-stu-id="7bab9-107">This object is not persisted in the system.</span></span>
<span data-ttu-id="7bab9-108">É um objeto temporário que você pode manipular e usar com o cmdlet New-AzRecoveryServicesBackupProtectionPolicy para criar uma nova política de backup.</span><span class="sxs-lookup"><span data-stu-id="7bab9-108">It is a temporary object that you can manipulate and use with the New-AzRecoveryServicesBackupProtectionPolicy cmdlet to create a new backup policy.</span></span>

## <span data-ttu-id="7bab9-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7bab9-109">EXAMPLES</span></span>

### <span data-ttu-id="7bab9-110">Exemplo 1: criar uma política de proteção de backup</span><span class="sxs-lookup"><span data-stu-id="7bab9-110">Example 1: Create a backup protection policy</span></span>
```
PS C:\>$RetPol = Get-AzRecoveryServicesBackupRetentionPolicyObject -WorkloadType AzureVM 
PS C:\> $RetPol.DailySchedule.DurationCountInDays = 365
PS C:\> $SchPol = Get-AzRecoveryServicesBackupSchedulePolicyObject -WorkloadType AzureVM 
PS C:\> New-AzRecoveryServicesBackupProtectionPolicy -Name "NewPolicy" -WorkloadType AzureVM -RetentionPolicy $RetPol -SchedulePolicy $SchPol
```

<span data-ttu-id="7bab9-111">O primeiro comando obtém o objeto da política de retenção e, em seguida, armazena-o na variável $RetPol.</span><span class="sxs-lookup"><span data-stu-id="7bab9-111">The first command gets the retention policy object, and then stores it in the $RetPol variable.</span></span>
<span data-ttu-id="7bab9-112">O segundo comando define a duração do objeto da política de retenção como 365 dias.</span><span class="sxs-lookup"><span data-stu-id="7bab9-112">The second command sets the duration for the retention policy object to 365 days.</span></span>
<span data-ttu-id="7bab9-113">O terceiro comando obtém o objeto de política de agendamento e, em seguida, armazena-o na variável $SchPol.</span><span class="sxs-lookup"><span data-stu-id="7bab9-113">The third command gets the schedule policy object, and then stores it in the $SchPol variable.</span></span>
<span data-ttu-id="7bab9-114">O último comando cria uma política de proteção de backup usando a política de retenção e a política de agendamento criadas com os comandos anteriores.</span><span class="sxs-lookup"><span data-stu-id="7bab9-114">The last command creates a backup protection policy using the retention policy and schedule policy created with the previous commands.</span></span>

## <span data-ttu-id="7bab9-115">OS</span><span class="sxs-lookup"><span data-stu-id="7bab9-115">PARAMETERS</span></span>

### <span data-ttu-id="7bab9-116">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="7bab9-116">-BackupManagementType</span></span>
<span data-ttu-id="7bab9-117">Especifica o tipo de gerenciamento de backup.</span><span class="sxs-lookup"><span data-stu-id="7bab9-117">Specifies the Backup management type.</span></span>
<span data-ttu-id="7bab9-118">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="7bab9-118">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="7bab9-119">AzureVM</span><span class="sxs-lookup"><span data-stu-id="7bab9-119">AzureVM</span></span> 
- <span data-ttu-id="7bab9-120">AzureSQLDatabase</span><span class="sxs-lookup"><span data-stu-id="7bab9-120">AzureSQLDatabase</span></span>
- <span data-ttu-id="7bab9-121">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="7bab9-121">AzureStorage</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType]
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL, AzureStorage, AzureWorkload

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bab9-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7bab9-122">-DefaultProfile</span></span>
<span data-ttu-id="7bab9-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7bab9-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7bab9-124">-Workloadtype</span><span class="sxs-lookup"><span data-stu-id="7bab9-124">-WorkloadType</span></span>
<span data-ttu-id="7bab9-125">Especifica o tipo de carga de trabalho.</span><span class="sxs-lookup"><span data-stu-id="7bab9-125">Specifies the workload type.</span></span>
<span data-ttu-id="7bab9-126">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="7bab9-126">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="7bab9-127">AzureVM</span><span class="sxs-lookup"><span data-stu-id="7bab9-127">AzureVM</span></span> 
- <span data-ttu-id="7bab9-128">AzureSQLDatabase</span><span class="sxs-lookup"><span data-stu-id="7bab9-128">AzureSQLDatabase</span></span>
- <span data-ttu-id="7bab9-129">AzureFiles</span><span class="sxs-lookup"><span data-stu-id="7bab9-129">AzureFiles</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, AzureSQLDatabase, AzureFiles, MSSQL

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bab9-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7bab9-130">CommonParameters</span></span>
<span data-ttu-id="7bab9-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7bab9-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7bab9-132">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7bab9-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7bab9-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7bab9-133">INPUTS</span></span>

### <span data-ttu-id="7bab9-134">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="7bab9-134">None</span></span>

## <span data-ttu-id="7bab9-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7bab9-135">OUTPUTS</span></span>

### <span data-ttu-id="7bab9-136">Microsoft. Azure. Commands. Recoveryservices. backup. cmdlets. Models. RetentionPolicyBase</span><span class="sxs-lookup"><span data-stu-id="7bab9-136">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RetentionPolicyBase</span></span>

## <span data-ttu-id="7bab9-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7bab9-137">NOTES</span></span>

## <span data-ttu-id="7bab9-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7bab9-138">RELATED LINKS</span></span>

[<span data-ttu-id="7bab9-139">Get-AzRecoveryServicesBackupSchedulePolicyObject</span><span class="sxs-lookup"><span data-stu-id="7bab9-139">Get-AzRecoveryServicesBackupSchedulePolicyObject</span></span>](./Get-AzRecoveryServicesBackupSchedulePolicyObject.md)

[<span data-ttu-id="7bab9-140">New-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="7bab9-140">New-AzRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzRecoveryServicesBackupProtectionPolicy.md)


