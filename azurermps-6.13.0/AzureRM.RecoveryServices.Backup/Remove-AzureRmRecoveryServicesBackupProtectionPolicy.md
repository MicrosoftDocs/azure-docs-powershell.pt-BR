---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: BFE741CC-C166-4534-93F4-D21AAFAD9FF6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/remove-azurermrecoveryservicesbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Remove-AzureRmRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Remove-AzureRmRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: 805deece859eb4baa05d8c3d34dfcc8a9d571354
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440726"
---
# <span data-ttu-id="6d6a4-101">Remove-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="6d6a4-101">Remove-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>

## <span data-ttu-id="6d6a4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6d6a4-102">SYNOPSIS</span></span>
<span data-ttu-id="6d6a4-103">Exclui uma política de proteção de backup de um cofre.</span><span class="sxs-lookup"><span data-stu-id="6d6a4-103">Deletes a Backup protection policy from a vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6d6a4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6d6a4-104">SYNTAX</span></span>

### <span data-ttu-id="6d6a4-105">PolicyName (padrão)</span><span class="sxs-lookup"><span data-stu-id="6d6a4-105">PolicyName (Default)</span></span>
```
Remove-AzureRmRecoveryServicesBackupProtectionPolicy [-Name] <String> [-PassThru] [-Force] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6d6a4-106">Políticaobject</span><span class="sxs-lookup"><span data-stu-id="6d6a4-106">PolicyObject</span></span>
```
Remove-AzureRmRecoveryServicesBackupProtectionPolicy [-Policy] <PolicyBase> [-PassThru] [-Force]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6d6a4-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6d6a4-107">DESCRIPTION</span></span>
<span data-ttu-id="6d6a4-108">O cmdlet **Remove-AzureRmRecoveryServicesBackupProtectionPolicy** exclui políticas de backup para um cofre.</span><span class="sxs-lookup"><span data-stu-id="6d6a4-108">The **Remove-AzureRmRecoveryServicesBackupProtectionPolicy** cmdlet deletes backup policies for a vault.</span></span>
<span data-ttu-id="6d6a4-109">Antes de poder excluir uma política de proteção de backup, a política não deve ter itens de backup associados.</span><span class="sxs-lookup"><span data-stu-id="6d6a4-109">Before you can delete a Backup protection policy, the policy must not have any associated Backup items.</span></span>
<span data-ttu-id="6d6a4-110">Antes de excluir a política, verifique se cada item associado está associado a alguma outra política.</span><span class="sxs-lookup"><span data-stu-id="6d6a4-110">Before you delete the policy, make sure that each associated item is associated with some other policy.</span></span>
<span data-ttu-id="6d6a4-111">Para associar outra política a um item de backup, use o cmdlet Enable-AzureRmRecoveryServicesBackupProtection.</span><span class="sxs-lookup"><span data-stu-id="6d6a4-111">To associate another policy with a Backup item, use the Enable-AzureRmRecoveryServicesBackupProtection cmdlet.</span></span>
<span data-ttu-id="6d6a4-112">Defina o contexto do cofre usando o cmdlet Set-AzureRmRecoveryServicesVaultContext antes de usar o cmdlet atual.</span><span class="sxs-lookup"><span data-stu-id="6d6a4-112">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="6d6a4-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6d6a4-113">EXAMPLES</span></span>

### <span data-ttu-id="6d6a4-114">Exemplo 1: remover uma política</span><span class="sxs-lookup"><span data-stu-id="6d6a4-114">Example 1: Remove a policy</span></span>
```
PS C:\>$Pol= Get-AzureRmRecoveryServicesBackupProtectionPolicy -Name "NewPolicy"
PS C:\> Remove-AzureRmRecoveryServicesBackupProtectionPolicy -Policy $Pol
```

<span data-ttu-id="6d6a4-115">O primeiro comando obtém a política de proteção de backup chamada NewPolicy e a armazena na variável $Pol.</span><span class="sxs-lookup"><span data-stu-id="6d6a4-115">The first command gets the Backup protection policy named NewPolicy, and then stores it in the $Pol variable.</span></span>
<span data-ttu-id="6d6a4-116">O segundo comando Remove o objeto de política em $Pol.</span><span class="sxs-lookup"><span data-stu-id="6d6a4-116">The second command removes the policy object in $Pol.</span></span>

## <span data-ttu-id="6d6a4-117">OS</span><span class="sxs-lookup"><span data-stu-id="6d6a4-117">PARAMETERS</span></span>

### <span data-ttu-id="6d6a4-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d6a4-118">-DefaultProfile</span></span>
<span data-ttu-id="6d6a4-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6d6a4-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d6a4-120">-Force</span><span class="sxs-lookup"><span data-stu-id="6d6a4-120">-Force</span></span>
<span data-ttu-id="6d6a4-121">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="6d6a4-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="6d6a4-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="6d6a4-122">-Name</span></span>
<span data-ttu-id="6d6a4-123">Especifica o nome da política de proteção de backup a ser removida.</span><span class="sxs-lookup"><span data-stu-id="6d6a4-123">Specifies the name of the Backup protection policy to remove.</span></span>

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

### <span data-ttu-id="6d6a4-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6d6a4-124">-PassThru</span></span>
<span data-ttu-id="6d6a4-125">Retorne a política a ser excluída.</span><span class="sxs-lookup"><span data-stu-id="6d6a4-125">Return the policy to be deleted.</span></span>

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

### <span data-ttu-id="6d6a4-126">-Política</span><span class="sxs-lookup"><span data-stu-id="6d6a4-126">-Policy</span></span>
<span data-ttu-id="6d6a4-127">Especifica a política de proteção de backup a ser removida.</span><span class="sxs-lookup"><span data-stu-id="6d6a4-127">Specifies the Backup protection policy to remove.</span></span>
<span data-ttu-id="6d6a4-128">Para obter um objeto **BackupPolicy** , use o cmdlet Get-AzureRmRecoveryServicesBackupProtectionPolicy.</span><span class="sxs-lookup"><span data-stu-id="6d6a4-128">To obtain an **BackupPolicy** object, use the Get-AzureRmRecoveryServicesBackupProtectionPolicy cmdlet.</span></span>

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

### <span data-ttu-id="6d6a4-129">-Cofreid</span><span class="sxs-lookup"><span data-stu-id="6d6a4-129">-VaultId</span></span>
<span data-ttu-id="6d6a4-130">ID do braço do cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="6d6a4-130">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="6d6a4-131">-Confirme</span><span class="sxs-lookup"><span data-stu-id="6d6a4-131">-Confirm</span></span>
<span data-ttu-id="6d6a4-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6d6a4-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6d6a4-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6d6a4-133">-WhatIf</span></span>
<span data-ttu-id="6d6a4-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="6d6a4-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6d6a4-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6d6a4-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6d6a4-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d6a4-136">CommonParameters</span></span>
<span data-ttu-id="6d6a4-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d6a4-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d6a4-138">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6d6a4-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d6a4-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6d6a4-139">INPUTS</span></span>

### <span data-ttu-id="6d6a4-140">Microsoft. Azure. Commands. Recoveryservices. backup. cmdlets. Models. PolicyBase</span><span class="sxs-lookup"><span data-stu-id="6d6a4-140">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span></span>
<span data-ttu-id="6d6a4-141">Parâmetros: Policy (ByValue)</span><span class="sxs-lookup"><span data-stu-id="6d6a4-141">Parameters: Policy (ByValue)</span></span>

### <span data-ttu-id="6d6a4-142">System. String</span><span class="sxs-lookup"><span data-stu-id="6d6a4-142">System.String</span></span>
<span data-ttu-id="6d6a4-143">Parâmetros: Vaultid (ByValue)</span><span class="sxs-lookup"><span data-stu-id="6d6a4-143">Parameters: VaultId (ByValue)</span></span>

## <span data-ttu-id="6d6a4-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6d6a4-144">OUTPUTS</span></span>

### <span data-ttu-id="6d6a4-145">Microsoft. Azure. Commands. Recoveryservices. backup. cmdlets. Models. PolicyBase</span><span class="sxs-lookup"><span data-stu-id="6d6a4-145">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span></span>

## <span data-ttu-id="6d6a4-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6d6a4-146">NOTES</span></span>

## <span data-ttu-id="6d6a4-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6d6a4-147">RELATED LINKS</span></span>

[<span data-ttu-id="6d6a4-148">Get-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="6d6a4-148">Get-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzureRmRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="6d6a4-149">New-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="6d6a4-149">New-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzureRmRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="6d6a4-150">Set-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="6d6a4-150">Set-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./Set-AzureRmRecoveryServicesBackupProtectionPolicy.md)


