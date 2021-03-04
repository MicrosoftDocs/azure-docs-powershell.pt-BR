---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/undo-azrecoveryservicesbackupitemdeletion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Undo-AzRecoveryServicesBackupItemDeletion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Undo-AzRecoveryServicesBackupItemDeletion.md
ms.openlocfilehash: f7e82c2ccc939b0492575766c621a81ef9a25e9b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101893122"
---
# <span data-ttu-id="e254a-101">Undo-AzRecoveryServicesBackupItemDeletion</span><span class="sxs-lookup"><span data-stu-id="e254a-101">Undo-AzRecoveryServicesBackupItemDeletion</span></span>

## <span data-ttu-id="e254a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e254a-102">SYNOPSIS</span></span>
<span data-ttu-id="e254a-103">Se um item de backup for excluído e estiver presente em um estado excluído de forma suave, este comando retornará o item para um estado em que os dados serão mantidos para sempre</span><span class="sxs-lookup"><span data-stu-id="e254a-103">If a backup item is deleted and present in a soft-deleted state, this command brings the item back to a state where the data is retained forever</span></span> 

## <span data-ttu-id="e254a-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="e254a-104">SYNTAX</span></span>

```
Undo-AzRecoveryServicesBackupItemDeletion [-Item] <ItemBase> [-Force] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e254a-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="e254a-105">DESCRIPTION</span></span>
<span data-ttu-id="e254a-106">O Undo-AzRecoveryServicesBackupItemDeletion cmdlet reverte um item excluído de forma suave para um estado em que a proteção é interrompida, mas os dados são mantidos para sempre.</span><span class="sxs-lookup"><span data-stu-id="e254a-106">The Undo-AzRecoveryServicesBackupItemDeletion cmdlet reverts a soft-deleted item to a state where the protection is stopped but data is retained forever.</span></span>

## <span data-ttu-id="e254a-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e254a-107">EXAMPLES</span></span>

### <span data-ttu-id="e254a-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e254a-108">Example 1</span></span>
```powershell
PS C:\> $Cont = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVM
PS C:\> $PI = Get-AzRecoveryServicesBackupItem -Container $Cont[0] -WorkloadType AzureVM 
PS C:\> Disable-AzRecoveryServicesBackupProtection -Item $PI[0] -RemoveRecoveryPoints
PS C:\> $PI = Get-AzRecoveryServicesBackupItem -Container $Cont[0] -WorkloadType AzureVM | Where-Object {$_.DeleteState -eq "ToBeDeleted"}
PS C:\> Undo-AzRecoveryServicesBackupItemDeletion -Item $PI[0]
```

<span data-ttu-id="e254a-109">O primeiro comando obtém uma matriz de contêineres de backup e, em seguida, armazena-o na matriz $Cont.</span><span class="sxs-lookup"><span data-stu-id="e254a-109">The first command gets an array of backup containers, and then stores it in the $Cont array.</span></span>
<span data-ttu-id="e254a-110">O segundo comando obtém o item backup correspondente ao primeiro item de contêiner e o armazena na variável $PI.</span><span class="sxs-lookup"><span data-stu-id="e254a-110">The second command gets the Backup item corresponding to the first container item, and then stores it in the $PI variable.</span></span>
<span data-ttu-id="e254a-111">O terceiro comando desabilita a proteção de backup do item no $PI 0 e coloca o item em um \[ \] estado softdeleted.</span><span class="sxs-lookup"><span data-stu-id="e254a-111">The third command disables Backup protection for the item in $PI\[0\] and puts the item in a softdeleted state.</span></span>
<span data-ttu-id="e254a-112">O quarto comando obtém o item que está em um estado softdeleted.</span><span class="sxs-lookup"><span data-stu-id="e254a-112">The fourth command gets the item which is in a softdeleted state.</span></span>
<span data-ttu-id="e254a-113">O último comando traz a VM softdeleted para um estado em que a proteção é interrompida, mas os dados são mantidos para sempre.</span><span class="sxs-lookup"><span data-stu-id="e254a-113">The last command brings the softdeleted VM to a state where the protection is stopped but data is retained forever.</span></span>

### <span data-ttu-id="e254a-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="e254a-114">Example 2</span></span>

<span data-ttu-id="e254a-115">Reidrata um Item excluído de forma suave.</span><span class="sxs-lookup"><span data-stu-id="e254a-115">Rehydrates a soft-deleted Item.</span></span> <span data-ttu-id="e254a-116">(gerado automaticamente)</span><span class="sxs-lookup"><span data-stu-id="e254a-116">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Undo-AzRecoveryServicesBackupItemDeletion -Item $PI[0] -VaultId $vault.ID
```

## <span data-ttu-id="e254a-117">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="e254a-117">PARAMETERS</span></span>

### <span data-ttu-id="e254a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e254a-118">-DefaultProfile</span></span>
<span data-ttu-id="e254a-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e254a-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e254a-120">-Force</span><span class="sxs-lookup"><span data-stu-id="e254a-120">-Force</span></span>
<span data-ttu-id="e254a-121">Force desabilita a proteção de backup (impede a caixa de diálogo de confirmação).</span><span class="sxs-lookup"><span data-stu-id="e254a-121">Force disables backup protection (prevents confirmation dialog).</span></span>
<span data-ttu-id="e254a-122">Esse parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="e254a-122">This parameter is optional.</span></span>

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

### <span data-ttu-id="e254a-123">-Item</span><span class="sxs-lookup"><span data-stu-id="e254a-123">-Item</span></span>
<span data-ttu-id="e254a-124">Especifica o item de backup para o qual este cmdlet reverte a exclusão.</span><span class="sxs-lookup"><span data-stu-id="e254a-124">Specifies the backup item for which this cmdlet reverts the deletion.</span></span>
<span data-ttu-id="e254a-125">Para obter um AzureRmRecoveryServicesBackupItem, use Get-AzRecoveryServicesBackupItem cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e254a-125">To obtain an AzureRmRecoveryServicesBackupItem , use the Get-AzRecoveryServicesBackupItem cmdlet.</span></span>

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

### <span data-ttu-id="e254a-126">-VaultId</span><span class="sxs-lookup"><span data-stu-id="e254a-126">-VaultId</span></span>
<span data-ttu-id="e254a-127">ARM ID do Cofre de Serviços de Recuperação.</span><span class="sxs-lookup"><span data-stu-id="e254a-127">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="e254a-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e254a-128">-Confirm</span></span>
<span data-ttu-id="e254a-129">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e254a-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e254a-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e254a-130">-WhatIf</span></span>
<span data-ttu-id="e254a-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e254a-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e254a-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e254a-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e254a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e254a-133">CommonParameters</span></span>
<span data-ttu-id="e254a-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e254a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e254a-135">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e254a-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e254a-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e254a-136">INPUTS</span></span>

### <span data-ttu-id="e254a-137">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span><span class="sxs-lookup"><span data-stu-id="e254a-137">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

### <span data-ttu-id="e254a-138">System.String</span><span class="sxs-lookup"><span data-stu-id="e254a-138">System.String</span></span>

## <span data-ttu-id="e254a-139">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="e254a-139">OUTPUTS</span></span>

### <span data-ttu-id="e254a-140">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span><span class="sxs-lookup"><span data-stu-id="e254a-140">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="e254a-141">NOTES</span><span class="sxs-lookup"><span data-stu-id="e254a-141">NOTES</span></span>

## <span data-ttu-id="e254a-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e254a-142">RELATED LINKS</span></span>

[<span data-ttu-id="e254a-143">Get-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="e254a-143">Get-AzRecoveryServicesBackupContainer</span></span>]()

[<span data-ttu-id="e254a-144">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="e254a-144">Get-AzRecoveryServicesBackupItem</span></span>]()

