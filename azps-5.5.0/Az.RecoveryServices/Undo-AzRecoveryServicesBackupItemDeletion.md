---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/undo-azrecoveryservicesbackupitemdeletion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Undo-AzRecoveryServicesBackupItemDeletion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Undo-AzRecoveryServicesBackupItemDeletion.md
ms.openlocfilehash: 62d8dc302dc5819272034cfdd1c3fd0c0c79f54c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113363"
---
# <span data-ttu-id="e5b9b-101">Undo-AzRecoveryServicesBackupItemDeletion</span><span class="sxs-lookup"><span data-stu-id="e5b9b-101">Undo-AzRecoveryServicesBackupItemDeletion</span></span>

## <span data-ttu-id="e5b9b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e5b9b-102">SYNOPSIS</span></span>
<span data-ttu-id="e5b9b-103">Se um item de backup for excluído e presente em um estado de exclusão suave, esse comando retornará ao estado em que os dados serão mantidos para sempre</span><span class="sxs-lookup"><span data-stu-id="e5b9b-103">If a backup item is deleted and present in a soft-deleted state, this command brings the item back to a state where the data is retained forever</span></span> 

## <span data-ttu-id="e5b9b-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e5b9b-104">SYNTAX</span></span>

```
Undo-AzRecoveryServicesBackupItemDeletion [-Item] <ItemBase> [-Force] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e5b9b-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="e5b9b-105">DESCRIPTION</span></span>
<span data-ttu-id="e5b9b-106">O Undo-AzRecoveryServicesBackupItemDeletion cmdlet reverte um item excluído suavemente para um estado em que a proteção é interrompida, mas os dados são mantidos para sempre.</span><span class="sxs-lookup"><span data-stu-id="e5b9b-106">The Undo-AzRecoveryServicesBackupItemDeletion cmdlet reverts a soft-deleted item to a state where the protection is stopped but data is retained forever.</span></span>

## <span data-ttu-id="e5b9b-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="e5b9b-107">EXAMPLES</span></span>

### <span data-ttu-id="e5b9b-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e5b9b-108">Example 1</span></span>
```powershell
PS C:\> $Cont = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVM
PS C:\> $PI = Get-AzRecoveryServicesBackupItem -Container $Cont[0] -WorkloadType AzureVM 
PS C:\> Disable-AzRecoveryServicesBackupProtection -Item $PI[0] -RemoveRecoveryPoints
PS C:\> $PI = Get-AzRecoveryServicesBackupItem -Container $Cont[0] -WorkloadType AzureVM | Where-Object {$_.DeleteState -eq "ToBeDeleted"}
PS C:\> Undo-AzRecoveryServicesBackupItemDeletion -Item $PI[0]
```

<span data-ttu-id="e5b9b-109">O primeiro comando obtém uma matriz de contêineres de backup e, em seguida, o armazena na matriz $Cont dados.</span><span class="sxs-lookup"><span data-stu-id="e5b9b-109">The first command gets an array of backup containers, and then stores it in the $Cont array.</span></span>
<span data-ttu-id="e5b9b-110">O segundo comando obtém o item de Backup correspondente ao primeiro item de contêiner e o armazena na variável $PI dados.</span><span class="sxs-lookup"><span data-stu-id="e5b9b-110">The second command gets the Backup item corresponding to the first container item, and then stores it in the $PI variable.</span></span>
<span data-ttu-id="e5b9b-111">O terceiro comando desabilita a proteção de backup para o item no $PI 0 e coloca o item em um \[ \] estado softdeleted.</span><span class="sxs-lookup"><span data-stu-id="e5b9b-111">The third command disables Backup protection for the item in $PI\[0\] and puts the item in a softdeleted state.</span></span>
<span data-ttu-id="e5b9b-112">O quarto comando obtém o item que está em um estado softdeleted.</span><span class="sxs-lookup"><span data-stu-id="e5b9b-112">The fourth command gets the item which is in a softdeleted state.</span></span>
<span data-ttu-id="e5b9b-113">O último comando leva o VM softdeleted a um estado onde a proteção é interrompida, mas os dados são mantidos para sempre.</span><span class="sxs-lookup"><span data-stu-id="e5b9b-113">The last command brings the softdeleted VM to a state where the protection is stopped but data is retained forever.</span></span>

### <span data-ttu-id="e5b9b-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="e5b9b-114">Example 2</span></span>

<span data-ttu-id="e5b9b-115">Reativa um Item excluído suavemente.</span><span class="sxs-lookup"><span data-stu-id="e5b9b-115">Rehydrates a soft-deleted Item.</span></span> <span data-ttu-id="e5b9b-116">(gerado automaticamente)</span><span class="sxs-lookup"><span data-stu-id="e5b9b-116">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Undo-AzRecoveryServicesBackupItemDeletion -Item $PI[0] -VaultId $vault.ID
```

## <span data-ttu-id="e5b9b-117">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e5b9b-117">PARAMETERS</span></span>

### <span data-ttu-id="e5b9b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5b9b-118">-DefaultProfile</span></span>
<span data-ttu-id="e5b9b-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e5b9b-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e5b9b-120">-Forçar</span><span class="sxs-lookup"><span data-stu-id="e5b9b-120">-Force</span></span>
<span data-ttu-id="e5b9b-121">A força desabilita a proteção de backup (impede a caixa de diálogo de confirmação).</span><span class="sxs-lookup"><span data-stu-id="e5b9b-121">Force disables backup protection (prevents confirmation dialog).</span></span>
<span data-ttu-id="e5b9b-122">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="e5b9b-122">This parameter is optional.</span></span>

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

### <span data-ttu-id="e5b9b-123">-Item</span><span class="sxs-lookup"><span data-stu-id="e5b9b-123">-Item</span></span>
<span data-ttu-id="e5b9b-124">Especifica o item de backup para o qual este cmdlet reverte a exclusão.</span><span class="sxs-lookup"><span data-stu-id="e5b9b-124">Specifies the backup item for which this cmdlet reverts the deletion.</span></span>
<span data-ttu-id="e5b9b-125">Para obter um cmdlet AzureRmRecoveryServicesBackupItem, use o cmdlet Get-AzRecoveryServicesBackupItem AzureRmRecoveryServicesBackupItem.</span><span class="sxs-lookup"><span data-stu-id="e5b9b-125">To obtain an AzureRmRecoveryServicesBackupItem , use the Get-AzRecoveryServicesBackupItem cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e5b9b-126">-VaultId</span><span class="sxs-lookup"><span data-stu-id="e5b9b-126">-VaultId</span></span>
<span data-ttu-id="e5b9b-127">ID arm do Cofre de Serviços de Recuperação.</span><span class="sxs-lookup"><span data-stu-id="e5b9b-127">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="e5b9b-128">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="e5b9b-128">-Confirm</span></span>
<span data-ttu-id="e5b9b-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e5b9b-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e5b9b-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e5b9b-130">-WhatIf</span></span>
<span data-ttu-id="e5b9b-131">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="e5b9b-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e5b9b-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e5b9b-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e5b9b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5b9b-133">CommonParameters</span></span>
<span data-ttu-id="e5b9b-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5b9b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5b9b-135">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e5b9b-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5b9b-136">Entradas</span><span class="sxs-lookup"><span data-stu-id="e5b9b-136">INPUTS</span></span>

### <span data-ttu-id="e5b9b-137">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span><span class="sxs-lookup"><span data-stu-id="e5b9b-137">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

### <span data-ttu-id="e5b9b-138">System.String</span><span class="sxs-lookup"><span data-stu-id="e5b9b-138">System.String</span></span>

## <span data-ttu-id="e5b9b-139">Saídas</span><span class="sxs-lookup"><span data-stu-id="e5b9b-139">OUTPUTS</span></span>

### <span data-ttu-id="e5b9b-140">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span><span class="sxs-lookup"><span data-stu-id="e5b9b-140">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="e5b9b-141">Notas</span><span class="sxs-lookup"><span data-stu-id="e5b9b-141">NOTES</span></span>

## <span data-ttu-id="e5b9b-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e5b9b-142">RELATED LINKS</span></span>

[<span data-ttu-id="e5b9b-143">Get-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="e5b9b-143">Get-AzRecoveryServicesBackupContainer</span></span>]()

[<span data-ttu-id="e5b9b-144">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="e5b9b-144">Get-AzRecoveryServicesBackupItem</span></span>]()

