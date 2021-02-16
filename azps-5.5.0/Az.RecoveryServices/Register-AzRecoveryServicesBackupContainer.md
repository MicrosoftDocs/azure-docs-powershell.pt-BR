---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/register-azrecoveryservicesbackupcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Register-AzRecoveryServicesBackupContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Register-AzRecoveryServicesBackupContainer.md
ms.openlocfilehash: cfa8abf93fcb7eb4cd3848b1a5f69cf28a5fe6ab
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114039"
---
# <span data-ttu-id="ca46c-101">Register-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="ca46c-101">Register-AzRecoveryServicesBackupContainer</span></span>

## <span data-ttu-id="ca46c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ca46c-102">SYNOPSIS</span></span>
<span data-ttu-id="ca46c-103">O cmdlet **Register-AzRecoveryServicesBackupContainer** registra um VM do Azure para AzureWorkloads com tipo de carga de trabalho específico.</span><span class="sxs-lookup"><span data-stu-id="ca46c-103">The **Register-AzRecoveryServicesBackupContainer** cmdlet registers an Azure VM for AzureWorkloads with specific workloadType.</span></span>

## <span data-ttu-id="ca46c-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ca46c-104">SYNTAX</span></span>

### <span data-ttu-id="ca46c-105">Registro (Padrão)</span><span class="sxs-lookup"><span data-stu-id="ca46c-105">Register (Default)</span></span>
```
Register-AzRecoveryServicesBackupContainer [-ResourceId] <String>
 [-BackupManagementType] <BackupManagementType> [-WorkloadType] <WorkloadType> [-Force] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ca46c-106">Registrar</span><span class="sxs-lookup"><span data-stu-id="ca46c-106">ReRegister</span></span>
```
Register-AzRecoveryServicesBackupContainer [-Container] <ContainerBase>
 [-BackupManagementType] <BackupManagementType> [-WorkloadType] <WorkloadType> [-Force] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ca46c-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="ca46c-107">DESCRIPTION</span></span>
<span data-ttu-id="ca46c-108">Esse comando permite que o Backup do Azure converta o Recurso em um Contêiner de Backup que é registrado no cofre de serviços de Recuperação determinado.</span><span class="sxs-lookup"><span data-stu-id="ca46c-108">This command allows Azure Backup to convert the Resource to a Backup Container which is then registered to the given Recovery services vault.</span></span> <span data-ttu-id="ca46c-109">O serviço backup do Azure pode descobrir cargas de trabalho de determinado tipo de carga de trabalho dentro desse contêiner para serem protegidas mais tarde.</span><span class="sxs-lookup"><span data-stu-id="ca46c-109">The Azure Backup service can then discover workloads of the given workload type within this container to be protected later.</span></span>

## <span data-ttu-id="ca46c-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="ca46c-110">EXAMPLES</span></span>

### <span data-ttu-id="ca46c-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ca46c-111">Example 1</span></span>
```
PS C:\> Register-AzRecoveryServicesBackupContainer -ResourceId <AzureVMID> -VaultId <vaultID> -WorkloadType �MSSQL� -BackupManagementType �AzureWorkload�
```

<span data-ttu-id="ca46c-112">O cmdlet registra um VM do azure como um contêiner para o MSSQL da carga de trabalho.</span><span class="sxs-lookup"><span data-stu-id="ca46c-112">The cmdlet registers an azure VM as a container for the workload MSSQL.</span></span>

## <span data-ttu-id="ca46c-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ca46c-113">PARAMETERS</span></span>

### <span data-ttu-id="ca46c-114">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="ca46c-114">-BackupManagementType</span></span>
<span data-ttu-id="ca46c-115">A classe de recursos que está sendo protegida.</span><span class="sxs-lookup"><span data-stu-id="ca46c-115">The class of resources being protected.</span></span> <span data-ttu-id="ca46c-116">Atualmente, o valor com suporte para este cmdlet é o AzureWorkload</span><span class="sxs-lookup"><span data-stu-id="ca46c-116">Currently the value supported for this cmdlet is AzureWorkload</span></span>

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

### <span data-ttu-id="ca46c-117">-Contêiner</span><span class="sxs-lookup"><span data-stu-id="ca46c-117">-Container</span></span>
<span data-ttu-id="ca46c-118">Contêiner onde o item reside</span><span class="sxs-lookup"><span data-stu-id="ca46c-118">Container where the item resides</span></span>

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

### <span data-ttu-id="ca46c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca46c-119">-DefaultProfile</span></span>
<span data-ttu-id="ca46c-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ca46c-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ca46c-121">-Forçar</span><span class="sxs-lookup"><span data-stu-id="ca46c-121">-Force</span></span>
<span data-ttu-id="ca46c-122">Forçar o contêiner de registros (impede a caixa de diálogo de confirmação).</span><span class="sxs-lookup"><span data-stu-id="ca46c-122">Force registers container (prevents confirmation dialog).</span></span> <span data-ttu-id="ca46c-123">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="ca46c-123">This parameter is optional.</span></span>

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

### <span data-ttu-id="ca46c-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ca46c-124">-ResourceId</span></span>
<span data-ttu-id="ca46c-125">A ID do Recurso do Azure cujo item representativo precisa ser verificado se ele já está protegido por algum Cofre recoveryServices na assinatura.</span><span class="sxs-lookup"><span data-stu-id="ca46c-125">ID of the Azure Resource whose representative item needs to be checked if it is already protected by some RecoveryServices Vault in the subscription.</span></span>

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

### <span data-ttu-id="ca46c-126">-VaultId</span><span class="sxs-lookup"><span data-stu-id="ca46c-126">-VaultId</span></span>
<span data-ttu-id="ca46c-127">ID arm do Cofre de Serviços de Recuperação.</span><span class="sxs-lookup"><span data-stu-id="ca46c-127">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="ca46c-128">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="ca46c-128">-WorkloadType</span></span>
<span data-ttu-id="ca46c-129">Tipo de carga de trabalho do recurso.</span><span class="sxs-lookup"><span data-stu-id="ca46c-129">Workload type of the resource.</span></span> <span data-ttu-id="ca46c-130">O valor com suporte atual é AzureVM, WindowsServer, AzureFiles, MSSQL</span><span class="sxs-lookup"><span data-stu-id="ca46c-130">The current supported value is AzureVM, WindowsServer, AzureFiles, MSSQL</span></span>

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

### <span data-ttu-id="ca46c-131">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="ca46c-131">-Confirm</span></span>
<span data-ttu-id="ca46c-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ca46c-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ca46c-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ca46c-133">-WhatIf</span></span>
<span data-ttu-id="ca46c-134">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="ca46c-134">Shows what would happen if the cmdlet runs.</span></span>

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

### <span data-ttu-id="ca46c-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca46c-135">CommonParameters</span></span>
<span data-ttu-id="ca46c-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca46c-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca46c-137">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ca46c-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca46c-138">Entradas</span><span class="sxs-lookup"><span data-stu-id="ca46c-138">INPUTS</span></span>

### <span data-ttu-id="ca46c-139">System.String</span><span class="sxs-lookup"><span data-stu-id="ca46c-139">System.String</span></span>

## <span data-ttu-id="ca46c-140">Saídas</span><span class="sxs-lookup"><span data-stu-id="ca46c-140">OUTPUTS</span></span>

### <span data-ttu-id="ca46c-141">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span><span class="sxs-lookup"><span data-stu-id="ca46c-141">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>

## <span data-ttu-id="ca46c-142">Notas</span><span class="sxs-lookup"><span data-stu-id="ca46c-142">NOTES</span></span>

## <span data-ttu-id="ca46c-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ca46c-143">RELATED LINKS</span></span>
