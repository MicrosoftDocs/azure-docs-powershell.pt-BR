---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: 2E202D0D-076D-431D-9338-9A84ABC0B461
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/get-azurermrecoveryservicesbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: 3220ef801ff86a3fb95a4595efd8c94330bfcba1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602148"
---
# <span data-ttu-id="29057-101">Get-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="29057-101">Get-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>

## <span data-ttu-id="29057-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="29057-102">SYNOPSIS</span></span>
<span data-ttu-id="29057-103">Obtém as políticas de proteção de backup para um cofre.</span><span class="sxs-lookup"><span data-stu-id="29057-103">Gets Backup protection policies for a vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="29057-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="29057-104">SYNTAX</span></span>

### <span data-ttu-id="29057-105">Noparamset (padrão)</span><span class="sxs-lookup"><span data-stu-id="29057-105">NoParamSet (Default)</span></span>
```
Get-AzureRmRecoveryServicesBackupProtectionPolicy [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="29057-106">PolicyNameParamSet</span><span class="sxs-lookup"><span data-stu-id="29057-106">PolicyNameParamSet</span></span>
```
Get-AzureRmRecoveryServicesBackupProtectionPolicy [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="29057-107">WorkloadParamSet</span><span class="sxs-lookup"><span data-stu-id="29057-107">WorkloadParamSet</span></span>
```
Get-AzureRmRecoveryServicesBackupProtectionPolicy [-WorkloadType] <WorkloadType>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="29057-108">WorkloadBackupManagementTypeParamSet</span><span class="sxs-lookup"><span data-stu-id="29057-108">WorkloadBackupManagementTypeParamSet</span></span>
```
Get-AzureRmRecoveryServicesBackupProtectionPolicy [-WorkloadType] <WorkloadType>
 [-BackupManagementType] <BackupManagementType> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="29057-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="29057-109">DESCRIPTION</span></span>
<span data-ttu-id="29057-110">O cmdlet **Get-AzureRmRecoveryServicesBackupProtectionPolicy** Obtém as políticas de proteção de backup do Azure para um cofre.</span><span class="sxs-lookup"><span data-stu-id="29057-110">The **Get-AzureRmRecoveryServicesBackupProtectionPolicy** cmdlet gets Azure Backup protection policies for a vault.</span></span>

<span data-ttu-id="29057-111">Defina o contexto do cofre usando o cmdlet Set-AzureRmRecoveryServicesVaultContext antes de usar o cmdlet atual.</span><span class="sxs-lookup"><span data-stu-id="29057-111">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="29057-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="29057-112">EXAMPLES</span></span>

### <span data-ttu-id="29057-113">Exemplo 1: obter todas as políticas no cofre</span><span class="sxs-lookup"><span data-stu-id="29057-113">Example 1: Get all policies in the vault</span></span>
```
PS C:\> Get-AzureRmRecoveryServicesBackupProtectionPolicy 
Name                 WorkloadType       BackupManagementType BackupTime                DaysOfWeek   
----                 ------------       -------------------- ----------                ----------   
DefaultPolicy        AzureVM            AzureVM              4/14/2016 5:00:00 PM                   
NewPolicy            AzureVM            AzureVM              4/23/2016 5:30:00 PM                   
NewPolicy2           AzureVM            AzureVM              4/24/2016 1:30:00 AM
```

<span data-ttu-id="29057-114">Esse comando obtém todas as políticas de proteção criadas no cofre.</span><span class="sxs-lookup"><span data-stu-id="29057-114">This command gets all protection policies created in the vault.</span></span>

### <span data-ttu-id="29057-115">Exemplo 2: obter uma política específica</span><span class="sxs-lookup"><span data-stu-id="29057-115">Example 2: Get a specific policy</span></span>
```
PS C:\> $Pol= Get-AzureRmRecoveryServicesBackupProtectionPolicy -Name "DefaultPolicy"
```

<span data-ttu-id="29057-116">Esse comando obtém a política de proteção chamada DefaultPolicy e a armazena na variável $Pol.</span><span class="sxs-lookup"><span data-stu-id="29057-116">This command gets the protection policy named DefaultPolicy, and then stores it in the $Pol variable.</span></span>

## <span data-ttu-id="29057-117">OS</span><span class="sxs-lookup"><span data-stu-id="29057-117">PARAMETERS</span></span>

### <span data-ttu-id="29057-118">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="29057-118">-BackupManagementType</span></span>
<span data-ttu-id="29057-119">Especifica o tipo de gerenciamento de backup.</span><span class="sxs-lookup"><span data-stu-id="29057-119">Specifies the Backup management type.</span></span>
<span data-ttu-id="29057-120">No momento, somente há suporte para AzureVM.</span><span class="sxs-lookup"><span data-stu-id="29057-120">Currently, only AzureVM is supported.</span></span>

```yaml
Type: BackupManagementType
Parameter Sets: WorkloadBackupManagementTypeParamSet
Aliases: 
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29057-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29057-121">-DefaultProfile</span></span>
<span data-ttu-id="29057-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="29057-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="29057-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="29057-123">-Name</span></span>
<span data-ttu-id="29057-124">Especifica o nome da política.</span><span class="sxs-lookup"><span data-stu-id="29057-124">Specifies the name of the policy.</span></span>

```yaml
Type: String
Parameter Sets: PolicyNameParamSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29057-125">-Workloadtype</span><span class="sxs-lookup"><span data-stu-id="29057-125">-WorkloadType</span></span>
<span data-ttu-id="29057-126">Especifica o tipo de carga de trabalho.</span><span class="sxs-lookup"><span data-stu-id="29057-126">Specifies the workload type.</span></span>
<span data-ttu-id="29057-127">No momento, somente há suporte para AzureVM.</span><span class="sxs-lookup"><span data-stu-id="29057-127">Currently, only AzureVM is supported.</span></span>

```yaml
Type: WorkloadType
Parameter Sets: WorkloadParamSet, WorkloadBackupManagementTypeParamSet
Aliases: 
Accepted values: AzureVM, AzureSQLDatabase

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29057-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29057-128">CommonParameters</span></span>
<span data-ttu-id="29057-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29057-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29057-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="29057-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29057-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="29057-131">INPUTS</span></span>

### <span data-ttu-id="29057-132">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="29057-132">None</span></span>
<span data-ttu-id="29057-133">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="29057-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="29057-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="29057-134">OUTPUTS</span></span>

### <span data-ttu-id="29057-135">Microsoft. Azure. Commands. Recoveryservices. backup. cmdlets. Models. PolicyBase</span><span class="sxs-lookup"><span data-stu-id="29057-135">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span></span>

### <span data-ttu-id="29057-136">System. Collections. Generic. IList ' 1 [Microsoft. Azure. Commands. Recoveryservices. backup. cmdlets. Models. PolicyBase]</span><span class="sxs-lookup"><span data-stu-id="29057-136">System.Collections.Generic.IList\`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase]</span></span>

## <span data-ttu-id="29057-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="29057-137">NOTES</span></span>

## <span data-ttu-id="29057-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="29057-138">RELATED LINKS</span></span>

[<span data-ttu-id="29057-139">New-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="29057-139">New-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzureRmRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="29057-140">Remove-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="29057-140">Remove-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./Remove-AzureRmRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="29057-141">Set-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="29057-141">Set-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./Set-AzureRmRecoveryServicesBackupProtectionPolicy.md)


