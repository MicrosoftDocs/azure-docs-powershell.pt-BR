---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/enable-azrecoveryservicesbackupautoprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Enable-AzRecoveryServicesBackupAutoProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Enable-AzRecoveryServicesBackupAutoProtection.md
ms.openlocfilehash: e47ed3d2859a78837c57803789721005a5248204
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94281966"
---
# <span data-ttu-id="61ff0-101">Enable-AzRecoveryServicesBackupAutoProtection</span><span class="sxs-lookup"><span data-stu-id="61ff0-101">Enable-AzRecoveryServicesBackupAutoProtection</span></span>

## <span data-ttu-id="61ff0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="61ff0-102">SYNOPSIS</span></span>
<span data-ttu-id="61ff0-103">O cmdlet **Enable-AzRecoveryServicesBackupAutoProtection** define a proteção automática do bancos de dados SQL atuais e dos futuros bancos de dados SQL dentro da instância fornecida com a política fornecida.</span><span class="sxs-lookup"><span data-stu-id="61ff0-103">The **Enable-AzRecoveryServicesBackupAutoProtection** cmdlet sets up automatic protection of current and any future SQL DBs within the given instance with the supplied policy.</span></span>

## <span data-ttu-id="61ff0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="61ff0-104">SYNTAX</span></span>

```
Enable-AzRecoveryServicesBackupAutoProtection [-InputItem] <ProtectableItemBase>
 [-BackupManagementType] <BackupManagementType> [-WorkloadType] <WorkloadType> [-Policy] <PolicyBase>
 [-PassThru] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="61ff0-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="61ff0-105">DESCRIPTION</span></span>
<span data-ttu-id="61ff0-106">Esse comando permite que os usuários protejam automaticamente todos os bancos de dados existentes do SQL existentes e qualquer BD que serão adicionados posteriormente com a política determinada.</span><span class="sxs-lookup"><span data-stu-id="61ff0-106">This command allows users to automatically protect all existing unprotected SQL DBs and any DB which will be added later with the given policy.</span></span>  <span data-ttu-id="61ff0-107">Como a instrução é fazer o backup de todos os bancos de usuários futuros, a operação é feita em um nível de SQLInstance, o serviço de backup do Azure examinará regularmente os contêineres protegidos automaticamente para qualquer novo bancos de bancos e os protegerá automaticamente.</span><span class="sxs-lookup"><span data-stu-id="61ff0-107">Since the instruction is to back up all future DBs, the operation is done at a SQLInstance level, Azure backup service will then regularly scan auto-protected containers for any new DBs and automatically protect them.</span></span>

## <span data-ttu-id="61ff0-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="61ff0-108">EXAMPLES</span></span>

### <span data-ttu-id="61ff0-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="61ff0-109">Example 1</span></span>
```powershell
PS C:\> $Pol = Get-AzRecoveryServicesBackupProtectionPolicy -Name "DefaultSQLPolicy"
PS C:\> $SQLInstance = Get-AzRecoveryServicesBackupProtectableItem -workloadType MSSQL -ItemType SQLInstance -VaultId $targetVault.ID -Name "MSSQLInstance" -ServerName "TestSQLServer" 
PS C:\> Enable-AzRecoveryServicesBackupAutoProtection -InputItem $SQLInstance -BackupManagementType AzureWorkload -WorkloadType MSSQL -Policy $Pol -VaultId $targetvault.ID 
```

<span data-ttu-id="61ff0-110">O primeiro cmdlet obtém um objeto de política padrão e, em seguida, armazena-o na variável $Pol.</span><span class="sxs-lookup"><span data-stu-id="61ff0-110">The first cmdlet gets a default policy object, and then stores it in the $Pol variable.</span></span>
<span data-ttu-id="61ff0-111">O segundo cmdlet busca o SQLInstance relevante que é um item de proteção.</span><span class="sxs-lookup"><span data-stu-id="61ff0-111">The second cmdlet fetches the relevant SQLInstance which is a protectable item.</span></span> <span data-ttu-id="61ff0-112">Em seguida, o comando 3º configura a proteção automática dessa instância usando a política em $Pol.</span><span class="sxs-lookup"><span data-stu-id="61ff0-112">The 3rd command then sets up auto protection for this instance using the policy in $Pol.</span></span>

### <span data-ttu-id="61ff0-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="61ff0-113">Example 2</span></span>

<span data-ttu-id="61ff0-114">Esses comandos permitem que os usuários protejam automaticamente todos os bancos de dados desprotegidos existentes e qualquer banco de dados que será adicionado posteriormente com a política fornecida.</span><span class="sxs-lookup"><span data-stu-id="61ff0-114">This commands allows users to automatically protect all existing unprotected DBs and any DB which will be added later with the given policy.</span></span> <span data-ttu-id="61ff0-115">(gerado automaticamente)</span><span class="sxs-lookup"><span data-stu-id="61ff0-115">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Enable-AzRecoveryServicesBackupAutoProtection -BackupManagementType AzureVM -InputItem <ProtectableItemBase> -Policy $Pol -VaultId $vault.ID -WorkloadType AzureVM
```

## <span data-ttu-id="61ff0-116">OS</span><span class="sxs-lookup"><span data-stu-id="61ff0-116">PARAMETERS</span></span>

### <span data-ttu-id="61ff0-117">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="61ff0-117">-BackupManagementType</span></span>
<span data-ttu-id="61ff0-118">A classe de recursos que estão sendo protegidos.</span><span class="sxs-lookup"><span data-stu-id="61ff0-118">The class of resources being protected.</span></span> <span data-ttu-id="61ff0-119">Atualmente, os valores com suporte para esse cmdlet são MAB, AzureWorkload, AzureVM</span><span class="sxs-lookup"><span data-stu-id="61ff0-119">Currently the values supported for this cmdlet are MAB, AzureWorkload, AzureVM</span></span>

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

### <span data-ttu-id="61ff0-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61ff0-120">-DefaultProfile</span></span>
<span data-ttu-id="61ff0-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="61ff0-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="61ff0-122">-InputItem</span><span class="sxs-lookup"><span data-stu-id="61ff0-122">-InputItem</span></span>
<span data-ttu-id="61ff0-123">Especifica o objeto de item protector que pode ser passado como uma entrada.</span><span class="sxs-lookup"><span data-stu-id="61ff0-123">Specifies the protectable item object that can be passed as an input.</span></span> <span data-ttu-id="61ff0-124">O valor atual com suporte é um objeto protectableItem do tipo "SQLInstance".</span><span class="sxs-lookup"><span data-stu-id="61ff0-124">The current supported value is a protectableItem object of type "SQLInstance".</span></span> 

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

### <span data-ttu-id="61ff0-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="61ff0-125">-PassThru</span></span>
<span data-ttu-id="61ff0-126">Retornar o resultado da proteção automática.</span><span class="sxs-lookup"><span data-stu-id="61ff0-126">Return the result for auto protection.</span></span>

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

### <span data-ttu-id="61ff0-127">-Política</span><span class="sxs-lookup"><span data-stu-id="61ff0-127">-Policy</span></span>
<span data-ttu-id="61ff0-128">Objeto de política de proteção.</span><span class="sxs-lookup"><span data-stu-id="61ff0-128">Protection policy object.</span></span>

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

### <span data-ttu-id="61ff0-129">-Cofreid</span><span class="sxs-lookup"><span data-stu-id="61ff0-129">-VaultId</span></span>
<span data-ttu-id="61ff0-130">ID do braço do cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="61ff0-130">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="61ff0-131">-Workloadtype</span><span class="sxs-lookup"><span data-stu-id="61ff0-131">-WorkloadType</span></span>
<span data-ttu-id="61ff0-132">Tipo de carga de trabalho do recurso.</span><span class="sxs-lookup"><span data-stu-id="61ff0-132">Workload type of the resource.</span></span> <span data-ttu-id="61ff0-133">Os valores atuais com suporte são AzureVM, WindowsServer, MSSQL</span><span class="sxs-lookup"><span data-stu-id="61ff0-133">The current supported values are AzureVM, WindowsServer, MSSQL</span></span>

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

### <span data-ttu-id="61ff0-134">-Confirme</span><span class="sxs-lookup"><span data-stu-id="61ff0-134">-Confirm</span></span>
<span data-ttu-id="61ff0-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="61ff0-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="61ff0-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="61ff0-136">-WhatIf</span></span>
<span data-ttu-id="61ff0-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="61ff0-137">Shows what would happen if the cmdlet runs.</span></span>


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

### <span data-ttu-id="61ff0-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61ff0-138">CommonParameters</span></span>
<span data-ttu-id="61ff0-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61ff0-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61ff0-140">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="61ff0-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61ff0-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="61ff0-141">INPUTS</span></span>

### <span data-ttu-id="61ff0-142">System. String</span><span class="sxs-lookup"><span data-stu-id="61ff0-142">System.String</span></span>

## <span data-ttu-id="61ff0-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="61ff0-143">OUTPUTS</span></span>

### <span data-ttu-id="61ff0-144">System. Object</span><span class="sxs-lookup"><span data-stu-id="61ff0-144">System.Object</span></span>

## <span data-ttu-id="61ff0-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="61ff0-145">NOTES</span></span>

## <span data-ttu-id="61ff0-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="61ff0-146">RELATED LINKS</span></span>
