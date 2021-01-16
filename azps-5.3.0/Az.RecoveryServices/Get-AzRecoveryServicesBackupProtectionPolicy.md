---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 2E202D0D-076D-431D-9338-9A84ABC0B461
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: 9595f3fc3062d6afdd5b5bbfab74f297b39b3f6c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98271385"
---
# <span data-ttu-id="2b78f-101">Get-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="2b78f-101">Get-AzRecoveryServicesBackupProtectionPolicy</span></span>

## <span data-ttu-id="2b78f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2b78f-102">SYNOPSIS</span></span>
<span data-ttu-id="2b78f-103">Obtém as políticas de proteção de backup para um cofre.</span><span class="sxs-lookup"><span data-stu-id="2b78f-103">Gets Backup protection policies for a vault.</span></span>

## <span data-ttu-id="2b78f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2b78f-104">SYNTAX</span></span>

### <span data-ttu-id="2b78f-105">Noparamset (padrão)</span><span class="sxs-lookup"><span data-stu-id="2b78f-105">NoParamSet (Default)</span></span>
```
Get-AzRecoveryServicesBackupProtectionPolicy [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2b78f-106">PolicyNameParamSet</span><span class="sxs-lookup"><span data-stu-id="2b78f-106">PolicyNameParamSet</span></span>
```
Get-AzRecoveryServicesBackupProtectionPolicy [-Name] <String> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2b78f-107">WorkloadParamSet</span><span class="sxs-lookup"><span data-stu-id="2b78f-107">WorkloadParamSet</span></span>
```
Get-AzRecoveryServicesBackupProtectionPolicy [-WorkloadType] <WorkloadType> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2b78f-108">WorkloadBackupManagementTypeParamSet</span><span class="sxs-lookup"><span data-stu-id="2b78f-108">WorkloadBackupManagementTypeParamSet</span></span>
```
Get-AzRecoveryServicesBackupProtectionPolicy [-WorkloadType] <WorkloadType>
 [-BackupManagementType] <BackupManagementType> [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2b78f-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2b78f-109">DESCRIPTION</span></span>
<span data-ttu-id="2b78f-110">O cmdlet **Get-AzRecoveryServicesBackupProtectionPolicy** Obtém as políticas de proteção de backup do Azure para um cofre.</span><span class="sxs-lookup"><span data-stu-id="2b78f-110">The **Get-AzRecoveryServicesBackupProtectionPolicy** cmdlet gets Azure Backup protection policies for a vault.</span></span>
<span data-ttu-id="2b78f-111">Defina o contexto do cofre usando o cmdlet Set-AzRecoveryServicesVaultContext antes de usar o cmdlet atual.</span><span class="sxs-lookup"><span data-stu-id="2b78f-111">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="2b78f-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2b78f-112">EXAMPLES</span></span>

### <span data-ttu-id="2b78f-113">Exemplo 1: obter todas as políticas no cofre</span><span class="sxs-lookup"><span data-stu-id="2b78f-113">Example 1: Get all policies in the vault</span></span>
```
PS C:\> Get-AzRecoveryServicesBackupProtectionPolicy 
Name                 WorkloadType       BackupManagementType BackupTime                DaysOfWeek   
----                 ------------       -------------------- ----------                ----------   
DefaultPolicy        AzureVM            AzureVM              4/14/2016 5:00:00 PM                   
NewPolicy            AzureVM            AzureVM              4/23/2016 5:30:00 PM                   
NewPolicy2           AzureVM            AzureVM              4/24/2016 1:30:00 AM
```

<span data-ttu-id="2b78f-114">Esse comando obtém todas as políticas de proteção criadas no cofre.</span><span class="sxs-lookup"><span data-stu-id="2b78f-114">This command gets all protection policies created in the vault.</span></span>

### <span data-ttu-id="2b78f-115">Exemplo 2: obter uma política específica</span><span class="sxs-lookup"><span data-stu-id="2b78f-115">Example 2: Get a specific policy</span></span>
```
PS C:\> $Pol= Get-AzRecoveryServicesBackupProtectionPolicy -Name "DefaultPolicy"
```

<span data-ttu-id="2b78f-116">Esse comando obtém a política de proteção chamada DefaultPolicy e a armazena na variável $Pol.</span><span class="sxs-lookup"><span data-stu-id="2b78f-116">This command gets the protection policy named DefaultPolicy, and then stores it in the $Pol variable.</span></span>

## <span data-ttu-id="2b78f-117">OS</span><span class="sxs-lookup"><span data-stu-id="2b78f-117">PARAMETERS</span></span>

### <span data-ttu-id="2b78f-118">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="2b78f-118">-BackupManagementType</span></span>
<span data-ttu-id="2b78f-119">A classe de recursos que estão sendo protegidos.</span><span class="sxs-lookup"><span data-stu-id="2b78f-119">The class of resources being protected.</span></span> <span data-ttu-id="2b78f-120">Atualmente, os valores com suporte para esse cmdlet são AzureVM, AzureStorage, AzureWorkload</span><span class="sxs-lookup"><span data-stu-id="2b78f-120">Currently the values supported for this cmdlet are AzureVM, AzureStorage, AzureWorkload</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType]
Parameter Sets: WorkloadBackupManagementTypeParamSet
Aliases:
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureStorage, AzureWorkload, MAB

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b78f-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b78f-121">-DefaultProfile</span></span>
<span data-ttu-id="2b78f-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2b78f-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2b78f-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="2b78f-123">-Name</span></span>
<span data-ttu-id="2b78f-124">Especifica o nome da política.</span><span class="sxs-lookup"><span data-stu-id="2b78f-124">Specifies the name of the policy.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicyNameParamSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b78f-125">-Cofreid</span><span class="sxs-lookup"><span data-stu-id="2b78f-125">-VaultId</span></span>
<span data-ttu-id="2b78f-126">ID do braço do cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="2b78f-126">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="2b78f-127">-Workloadtype</span><span class="sxs-lookup"><span data-stu-id="2b78f-127">-WorkloadType</span></span>
<span data-ttu-id="2b78f-128">Tipo de carga de trabalho do recurso.</span><span class="sxs-lookup"><span data-stu-id="2b78f-128">Workload type of the resource.</span></span> <span data-ttu-id="2b78f-129">Os valores atuais com suporte são AzureVM, AzureFiles, MSSQL</span><span class="sxs-lookup"><span data-stu-id="2b78f-129">The current supported values are AzureVM, AzureFiles, MSSQL</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType]
Parameter Sets: WorkloadParamSet, WorkloadBackupManagementTypeParamSet
Aliases:
Accepted values: AzureVM, AzureSQLDatabase, AzureFiles, MSSQL

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b78f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b78f-130">CommonParameters</span></span>
<span data-ttu-id="2b78f-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2b78f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b78f-132">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2b78f-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b78f-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2b78f-133">INPUTS</span></span>

### <span data-ttu-id="2b78f-134">System. String</span><span class="sxs-lookup"><span data-stu-id="2b78f-134">System.String</span></span>

## <span data-ttu-id="2b78f-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2b78f-135">OUTPUTS</span></span>

### <span data-ttu-id="2b78f-136">Microsoft. Azure. Commands. Recoveryservices. backup. cmdlets. Models. PolicyBase</span><span class="sxs-lookup"><span data-stu-id="2b78f-136">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span></span>

## <span data-ttu-id="2b78f-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2b78f-137">NOTES</span></span>

## <span data-ttu-id="2b78f-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2b78f-138">RELATED LINKS</span></span>

[<span data-ttu-id="2b78f-139">New-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="2b78f-139">New-AzRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="2b78f-140">Remove-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="2b78f-140">Remove-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Remove-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="2b78f-141">Set-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="2b78f-141">Set-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Set-AzRecoveryServicesBackupProtectionPolicy.md)


