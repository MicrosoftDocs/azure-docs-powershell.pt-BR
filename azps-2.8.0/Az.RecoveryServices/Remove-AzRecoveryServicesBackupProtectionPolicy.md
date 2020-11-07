---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: BFE741CC-C166-4534-93F4-D21AAFAD9FF6
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: b900e9b137c8268969ef1eb715f0b79356abc720
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93773462"
---
# <span data-ttu-id="6f80c-101">Remove-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="6f80c-101">Remove-AzRecoveryServicesBackupProtectionPolicy</span></span>

## <span data-ttu-id="6f80c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6f80c-102">SYNOPSIS</span></span>
<span data-ttu-id="6f80c-103">Exclui uma política de proteção de backup de um cofre.</span><span class="sxs-lookup"><span data-stu-id="6f80c-103">Deletes a Backup protection policy from a vault.</span></span>

## <span data-ttu-id="6f80c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6f80c-104">SYNTAX</span></span>

### <span data-ttu-id="6f80c-105">PolicyName (padrão)</span><span class="sxs-lookup"><span data-stu-id="6f80c-105">PolicyName (Default)</span></span>
```
Remove-AzRecoveryServicesBackupProtectionPolicy [-Name] <String> [-PassThru] [-Force] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6f80c-106">Políticaobject</span><span class="sxs-lookup"><span data-stu-id="6f80c-106">PolicyObject</span></span>
```
Remove-AzRecoveryServicesBackupProtectionPolicy [-Policy] <PolicyBase> [-PassThru] [-Force] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6f80c-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6f80c-107">DESCRIPTION</span></span>
<span data-ttu-id="6f80c-108">O cmdlet **Remove-AzRecoveryServicesBackupProtectionPolicy** exclui políticas de backup para um cofre.</span><span class="sxs-lookup"><span data-stu-id="6f80c-108">The **Remove-AzRecoveryServicesBackupProtectionPolicy** cmdlet deletes backup policies for a vault.</span></span>
<span data-ttu-id="6f80c-109">Antes de poder excluir uma política de proteção de backup, a política não deve ter itens de backup associados.</span><span class="sxs-lookup"><span data-stu-id="6f80c-109">Before you can delete a Backup protection policy, the policy must not have any associated Backup items.</span></span>
<span data-ttu-id="6f80c-110">Antes de excluir a política, verifique se cada item associado está associado a alguma outra política.</span><span class="sxs-lookup"><span data-stu-id="6f80c-110">Before you delete the policy, make sure that each associated item is associated with some other policy.</span></span>
<span data-ttu-id="6f80c-111">Para associar outra política a um item de backup, use o cmdlet Enable-AzRecoveryServicesBackupProtection.</span><span class="sxs-lookup"><span data-stu-id="6f80c-111">To associate another policy with a Backup item, use the Enable-AzRecoveryServicesBackupProtection cmdlet.</span></span>
<span data-ttu-id="6f80c-112">Defina o contexto do cofre usando o cmdlet Set-AzRecoveryServicesVaultContext antes de usar o cmdlet atual.</span><span class="sxs-lookup"><span data-stu-id="6f80c-112">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="6f80c-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6f80c-113">EXAMPLES</span></span>

### <span data-ttu-id="6f80c-114">Exemplo 1: remover uma política</span><span class="sxs-lookup"><span data-stu-id="6f80c-114">Example 1: Remove a policy</span></span>
```
PS C:\>$Pol= Get-AzRecoveryServicesBackupProtectionPolicy -Name "NewPolicy"
PS C:\> Remove-AzRecoveryServicesBackupProtectionPolicy -Policy $Pol
```

<span data-ttu-id="6f80c-115">O primeiro comando obtém a política de proteção de backup chamada NewPolicy e a armazena na variável $Pol.</span><span class="sxs-lookup"><span data-stu-id="6f80c-115">The first command gets the Backup protection policy named NewPolicy, and then stores it in the $Pol variable.</span></span>
<span data-ttu-id="6f80c-116">O segundo comando Remove o objeto de política em $Pol.</span><span class="sxs-lookup"><span data-stu-id="6f80c-116">The second command removes the policy object in $Pol.</span></span>

## <span data-ttu-id="6f80c-117">OS</span><span class="sxs-lookup"><span data-stu-id="6f80c-117">PARAMETERS</span></span>

### <span data-ttu-id="6f80c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f80c-118">-DefaultProfile</span></span>
<span data-ttu-id="6f80c-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6f80c-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6f80c-120">-Force</span><span class="sxs-lookup"><span data-stu-id="6f80c-120">-Force</span></span>
<span data-ttu-id="6f80c-121">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="6f80c-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="6f80c-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="6f80c-122">-Name</span></span>
<span data-ttu-id="6f80c-123">Especifica o nome da política de proteção de backup a ser removida.</span><span class="sxs-lookup"><span data-stu-id="6f80c-123">Specifies the name of the Backup protection policy to remove.</span></span>

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

### <span data-ttu-id="6f80c-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6f80c-124">-PassThru</span></span>
<span data-ttu-id="6f80c-125">Retorne a política a ser excluída.</span><span class="sxs-lookup"><span data-stu-id="6f80c-125">Return the policy to be deleted.</span></span>

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

### <span data-ttu-id="6f80c-126">-Política</span><span class="sxs-lookup"><span data-stu-id="6f80c-126">-Policy</span></span>
<span data-ttu-id="6f80c-127">Especifica a política de proteção de backup a ser removida.</span><span class="sxs-lookup"><span data-stu-id="6f80c-127">Specifies the Backup protection policy to remove.</span></span>
<span data-ttu-id="6f80c-128">Para obter um objeto **BackupPolicy** , use o cmdlet Get-AzRecoveryServicesBackupProtectionPolicy.</span><span class="sxs-lookup"><span data-stu-id="6f80c-128">To obtain an **BackupPolicy** object, use the Get-AzRecoveryServicesBackupProtectionPolicy cmdlet.</span></span>

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

### <span data-ttu-id="6f80c-129">-Cofreid</span><span class="sxs-lookup"><span data-stu-id="6f80c-129">-VaultId</span></span>
<span data-ttu-id="6f80c-130">ID do braço do cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="6f80c-130">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="6f80c-131">-Confirme</span><span class="sxs-lookup"><span data-stu-id="6f80c-131">-Confirm</span></span>
<span data-ttu-id="6f80c-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6f80c-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6f80c-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6f80c-133">-WhatIf</span></span>
<span data-ttu-id="6f80c-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="6f80c-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6f80c-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6f80c-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6f80c-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f80c-136">CommonParameters</span></span>
<span data-ttu-id="6f80c-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6f80c-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f80c-138">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6f80c-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f80c-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6f80c-139">INPUTS</span></span>

### <span data-ttu-id="6f80c-140">Microsoft. Azure. Commands. Recoveryservices. backup. cmdlets. Models. PolicyBase</span><span class="sxs-lookup"><span data-stu-id="6f80c-140">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span></span>

### <span data-ttu-id="6f80c-141">System. String</span><span class="sxs-lookup"><span data-stu-id="6f80c-141">System.String</span></span>

## <span data-ttu-id="6f80c-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6f80c-142">OUTPUTS</span></span>

### <span data-ttu-id="6f80c-143">Microsoft. Azure. Commands. Recoveryservices. backup. cmdlets. Models. PolicyBase</span><span class="sxs-lookup"><span data-stu-id="6f80c-143">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span></span>

## <span data-ttu-id="6f80c-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6f80c-144">NOTES</span></span>

## <span data-ttu-id="6f80c-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6f80c-145">RELATED LINKS</span></span>

[<span data-ttu-id="6f80c-146">Get-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="6f80c-146">Get-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="6f80c-147">New-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="6f80c-147">New-AzRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="6f80c-148">Set-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="6f80c-148">Set-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Set-AzRecoveryServicesBackupProtectionPolicy.md)

