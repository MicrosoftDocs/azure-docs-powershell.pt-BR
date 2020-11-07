---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/undo-azrecoveryservicesbackupitemdeletion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Undo-AzRecoveryServicesBackupItemDeletion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Undo-AzRecoveryServicesBackupItemDeletion.md
ms.openlocfilehash: 36b93041a2dfa4ba64779b2a92aeee50da53ce44
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93773434"
---
# <span data-ttu-id="1ba53-101">Undo-AzRecoveryServicesBackupItemDeletion</span><span class="sxs-lookup"><span data-stu-id="1ba53-101">Undo-AzRecoveryServicesBackupItemDeletion</span></span>

## <span data-ttu-id="1ba53-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1ba53-102">SYNOPSIS</span></span>
<span data-ttu-id="1ba53-103">Rehydrates um item excluído de uma tela</span><span class="sxs-lookup"><span data-stu-id="1ba53-103">Rehydrates a soft-deleted Item</span></span>

## <span data-ttu-id="1ba53-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1ba53-104">SYNTAX</span></span>

```
Undo-AzRecoveryServicesBackupItemDeletion [-Item] <ItemBase> [-Force] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1ba53-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1ba53-105">DESCRIPTION</span></span>
<span data-ttu-id="1ba53-106">O cmdlet Undo-AzRecoveryServicesBackupItemDeletion rehydrates um item excluído de uma mídia.</span><span class="sxs-lookup"><span data-stu-id="1ba53-106">The Undo-AzRecoveryServicesBackupItemDeletion cmdlet rehydrates a soft-deleted item.</span></span>
<span data-ttu-id="1ba53-107">Defina o contexto do cofre usando o cmdlet Set-AzRecoveryServicesVaultContext antes de usar o cmdlet atual.</span><span class="sxs-lookup"><span data-stu-id="1ba53-107">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="1ba53-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1ba53-108">EXAMPLES</span></span>

### <span data-ttu-id="1ba53-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="1ba53-109">Example 1</span></span>
```powershell
PS C:\> $Cont = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVM
PS C:\> $PI = Get-AzRecoveryServicesBackupItem -Container $Cont[0] -WorkloadType AzureVM 
PS C:\> Disable-AzRecoveryServicesBackupProtection -Item $PI[0] -RemoveRecoveryPoints
PS C:\> $PI = Get-AzRecoveryServicesBackupItem -Container $Cont[0] -WorkloadType AzureVM 
PS C:\> Undo-AzRecoveryServicesBackupItemDeletion -Item $PI[0]
```

<span data-ttu-id="1ba53-110">O primeiro comando obtém uma matriz de contêineres de backup e, em seguida, armazena-o na matriz $Cont.</span><span class="sxs-lookup"><span data-stu-id="1ba53-110">The first command gets an array of backup containers, and then stores it in the $Cont array.</span></span>
<span data-ttu-id="1ba53-111">O segundo comando obtém o item de backup correspondente ao primeiro item de contêiner e, em seguida, armazena-o na variável $PI.</span><span class="sxs-lookup"><span data-stu-id="1ba53-111">The second command gets the Backup item corresponding to the first container item, and then stores it in the $PI variable.</span></span>
<span data-ttu-id="1ba53-112">O terceiro comando desabilita a proteção de backup para o item em $PI \[ 0 \] e coloca o item em um estado SoftDeleted.</span><span class="sxs-lookup"><span data-stu-id="1ba53-112">The third command disables Backup protection for the item in $PI\[0\] and puts the item in a softdeleted state.</span></span>
<span data-ttu-id="1ba53-113">O quarto comando o novo item que está em um estado SoftDeleted.</span><span class="sxs-lookup"><span data-stu-id="1ba53-113">The fourth command the new item which is in a softdeleted state.</span></span>
<span data-ttu-id="1ba53-114">O último comando rehydrates a VM SoftDeleted.</span><span class="sxs-lookup"><span data-stu-id="1ba53-114">The last command rehydrates the softdeleted VM.</span></span>


## <span data-ttu-id="1ba53-115">OS</span><span class="sxs-lookup"><span data-stu-id="1ba53-115">PARAMETERS</span></span>

### <span data-ttu-id="1ba53-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ba53-116">-DefaultProfile</span></span>
<span data-ttu-id="1ba53-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1ba53-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1ba53-118">-Force</span><span class="sxs-lookup"><span data-stu-id="1ba53-118">-Force</span></span>
<span data-ttu-id="1ba53-119">Force desabilita a proteção de backup (impede a caixa de diálogo de confirmação).</span><span class="sxs-lookup"><span data-stu-id="1ba53-119">Force disables backup protection (prevents confirmation dialog).</span></span>
<span data-ttu-id="1ba53-120">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="1ba53-120">This parameter is optional.</span></span>

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

### <span data-ttu-id="1ba53-121">-Item</span><span class="sxs-lookup"><span data-stu-id="1ba53-121">-Item</span></span>
<span data-ttu-id="1ba53-122">Especifica o item de backup para o qual esse cmdlet desabilita a proteção.</span><span class="sxs-lookup"><span data-stu-id="1ba53-122">Specifies the Backup item for which this cmdlet disables protection.</span></span>
<span data-ttu-id="1ba53-123">Para obter um AzureRmRecoveryServicesBackupItem, use o cmdlet Get-AzRecoveryServicesBackupItem.</span><span class="sxs-lookup"><span data-stu-id="1ba53-123">To obtain an AzureRmRecoveryServicesBackupItem , use the Get-AzRecoveryServicesBackupItem cmdlet.</span></span>

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

### <span data-ttu-id="1ba53-124">-Cofreid</span><span class="sxs-lookup"><span data-stu-id="1ba53-124">-VaultId</span></span>
<span data-ttu-id="1ba53-125">ID do braço do cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="1ba53-125">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="1ba53-126">-Confirme</span><span class="sxs-lookup"><span data-stu-id="1ba53-126">-Confirm</span></span>
<span data-ttu-id="1ba53-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1ba53-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1ba53-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1ba53-128">-WhatIf</span></span>
<span data-ttu-id="1ba53-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="1ba53-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1ba53-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1ba53-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1ba53-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ba53-131">CommonParameters</span></span>
<span data-ttu-id="1ba53-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ba53-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ba53-133">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1ba53-133">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ba53-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1ba53-134">INPUTS</span></span>

### <span data-ttu-id="1ba53-135">Microsoft. Azure. Commands. Recoveryservices. backup. cmdlets. Models. dobase</span><span class="sxs-lookup"><span data-stu-id="1ba53-135">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

### <span data-ttu-id="1ba53-136">System. String</span><span class="sxs-lookup"><span data-stu-id="1ba53-136">System.String</span></span>

## <span data-ttu-id="1ba53-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1ba53-137">OUTPUTS</span></span>

### <span data-ttu-id="1ba53-138">Microsoft. Azure. Commands. Recoveryservices. backup. cmdlets. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="1ba53-138">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="1ba53-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1ba53-139">NOTES</span></span>

## <span data-ttu-id="1ba53-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1ba53-140">RELATED LINKS</span></span>

[<span data-ttu-id="1ba53-141">Get-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="1ba53-141">Get-AzRecoveryServicesBackupContainer</span></span>]()

[<span data-ttu-id="1ba53-142">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="1ba53-142">Get-AzRecoveryServicesBackupItem</span></span>]()

