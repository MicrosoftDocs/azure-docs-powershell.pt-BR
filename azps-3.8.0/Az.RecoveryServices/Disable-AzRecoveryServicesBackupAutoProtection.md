---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/disable-azrecoveryservicesbackupautoprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Disable-AzRecoveryServicesBackupAutoProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Disable-AzRecoveryServicesBackupAutoProtection.md
ms.openlocfilehash: 97eae8c5c545297a7d6287a951ec02433d591168
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93778287"
---
# <span data-ttu-id="14619-101">Disable-AzRecoveryServicesBackupAutoProtection</span><span class="sxs-lookup"><span data-stu-id="14619-101">Disable-AzRecoveryServicesBackupAutoProtection</span></span>

## <span data-ttu-id="14619-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="14619-102">SYNOPSIS</span></span>
<span data-ttu-id="14619-103">Desabilita o backup automático para um item de proteção.</span><span class="sxs-lookup"><span data-stu-id="14619-103">Disables auto backup for a protectable item.</span></span>

## <span data-ttu-id="14619-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="14619-104">SYNTAX</span></span>

```
Disable-AzRecoveryServicesBackupAutoProtection [-InputItem] <ProtectableItemBase>
 [-BackupManagementType] <BackupManagementType> [-WorkloadType] <WorkloadType> [-PassThru] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="14619-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="14619-105">DESCRIPTION</span></span>
<span data-ttu-id="14619-106">O cmdlet **Disable-AzRecoveryServicesBackupAutoProtection** desabilita a proteção em um item de proteção.</span><span class="sxs-lookup"><span data-stu-id="14619-106">The **Disable-AzRecoveryServicesBackupAutoProtection** cmdlet disables protection on a protectable item.</span></span>

## <span data-ttu-id="14619-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="14619-107">EXAMPLES</span></span>

### <span data-ttu-id="14619-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="14619-108">Example 1</span></span>
```
PS C:\> $container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVMAppContainer
PS C:\> Get-AzRecoveryServicesBackupProtectableItem -Container $container -WorkloadType "MSSQL" -ItemType "SQLInstance" | Disable-AzRecoveryServicesBackupAutoProtection -BackupManagementType "AzureWorkload" -WorkloadType "MSSQL"
```

<span data-ttu-id="14619-109">O primeiro cmdlet desabilita a política de proteção de backup.</span><span class="sxs-lookup"><span data-stu-id="14619-109">The first cmdlet disables the Backup protection policy.</span></span>

## <span data-ttu-id="14619-110">OS</span><span class="sxs-lookup"><span data-stu-id="14619-110">PARAMETERS</span></span>

### <span data-ttu-id="14619-111">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="14619-111">-BackupManagementType</span></span>
<span data-ttu-id="14619-112">Tipo de gerenciamento de backup do recurso (por exemplo: MAB, DPM).</span><span class="sxs-lookup"><span data-stu-id="14619-112">Backup Management type of the resource (for example: MAB, DPM).</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL, AzureStorage, AzureWorkload

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14619-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14619-113">-DefaultProfile</span></span>
<span data-ttu-id="14619-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="14619-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="14619-115">-InputItem</span><span class="sxs-lookup"><span data-stu-id="14619-115">-InputItem</span></span>
<span data-ttu-id="14619-116">ID do item</span><span class="sxs-lookup"><span data-stu-id="14619-116">Item Id</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ProtectableItemBase
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="14619-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="14619-117">-PassThru</span></span>
<span data-ttu-id="14619-118">Retornar o resultado da proteção automática.</span><span class="sxs-lookup"><span data-stu-id="14619-118">Return the result for auto protection.</span></span>

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

### <span data-ttu-id="14619-119">-Cofreid</span><span class="sxs-lookup"><span data-stu-id="14619-119">-VaultId</span></span>
<span data-ttu-id="14619-120">ID do braço do cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="14619-120">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="14619-121">-Workloadtype</span><span class="sxs-lookup"><span data-stu-id="14619-121">-WorkloadType</span></span>
<span data-ttu-id="14619-122">Tipo de carga de trabalho do recurso (por exemplo: AzureVM, WindowsServer, AzureFiles).</span><span class="sxs-lookup"><span data-stu-id="14619-122">Workload type of the resource (for example: AzureVM, WindowsServer, AzureFiles).</span></span>

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

### <span data-ttu-id="14619-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="14619-123">-Confirm</span></span>
<span data-ttu-id="14619-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="14619-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="14619-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="14619-125">-WhatIf</span></span>
<span data-ttu-id="14619-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="14619-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="14619-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="14619-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="14619-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14619-128">CommonParameters</span></span>
<span data-ttu-id="14619-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14619-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14619-130">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="14619-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14619-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="14619-131">INPUTS</span></span>

### <span data-ttu-id="14619-132">System. String</span><span class="sxs-lookup"><span data-stu-id="14619-132">System.String</span></span>

## <span data-ttu-id="14619-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="14619-133">OUTPUTS</span></span>

### <span data-ttu-id="14619-134">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="14619-134">System.Boolean</span></span>

## <span data-ttu-id="14619-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="14619-135">NOTES</span></span>

## <span data-ttu-id="14619-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="14619-136">RELATED LINKS</span></span>
