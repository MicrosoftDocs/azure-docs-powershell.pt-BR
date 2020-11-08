---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/register-azrecoveryservicesbackupcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Register-AzRecoveryServicesBackupContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Register-AzRecoveryServicesBackupContainer.md
ms.openlocfilehash: cfa8abf93fcb7eb4cd3848b1a5f69cf28a5fe6ab
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94118049"
---
# <span data-ttu-id="50ad8-101">Register-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="50ad8-101">Register-AzRecoveryServicesBackupContainer</span></span>

## <span data-ttu-id="50ad8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="50ad8-102">SYNOPSIS</span></span>
<span data-ttu-id="50ad8-103">O cmdlet **Register-AzRecoveryServicesBackupContainer** registra uma VM do Azure para AzureWorkloads com workloadtype específico.</span><span class="sxs-lookup"><span data-stu-id="50ad8-103">The **Register-AzRecoveryServicesBackupContainer** cmdlet registers an Azure VM for AzureWorkloads with specific workloadType.</span></span>

## <span data-ttu-id="50ad8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="50ad8-104">SYNTAX</span></span>

### <span data-ttu-id="50ad8-105">Register (padrão)</span><span class="sxs-lookup"><span data-stu-id="50ad8-105">Register (Default)</span></span>
```
Register-AzRecoveryServicesBackupContainer [-ResourceId] <String>
 [-BackupManagementType] <BackupManagementType> [-WorkloadType] <WorkloadType> [-Force] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50ad8-106">Registre</span><span class="sxs-lookup"><span data-stu-id="50ad8-106">ReRegister</span></span>
```
Register-AzRecoveryServicesBackupContainer [-Container] <ContainerBase>
 [-BackupManagementType] <BackupManagementType> [-WorkloadType] <WorkloadType> [-Force] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="50ad8-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="50ad8-107">DESCRIPTION</span></span>
<span data-ttu-id="50ad8-108">Esse comando permite que o Azure backup converta o recurso em um contêiner de backup que, em seguida, será registrado para o cofre de serviços de recuperação fornecido.</span><span class="sxs-lookup"><span data-stu-id="50ad8-108">This command allows Azure Backup to convert the Resource to a Backup Container which is then registered to the given Recovery services vault.</span></span> <span data-ttu-id="50ad8-109">O serviço de backup do Azure pode descobrir que as cargas de trabalho do tipo de carga de trabalho fornecido dentro deste contêiner sejam protegidas mais tarde.</span><span class="sxs-lookup"><span data-stu-id="50ad8-109">The Azure Backup service can then discover workloads of the given workload type within this container to be protected later.</span></span>

## <span data-ttu-id="50ad8-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="50ad8-110">EXAMPLES</span></span>

### <span data-ttu-id="50ad8-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="50ad8-111">Example 1</span></span>
```
PS C:\> Register-AzRecoveryServicesBackupContainer -ResourceId <AzureVMID> -VaultId <vaultID> -WorkloadType �MSSQL� -BackupManagementType �AzureWorkload�
```

<span data-ttu-id="50ad8-112">O cmdlet registra uma VM do Azure como um contêiner para a carga de trabalho MSSQL.</span><span class="sxs-lookup"><span data-stu-id="50ad8-112">The cmdlet registers an azure VM as a container for the workload MSSQL.</span></span>

## <span data-ttu-id="50ad8-113">OS</span><span class="sxs-lookup"><span data-stu-id="50ad8-113">PARAMETERS</span></span>

### <span data-ttu-id="50ad8-114">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="50ad8-114">-BackupManagementType</span></span>
<span data-ttu-id="50ad8-115">A classe de recursos que estão sendo protegidos.</span><span class="sxs-lookup"><span data-stu-id="50ad8-115">The class of resources being protected.</span></span> <span data-ttu-id="50ad8-116">Atualmente, o valor com suporte para esse cmdlet é AzureWorkload</span><span class="sxs-lookup"><span data-stu-id="50ad8-116">Currently the value supported for this cmdlet is AzureWorkload</span></span>

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

### <span data-ttu-id="50ad8-117">-Contêiner</span><span class="sxs-lookup"><span data-stu-id="50ad8-117">-Container</span></span>
<span data-ttu-id="50ad8-118">Contêiner em que o item reside</span><span class="sxs-lookup"><span data-stu-id="50ad8-118">Container where the item resides</span></span>

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

### <span data-ttu-id="50ad8-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50ad8-119">-DefaultProfile</span></span>
<span data-ttu-id="50ad8-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="50ad8-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="50ad8-121">-Force</span><span class="sxs-lookup"><span data-stu-id="50ad8-121">-Force</span></span>
<span data-ttu-id="50ad8-122">Forçar Contêiner de registradores (impede a caixa de diálogo de confirmação).</span><span class="sxs-lookup"><span data-stu-id="50ad8-122">Force registers container (prevents confirmation dialog).</span></span> <span data-ttu-id="50ad8-123">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="50ad8-123">This parameter is optional.</span></span>

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

### <span data-ttu-id="50ad8-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="50ad8-124">-ResourceId</span></span>
<span data-ttu-id="50ad8-125">ID do recurso do Azure cujo item representativo precisa ser verificado se já está protegido por algum cofre Recoveryservices na assinatura.</span><span class="sxs-lookup"><span data-stu-id="50ad8-125">ID of the Azure Resource whose representative item needs to be checked if it is already protected by some RecoveryServices Vault in the subscription.</span></span>

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

### <span data-ttu-id="50ad8-126">-Cofreid</span><span class="sxs-lookup"><span data-stu-id="50ad8-126">-VaultId</span></span>
<span data-ttu-id="50ad8-127">ID do braço do cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="50ad8-127">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="50ad8-128">-Workloadtype</span><span class="sxs-lookup"><span data-stu-id="50ad8-128">-WorkloadType</span></span>
<span data-ttu-id="50ad8-129">Tipo de carga de trabalho do recurso.</span><span class="sxs-lookup"><span data-stu-id="50ad8-129">Workload type of the resource.</span></span> <span data-ttu-id="50ad8-130">O valor atual com suporte é AzureVM, WindowsServer, AzureFiles, MSSQL</span><span class="sxs-lookup"><span data-stu-id="50ad8-130">The current supported value is AzureVM, WindowsServer, AzureFiles, MSSQL</span></span>

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

### <span data-ttu-id="50ad8-131">-Confirme</span><span class="sxs-lookup"><span data-stu-id="50ad8-131">-Confirm</span></span>
<span data-ttu-id="50ad8-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="50ad8-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="50ad8-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="50ad8-133">-WhatIf</span></span>
<span data-ttu-id="50ad8-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="50ad8-134">Shows what would happen if the cmdlet runs.</span></span>

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

### <span data-ttu-id="50ad8-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50ad8-135">CommonParameters</span></span>
<span data-ttu-id="50ad8-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50ad8-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50ad8-137">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="50ad8-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50ad8-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="50ad8-138">INPUTS</span></span>

### <span data-ttu-id="50ad8-139">System. String</span><span class="sxs-lookup"><span data-stu-id="50ad8-139">System.String</span></span>

## <span data-ttu-id="50ad8-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="50ad8-140">OUTPUTS</span></span>

### <span data-ttu-id="50ad8-141">Microsoft. Azure. Commands. Recoveryservices. backup. cmdlets. Models. ContainerBase</span><span class="sxs-lookup"><span data-stu-id="50ad8-141">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>

## <span data-ttu-id="50ad8-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="50ad8-142">NOTES</span></span>

## <span data-ttu-id="50ad8-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="50ad8-143">RELATED LINKS</span></span>
