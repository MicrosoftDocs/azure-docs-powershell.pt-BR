---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: ECD3F05A-9350-407E-8B48-67443547652F
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/disable-azrecoveryservicesbackupprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Disable-AzRecoveryServicesBackupProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Disable-AzRecoveryServicesBackupProtection.md
ms.openlocfilehash: bb0f3b18697b3f9e17b8e1744361346e68c47357
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886417"
---
# <span data-ttu-id="ecd9f-101">Disable-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="ecd9f-101">Disable-AzRecoveryServicesBackupProtection</span></span>

## <span data-ttu-id="ecd9f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ecd9f-102">SYNOPSIS</span></span>
<span data-ttu-id="ecd9f-103">Desabilita a proteção para um item protegido por backup.</span><span class="sxs-lookup"><span data-stu-id="ecd9f-103">Disables protection for a Backup-protected item.</span></span>

## <span data-ttu-id="ecd9f-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="ecd9f-104">SYNTAX</span></span>

```
Disable-AzRecoveryServicesBackupProtection [-Item] <ItemBase> [-RemoveRecoveryPoints] [-Force]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ecd9f-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="ecd9f-105">DESCRIPTION</span></span>
<span data-ttu-id="ecd9f-106">O cmdlet **Disable-AzRecoveryServicesBackupProtection** desabilita a proteção para um item protegido por backup do Azure.</span><span class="sxs-lookup"><span data-stu-id="ecd9f-106">The **Disable-AzRecoveryServicesBackupProtection** cmdlet disables protection for an Azure Backup-protected item.</span></span>
<span data-ttu-id="ecd9f-107">Este cmdlet interrompe o backup agendado regular de um item.</span><span class="sxs-lookup"><span data-stu-id="ecd9f-107">This cmdlet stops regular scheduled backup of an item.</span></span>
<span data-ttu-id="ecd9f-108">Esse cmdlet também pode excluir pontos de recuperação existentes para o item de backup se for executado com o parâmetro RemoveRecoveryPoints.</span><span class="sxs-lookup"><span data-stu-id="ecd9f-108">This cmdlet can also delete existing recovery points for the backup item if executed with RemoveRecoveryPoints parameter.</span></span>
<span data-ttu-id="ecd9f-109">De definir o contexto do cofre usando o cmdlet Set-AzRecoveryServicesVaultContext antes de usar o cmdlet atual.</span><span class="sxs-lookup"><span data-stu-id="ecd9f-109">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="ecd9f-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ecd9f-110">EXAMPLES</span></span>

### <span data-ttu-id="ecd9f-111">Exemplo 1: Desabilitar a proteção de backup</span><span class="sxs-lookup"><span data-stu-id="ecd9f-111">Example 1: Disable Backup protection</span></span>
```powershell
PS C:\> $Cont = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered 
PS C:\> $PI = Get-AzRecoveryServicesBackupItem -Container $Cont[0] -WorkloadType AzureVM 
PS C:\> Disable-AzRecoveryServicesBackupProtection -Item $PI[0]
```

<span data-ttu-id="ecd9f-112">O primeiro comando obtém uma matriz de contêineres de backup e, em seguida, armazena-o na matriz $Cont.</span><span class="sxs-lookup"><span data-stu-id="ecd9f-112">The first command gets an array of backup containers, and then stores it in the $Cont array.</span></span>
<span data-ttu-id="ecd9f-113">O segundo comando obtém o item backup correspondente ao primeiro item de contêiner e o armazena na variável $PI.</span><span class="sxs-lookup"><span data-stu-id="ecd9f-113">The second command gets the Backup item corresponding to the first container item, and then stores it in the $PI variable.</span></span>
<span data-ttu-id="ecd9f-114">O último comando desabilita a proteção de backup para o item $PI \[ 0 \] , mas mantém os dados.</span><span class="sxs-lookup"><span data-stu-id="ecd9f-114">The last command disables Backup protection for the item in $PI\[0\], but retains the data.</span></span>

### <span data-ttu-id="ecd9f-115">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="ecd9f-115">Example 2</span></span>

<span data-ttu-id="ecd9f-116">Desabilita a proteção para um item protegido por backup.</span><span class="sxs-lookup"><span data-stu-id="ecd9f-116">Disables protection for a Backup-protected item.</span></span> <span data-ttu-id="ecd9f-117">(gerado automaticamente)</span><span class="sxs-lookup"><span data-stu-id="ecd9f-117">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Disable-AzRecoveryServicesBackupProtection -Item $PI[0] -RemoveRecoveryPoints -VaultId $vault.ID
```

## <span data-ttu-id="ecd9f-118">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="ecd9f-118">PARAMETERS</span></span>

### <span data-ttu-id="ecd9f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ecd9f-119">-DefaultProfile</span></span>
<span data-ttu-id="ecd9f-120">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="ecd9f-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ecd9f-121">-Force</span><span class="sxs-lookup"><span data-stu-id="ecd9f-121">-Force</span></span>
<span data-ttu-id="ecd9f-122">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="ecd9f-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ecd9f-123">-Item</span><span class="sxs-lookup"><span data-stu-id="ecd9f-123">-Item</span></span>
<span data-ttu-id="ecd9f-124">Especifica o item Backup para o qual este cmdlet desabilita a proteção.</span><span class="sxs-lookup"><span data-stu-id="ecd9f-124">Specifies the Backup item for which this cmdlet disables protection.</span></span>
<span data-ttu-id="ecd9f-125">Para obter um **AzureRmRecoveryServicesBackupItem,** use Get-AzRecoveryServicesBackupItem cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ecd9f-125">To obtain an **AzureRmRecoveryServicesBackupItem**, use the Get-AzRecoveryServicesBackupItem cmdlet.</span></span>

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

### <span data-ttu-id="ecd9f-126">-RemoveRecoveryPoints</span><span class="sxs-lookup"><span data-stu-id="ecd9f-126">-RemoveRecoveryPoints</span></span>
<span data-ttu-id="ecd9f-127">Indica que esse cmdlet exclui pontos de recuperação existentes.</span><span class="sxs-lookup"><span data-stu-id="ecd9f-127">Indicates that this cmdlet deletes existing recovery points.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ecd9f-128">-VaultId</span><span class="sxs-lookup"><span data-stu-id="ecd9f-128">-VaultId</span></span>
<span data-ttu-id="ecd9f-129">ARM ID do Cofre de Serviços de Recuperação.</span><span class="sxs-lookup"><span data-stu-id="ecd9f-129">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="ecd9f-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ecd9f-130">-Confirm</span></span>
<span data-ttu-id="ecd9f-131">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ecd9f-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ecd9f-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ecd9f-132">-WhatIf</span></span>
<span data-ttu-id="ecd9f-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ecd9f-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ecd9f-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ecd9f-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ecd9f-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ecd9f-135">CommonParameters</span></span>
<span data-ttu-id="ecd9f-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ecd9f-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ecd9f-137">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ecd9f-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ecd9f-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ecd9f-138">INPUTS</span></span>

### <span data-ttu-id="ecd9f-139">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span><span class="sxs-lookup"><span data-stu-id="ecd9f-139">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

### <span data-ttu-id="ecd9f-140">System.String</span><span class="sxs-lookup"><span data-stu-id="ecd9f-140">System.String</span></span>

## <span data-ttu-id="ecd9f-141">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="ecd9f-141">OUTPUTS</span></span>

### <span data-ttu-id="ecd9f-142">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span><span class="sxs-lookup"><span data-stu-id="ecd9f-142">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="ecd9f-143">NOTES</span><span class="sxs-lookup"><span data-stu-id="ecd9f-143">NOTES</span></span>

## <span data-ttu-id="ecd9f-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ecd9f-144">RELATED LINKS</span></span>

[<span data-ttu-id="ecd9f-145">Enable-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="ecd9f-145">Enable-AzRecoveryServicesBackupProtection</span></span>](./Enable-AzRecoveryServicesBackupProtection.md)

[<span data-ttu-id="ecd9f-146">Get-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="ecd9f-146">Get-AzRecoveryServicesBackupContainer</span></span>](./Get-AzRecoveryServicesBackupContainer.md)

[<span data-ttu-id="ecd9f-147">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="ecd9f-147">Get-AzRecoveryServicesBackupItem</span></span>](./Get-AzRecoveryServicesBackupItem.md)


