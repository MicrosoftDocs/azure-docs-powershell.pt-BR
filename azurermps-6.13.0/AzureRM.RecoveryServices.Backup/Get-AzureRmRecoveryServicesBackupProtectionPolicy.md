---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: 2E202D0D-076D-431D-9338-9A84ABC0B461
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/get-azurermrecoveryservicesbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: d08bd0a02878b1b99b3243e80512df30eca6e1c9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430084"
---
# <span data-ttu-id="480eb-101">Get-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="480eb-101">Get-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>

## <span data-ttu-id="480eb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="480eb-102">SYNOPSIS</span></span>
<span data-ttu-id="480eb-103">Obtém as políticas de proteção de backup para um cofre.</span><span class="sxs-lookup"><span data-stu-id="480eb-103">Gets Backup protection policies for a vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="480eb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="480eb-104">SYNTAX</span></span>

### <span data-ttu-id="480eb-105">Noparamset (padrão)</span><span class="sxs-lookup"><span data-stu-id="480eb-105">NoParamSet (Default)</span></span>
```
Get-AzureRmRecoveryServicesBackupProtectionPolicy [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="480eb-106">PolicyNameParamSet</span><span class="sxs-lookup"><span data-stu-id="480eb-106">PolicyNameParamSet</span></span>
```
Get-AzureRmRecoveryServicesBackupProtectionPolicy [-Name] <String> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="480eb-107">WorkloadParamSet</span><span class="sxs-lookup"><span data-stu-id="480eb-107">WorkloadParamSet</span></span>
```
Get-AzureRmRecoveryServicesBackupProtectionPolicy [-WorkloadType] <WorkloadType> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="480eb-108">WorkloadBackupManagementTypeParamSet</span><span class="sxs-lookup"><span data-stu-id="480eb-108">WorkloadBackupManagementTypeParamSet</span></span>
```
Get-AzureRmRecoveryServicesBackupProtectionPolicy [-WorkloadType] <WorkloadType>
 [-BackupManagementType] <BackupManagementType> [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="480eb-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="480eb-109">DESCRIPTION</span></span>
<span data-ttu-id="480eb-110">O cmdlet **Get-AzureRmRecoveryServicesBackupProtectionPolicy** Obtém as políticas de proteção de backup do Azure para um cofre.</span><span class="sxs-lookup"><span data-stu-id="480eb-110">The **Get-AzureRmRecoveryServicesBackupProtectionPolicy** cmdlet gets Azure Backup protection policies for a vault.</span></span>
<span data-ttu-id="480eb-111">Defina o contexto do cofre usando o cmdlet Set-AzureRmRecoveryServicesVaultContext antes de usar o cmdlet atual.</span><span class="sxs-lookup"><span data-stu-id="480eb-111">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="480eb-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="480eb-112">EXAMPLES</span></span>

### <span data-ttu-id="480eb-113">Exemplo 1: obter todas as políticas no cofre</span><span class="sxs-lookup"><span data-stu-id="480eb-113">Example 1: Get all policies in the vault</span></span>
```
PS C:\> Get-AzureRmRecoveryServicesBackupProtectionPolicy 
Name                 WorkloadType       BackupManagementType BackupTime                DaysOfWeek   
----                 ------------       -------------------- ----------                ----------   
DefaultPolicy        AzureVM            AzureVM              4/14/2016 5:00:00 PM                   
NewPolicy            AzureVM            AzureVM              4/23/2016 5:30:00 PM                   
NewPolicy2           AzureVM            AzureVM              4/24/2016 1:30:00 AM
```

<span data-ttu-id="480eb-114">Esse comando obtém todas as políticas de proteção criadas no cofre.</span><span class="sxs-lookup"><span data-stu-id="480eb-114">This command gets all protection policies created in the vault.</span></span>

### <span data-ttu-id="480eb-115">Exemplo 2: obter uma política específica</span><span class="sxs-lookup"><span data-stu-id="480eb-115">Example 2: Get a specific policy</span></span>
```
PS C:\> $Pol= Get-AzureRmRecoveryServicesBackupProtectionPolicy -Name "DefaultPolicy"
```

<span data-ttu-id="480eb-116">Esse comando obtém a política de proteção chamada DefaultPolicy e a armazena na variável $Pol.</span><span class="sxs-lookup"><span data-stu-id="480eb-116">This command gets the protection policy named DefaultPolicy, and then stores it in the $Pol variable.</span></span>

## <span data-ttu-id="480eb-117">OS</span><span class="sxs-lookup"><span data-stu-id="480eb-117">PARAMETERS</span></span>

### <span data-ttu-id="480eb-118">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="480eb-118">-BackupManagementType</span></span>
<span data-ttu-id="480eb-119">Especifica o tipo de gerenciamento de backup.</span><span class="sxs-lookup"><span data-stu-id="480eb-119">Specifies the Backup management type.</span></span>
<span data-ttu-id="480eb-120">No momento, só há suporte para AzureVM, AzureStorage.</span><span class="sxs-lookup"><span data-stu-id="480eb-120">Currently, only AzureVM, AzureStorage is supported.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType]
Parameter Sets: WorkloadBackupManagementTypeParamSet
Aliases:
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL, AzureStorage

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="480eb-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="480eb-121">-DefaultProfile</span></span>
<span data-ttu-id="480eb-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="480eb-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="480eb-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="480eb-123">-Name</span></span>
<span data-ttu-id="480eb-124">Especifica o nome da política.</span><span class="sxs-lookup"><span data-stu-id="480eb-124">Specifies the name of the policy.</span></span>

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

### <span data-ttu-id="480eb-125">-Cofreid</span><span class="sxs-lookup"><span data-stu-id="480eb-125">-VaultId</span></span>
<span data-ttu-id="480eb-126">ID do braço do cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="480eb-126">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="480eb-127">-Workloadtype</span><span class="sxs-lookup"><span data-stu-id="480eb-127">-WorkloadType</span></span>
<span data-ttu-id="480eb-128">Especifica o tipo de carga de trabalho.</span><span class="sxs-lookup"><span data-stu-id="480eb-128">Specifies the workload type.</span></span>
<span data-ttu-id="480eb-129">No momento, só há suporte para AzureVM, AzureFiles.</span><span class="sxs-lookup"><span data-stu-id="480eb-129">Currently, only AzureVM, AzureFiles is supported.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType]
Parameter Sets: WorkloadParamSet, WorkloadBackupManagementTypeParamSet
Aliases:
Accepted values: AzureVM, AzureSQLDatabase, AzureFiles

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="480eb-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="480eb-130">CommonParameters</span></span>
<span data-ttu-id="480eb-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="480eb-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="480eb-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="480eb-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="480eb-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="480eb-133">INPUTS</span></span>

### <span data-ttu-id="480eb-134">System. String</span><span class="sxs-lookup"><span data-stu-id="480eb-134">System.String</span></span>
<span data-ttu-id="480eb-135">Parâmetros: Vaultid (ByValue)</span><span class="sxs-lookup"><span data-stu-id="480eb-135">Parameters: VaultId (ByValue)</span></span>

## <span data-ttu-id="480eb-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="480eb-136">OUTPUTS</span></span>

### <span data-ttu-id="480eb-137">Microsoft. Azure. Commands. Recoveryservices. backup. cmdlets. Models. PolicyBase</span><span class="sxs-lookup"><span data-stu-id="480eb-137">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span></span>

## <span data-ttu-id="480eb-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="480eb-138">NOTES</span></span>

## <span data-ttu-id="480eb-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="480eb-139">RELATED LINKS</span></span>

[<span data-ttu-id="480eb-140">New-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="480eb-140">New-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzureRmRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="480eb-141">Remove-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="480eb-141">Remove-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./Remove-AzureRmRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="480eb-142">Set-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="480eb-142">Set-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./Set-AzureRmRecoveryServicesBackupProtectionPolicy.md)


