---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/register-azrecoveryservicesbackupcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Register-AzRecoveryServicesBackupContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Register-AzRecoveryServicesBackupContainer.md
ms.openlocfilehash: eeffbbd62a4c161b95004c6f4bd40d31fbd02517
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93599645"
---
# <span data-ttu-id="fc0cc-101">Register-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="fc0cc-101">Register-AzRecoveryServicesBackupContainer</span></span>

## <span data-ttu-id="fc0cc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fc0cc-102">SYNOPSIS</span></span>
<span data-ttu-id="fc0cc-103">Esse comando permite que o Azure backup converta o recurso em um contêiner de backup que, em seguida, será registrado para o cofre de serviços de recuperação fornecido.</span><span class="sxs-lookup"><span data-stu-id="fc0cc-103">This command allows Azure Backup to convert the �Resource� to a �Backup Container� which is then registered to the given Recovery services vault.</span></span> <span data-ttu-id="fc0cc-104">O serviço de backup do Azure pode descobrir que as cargas de trabalho do tipo de carga de trabalho fornecido dentro deste contêiner sejam protegidas mais tarde.</span><span class="sxs-lookup"><span data-stu-id="fc0cc-104">The Azure Backup service can then discover workloads of the given workload type within this container to be protected later.</span></span>

## <span data-ttu-id="fc0cc-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fc0cc-105">SYNTAX</span></span>

### <span data-ttu-id="fc0cc-106">Register (padrão)</span><span class="sxs-lookup"><span data-stu-id="fc0cc-106">Register (Default)</span></span>
```
Register-AzRecoveryServicesBackupContainer [-ResourceId] <String>
 [-BackupManagementType] <BackupManagementType> [-WorkloadType] <WorkloadType> [-Force] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fc0cc-107">Registre</span><span class="sxs-lookup"><span data-stu-id="fc0cc-107">ReRegister</span></span>
```
Register-AzRecoveryServicesBackupContainer [-Container] <ContainerBase>
 [-BackupManagementType] <BackupManagementType> [-WorkloadType] <WorkloadType> [-Force] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fc0cc-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fc0cc-108">DESCRIPTION</span></span>
<span data-ttu-id="fc0cc-109">O cmdlet registra uma VM do Azure para AzureWorkloads com workloadtype específico.</span><span class="sxs-lookup"><span data-stu-id="fc0cc-109">The cmdlet registers an Azure VM for AzureWorkloads with specific workloadType.</span></span>

## <span data-ttu-id="fc0cc-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fc0cc-110">EXAMPLES</span></span>

### <span data-ttu-id="fc0cc-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="fc0cc-111">Example 1</span></span>
```
PS C:\> Register-AzRecoveryServicesBackupContainer -ResourceId <AzureVMID> -VaultId <vaultID> -WorkloadType �MSSQL� -BackupManagementType �AzureWorkload�
```

<span data-ttu-id="fc0cc-112">O cmdlet registra uma VM do Azure para a carga de trabalho MSSQL.</span><span class="sxs-lookup"><span data-stu-id="fc0cc-112">The cmdlet registers an azure VM for the workload MSSQL.</span></span>

## <span data-ttu-id="fc0cc-113">OS</span><span class="sxs-lookup"><span data-stu-id="fc0cc-113">PARAMETERS</span></span>

### <span data-ttu-id="fc0cc-114">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="fc0cc-114">-BackupManagementType</span></span>
<span data-ttu-id="fc0cc-115">O tipo de gerenciamento de backup do contêiner de backup do Azure</span><span class="sxs-lookup"><span data-stu-id="fc0cc-115">The backup management type of the Azure Backup container</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType
Parameter Sets: (All)
Aliases:
Accepted values: AzureWorkload

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc0cc-116">-Contêiner</span><span class="sxs-lookup"><span data-stu-id="fc0cc-116">-Container</span></span>
<span data-ttu-id="fc0cc-117">Contêiner em que o item reside</span><span class="sxs-lookup"><span data-stu-id="fc0cc-117">Container where the item resides</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase
Parameter Sets: ReRegister
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc0cc-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc0cc-118">-DefaultProfile</span></span>
<span data-ttu-id="fc0cc-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fc0cc-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fc0cc-120">-Force</span><span class="sxs-lookup"><span data-stu-id="fc0cc-120">-Force</span></span>
<span data-ttu-id="fc0cc-121">Forçar Contêiner de registradores (impede a caixa de diálogo de confirmação).</span><span class="sxs-lookup"><span data-stu-id="fc0cc-121">Force registers container (prevents confirmation dialog).</span></span> <span data-ttu-id="fc0cc-122">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="fc0cc-122">This parameter is optional.</span></span>

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

### <span data-ttu-id="fc0cc-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fc0cc-123">-ResourceId</span></span>
<span data-ttu-id="fc0cc-124">ID do recurso do Azure cujo item representativo precisa ser verificado se já está protegido por algum cofre Recoveryservices na assinatura.</span><span class="sxs-lookup"><span data-stu-id="fc0cc-124">ID of the Azure Resource whose representative item needs to be checked if it is already protected by some RecoveryServices Vault in the subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Register
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc0cc-125">-Cofreid</span><span class="sxs-lookup"><span data-stu-id="fc0cc-125">-VaultId</span></span>
<span data-ttu-id="fc0cc-126">ID do braço do cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="fc0cc-126">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="fc0cc-127">-Workloadtype</span><span class="sxs-lookup"><span data-stu-id="fc0cc-127">-WorkloadType</span></span>
<span data-ttu-id="fc0cc-128">Tipo de carga de trabalho do recurso (por exemplo: AzureVM, WindowsServer, AzureFiles, MSSQL).</span><span class="sxs-lookup"><span data-stu-id="fc0cc-128">Workload type of the resource (for example: AzureVM, WindowsServer, AzureFiles, MSSQL).</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, AzureSQLDatabase, AzureFiles, MSSQL

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc0cc-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="fc0cc-129">-Confirm</span></span>
<span data-ttu-id="fc0cc-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fc0cc-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fc0cc-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fc0cc-131">-WhatIf</span></span>
<span data-ttu-id="fc0cc-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="fc0cc-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fc0cc-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="fc0cc-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fc0cc-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc0cc-134">CommonParameters</span></span>
<span data-ttu-id="fc0cc-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc0cc-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc0cc-136">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc0cc-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc0cc-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fc0cc-137">INPUTS</span></span>

### <span data-ttu-id="fc0cc-138">System. String</span><span class="sxs-lookup"><span data-stu-id="fc0cc-138">System.String</span></span>

## <span data-ttu-id="fc0cc-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fc0cc-139">OUTPUTS</span></span>

### <span data-ttu-id="fc0cc-140">Microsoft. Azure. Commands. Recoveryservices. backup. cmdlets. Models. ContainerBase</span><span class="sxs-lookup"><span data-stu-id="fc0cc-140">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>

## <span data-ttu-id="fc0cc-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fc0cc-141">NOTES</span></span>

## <span data-ttu-id="fc0cc-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fc0cc-142">RELATED LINKS</span></span>