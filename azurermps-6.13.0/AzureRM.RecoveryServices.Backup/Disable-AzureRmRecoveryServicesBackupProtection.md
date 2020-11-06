---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: ECD3F05A-9350-407E-8B48-67443547652F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/disable-azurermrecoveryservicesbackupprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Disable-AzureRmRecoveryServicesBackupProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Disable-AzureRmRecoveryServicesBackupProtection.md
ms.openlocfilehash: 07406378df0439171c5be2e7558e8ac33cb32687
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602460"
---
# <span data-ttu-id="49575-101">Disable-AzureRmRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="49575-101">Disable-AzureRmRecoveryServicesBackupProtection</span></span>

## <span data-ttu-id="49575-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="49575-102">SYNOPSIS</span></span>
<span data-ttu-id="49575-103">Desabilita a proteção para um item protegido por backup.</span><span class="sxs-lookup"><span data-stu-id="49575-103">Disables protection for a Backup-protected item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="49575-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="49575-104">SYNTAX</span></span>

```
Disable-AzureRmRecoveryServicesBackupProtection [-Item] <ItemBase> [-RemoveRecoveryPoints] [-Force]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="49575-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="49575-105">DESCRIPTION</span></span>
<span data-ttu-id="49575-106">O cmdlet **Disable-AzureRmRecoveryServicesBackupProtection** desabilita a proteção para um item do Azure protegido pelo backup.</span><span class="sxs-lookup"><span data-stu-id="49575-106">The **Disable-AzureRmRecoveryServicesBackupProtection** cmdlet disables protection for an Azure Backup-protected item.</span></span>
<span data-ttu-id="49575-107">Esse cmdlet para o backup agendado regular de um item.</span><span class="sxs-lookup"><span data-stu-id="49575-107">This cmdlet stops regular scheduled backup of an item.</span></span>
<span data-ttu-id="49575-108">Esse cmdlet também pode excluir pontos de recuperação existentes para o item de backup.</span><span class="sxs-lookup"><span data-stu-id="49575-108">This cmdlet can also delete existing recovery points for the backup item.</span></span>
<span data-ttu-id="49575-109">Defina o contexto do cofre usando o cmdlet Set-AzureRmRecoveryServicesVaultContext antes de usar o cmdlet atual.</span><span class="sxs-lookup"><span data-stu-id="49575-109">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="49575-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="49575-110">EXAMPLES</span></span>

### <span data-ttu-id="49575-111">Exemplo 1: desabilitar a proteção de backup</span><span class="sxs-lookup"><span data-stu-id="49575-111">Example 1: Disable Backup protection</span></span>
```
PS C:\> $Cont = Get-AzureRmRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered 
PS C:\> $PI = Get-AzureRmRecoveryServicesBackupItem -Container $Cont[0] -WorkloadType AzureVM 
PS C:\> Disable-AzureRmRecoveryServicesBackupProtection -Item $PI[0]
```

<span data-ttu-id="49575-112">O primeiro comando obtém uma matriz de contêineres de backup e, em seguida, armazena-o na matriz $Cont.</span><span class="sxs-lookup"><span data-stu-id="49575-112">The first command gets an array of backup containers, and then stores it in the $Cont array.</span></span>
<span data-ttu-id="49575-113">O segundo comando obtém o item de backup correspondente ao primeiro item de contêiner e, em seguida, armazena-o na variável $PI.</span><span class="sxs-lookup"><span data-stu-id="49575-113">The second command gets the Backup item corresponding to the first container item, and then stores it in the $PI variable.</span></span>
<span data-ttu-id="49575-114">O último comando desabilita a proteção de backup para o item no $PI \[ 0 \] , mas mantém os dados.</span><span class="sxs-lookup"><span data-stu-id="49575-114">The last command disables Backup protection for the item in $PI\[0\], but retains the data.</span></span>

## <span data-ttu-id="49575-115">OS</span><span class="sxs-lookup"><span data-stu-id="49575-115">PARAMETERS</span></span>

### <span data-ttu-id="49575-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49575-116">-DefaultProfile</span></span>
<span data-ttu-id="49575-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="49575-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="49575-118">-Force</span><span class="sxs-lookup"><span data-stu-id="49575-118">-Force</span></span>
<span data-ttu-id="49575-119">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="49575-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="49575-120">-Item</span><span class="sxs-lookup"><span data-stu-id="49575-120">-Item</span></span>
<span data-ttu-id="49575-121">Especifica o item de backup para o qual esse cmdlet desabilita a proteção.</span><span class="sxs-lookup"><span data-stu-id="49575-121">Specifies the Backup item for which this cmdlet disables protection.</span></span>
<span data-ttu-id="49575-122">Para obter um **AzureRmRecoveryServicesBackupItem** , use o cmdlet Get-AzureRmRecoveryServicesBackupItem.</span><span class="sxs-lookup"><span data-stu-id="49575-122">To obtain an **AzureRmRecoveryServicesBackupItem** , use the Get-AzureRmRecoveryServicesBackupItem cmdlet.</span></span>

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

### <span data-ttu-id="49575-123">-RemoveRecoveryPoints</span><span class="sxs-lookup"><span data-stu-id="49575-123">-RemoveRecoveryPoints</span></span>
<span data-ttu-id="49575-124">Indica que esse cmdlet exclui pontos de recuperação existentes.</span><span class="sxs-lookup"><span data-stu-id="49575-124">Indicates that this cmdlet deletes existing recovery points.</span></span>
<span data-ttu-id="49575-125">Para excluir pontos de recuperação armazenados mais tarde, execute este cmdlet novamente e especifique esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="49575-125">To delete stored recovery points later, run this cmdlet again and specify this parameter.</span></span>

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

### <span data-ttu-id="49575-126">-Cofreid</span><span class="sxs-lookup"><span data-stu-id="49575-126">-VaultId</span></span>
<span data-ttu-id="49575-127">ID do braço do cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="49575-127">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="49575-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="49575-128">-Confirm</span></span>
<span data-ttu-id="49575-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="49575-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="49575-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="49575-130">-WhatIf</span></span>
<span data-ttu-id="49575-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="49575-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="49575-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="49575-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="49575-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49575-133">CommonParameters</span></span>
<span data-ttu-id="49575-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49575-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49575-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="49575-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49575-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="49575-136">INPUTS</span></span>

### <span data-ttu-id="49575-137">Microsoft. Azure. Commands. Recoveryservices. backup. cmdlets. Models. dobase</span><span class="sxs-lookup"><span data-stu-id="49575-137">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>
<span data-ttu-id="49575-138">Parâmetros: Item (ByValue)</span><span class="sxs-lookup"><span data-stu-id="49575-138">Parameters: Item (ByValue)</span></span>

### <span data-ttu-id="49575-139">System. String</span><span class="sxs-lookup"><span data-stu-id="49575-139">System.String</span></span>
<span data-ttu-id="49575-140">Parâmetros: Vaultid (ByValue)</span><span class="sxs-lookup"><span data-stu-id="49575-140">Parameters: VaultId (ByValue)</span></span>

## <span data-ttu-id="49575-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="49575-141">OUTPUTS</span></span>

### <span data-ttu-id="49575-142">Microsoft. Azure. Commands. Recoveryservices. backup. cmdlets. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="49575-142">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="49575-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="49575-143">NOTES</span></span>

## <span data-ttu-id="49575-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="49575-144">RELATED LINKS</span></span>

[<span data-ttu-id="49575-145">Enable-AzureRmRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="49575-145">Enable-AzureRmRecoveryServicesBackupProtection</span></span>](./Enable-AzureRmRecoveryServicesBackupProtection.md)

[<span data-ttu-id="49575-146">Get-AzureRmRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="49575-146">Get-AzureRmRecoveryServicesBackupContainer</span></span>](./Get-AzureRmRecoveryServicesBackupContainer.md)

[<span data-ttu-id="49575-147">Get-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="49575-147">Get-AzureRmRecoveryServicesBackupItem</span></span>](./Get-AzureRmRecoveryServicesBackupItem.md)


