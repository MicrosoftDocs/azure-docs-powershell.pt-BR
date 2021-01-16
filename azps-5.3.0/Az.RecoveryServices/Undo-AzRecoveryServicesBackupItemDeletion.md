---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/undo-azrecoveryservicesbackupitemdeletion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Undo-AzRecoveryServicesBackupItemDeletion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Undo-AzRecoveryServicesBackupItemDeletion.md
ms.openlocfilehash: 62d8dc302dc5819272034cfdd1c3fd0c0c79f54c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98271627"
---
# <span data-ttu-id="0e88c-101">Undo-AzRecoveryServicesBackupItemDeletion</span><span class="sxs-lookup"><span data-stu-id="0e88c-101">Undo-AzRecoveryServicesBackupItemDeletion</span></span>

## <span data-ttu-id="0e88c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0e88c-102">SYNOPSIS</span></span>
<span data-ttu-id="0e88c-103">Se um item de backup for excluído e estiver presente em um estado excluído de forma flexível, esse comando colocará o item novamente em um estado em que os dados são mantidos para sempre</span><span class="sxs-lookup"><span data-stu-id="0e88c-103">If a backup item is deleted and present in a soft-deleted state, this command brings the item back to a state where the data is retained forever</span></span> 

## <span data-ttu-id="0e88c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0e88c-104">SYNTAX</span></span>

```
Undo-AzRecoveryServicesBackupItemDeletion [-Item] <ItemBase> [-Force] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0e88c-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0e88c-105">DESCRIPTION</span></span>
<span data-ttu-id="0e88c-106">O cmdlet Undo-AzRecoveryServicesBackupItemDeletion reverte um item excluído de forma flexível para um estado em que a proteção é interrompida, mas os dados são mantidos para sempre.</span><span class="sxs-lookup"><span data-stu-id="0e88c-106">The Undo-AzRecoveryServicesBackupItemDeletion cmdlet reverts a soft-deleted item to a state where the protection is stopped but data is retained forever.</span></span>

## <span data-ttu-id="0e88c-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0e88c-107">EXAMPLES</span></span>

### <span data-ttu-id="0e88c-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="0e88c-108">Example 1</span></span>
```powershell
PS C:\> $Cont = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVM
PS C:\> $PI = Get-AzRecoveryServicesBackupItem -Container $Cont[0] -WorkloadType AzureVM 
PS C:\> Disable-AzRecoveryServicesBackupProtection -Item $PI[0] -RemoveRecoveryPoints
PS C:\> $PI = Get-AzRecoveryServicesBackupItem -Container $Cont[0] -WorkloadType AzureVM | Where-Object {$_.DeleteState -eq "ToBeDeleted"}
PS C:\> Undo-AzRecoveryServicesBackupItemDeletion -Item $PI[0]
```

<span data-ttu-id="0e88c-109">O primeiro comando obtém uma matriz de contêineres de backup e, em seguida, armazena-o na matriz $Cont.</span><span class="sxs-lookup"><span data-stu-id="0e88c-109">The first command gets an array of backup containers, and then stores it in the $Cont array.</span></span>
<span data-ttu-id="0e88c-110">O segundo comando obtém o item de backup correspondente ao primeiro item de contêiner e, em seguida, armazena-o na variável $PI.</span><span class="sxs-lookup"><span data-stu-id="0e88c-110">The second command gets the Backup item corresponding to the first container item, and then stores it in the $PI variable.</span></span>
<span data-ttu-id="0e88c-111">O terceiro comando desabilita a proteção de backup para o item em $PI \[ 0 \] e coloca o item em um estado SoftDeleted.</span><span class="sxs-lookup"><span data-stu-id="0e88c-111">The third command disables Backup protection for the item in $PI\[0\] and puts the item in a softdeleted state.</span></span>
<span data-ttu-id="0e88c-112">O quarto comando obtém o item que está em um estado SoftDeleted.</span><span class="sxs-lookup"><span data-stu-id="0e88c-112">The fourth command gets the item which is in a softdeleted state.</span></span>
<span data-ttu-id="0e88c-113">O último comando leva a VM SoftDeleted a um estado em que a proteção é interrompida, mas os dados são mantidos para sempre.</span><span class="sxs-lookup"><span data-stu-id="0e88c-113">The last command brings the softdeleted VM to a state where the protection is stopped but data is retained forever.</span></span>

### <span data-ttu-id="0e88c-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="0e88c-114">Example 2</span></span>

<span data-ttu-id="0e88c-115">Rehydrates um item excluído de uma tela.</span><span class="sxs-lookup"><span data-stu-id="0e88c-115">Rehydrates a soft-deleted Item.</span></span> <span data-ttu-id="0e88c-116">(gerado automaticamente)</span><span class="sxs-lookup"><span data-stu-id="0e88c-116">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Undo-AzRecoveryServicesBackupItemDeletion -Item $PI[0] -VaultId $vault.ID
```

## <span data-ttu-id="0e88c-117">OS</span><span class="sxs-lookup"><span data-stu-id="0e88c-117">PARAMETERS</span></span>

### <span data-ttu-id="0e88c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e88c-118">-DefaultProfile</span></span>
<span data-ttu-id="0e88c-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0e88c-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0e88c-120">-Force</span><span class="sxs-lookup"><span data-stu-id="0e88c-120">-Force</span></span>
<span data-ttu-id="0e88c-121">Force desabilita a proteção de backup (impede a caixa de diálogo de confirmação).</span><span class="sxs-lookup"><span data-stu-id="0e88c-121">Force disables backup protection (prevents confirmation dialog).</span></span>
<span data-ttu-id="0e88c-122">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="0e88c-122">This parameter is optional.</span></span>

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

### <span data-ttu-id="0e88c-123">-Item</span><span class="sxs-lookup"><span data-stu-id="0e88c-123">-Item</span></span>
<span data-ttu-id="0e88c-124">Especifica o item de backup para o qual esse cmdlet reverte a exclusão.</span><span class="sxs-lookup"><span data-stu-id="0e88c-124">Specifies the backup item for which this cmdlet reverts the deletion.</span></span>
<span data-ttu-id="0e88c-125">Para obter um AzureRmRecoveryServicesBackupItem, use o cmdlet Get-AzRecoveryServicesBackupItem.</span><span class="sxs-lookup"><span data-stu-id="0e88c-125">To obtain an AzureRmRecoveryServicesBackupItem , use the Get-AzRecoveryServicesBackupItem cmdlet.</span></span>

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

### <span data-ttu-id="0e88c-126">-Cofreid</span><span class="sxs-lookup"><span data-stu-id="0e88c-126">-VaultId</span></span>
<span data-ttu-id="0e88c-127">ID do braço do cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="0e88c-127">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="0e88c-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="0e88c-128">-Confirm</span></span>
<span data-ttu-id="0e88c-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0e88c-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0e88c-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0e88c-130">-WhatIf</span></span>
<span data-ttu-id="0e88c-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="0e88c-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0e88c-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0e88c-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0e88c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e88c-133">CommonParameters</span></span>
<span data-ttu-id="0e88c-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0e88c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e88c-135">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0e88c-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e88c-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0e88c-136">INPUTS</span></span>

### <span data-ttu-id="0e88c-137">Microsoft. Azure. Commands. Recoveryservices. backup. cmdlets. Models. dobase</span><span class="sxs-lookup"><span data-stu-id="0e88c-137">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

### <span data-ttu-id="0e88c-138">System. String</span><span class="sxs-lookup"><span data-stu-id="0e88c-138">System.String</span></span>

## <span data-ttu-id="0e88c-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0e88c-139">OUTPUTS</span></span>

### <span data-ttu-id="0e88c-140">Microsoft. Azure. Commands. Recoveryservices. backup. cmdlets. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="0e88c-140">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="0e88c-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0e88c-141">NOTES</span></span>

## <span data-ttu-id="0e88c-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0e88c-142">RELATED LINKS</span></span>

[<span data-ttu-id="0e88c-143">Get-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="0e88c-143">Get-AzRecoveryServicesBackupContainer</span></span>]()

[<span data-ttu-id="0e88c-144">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="0e88c-144">Get-AzRecoveryServicesBackupItem</span></span>]()

