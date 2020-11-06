---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/enable-azrecoveryservicesbackupautoprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Enable-AzRecoveryServicesBackupAutoProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Enable-AzRecoveryServicesBackupAutoProtection.md
ms.openlocfilehash: a17c7b8addf1bf1218131e8e950185d9da6c22d0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93599751"
---
# <span data-ttu-id="98f1b-101">Enable-AzRecoveryServicesBackupAutoProtection</span><span class="sxs-lookup"><span data-stu-id="98f1b-101">Enable-AzRecoveryServicesBackupAutoProtection</span></span>

## <span data-ttu-id="98f1b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="98f1b-102">SYNOPSIS</span></span>
<span data-ttu-id="98f1b-103">Esses comandos permitem que os usuários protejam automaticamente todos os bancos de dados desprotegidos existentes e qualquer banco de dados que será adicionado posteriormente com a política fornecida.</span><span class="sxs-lookup"><span data-stu-id="98f1b-103">This commands allows users to automatically protect all existing unprotected DBs and any DB which will be added later with the given policy.</span></span> <span data-ttu-id="98f1b-104">O serviço de backup do Azure examinará regularmente os contêineres protegidos automaticamente para qualquer novo bancos de bancos e os protegerá automaticamente.</span><span class="sxs-lookup"><span data-stu-id="98f1b-104">Azure backup service will then regularly scan auto-protected containers for any new DBs and automatically protect them.</span></span>

## <span data-ttu-id="98f1b-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="98f1b-105">SYNTAX</span></span>

```
Enable-AzRecoveryServicesBackupAutoProtection [-InputItem] <ProtectableItemBase>
 [-BackupManagementType] <BackupManagementType> [-WorkloadType] <WorkloadType> [-Policy] <PolicyBase>
 [-PassThru] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="98f1b-106">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="98f1b-106">DESCRIPTION</span></span>
<span data-ttu-id="98f1b-107">O cmdlet **Enable-AzRecoveryServicesBackupAutoProtection** define a política de proteção de backup automático do Azure em um item que permite proteção.</span><span class="sxs-lookup"><span data-stu-id="98f1b-107">The **Enable-AzRecoveryServicesBackupAutoProtection** cmdlet sets Azure auto Backup protection policy on an protectable item.</span></span>

## <span data-ttu-id="98f1b-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="98f1b-108">EXAMPLES</span></span>

### <span data-ttu-id="98f1b-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="98f1b-109">Example 1</span></span>
```
PS C:\> $Pol = Get-AzRecoveryServicesBackupProtectionPolicy -Name "DefaultPolicy"
PS C:\> $container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVMAppContainer
PS C:\> Get-AzRecoveryServicesBackupProtectableItem -Container $container -WorkloadType "MSSQL" -ItemType "SQLInstance" | Enable-AzRecoveryServicesBackupAutoProtection -BackupManagementType "AzureWorkload" -WorkloadType "MSSQL" -Policy $Pol
```

<span data-ttu-id="98f1b-110">O primeiro cmdlet obtém um objeto de política padrão e, em seguida, armazena-o na variável $Pol.</span><span class="sxs-lookup"><span data-stu-id="98f1b-110">The first cmdlet gets a default policy object, and then stores it in the $Pol variable.</span></span>
<span data-ttu-id="98f1b-111">O segundo cmdlet define a política de proteção de backup para o AzureWorkload usando a política em $Pol.</span><span class="sxs-lookup"><span data-stu-id="98f1b-111">The second cmdlet sets the Backup protection policy for the AzureWorkload using the policy in $Pol.</span></span>

## <span data-ttu-id="98f1b-112">OS</span><span class="sxs-lookup"><span data-stu-id="98f1b-112">PARAMETERS</span></span>

### <span data-ttu-id="98f1b-113">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="98f1b-113">-BackupManagementType</span></span>
<span data-ttu-id="98f1b-114">Tipo de gerenciamento de backup do recurso (por exemplo: MAB, DPM, AzureWorkload).</span><span class="sxs-lookup"><span data-stu-id="98f1b-114">Backup Management type of the resource (for example: MAB, DPM, AzureWorkload).</span></span>

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

### <span data-ttu-id="98f1b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98f1b-115">-DefaultProfile</span></span>
<span data-ttu-id="98f1b-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="98f1b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="98f1b-117">-InputItem</span><span class="sxs-lookup"><span data-stu-id="98f1b-117">-InputItem</span></span>
<span data-ttu-id="98f1b-118">Especifica o objeto de item protector que pode ser passado como uma entrada.</span><span class="sxs-lookup"><span data-stu-id="98f1b-118">Specifies the protectable item object that can be passed as an input.</span></span>

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

### <span data-ttu-id="98f1b-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="98f1b-119">-PassThru</span></span>
<span data-ttu-id="98f1b-120">Retornar o resultado da proteção automática.</span><span class="sxs-lookup"><span data-stu-id="98f1b-120">Return the result for auto protection.</span></span>

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

### <span data-ttu-id="98f1b-121">-Política</span><span class="sxs-lookup"><span data-stu-id="98f1b-121">-Policy</span></span>
<span data-ttu-id="98f1b-122">Objeto de política de proteção.</span><span class="sxs-lookup"><span data-stu-id="98f1b-122">Protection policy object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98f1b-123">-Cofreid</span><span class="sxs-lookup"><span data-stu-id="98f1b-123">-VaultId</span></span>
<span data-ttu-id="98f1b-124">ID do braço do cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="98f1b-124">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="98f1b-125">-Workloadtype</span><span class="sxs-lookup"><span data-stu-id="98f1b-125">-WorkloadType</span></span>
<span data-ttu-id="98f1b-126">Tipo de carga de trabalho do recurso (por exemplo: AzureVM, WindowsServer, AzureFiles, MSSQL).</span><span class="sxs-lookup"><span data-stu-id="98f1b-126">Workload type of the resource (for example: AzureVM, WindowsServer, AzureFiles, MSSQL).</span></span>

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

### <span data-ttu-id="98f1b-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="98f1b-127">-Confirm</span></span>
<span data-ttu-id="98f1b-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="98f1b-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="98f1b-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="98f1b-129">-WhatIf</span></span>
<span data-ttu-id="98f1b-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="98f1b-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="98f1b-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="98f1b-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="98f1b-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98f1b-132">CommonParameters</span></span>
<span data-ttu-id="98f1b-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="98f1b-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98f1b-134">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="98f1b-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98f1b-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="98f1b-135">INPUTS</span></span>

### <span data-ttu-id="98f1b-136">System. String</span><span class="sxs-lookup"><span data-stu-id="98f1b-136">System.String</span></span>

## <span data-ttu-id="98f1b-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="98f1b-137">OUTPUTS</span></span>

### <span data-ttu-id="98f1b-138">System. Object</span><span class="sxs-lookup"><span data-stu-id="98f1b-138">System.Object</span></span>

## <span data-ttu-id="98f1b-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="98f1b-139">NOTES</span></span>

## <span data-ttu-id="98f1b-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="98f1b-140">RELATED LINKS</span></span>