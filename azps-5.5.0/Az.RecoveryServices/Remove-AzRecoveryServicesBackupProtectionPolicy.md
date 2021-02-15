---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: BFE741CC-C166-4534-93F4-D21AAFAD9FF6
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: c3f4bb9b7c3d2b862ff78fdb35517f5837ffedf0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112689"
---
# <span data-ttu-id="97acd-101">Remove-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="97acd-101">Remove-AzRecoveryServicesBackupProtectionPolicy</span></span>

## <span data-ttu-id="97acd-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="97acd-102">SYNOPSIS</span></span>
<span data-ttu-id="97acd-103">Exclui uma política de proteção de backup de um cofre.</span><span class="sxs-lookup"><span data-stu-id="97acd-103">Deletes a Backup protection policy from a vault.</span></span>

## <span data-ttu-id="97acd-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="97acd-104">SYNTAX</span></span>

### <span data-ttu-id="97acd-105">Nomeda Política (Padrão)</span><span class="sxs-lookup"><span data-stu-id="97acd-105">PolicyName (Default)</span></span>
```
Remove-AzRecoveryServicesBackupProtectionPolicy [-Name] <String> [-PassThru] [-Force] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="97acd-106">PolicyObject</span><span class="sxs-lookup"><span data-stu-id="97acd-106">PolicyObject</span></span>
```
Remove-AzRecoveryServicesBackupProtectionPolicy [-Policy] <PolicyBase> [-PassThru] [-Force] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="97acd-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="97acd-107">DESCRIPTION</span></span>
<span data-ttu-id="97acd-108">O **cmdlet Remove-AzRecoveryServicesBackupProtectionPolicy** exclui as políticas de backup de um cofre.</span><span class="sxs-lookup"><span data-stu-id="97acd-108">The **Remove-AzRecoveryServicesBackupProtectionPolicy** cmdlet deletes backup policies for a vault.</span></span>
<span data-ttu-id="97acd-109">Antes de excluir uma política de proteção de Backup, a política não deve ter itens de Backup associados.</span><span class="sxs-lookup"><span data-stu-id="97acd-109">Before you can delete a Backup protection policy, the policy must not have any associated Backup items.</span></span>
<span data-ttu-id="97acd-110">Antes de excluir a política, certifique-se de que cada item associado está associado a alguma outra política.</span><span class="sxs-lookup"><span data-stu-id="97acd-110">Before you delete the policy, make sure that each associated item is associated with some other policy.</span></span>
<span data-ttu-id="97acd-111">Para associar outra política a um item de Backup, use Enable-AzRecoveryServicesBackupProtection cmdlet.</span><span class="sxs-lookup"><span data-stu-id="97acd-111">To associate another policy with a Backup item, use the Enable-AzRecoveryServicesBackupProtection cmdlet.</span></span>
<span data-ttu-id="97acd-112">De definir o contexto do cofre usando o Set-AzRecoveryServicesVaultContext cmdlet antes de usar o cmdlet atual.</span><span class="sxs-lookup"><span data-stu-id="97acd-112">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="97acd-113">Exemplos</span><span class="sxs-lookup"><span data-stu-id="97acd-113">EXAMPLES</span></span>

### <span data-ttu-id="97acd-114">Exemplo 1: Remover uma política</span><span class="sxs-lookup"><span data-stu-id="97acd-114">Example 1: Remove a policy</span></span>
```powershell
PS C:\>$Pol= Get-AzRecoveryServicesBackupProtectionPolicy -Name "NewPolicy"
PS C:\> Remove-AzRecoveryServicesBackupProtectionPolicy -Policy $Pol
```

<span data-ttu-id="97acd-115">O primeiro comando obtém a política de proteção de backup chamada NewPolicy e a armazena na variável $Pol backup.</span><span class="sxs-lookup"><span data-stu-id="97acd-115">The first command gets the Backup protection policy named NewPolicy, and then stores it in the $Pol variable.</span></span>
<span data-ttu-id="97acd-116">O segundo comando remove o objeto de política no $Pol.</span><span class="sxs-lookup"><span data-stu-id="97acd-116">The second command removes the policy object in $Pol.</span></span>

### <span data-ttu-id="97acd-117">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="97acd-117">Example 2</span></span>

<span data-ttu-id="97acd-118">Exclui uma política de proteção de backup de um cofre.</span><span class="sxs-lookup"><span data-stu-id="97acd-118">Deletes a Backup protection policy from a vault.</span></span> <span data-ttu-id="97acd-119">(gerado automaticamente)</span><span class="sxs-lookup"><span data-stu-id="97acd-119">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Remove-AzRecoveryServicesBackupProtectionPolicy -Name 'V2VM' -VaultId $vault.ID
```

## <span data-ttu-id="97acd-120">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="97acd-120">PARAMETERS</span></span>

### <span data-ttu-id="97acd-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97acd-121">-DefaultProfile</span></span>
<span data-ttu-id="97acd-122">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="97acd-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="97acd-123">-Forçar</span><span class="sxs-lookup"><span data-stu-id="97acd-123">-Force</span></span>
<span data-ttu-id="97acd-124">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="97acd-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="97acd-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="97acd-125">-Name</span></span>
<span data-ttu-id="97acd-126">Especifica o nome da política de proteção de backup a ser removido.</span><span class="sxs-lookup"><span data-stu-id="97acd-126">Specifies the name of the Backup protection policy to remove.</span></span>

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

### <span data-ttu-id="97acd-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="97acd-127">-PassThru</span></span>
<span data-ttu-id="97acd-128">Retorne a política a ser excluída.</span><span class="sxs-lookup"><span data-stu-id="97acd-128">Return the policy to be deleted.</span></span>

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

### <span data-ttu-id="97acd-129">-Política</span><span class="sxs-lookup"><span data-stu-id="97acd-129">-Policy</span></span>
<span data-ttu-id="97acd-130">Especifica a política de proteção de backup a ser removido.</span><span class="sxs-lookup"><span data-stu-id="97acd-130">Specifies the Backup protection policy to remove.</span></span>
<span data-ttu-id="97acd-131">Para obter um **objeto BackupPolicy,** use o cmdlet Get-AzRecoveryServicesBackupProtectionPolicy backup.</span><span class="sxs-lookup"><span data-stu-id="97acd-131">To obtain an **BackupPolicy** object, use the Get-AzRecoveryServicesBackupProtectionPolicy cmdlet.</span></span>

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

### <span data-ttu-id="97acd-132">-VaultId</span><span class="sxs-lookup"><span data-stu-id="97acd-132">-VaultId</span></span>
<span data-ttu-id="97acd-133">ID arm do Cofre de Serviços de Recuperação.</span><span class="sxs-lookup"><span data-stu-id="97acd-133">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="97acd-134">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="97acd-134">-Confirm</span></span>
<span data-ttu-id="97acd-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="97acd-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="97acd-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="97acd-136">-WhatIf</span></span>
<span data-ttu-id="97acd-137">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="97acd-137">Shows what would happen if the cmdlet runs.</span></span>

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

### <span data-ttu-id="97acd-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97acd-138">CommonParameters</span></span>
<span data-ttu-id="97acd-139">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97acd-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97acd-140">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="97acd-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97acd-141">Entradas</span><span class="sxs-lookup"><span data-stu-id="97acd-141">INPUTS</span></span>

### <span data-ttu-id="97acd-142">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span><span class="sxs-lookup"><span data-stu-id="97acd-142">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span></span>

### <span data-ttu-id="97acd-143">System.String</span><span class="sxs-lookup"><span data-stu-id="97acd-143">System.String</span></span>

## <span data-ttu-id="97acd-144">Saídas</span><span class="sxs-lookup"><span data-stu-id="97acd-144">OUTPUTS</span></span>

### <span data-ttu-id="97acd-145">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span><span class="sxs-lookup"><span data-stu-id="97acd-145">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span></span>

## <span data-ttu-id="97acd-146">Notas</span><span class="sxs-lookup"><span data-stu-id="97acd-146">NOTES</span></span>

## <span data-ttu-id="97acd-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="97acd-147">RELATED LINKS</span></span>

[<span data-ttu-id="97acd-148">Get-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="97acd-148">Get-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="97acd-149">New-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="97acd-149">New-AzRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="97acd-150">Set-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="97acd-150">Set-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Set-AzRecoveryServicesBackupProtectionPolicy.md)


