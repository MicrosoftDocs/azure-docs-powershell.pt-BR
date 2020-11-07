---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 2E202D0D-076D-431D-9338-9A84ABC0B461
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: 9595f3fc3062d6afdd5b5bbfab74f297b39b3f6c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93955315"
---
# <span data-ttu-id="face6-101">Get-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="face6-101">Get-AzRecoveryServicesBackupProtectionPolicy</span></span>

## <span data-ttu-id="face6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="face6-102">SYNOPSIS</span></span>
<span data-ttu-id="face6-103">Obtém as políticas de proteção de backup para um cofre.</span><span class="sxs-lookup"><span data-stu-id="face6-103">Gets Backup protection policies for a vault.</span></span>

## <span data-ttu-id="face6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="face6-104">SYNTAX</span></span>

### <span data-ttu-id="face6-105">Noparamset (padrão)</span><span class="sxs-lookup"><span data-stu-id="face6-105">NoParamSet (Default)</span></span>
```
Get-AzRecoveryServicesBackupProtectionPolicy [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="face6-106">PolicyNameParamSet</span><span class="sxs-lookup"><span data-stu-id="face6-106">PolicyNameParamSet</span></span>
```
Get-AzRecoveryServicesBackupProtectionPolicy [-Name] <String> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="face6-107">WorkloadParamSet</span><span class="sxs-lookup"><span data-stu-id="face6-107">WorkloadParamSet</span></span>
```
Get-AzRecoveryServicesBackupProtectionPolicy [-WorkloadType] <WorkloadType> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="face6-108">WorkloadBackupManagementTypeParamSet</span><span class="sxs-lookup"><span data-stu-id="face6-108">WorkloadBackupManagementTypeParamSet</span></span>
```
Get-AzRecoveryServicesBackupProtectionPolicy [-WorkloadType] <WorkloadType>
 [-BackupManagementType] <BackupManagementType> [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="face6-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="face6-109">DESCRIPTION</span></span>
<span data-ttu-id="face6-110">O cmdlet **Get-AzRecoveryServicesBackupProtectionPolicy** Obtém as políticas de proteção de backup do Azure para um cofre.</span><span class="sxs-lookup"><span data-stu-id="face6-110">The **Get-AzRecoveryServicesBackupProtectionPolicy** cmdlet gets Azure Backup protection policies for a vault.</span></span>
<span data-ttu-id="face6-111">Defina o contexto do cofre usando o cmdlet Set-AzRecoveryServicesVaultContext antes de usar o cmdlet atual.</span><span class="sxs-lookup"><span data-stu-id="face6-111">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="face6-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="face6-112">EXAMPLES</span></span>

### <span data-ttu-id="face6-113">Exemplo 1: obter todas as políticas no cofre</span><span class="sxs-lookup"><span data-stu-id="face6-113">Example 1: Get all policies in the vault</span></span>
```
PS C:\> Get-AzRecoveryServicesBackupProtectionPolicy 
Name                 WorkloadType       BackupManagementType BackupTime                DaysOfWeek   
----                 ------------       -------------------- ----------                ----------   
DefaultPolicy        AzureVM            AzureVM              4/14/2016 5:00:00 PM                   
NewPolicy            AzureVM            AzureVM              4/23/2016 5:30:00 PM                   
NewPolicy2           AzureVM            AzureVM              4/24/2016 1:30:00 AM
```

<span data-ttu-id="face6-114">Esse comando obtém todas as políticas de proteção criadas no cofre.</span><span class="sxs-lookup"><span data-stu-id="face6-114">This command gets all protection policies created in the vault.</span></span>

### <span data-ttu-id="face6-115">Exemplo 2: obter uma política específica</span><span class="sxs-lookup"><span data-stu-id="face6-115">Example 2: Get a specific policy</span></span>
```
PS C:\> $Pol= Get-AzRecoveryServicesBackupProtectionPolicy -Name "DefaultPolicy"
```

<span data-ttu-id="face6-116">Esse comando obtém a política de proteção chamada DefaultPolicy e a armazena na variável $Pol.</span><span class="sxs-lookup"><span data-stu-id="face6-116">This command gets the protection policy named DefaultPolicy, and then stores it in the $Pol variable.</span></span>

## <span data-ttu-id="face6-117">OS</span><span class="sxs-lookup"><span data-stu-id="face6-117">PARAMETERS</span></span>

### <span data-ttu-id="face6-118">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="face6-118">-BackupManagementType</span></span>
<span data-ttu-id="face6-119">A classe de recursos que estão sendo protegidos.</span><span class="sxs-lookup"><span data-stu-id="face6-119">The class of resources being protected.</span></span> <span data-ttu-id="face6-120">Atualmente, os valores com suporte para esse cmdlet são AzureVM, AzureStorage, AzureWorkload</span><span class="sxs-lookup"><span data-stu-id="face6-120">Currently the values supported for this cmdlet are AzureVM, AzureStorage, AzureWorkload</span></span>

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

### <span data-ttu-id="face6-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="face6-121">-DefaultProfile</span></span>
<span data-ttu-id="face6-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="face6-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="face6-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="face6-123">-Name</span></span>
<span data-ttu-id="face6-124">Especifica o nome da política.</span><span class="sxs-lookup"><span data-stu-id="face6-124">Specifies the name of the policy.</span></span>

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

### <span data-ttu-id="face6-125">-Cofreid</span><span class="sxs-lookup"><span data-stu-id="face6-125">-VaultId</span></span>
<span data-ttu-id="face6-126">ID do braço do cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="face6-126">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="face6-127">-Workloadtype</span><span class="sxs-lookup"><span data-stu-id="face6-127">-WorkloadType</span></span>
<span data-ttu-id="face6-128">Tipo de carga de trabalho do recurso.</span><span class="sxs-lookup"><span data-stu-id="face6-128">Workload type of the resource.</span></span> <span data-ttu-id="face6-129">Os valores atuais com suporte são AzureVM, AzureFiles, MSSQL</span><span class="sxs-lookup"><span data-stu-id="face6-129">The current supported values are AzureVM, AzureFiles, MSSQL</span></span>

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

### <span data-ttu-id="face6-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="face6-130">CommonParameters</span></span>
<span data-ttu-id="face6-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="face6-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="face6-132">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="face6-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="face6-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="face6-133">INPUTS</span></span>

### <span data-ttu-id="face6-134">System. String</span><span class="sxs-lookup"><span data-stu-id="face6-134">System.String</span></span>

## <span data-ttu-id="face6-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="face6-135">OUTPUTS</span></span>

### <span data-ttu-id="face6-136">Microsoft. Azure. Commands. Recoveryservices. backup. cmdlets. Models. PolicyBase</span><span class="sxs-lookup"><span data-stu-id="face6-136">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span></span>

## <span data-ttu-id="face6-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="face6-137">NOTES</span></span>

## <span data-ttu-id="face6-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="face6-138">RELATED LINKS</span></span>

[<span data-ttu-id="face6-139">New-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="face6-139">New-AzRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="face6-140">Remove-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="face6-140">Remove-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Remove-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="face6-141">Set-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="face6-141">Set-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Set-AzRecoveryServicesBackupProtectionPolicy.md)


