---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/disable-azrecoveryservicesbackupautoprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Disable-AzRecoveryServicesBackupAutoProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Disable-AzRecoveryServicesBackupAutoProtection.md
ms.openlocfilehash: 2613761db4a975f1bd4e04458ccdc5df81c0a2d9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93773066"
---
# <span data-ttu-id="2bf8c-101">Disable-AzRecoveryServicesBackupAutoProtection</span><span class="sxs-lookup"><span data-stu-id="2bf8c-101">Disable-AzRecoveryServicesBackupAutoProtection</span></span>

## <span data-ttu-id="2bf8c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2bf8c-102">SYNOPSIS</span></span>
<span data-ttu-id="2bf8c-103">Desabilita o backup automático para um item de proteção.</span><span class="sxs-lookup"><span data-stu-id="2bf8c-103">Disables auto backup for a protectable item.</span></span>

## <span data-ttu-id="2bf8c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2bf8c-104">SYNTAX</span></span>

```
Disable-AzRecoveryServicesBackupAutoProtection [-InputItem] <ProtectableItemBase>
 [-BackupManagementType] <BackupManagementType> [-WorkloadType] <WorkloadType> [-PassThru] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2bf8c-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2bf8c-105">DESCRIPTION</span></span>
<span data-ttu-id="2bf8c-106">O cmdlet **Disable-AzRecoveryServicesBackupAutoProtection** desabilita a proteção em um item de proteção.</span><span class="sxs-lookup"><span data-stu-id="2bf8c-106">The **Disable-AzRecoveryServicesBackupAutoProtection** cmdlet disables protection on a protectable item.</span></span>

## <span data-ttu-id="2bf8c-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2bf8c-107">EXAMPLES</span></span>

### <span data-ttu-id="2bf8c-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="2bf8c-108">Example 1</span></span>
```
PS C:\> $container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVMAppContainer
PS C:\> Get-AzRecoveryServicesBackupProtectableItem -Container $container -WorkloadType "MSSQL" -ItemType "SQLInstance" | Disable-AzRecoveryServicesBackupAutoProtection -BackupManagementType "AzureWorkload" -WorkloadType "MSSQL"
```

<span data-ttu-id="2bf8c-109">O primeiro cmdlet desabilita a política de proteção de backup.</span><span class="sxs-lookup"><span data-stu-id="2bf8c-109">The first cmdlet disables the Backup protection policy.</span></span>

## <span data-ttu-id="2bf8c-110">OS</span><span class="sxs-lookup"><span data-stu-id="2bf8c-110">PARAMETERS</span></span>

### <span data-ttu-id="2bf8c-111">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="2bf8c-111">-BackupManagementType</span></span>
<span data-ttu-id="2bf8c-112">Tipo de gerenciamento de backup do recurso (por exemplo: MAB, DPM).</span><span class="sxs-lookup"><span data-stu-id="2bf8c-112">Backup Management type of the resource (for example: MAB, DPM).</span></span>

```yaml
Type: BackupManagementType
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL, AzureStorage, AzureWorkload

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2bf8c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2bf8c-113">-DefaultProfile</span></span>
<span data-ttu-id="2bf8c-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2bf8c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2bf8c-115">-InputItem</span><span class="sxs-lookup"><span data-stu-id="2bf8c-115">-InputItem</span></span>
<span data-ttu-id="2bf8c-116">ID do item</span><span class="sxs-lookup"><span data-stu-id="2bf8c-116">Item Id</span></span>

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

### <span data-ttu-id="2bf8c-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2bf8c-117">-PassThru</span></span>
<span data-ttu-id="2bf8c-118">Retornar o resultado da proteção automática.</span><span class="sxs-lookup"><span data-stu-id="2bf8c-118">Return the result for auto protection.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2bf8c-119">-Cofreid</span><span class="sxs-lookup"><span data-stu-id="2bf8c-119">-VaultId</span></span>
<span data-ttu-id="2bf8c-120">ID do braço do cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="2bf8c-120">ARM ID of the Recovery Services Vault.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2bf8c-121">-Workloadtype</span><span class="sxs-lookup"><span data-stu-id="2bf8c-121">-WorkloadType</span></span>
<span data-ttu-id="2bf8c-122">Tipo de carga de trabalho do recurso (por exemplo: AzureVM, WindowsServer, AzureFiles).</span><span class="sxs-lookup"><span data-stu-id="2bf8c-122">Workload type of the resource (for example: AzureVM, WindowsServer, AzureFiles).</span></span>

```yaml
Type: WorkloadType
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, AzureSQLDatabase, AzureFiles, MSSQL

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2bf8c-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="2bf8c-123">-Confirm</span></span>
<span data-ttu-id="2bf8c-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2bf8c-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2bf8c-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2bf8c-125">-WhatIf</span></span>
<span data-ttu-id="2bf8c-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="2bf8c-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2bf8c-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2bf8c-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2bf8c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2bf8c-128">CommonParameters</span></span>
<span data-ttu-id="2bf8c-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2bf8c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="2bf8c-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2bf8c-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2bf8c-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2bf8c-131">INPUTS</span></span>

### <span data-ttu-id="2bf8c-132">System. String</span><span class="sxs-lookup"><span data-stu-id="2bf8c-132">System.String</span></span>

## <span data-ttu-id="2bf8c-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2bf8c-133">OUTPUTS</span></span>

### <span data-ttu-id="2bf8c-134">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2bf8c-134">System.Boolean</span></span>

## <span data-ttu-id="2bf8c-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2bf8c-135">NOTES</span></span>

## <span data-ttu-id="2bf8c-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2bf8c-136">RELATED LINKS</span></span>
