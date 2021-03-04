---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/register-azrecoveryservicesbackupcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Register-AzRecoveryServicesBackupContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Register-AzRecoveryServicesBackupContainer.md
ms.openlocfilehash: 83a0e4edd82bd77358df1d95b53e388bb35a9e9b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885548"
---
# <span data-ttu-id="db928-101">Register-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="db928-101">Register-AzRecoveryServicesBackupContainer</span></span>

## <span data-ttu-id="db928-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="db928-102">SYNOPSIS</span></span>
<span data-ttu-id="db928-103">O cmdlet **Register-AzRecoveryServicesBackupContainer** registra uma VM do Azure para AzureWorkloads com workloadType específica.</span><span class="sxs-lookup"><span data-stu-id="db928-103">The **Register-AzRecoveryServicesBackupContainer** cmdlet registers an Azure VM for AzureWorkloads with specific workloadType.</span></span>

## <span data-ttu-id="db928-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="db928-104">SYNTAX</span></span>

### <span data-ttu-id="db928-105">Registrar (Padrão)</span><span class="sxs-lookup"><span data-stu-id="db928-105">Register (Default)</span></span>
```
Register-AzRecoveryServicesBackupContainer [-ResourceId] <String>
 [-BackupManagementType] <BackupManagementType> [-WorkloadType] <WorkloadType> [-Force] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="db928-106">ReRegister</span><span class="sxs-lookup"><span data-stu-id="db928-106">ReRegister</span></span>
```
Register-AzRecoveryServicesBackupContainer [-Container] <ContainerBase>
 [-BackupManagementType] <BackupManagementType> [-WorkloadType] <WorkloadType> [-Force] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="db928-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="db928-107">DESCRIPTION</span></span>
<span data-ttu-id="db928-108">Esse comando permite que o Backup do Azure converta o Recurso em um Contêiner de Backup que é registrado no cofre de serviços de Recuperação determinado.</span><span class="sxs-lookup"><span data-stu-id="db928-108">This command allows Azure Backup to convert the Resource to a Backup Container which is then registered to the given Recovery services vault.</span></span> <span data-ttu-id="db928-109">Em seguida, o serviço de Backup do Azure pode descobrir cargas de trabalho do tipo de carga de trabalho determinado dentro desse contêiner a serem protegidas posteriormente.</span><span class="sxs-lookup"><span data-stu-id="db928-109">The Azure Backup service can then discover workloads of the given workload type within this container to be protected later.</span></span>

## <span data-ttu-id="db928-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="db928-110">EXAMPLES</span></span>

### <span data-ttu-id="db928-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="db928-111">Example 1</span></span>
```
PS C:\> Register-AzRecoveryServicesBackupContainer -ResourceId <AzureVMID> -VaultId <vaultID> -WorkloadType �MSSQL� -BackupManagementType �AzureWorkload�
```

<span data-ttu-id="db928-112">O cmdlet registra uma VM do azure como um contêiner para a carga de trabalho MSSQL.</span><span class="sxs-lookup"><span data-stu-id="db928-112">The cmdlet registers an azure VM as a container for the workload MSSQL.</span></span>

## <span data-ttu-id="db928-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="db928-113">PARAMETERS</span></span>

### <span data-ttu-id="db928-114">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="db928-114">-BackupManagementType</span></span>
<span data-ttu-id="db928-115">A classe de recursos que está sendo protegida.</span><span class="sxs-lookup"><span data-stu-id="db928-115">The class of resources being protected.</span></span> <span data-ttu-id="db928-116">Atualmente, o valor suportado para este cmdlet é AzureWorkload</span><span class="sxs-lookup"><span data-stu-id="db928-116">Currently the value supported for this cmdlet is AzureWorkload</span></span>

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

### <span data-ttu-id="db928-117">-Container</span><span class="sxs-lookup"><span data-stu-id="db928-117">-Container</span></span>
<span data-ttu-id="db928-118">Contêiner onde o item reside</span><span class="sxs-lookup"><span data-stu-id="db928-118">Container where the item resides</span></span>

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

### <span data-ttu-id="db928-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db928-119">-DefaultProfile</span></span>
<span data-ttu-id="db928-120">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="db928-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="db928-121">-Force</span><span class="sxs-lookup"><span data-stu-id="db928-121">-Force</span></span>
<span data-ttu-id="db928-122">Force registra contêiner (impede a caixa de diálogo de confirmação).</span><span class="sxs-lookup"><span data-stu-id="db928-122">Force registers container (prevents confirmation dialog).</span></span> <span data-ttu-id="db928-123">Esse parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="db928-123">This parameter is optional.</span></span>

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

### <span data-ttu-id="db928-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="db928-124">-ResourceId</span></span>
<span data-ttu-id="db928-125">ID do Recurso do Azure cujo item representativo precisa ser verificado se ele já está protegido por alguns RecoveryServices Vault na assinatura.</span><span class="sxs-lookup"><span data-stu-id="db928-125">ID of the Azure Resource whose representative item needs to be checked if it is already protected by some RecoveryServices Vault in the subscription.</span></span>

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

### <span data-ttu-id="db928-126">-VaultId</span><span class="sxs-lookup"><span data-stu-id="db928-126">-VaultId</span></span>
<span data-ttu-id="db928-127">ARM ID do Cofre de Serviços de Recuperação.</span><span class="sxs-lookup"><span data-stu-id="db928-127">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="db928-128">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="db928-128">-WorkloadType</span></span>
<span data-ttu-id="db928-129">Tipo de carga de trabalho do recurso.</span><span class="sxs-lookup"><span data-stu-id="db928-129">Workload type of the resource.</span></span> <span data-ttu-id="db928-130">O valor suportado atual é AzureVM, WindowsServer, AzureFiles, MSSQL</span><span class="sxs-lookup"><span data-stu-id="db928-130">The current supported value is AzureVM, WindowsServer, AzureFiles, MSSQL</span></span>

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

### <span data-ttu-id="db928-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="db928-131">-Confirm</span></span>
<span data-ttu-id="db928-132">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="db928-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="db928-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="db928-133">-WhatIf</span></span>
<span data-ttu-id="db928-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="db928-134">Shows what would happen if the cmdlet runs.</span></span>

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

### <span data-ttu-id="db928-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db928-135">CommonParameters</span></span>
<span data-ttu-id="db928-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db928-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db928-137">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="db928-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db928-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="db928-138">INPUTS</span></span>

### <span data-ttu-id="db928-139">System.String</span><span class="sxs-lookup"><span data-stu-id="db928-139">System.String</span></span>

## <span data-ttu-id="db928-140">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="db928-140">OUTPUTS</span></span>

### <span data-ttu-id="db928-141">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span><span class="sxs-lookup"><span data-stu-id="db928-141">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>

## <span data-ttu-id="db928-142">NOTES</span><span class="sxs-lookup"><span data-stu-id="db928-142">NOTES</span></span>

## <span data-ttu-id="db928-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="db928-143">RELATED LINKS</span></span>
