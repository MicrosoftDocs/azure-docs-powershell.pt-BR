---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: ECD3F05A-9350-407E-8B48-67443547652F
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/disable-azrecoveryservicesbackupprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Disable-AzRecoveryServicesBackupProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Disable-AzRecoveryServicesBackupProtection.md
ms.openlocfilehash: 9dc42a137d3abcd23a64e096117be8d287571ecf
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98428069"
---
# <span data-ttu-id="aba79-101">Disable-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="aba79-101">Disable-AzRecoveryServicesBackupProtection</span></span>

## <span data-ttu-id="aba79-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="aba79-102">SYNOPSIS</span></span>
<span data-ttu-id="aba79-103">Desabilita a proteção para um item protegido por backup.</span><span class="sxs-lookup"><span data-stu-id="aba79-103">Disables protection for a Backup-protected item.</span></span>

## <span data-ttu-id="aba79-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="aba79-104">SYNTAX</span></span>

```
Disable-AzRecoveryServicesBackupProtection [-Item] <ItemBase> [-RemoveRecoveryPoints] [-Force]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aba79-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="aba79-105">DESCRIPTION</span></span>
<span data-ttu-id="aba79-106">O cmdlet **Disable-AzRecoveryServicesBackupProtection** desabilita a proteção para um item do Azure protegido pelo backup.</span><span class="sxs-lookup"><span data-stu-id="aba79-106">The **Disable-AzRecoveryServicesBackupProtection** cmdlet disables protection for an Azure Backup-protected item.</span></span>
<span data-ttu-id="aba79-107">Esse cmdlet para o backup agendado regular de um item.</span><span class="sxs-lookup"><span data-stu-id="aba79-107">This cmdlet stops regular scheduled backup of an item.</span></span>
<span data-ttu-id="aba79-108">Esse cmdlet também pode excluir pontos de recuperação existentes para o item de backup, se for executado com o parâmetro RemoveRecoveryPoints.</span><span class="sxs-lookup"><span data-stu-id="aba79-108">This cmdlet can also delete existing recovery points for the backup item if executed with RemoveRecoveryPoints parameter.</span></span>
<span data-ttu-id="aba79-109">Defina o contexto do cofre usando o cmdlet Set-AzRecoveryServicesVaultContext antes de usar o cmdlet atual.</span><span class="sxs-lookup"><span data-stu-id="aba79-109">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="aba79-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="aba79-110">EXAMPLES</span></span>

### <span data-ttu-id="aba79-111">Exemplo 1: desabilitar a proteção de backup</span><span class="sxs-lookup"><span data-stu-id="aba79-111">Example 1: Disable Backup protection</span></span>
```powershell
PS C:\> $Cont = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered 
PS C:\> $PI = Get-AzRecoveryServicesBackupItem -Container $Cont[0] -WorkloadType AzureVM 
PS C:\> Disable-AzRecoveryServicesBackupProtection -Item $PI[0]
```

<span data-ttu-id="aba79-112">O primeiro comando obtém uma matriz de contêineres de backup e, em seguida, armazena-o na matriz $Cont.</span><span class="sxs-lookup"><span data-stu-id="aba79-112">The first command gets an array of backup containers, and then stores it in the $Cont array.</span></span>
<span data-ttu-id="aba79-113">O segundo comando obtém o item de backup correspondente ao primeiro item de contêiner e, em seguida, armazena-o na variável $PI.</span><span class="sxs-lookup"><span data-stu-id="aba79-113">The second command gets the Backup item corresponding to the first container item, and then stores it in the $PI variable.</span></span>
<span data-ttu-id="aba79-114">O último comando desabilita a proteção de backup para o item no $PI \[ 0 \] , mas mantém os dados.</span><span class="sxs-lookup"><span data-stu-id="aba79-114">The last command disables Backup protection for the item in $PI\[0\], but retains the data.</span></span>

### <span data-ttu-id="aba79-115">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="aba79-115">Example 2</span></span>

<span data-ttu-id="aba79-116">Desabilita a proteção para um item protegido por backup.</span><span class="sxs-lookup"><span data-stu-id="aba79-116">Disables protection for a Backup-protected item.</span></span> <span data-ttu-id="aba79-117">(gerado automaticamente)</span><span class="sxs-lookup"><span data-stu-id="aba79-117">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Disable-AzRecoveryServicesBackupProtection -Item $PI[0] -RemoveRecoveryPoints -VaultId $vault.ID
```

## <span data-ttu-id="aba79-118">OS</span><span class="sxs-lookup"><span data-stu-id="aba79-118">PARAMETERS</span></span>

### <span data-ttu-id="aba79-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aba79-119">-DefaultProfile</span></span>
<span data-ttu-id="aba79-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="aba79-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aba79-121">-Force</span><span class="sxs-lookup"><span data-stu-id="aba79-121">-Force</span></span>
<span data-ttu-id="aba79-122">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="aba79-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="aba79-123">-Item</span><span class="sxs-lookup"><span data-stu-id="aba79-123">-Item</span></span>
<span data-ttu-id="aba79-124">Especifica o item de backup para o qual esse cmdlet desabilita a proteção.</span><span class="sxs-lookup"><span data-stu-id="aba79-124">Specifies the Backup item for which this cmdlet disables protection.</span></span>
<span data-ttu-id="aba79-125">Para obter um **AzureRmRecoveryServicesBackupItem**, use o cmdlet Get-AzRecoveryServicesBackupItem.</span><span class="sxs-lookup"><span data-stu-id="aba79-125">To obtain an **AzureRmRecoveryServicesBackupItem**, use the Get-AzRecoveryServicesBackupItem cmdlet.</span></span>

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

### <span data-ttu-id="aba79-126">-RemoveRecoveryPoints</span><span class="sxs-lookup"><span data-stu-id="aba79-126">-RemoveRecoveryPoints</span></span>
<span data-ttu-id="aba79-127">Indica que esse cmdlet exclui pontos de recuperação existentes.</span><span class="sxs-lookup"><span data-stu-id="aba79-127">Indicates that this cmdlet deletes existing recovery points.</span></span>

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

### <span data-ttu-id="aba79-128">-Cofreid</span><span class="sxs-lookup"><span data-stu-id="aba79-128">-VaultId</span></span>
<span data-ttu-id="aba79-129">ID do braço do cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="aba79-129">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="aba79-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="aba79-130">-Confirm</span></span>
<span data-ttu-id="aba79-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aba79-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aba79-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aba79-132">-WhatIf</span></span>
<span data-ttu-id="aba79-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="aba79-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aba79-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="aba79-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aba79-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aba79-135">CommonParameters</span></span>
<span data-ttu-id="aba79-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aba79-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aba79-137">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="aba79-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aba79-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="aba79-138">INPUTS</span></span>

### <span data-ttu-id="aba79-139">Microsoft. Azure. Commands. Recoveryservices. backup. cmdlets. Models. dobase</span><span class="sxs-lookup"><span data-stu-id="aba79-139">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

### <span data-ttu-id="aba79-140">System. String</span><span class="sxs-lookup"><span data-stu-id="aba79-140">System.String</span></span>

## <span data-ttu-id="aba79-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="aba79-141">OUTPUTS</span></span>

### <span data-ttu-id="aba79-142">Microsoft. Azure. Commands. Recoveryservices. backup. cmdlets. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="aba79-142">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="aba79-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="aba79-143">NOTES</span></span>

## <span data-ttu-id="aba79-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="aba79-144">RELATED LINKS</span></span>

[<span data-ttu-id="aba79-145">Enable-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="aba79-145">Enable-AzRecoveryServicesBackupProtection</span></span>](./Enable-AzRecoveryServicesBackupProtection.md)

[<span data-ttu-id="aba79-146">Get-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="aba79-146">Get-AzRecoveryServicesBackupContainer</span></span>](./Get-AzRecoveryServicesBackupContainer.md)

[<span data-ttu-id="aba79-147">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="aba79-147">Get-AzRecoveryServicesBackupItem</span></span>](./Get-AzRecoveryServicesBackupItem.md)


