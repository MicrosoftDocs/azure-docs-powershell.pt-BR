---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: BFE741CC-C166-4534-93F4-D21AAFAD9FF6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/remove-azurermrecoveryservicesbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Remove-AzureRmRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Remove-AzureRmRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: d687834c41f354897f64ca3300c7c8eaa47940b4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427483"
---
# <span data-ttu-id="04702-101">Remove-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="04702-101">Remove-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>

## <span data-ttu-id="04702-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="04702-102">SYNOPSIS</span></span>
<span data-ttu-id="04702-103">Exclui uma política de proteção de backup de um cofre.</span><span class="sxs-lookup"><span data-stu-id="04702-103">Deletes a Backup protection policy from a vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="04702-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="04702-104">SYNTAX</span></span>

### <span data-ttu-id="04702-105">PolicyName (padrão)</span><span class="sxs-lookup"><span data-stu-id="04702-105">PolicyName (Default)</span></span>
```
Remove-AzureRmRecoveryServicesBackupProtectionPolicy [-Name] <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="04702-106">Políticaobject</span><span class="sxs-lookup"><span data-stu-id="04702-106">PolicyObject</span></span>
```
Remove-AzureRmRecoveryServicesBackupProtectionPolicy [-Policy] <PolicyBase> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="04702-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="04702-107">DESCRIPTION</span></span>
<span data-ttu-id="04702-108">O cmdlet **Remove-AzureRmRecoveryServicesBackupProtectionPolicy** exclui políticas de backup para um cofre.</span><span class="sxs-lookup"><span data-stu-id="04702-108">The **Remove-AzureRmRecoveryServicesBackupProtectionPolicy** cmdlet deletes backup policies for a vault.</span></span>

<span data-ttu-id="04702-109">Antes de poder excluir uma política de proteção de backup, a política não deve ter itens de backup associados.</span><span class="sxs-lookup"><span data-stu-id="04702-109">Before you can delete a Backup protection policy, the policy must not have any associated Backup items.</span></span>
<span data-ttu-id="04702-110">Antes de excluir a política, verifique se cada item associado está associado a alguma outra política.</span><span class="sxs-lookup"><span data-stu-id="04702-110">Before you delete the policy, make sure that each associated item is associated with some other policy.</span></span>
<span data-ttu-id="04702-111">Para associar outra política a um item de backup, use o cmdlet Enable-AzureRmRecoveryServicesBackupProtection.</span><span class="sxs-lookup"><span data-stu-id="04702-111">To associate another policy with a Backup item, use the Enable-AzureRmRecoveryServicesBackupProtection cmdlet.</span></span>

<span data-ttu-id="04702-112">Defina o contexto do cofre usando o cmdlet Set-AzureRmRecoveryServicesVaultContext antes de usar o cmdlet atual.</span><span class="sxs-lookup"><span data-stu-id="04702-112">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="04702-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="04702-113">EXAMPLES</span></span>

### <span data-ttu-id="04702-114">Exemplo 1: remover uma política</span><span class="sxs-lookup"><span data-stu-id="04702-114">Example 1: Remove a policy</span></span>
```
PS C:\>$Pol= Get-AzureRmRecoveryServicesBackupProtectionPolicy -Name "NewPolicy"
PS C:\> Remove-AzureRmRecoveryServicesBackupProtectionPolicy -Policy $Pol
```

<span data-ttu-id="04702-115">O primeiro comando obtém a política de proteção de backup chamada NewPolicy e a armazena na variável $Pol.</span><span class="sxs-lookup"><span data-stu-id="04702-115">The first command gets the Backup protection policy named NewPolicy, and then stores it in the $Pol variable.</span></span>

<span data-ttu-id="04702-116">O segundo comando Remove o objeto de política em $Pol.</span><span class="sxs-lookup"><span data-stu-id="04702-116">The second command removes the policy object in $Pol.</span></span>

## <span data-ttu-id="04702-117">OS</span><span class="sxs-lookup"><span data-stu-id="04702-117">PARAMETERS</span></span>

### <span data-ttu-id="04702-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04702-118">-DefaultProfile</span></span>
<span data-ttu-id="04702-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="04702-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04702-120">-Force</span><span class="sxs-lookup"><span data-stu-id="04702-120">-Force</span></span>
<span data-ttu-id="04702-121">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="04702-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="04702-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="04702-122">-Name</span></span>
<span data-ttu-id="04702-123">Especifica o nome da política de proteção de backup a ser removida.</span><span class="sxs-lookup"><span data-stu-id="04702-123">Specifies the name of the Backup protection policy to remove.</span></span>

```yaml
Type: String
Parameter Sets: PolicyName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04702-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="04702-124">-PassThru</span></span>
<span data-ttu-id="04702-125">Retorne a política a ser excluída.</span><span class="sxs-lookup"><span data-stu-id="04702-125">Return the policy to be deleted.</span></span>

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

### <span data-ttu-id="04702-126">-Política</span><span class="sxs-lookup"><span data-stu-id="04702-126">-Policy</span></span>
<span data-ttu-id="04702-127">Especifica a política de proteção de backup a ser removida.</span><span class="sxs-lookup"><span data-stu-id="04702-127">Specifies the Backup protection policy to remove.</span></span>
<span data-ttu-id="04702-128">Para obter um objeto **BackupPolicy** , use o cmdlet Get-AzureRmRecoveryServicesBackupProtectionPolicy.</span><span class="sxs-lookup"><span data-stu-id="04702-128">To obtain an **BackupPolicy** object, use the Get-AzureRmRecoveryServicesBackupProtectionPolicy cmdlet.</span></span>

```yaml
Type: PolicyBase
Parameter Sets: PolicyObject
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="04702-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="04702-129">-Confirm</span></span>
<span data-ttu-id="04702-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="04702-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04702-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="04702-131">-WhatIf</span></span>
<span data-ttu-id="04702-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="04702-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="04702-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="04702-133">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04702-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04702-134">CommonParameters</span></span>
<span data-ttu-id="04702-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="04702-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04702-136">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="04702-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04702-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="04702-137">INPUTS</span></span>

### <span data-ttu-id="04702-138">PolicyBase</span><span class="sxs-lookup"><span data-stu-id="04702-138">PolicyBase</span></span>
<span data-ttu-id="04702-139">O parâmetro "política" aceita o valor do tipo "PolicyBase" da pipeline</span><span class="sxs-lookup"><span data-stu-id="04702-139">Parameter 'Policy' accepts value of type 'PolicyBase' from the pipeline</span></span>

## <span data-ttu-id="04702-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="04702-140">OUTPUTS</span></span>

## <span data-ttu-id="04702-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="04702-141">NOTES</span></span>

## <span data-ttu-id="04702-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="04702-142">RELATED LINKS</span></span>

[<span data-ttu-id="04702-143">Get-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="04702-143">Get-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzureRmRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="04702-144">New-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="04702-144">New-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzureRmRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="04702-145">Set-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="04702-145">Set-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./Set-AzureRmRecoveryServicesBackupProtectionPolicy.md)


