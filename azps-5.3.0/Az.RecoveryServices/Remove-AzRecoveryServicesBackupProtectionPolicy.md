---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: BFE741CC-C166-4534-93F4-D21AAFAD9FF6
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: c3f4bb9b7c3d2b862ff78fdb35517f5837ffedf0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98428048"
---
# <span data-ttu-id="53c2a-101">Remove-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="53c2a-101">Remove-AzRecoveryServicesBackupProtectionPolicy</span></span>

## <span data-ttu-id="53c2a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="53c2a-102">SYNOPSIS</span></span>
<span data-ttu-id="53c2a-103">Exclui uma política de proteção de backup de um cofre.</span><span class="sxs-lookup"><span data-stu-id="53c2a-103">Deletes a Backup protection policy from a vault.</span></span>

## <span data-ttu-id="53c2a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="53c2a-104">SYNTAX</span></span>

### <span data-ttu-id="53c2a-105">PolicyName (padrão)</span><span class="sxs-lookup"><span data-stu-id="53c2a-105">PolicyName (Default)</span></span>
```
Remove-AzRecoveryServicesBackupProtectionPolicy [-Name] <String> [-PassThru] [-Force] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="53c2a-106">Políticaobject</span><span class="sxs-lookup"><span data-stu-id="53c2a-106">PolicyObject</span></span>
```
Remove-AzRecoveryServicesBackupProtectionPolicy [-Policy] <PolicyBase> [-PassThru] [-Force] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="53c2a-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="53c2a-107">DESCRIPTION</span></span>
<span data-ttu-id="53c2a-108">O cmdlet **Remove-AzRecoveryServicesBackupProtectionPolicy** exclui políticas de backup para um cofre.</span><span class="sxs-lookup"><span data-stu-id="53c2a-108">The **Remove-AzRecoveryServicesBackupProtectionPolicy** cmdlet deletes backup policies for a vault.</span></span>
<span data-ttu-id="53c2a-109">Antes de poder excluir uma política de proteção de backup, a política não deve ter itens de backup associados.</span><span class="sxs-lookup"><span data-stu-id="53c2a-109">Before you can delete a Backup protection policy, the policy must not have any associated Backup items.</span></span>
<span data-ttu-id="53c2a-110">Antes de excluir a política, verifique se cada item associado está associado a alguma outra política.</span><span class="sxs-lookup"><span data-stu-id="53c2a-110">Before you delete the policy, make sure that each associated item is associated with some other policy.</span></span>
<span data-ttu-id="53c2a-111">Para associar outra política a um item de backup, use o cmdlet Enable-AzRecoveryServicesBackupProtection.</span><span class="sxs-lookup"><span data-stu-id="53c2a-111">To associate another policy with a Backup item, use the Enable-AzRecoveryServicesBackupProtection cmdlet.</span></span>
<span data-ttu-id="53c2a-112">Defina o contexto do cofre usando o cmdlet Set-AzRecoveryServicesVaultContext antes de usar o cmdlet atual.</span><span class="sxs-lookup"><span data-stu-id="53c2a-112">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="53c2a-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="53c2a-113">EXAMPLES</span></span>

### <span data-ttu-id="53c2a-114">Exemplo 1: remover uma política</span><span class="sxs-lookup"><span data-stu-id="53c2a-114">Example 1: Remove a policy</span></span>
```powershell
PS C:\>$Pol= Get-AzRecoveryServicesBackupProtectionPolicy -Name "NewPolicy"
PS C:\> Remove-AzRecoveryServicesBackupProtectionPolicy -Policy $Pol
```

<span data-ttu-id="53c2a-115">O primeiro comando obtém a política de proteção de backup chamada NewPolicy e a armazena na variável $Pol.</span><span class="sxs-lookup"><span data-stu-id="53c2a-115">The first command gets the Backup protection policy named NewPolicy, and then stores it in the $Pol variable.</span></span>
<span data-ttu-id="53c2a-116">O segundo comando Remove o objeto de política em $Pol.</span><span class="sxs-lookup"><span data-stu-id="53c2a-116">The second command removes the policy object in $Pol.</span></span>

### <span data-ttu-id="53c2a-117">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="53c2a-117">Example 2</span></span>

<span data-ttu-id="53c2a-118">Exclui uma política de proteção de backup de um cofre.</span><span class="sxs-lookup"><span data-stu-id="53c2a-118">Deletes a Backup protection policy from a vault.</span></span> <span data-ttu-id="53c2a-119">(gerado automaticamente)</span><span class="sxs-lookup"><span data-stu-id="53c2a-119">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Remove-AzRecoveryServicesBackupProtectionPolicy -Name 'V2VM' -VaultId $vault.ID
```

## <span data-ttu-id="53c2a-120">OS</span><span class="sxs-lookup"><span data-stu-id="53c2a-120">PARAMETERS</span></span>

### <span data-ttu-id="53c2a-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53c2a-121">-DefaultProfile</span></span>
<span data-ttu-id="53c2a-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="53c2a-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="53c2a-123">-Force</span><span class="sxs-lookup"><span data-stu-id="53c2a-123">-Force</span></span>
<span data-ttu-id="53c2a-124">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="53c2a-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="53c2a-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="53c2a-125">-Name</span></span>
<span data-ttu-id="53c2a-126">Especifica o nome da política de proteção de backup a ser removida.</span><span class="sxs-lookup"><span data-stu-id="53c2a-126">Specifies the name of the Backup protection policy to remove.</span></span>

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

### <span data-ttu-id="53c2a-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="53c2a-127">-PassThru</span></span>
<span data-ttu-id="53c2a-128">Retorne a política a ser excluída.</span><span class="sxs-lookup"><span data-stu-id="53c2a-128">Return the policy to be deleted.</span></span>

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

### <span data-ttu-id="53c2a-129">-Política</span><span class="sxs-lookup"><span data-stu-id="53c2a-129">-Policy</span></span>
<span data-ttu-id="53c2a-130">Especifica a política de proteção de backup a ser removida.</span><span class="sxs-lookup"><span data-stu-id="53c2a-130">Specifies the Backup protection policy to remove.</span></span>
<span data-ttu-id="53c2a-131">Para obter um objeto **BackupPolicy** , use o cmdlet Get-AzRecoveryServicesBackupProtectionPolicy.</span><span class="sxs-lookup"><span data-stu-id="53c2a-131">To obtain an **BackupPolicy** object, use the Get-AzRecoveryServicesBackupProtectionPolicy cmdlet.</span></span>

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

### <span data-ttu-id="53c2a-132">-Cofreid</span><span class="sxs-lookup"><span data-stu-id="53c2a-132">-VaultId</span></span>
<span data-ttu-id="53c2a-133">ID do braço do cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="53c2a-133">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="53c2a-134">-Confirme</span><span class="sxs-lookup"><span data-stu-id="53c2a-134">-Confirm</span></span>
<span data-ttu-id="53c2a-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="53c2a-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="53c2a-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="53c2a-136">-WhatIf</span></span>
<span data-ttu-id="53c2a-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="53c2a-137">Shows what would happen if the cmdlet runs.</span></span>

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

### <span data-ttu-id="53c2a-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53c2a-138">CommonParameters</span></span>
<span data-ttu-id="53c2a-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53c2a-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53c2a-140">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="53c2a-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53c2a-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="53c2a-141">INPUTS</span></span>

### <span data-ttu-id="53c2a-142">Microsoft. Azure. Commands. Recoveryservices. backup. cmdlets. Models. PolicyBase</span><span class="sxs-lookup"><span data-stu-id="53c2a-142">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span></span>

### <span data-ttu-id="53c2a-143">System. String</span><span class="sxs-lookup"><span data-stu-id="53c2a-143">System.String</span></span>

## <span data-ttu-id="53c2a-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="53c2a-144">OUTPUTS</span></span>

### <span data-ttu-id="53c2a-145">Microsoft. Azure. Commands. Recoveryservices. backup. cmdlets. Models. PolicyBase</span><span class="sxs-lookup"><span data-stu-id="53c2a-145">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span></span>

## <span data-ttu-id="53c2a-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="53c2a-146">NOTES</span></span>

## <span data-ttu-id="53c2a-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="53c2a-147">RELATED LINKS</span></span>

[<span data-ttu-id="53c2a-148">Get-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="53c2a-148">Get-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="53c2a-149">New-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="53c2a-149">New-AzRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="53c2a-150">Set-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="53c2a-150">Set-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Set-AzRecoveryServicesBackupProtectionPolicy.md)


