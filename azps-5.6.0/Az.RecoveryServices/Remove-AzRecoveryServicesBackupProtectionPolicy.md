---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: BFE741CC-C166-4534-93F4-D21AAFAD9FF6
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/remove-azrecoveryservicesbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: 4723fd3087b2f547659e72c1af6b0f5cb7764cf5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885526"
---
# <span data-ttu-id="e70f2-101">Remove-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="e70f2-101">Remove-AzRecoveryServicesBackupProtectionPolicy</span></span>

## <span data-ttu-id="e70f2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e70f2-102">SYNOPSIS</span></span>
<span data-ttu-id="e70f2-103">Exclui uma política de proteção de backup de um cofre.</span><span class="sxs-lookup"><span data-stu-id="e70f2-103">Deletes a Backup protection policy from a vault.</span></span>

## <span data-ttu-id="e70f2-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="e70f2-104">SYNTAX</span></span>

### <span data-ttu-id="e70f2-105">PolicyName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="e70f2-105">PolicyName (Default)</span></span>
```
Remove-AzRecoveryServicesBackupProtectionPolicy [-Name] <String> [-PassThru] [-Force] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e70f2-106">PolicyObject</span><span class="sxs-lookup"><span data-stu-id="e70f2-106">PolicyObject</span></span>
```
Remove-AzRecoveryServicesBackupProtectionPolicy [-Policy] <PolicyBase> [-PassThru] [-Force] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e70f2-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="e70f2-107">DESCRIPTION</span></span>
<span data-ttu-id="e70f2-108">O cmdlet **Remove-AzRecoveryServicesBackupProtectionPolicy** exclui as políticas de backup de um cofre.</span><span class="sxs-lookup"><span data-stu-id="e70f2-108">The **Remove-AzRecoveryServicesBackupProtectionPolicy** cmdlet deletes backup policies for a vault.</span></span>
<span data-ttu-id="e70f2-109">Antes de excluir uma política de proteção de backup, a política não deve ter itens de Backup associados.</span><span class="sxs-lookup"><span data-stu-id="e70f2-109">Before you can delete a Backup protection policy, the policy must not have any associated Backup items.</span></span>
<span data-ttu-id="e70f2-110">Antes de excluir a política, certifique-se de que cada item associado está associado a alguma outra política.</span><span class="sxs-lookup"><span data-stu-id="e70f2-110">Before you delete the policy, make sure that each associated item is associated with some other policy.</span></span>
<span data-ttu-id="e70f2-111">Para associar outra política a um item de Backup, use o cmdlet Enable-AzRecoveryServicesBackupProtection.</span><span class="sxs-lookup"><span data-stu-id="e70f2-111">To associate another policy with a Backup item, use the Enable-AzRecoveryServicesBackupProtection cmdlet.</span></span>
<span data-ttu-id="e70f2-112">De definir o contexto do cofre usando o cmdlet Set-AzRecoveryServicesVaultContext antes de usar o cmdlet atual.</span><span class="sxs-lookup"><span data-stu-id="e70f2-112">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="e70f2-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e70f2-113">EXAMPLES</span></span>

### <span data-ttu-id="e70f2-114">Exemplo 1: Remover uma política</span><span class="sxs-lookup"><span data-stu-id="e70f2-114">Example 1: Remove a policy</span></span>
```powershell
PS C:\>$Pol= Get-AzRecoveryServicesBackupProtectionPolicy -Name "NewPolicy"
PS C:\> Remove-AzRecoveryServicesBackupProtectionPolicy -Policy $Pol
```

<span data-ttu-id="e70f2-115">O primeiro comando obtém a política de proteção de backup chamada NewPolicy e a armazena na variável $Pol backup.</span><span class="sxs-lookup"><span data-stu-id="e70f2-115">The first command gets the Backup protection policy named NewPolicy, and then stores it in the $Pol variable.</span></span>
<span data-ttu-id="e70f2-116">O segundo comando remove o objeto policy no $Pol.</span><span class="sxs-lookup"><span data-stu-id="e70f2-116">The second command removes the policy object in $Pol.</span></span>

### <span data-ttu-id="e70f2-117">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="e70f2-117">Example 2</span></span>

<span data-ttu-id="e70f2-118">Exclui uma política de proteção de backup de um cofre.</span><span class="sxs-lookup"><span data-stu-id="e70f2-118">Deletes a Backup protection policy from a vault.</span></span> <span data-ttu-id="e70f2-119">(gerado automaticamente)</span><span class="sxs-lookup"><span data-stu-id="e70f2-119">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Remove-AzRecoveryServicesBackupProtectionPolicy -Name 'V2VM' -VaultId $vault.ID
```

## <span data-ttu-id="e70f2-120">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="e70f2-120">PARAMETERS</span></span>

### <span data-ttu-id="e70f2-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e70f2-121">-DefaultProfile</span></span>
<span data-ttu-id="e70f2-122">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="e70f2-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e70f2-123">-Force</span><span class="sxs-lookup"><span data-stu-id="e70f2-123">-Force</span></span>
<span data-ttu-id="e70f2-124">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="e70f2-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e70f2-125">-Name</span><span class="sxs-lookup"><span data-stu-id="e70f2-125">-Name</span></span>
<span data-ttu-id="e70f2-126">Especifica o nome da política de proteção de backup a ser removido.</span><span class="sxs-lookup"><span data-stu-id="e70f2-126">Specifies the name of the Backup protection policy to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicyName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e70f2-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e70f2-127">-PassThru</span></span>
<span data-ttu-id="e70f2-128">Retorne a política a ser excluída.</span><span class="sxs-lookup"><span data-stu-id="e70f2-128">Return the policy to be deleted.</span></span>

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

### <span data-ttu-id="e70f2-129">-Policy</span><span class="sxs-lookup"><span data-stu-id="e70f2-129">-Policy</span></span>
<span data-ttu-id="e70f2-130">Especifica a política de proteção de backup a ser removido.</span><span class="sxs-lookup"><span data-stu-id="e70f2-130">Specifies the Backup protection policy to remove.</span></span>
<span data-ttu-id="e70f2-131">Para obter um **objeto BackupPolicy,** use Get-AzRecoveryServicesBackupProtectionPolicy cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e70f2-131">To obtain an **BackupPolicy** object, use the Get-AzRecoveryServicesBackupProtectionPolicy cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase
Parameter Sets: PolicyObject
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e70f2-132">-VaultId</span><span class="sxs-lookup"><span data-stu-id="e70f2-132">-VaultId</span></span>
<span data-ttu-id="e70f2-133">ARM ID do Cofre de Serviços de Recuperação.</span><span class="sxs-lookup"><span data-stu-id="e70f2-133">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="e70f2-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e70f2-134">-Confirm</span></span>
<span data-ttu-id="e70f2-135">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e70f2-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e70f2-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e70f2-136">-WhatIf</span></span>
<span data-ttu-id="e70f2-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e70f2-137">Shows what would happen if the cmdlet runs.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e70f2-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e70f2-138">CommonParameters</span></span>
<span data-ttu-id="e70f2-139">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e70f2-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e70f2-140">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e70f2-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e70f2-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e70f2-141">INPUTS</span></span>

### <span data-ttu-id="e70f2-142">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span><span class="sxs-lookup"><span data-stu-id="e70f2-142">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span></span>

### <span data-ttu-id="e70f2-143">System.String</span><span class="sxs-lookup"><span data-stu-id="e70f2-143">System.String</span></span>

## <span data-ttu-id="e70f2-144">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="e70f2-144">OUTPUTS</span></span>

### <span data-ttu-id="e70f2-145">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span><span class="sxs-lookup"><span data-stu-id="e70f2-145">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span></span>

## <span data-ttu-id="e70f2-146">NOTES</span><span class="sxs-lookup"><span data-stu-id="e70f2-146">NOTES</span></span>

## <span data-ttu-id="e70f2-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e70f2-147">RELATED LINKS</span></span>

[<span data-ttu-id="e70f2-148">Get-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="e70f2-148">Get-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="e70f2-149">New-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="e70f2-149">New-AzRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="e70f2-150">Set-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="e70f2-150">Set-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Set-AzRecoveryServicesBackupProtectionPolicy.md)


