---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/enable-azrecoveryservicesbackupautoprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Enable-AzRecoveryServicesBackupAutoProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Enable-AzRecoveryServicesBackupAutoProtection.md
ms.openlocfilehash: 81fa8a4ada2f2479d9aa2ecceb1de3c05c3f34c8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892383"
---
# <span data-ttu-id="a3cf2-101">Enable-AzRecoveryServicesBackupAutoProtection</span><span class="sxs-lookup"><span data-stu-id="a3cf2-101">Enable-AzRecoveryServicesBackupAutoProtection</span></span>

## <span data-ttu-id="a3cf2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a3cf2-102">SYNOPSIS</span></span>
<span data-ttu-id="a3cf2-103">O cmdlet **Enable-AzRecoveryServicesBackupAutoProtection** configura a proteção automática de DBs atuais e futuros SQL DBs em determinada instância com a política fornecida.</span><span class="sxs-lookup"><span data-stu-id="a3cf2-103">The **Enable-AzRecoveryServicesBackupAutoProtection** cmdlet sets up automatic protection of current and any future SQL DBs within the given instance with the supplied policy.</span></span>

## <span data-ttu-id="a3cf2-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="a3cf2-104">SYNTAX</span></span>

```
Enable-AzRecoveryServicesBackupAutoProtection [-InputItem] <ProtectableItemBase>
 [-BackupManagementType] <BackupManagementType> [-WorkloadType] <WorkloadType> [-Policy] <PolicyBase>
 [-PassThru] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a3cf2-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="a3cf2-105">DESCRIPTION</span></span>
<span data-ttu-id="a3cf2-106">Esse comando permite que os usuários protejam automaticamente todos os DBs SQL DBs e qualquer DB que será adicionado posteriormente com a política determinada.</span><span class="sxs-lookup"><span data-stu-id="a3cf2-106">This command allows users to automatically protect all existing unprotected SQL DBs and any DB which will be added later with the given policy.</span></span>  <span data-ttu-id="a3cf2-107">Como a instrução é fazer backup de todos os DBs futuros, a operação é feita em um nível SQLInstance, o serviço de backup do Azure examinará regularmente os contêineres protegidos automaticamente por quaisquer novos DBs e os protegerá automaticamente.</span><span class="sxs-lookup"><span data-stu-id="a3cf2-107">Since the instruction is to back up all future DBs, the operation is done at a SQLInstance level, Azure backup service will then regularly scan auto-protected containers for any new DBs and automatically protect them.</span></span>

## <span data-ttu-id="a3cf2-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a3cf2-108">EXAMPLES</span></span>

### <span data-ttu-id="a3cf2-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a3cf2-109">Example 1</span></span>
```powershell
PS C:\> $Pol = Get-AzRecoveryServicesBackupProtectionPolicy -Name "DefaultSQLPolicy"
PS C:\> $SQLInstance = Get-AzRecoveryServicesBackupProtectableItem -workloadType MSSQL -ItemType SQLInstance -VaultId $targetVault.ID -Name "MSSQLInstance" -ServerName "TestSQLServer" 
PS C:\> Enable-AzRecoveryServicesBackupAutoProtection -InputItem $SQLInstance -BackupManagementType AzureWorkload -WorkloadType MSSQL -Policy $Pol -VaultId $targetvault.ID 
```

<span data-ttu-id="a3cf2-110">O primeiro cmdlet obtém um objeto de política padrão e o armazena na variável $Pol.</span><span class="sxs-lookup"><span data-stu-id="a3cf2-110">The first cmdlet gets a default policy object, and then stores it in the $Pol variable.</span></span>
<span data-ttu-id="a3cf2-111">O segundo cmdlet busca o SQLInstance relevante, que é um item protegido.</span><span class="sxs-lookup"><span data-stu-id="a3cf2-111">The second cmdlet fetches the relevant SQLInstance which is a protectable item.</span></span> <span data-ttu-id="a3cf2-112">Em seguida, o comando 3rd configura a proteção automática para essa instância usando a política em $Pol.</span><span class="sxs-lookup"><span data-stu-id="a3cf2-112">The 3rd command then sets up auto protection for this instance using the policy in $Pol.</span></span>

### <span data-ttu-id="a3cf2-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="a3cf2-113">Example 2</span></span>

<span data-ttu-id="a3cf2-114">Esses comandos permitem que os usuários protejam automaticamente todos os DBs desprotegidos existentes e qualquer DB que será adicionado posteriormente com a política determinada.</span><span class="sxs-lookup"><span data-stu-id="a3cf2-114">This commands allows users to automatically protect all existing unprotected DBs and any DB which will be added later with the given policy.</span></span> <span data-ttu-id="a3cf2-115">(gerado automaticamente)</span><span class="sxs-lookup"><span data-stu-id="a3cf2-115">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Enable-AzRecoveryServicesBackupAutoProtection -BackupManagementType AzureVM -InputItem <ProtectableItemBase> -Policy $Pol -VaultId $vault.ID -WorkloadType AzureVM
```

## <span data-ttu-id="a3cf2-116">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="a3cf2-116">PARAMETERS</span></span>

### <span data-ttu-id="a3cf2-117">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="a3cf2-117">-BackupManagementType</span></span>
<span data-ttu-id="a3cf2-118">A classe de recursos que está sendo protegida.</span><span class="sxs-lookup"><span data-stu-id="a3cf2-118">The class of resources being protected.</span></span> <span data-ttu-id="a3cf2-119">Atualmente, os valores suportados para este cmdlet são MAB, AzureWorkload, AzureVM</span><span class="sxs-lookup"><span data-stu-id="a3cf2-119">Currently the values supported for this cmdlet are MAB, AzureWorkload, AzureVM</span></span>

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

### <span data-ttu-id="a3cf2-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3cf2-120">-DefaultProfile</span></span>
<span data-ttu-id="a3cf2-121">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a3cf2-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a3cf2-122">-InputItem</span><span class="sxs-lookup"><span data-stu-id="a3cf2-122">-InputItem</span></span>
<span data-ttu-id="a3cf2-123">Especifica o objeto de item protegido que pode ser passado como uma entrada.</span><span class="sxs-lookup"><span data-stu-id="a3cf2-123">Specifies the protectable item object that can be passed as an input.</span></span> <span data-ttu-id="a3cf2-124">O valor suportado atual é um objeto protectableItem do tipo "SQLInstance".</span><span class="sxs-lookup"><span data-stu-id="a3cf2-124">The current supported value is a protectableItem object of type "SQLInstance".</span></span> 

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

### <span data-ttu-id="a3cf2-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a3cf2-125">-PassThru</span></span>
<span data-ttu-id="a3cf2-126">Retorne o resultado da proteção automática.</span><span class="sxs-lookup"><span data-stu-id="a3cf2-126">Return the result for auto protection.</span></span>

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

### <span data-ttu-id="a3cf2-127">-Policy</span><span class="sxs-lookup"><span data-stu-id="a3cf2-127">-Policy</span></span>
<span data-ttu-id="a3cf2-128">Objeto de política de proteção.</span><span class="sxs-lookup"><span data-stu-id="a3cf2-128">Protection policy object.</span></span>

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

### <span data-ttu-id="a3cf2-129">-VaultId</span><span class="sxs-lookup"><span data-stu-id="a3cf2-129">-VaultId</span></span>
<span data-ttu-id="a3cf2-130">ARM ID do Cofre de Serviços de Recuperação.</span><span class="sxs-lookup"><span data-stu-id="a3cf2-130">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="a3cf2-131">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="a3cf2-131">-WorkloadType</span></span>
<span data-ttu-id="a3cf2-132">Tipo de carga de trabalho do recurso.</span><span class="sxs-lookup"><span data-stu-id="a3cf2-132">Workload type of the resource.</span></span> <span data-ttu-id="a3cf2-133">Os valores atuais suportados são AzureVM, WindowsServer, MSSQL</span><span class="sxs-lookup"><span data-stu-id="a3cf2-133">The current supported values are AzureVM, WindowsServer, MSSQL</span></span>

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

### <span data-ttu-id="a3cf2-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a3cf2-134">-Confirm</span></span>
<span data-ttu-id="a3cf2-135">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a3cf2-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a3cf2-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a3cf2-136">-WhatIf</span></span>
<span data-ttu-id="a3cf2-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a3cf2-137">Shows what would happen if the cmdlet runs.</span></span>


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

### <span data-ttu-id="a3cf2-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3cf2-138">CommonParameters</span></span>
<span data-ttu-id="a3cf2-139">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3cf2-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3cf2-140">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a3cf2-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3cf2-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a3cf2-141">INPUTS</span></span>

### <span data-ttu-id="a3cf2-142">System.String</span><span class="sxs-lookup"><span data-stu-id="a3cf2-142">System.String</span></span>

## <span data-ttu-id="a3cf2-143">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="a3cf2-143">OUTPUTS</span></span>

### <span data-ttu-id="a3cf2-144">System.Object</span><span class="sxs-lookup"><span data-stu-id="a3cf2-144">System.Object</span></span>

## <span data-ttu-id="a3cf2-145">NOTES</span><span class="sxs-lookup"><span data-stu-id="a3cf2-145">NOTES</span></span>

## <span data-ttu-id="a3cf2-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a3cf2-146">RELATED LINKS</span></span>
