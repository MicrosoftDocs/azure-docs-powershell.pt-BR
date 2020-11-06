---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: 44622461-E567-4A0A-8F18-2D7B1BF86DA2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/enable-azurermrecoveryservicesbackupprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Enable-AzureRmRecoveryServicesBackupProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Enable-AzureRmRecoveryServicesBackupProtection.md
ms.openlocfilehash: efe4392fd57c5cb0beb6731fefb83878001b489b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427507"
---
# <span data-ttu-id="1a60b-101">Enable-AzureRmRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="1a60b-101">Enable-AzureRmRecoveryServicesBackupProtection</span></span>

## <span data-ttu-id="1a60b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1a60b-102">SYNOPSIS</span></span>
<span data-ttu-id="1a60b-103">Habilita o backup para um item com uma política de proteção de backup especificada.</span><span class="sxs-lookup"><span data-stu-id="1a60b-103">Enables backup for an item with a specified Backup protection policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1a60b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1a60b-104">SYNTAX</span></span>

### <span data-ttu-id="1a60b-105">AzureVMComputeEnableProtection (padrão)</span><span class="sxs-lookup"><span data-stu-id="1a60b-105">AzureVMComputeEnableProtection (Default)</span></span>
```
Enable-AzureRmRecoveryServicesBackupProtection [-Policy] <PolicyBase> [-Name] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1a60b-106">AzureVMClassicComputeEnableProtection</span><span class="sxs-lookup"><span data-stu-id="1a60b-106">AzureVMClassicComputeEnableProtection</span></span>
```
Enable-AzureRmRecoveryServicesBackupProtection [-Policy] <PolicyBase> [-Name] <String> [-ServiceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1a60b-107">ModifyProtection</span><span class="sxs-lookup"><span data-stu-id="1a60b-107">ModifyProtection</span></span>
```
Enable-AzureRmRecoveryServicesBackupProtection [-Policy] <PolicyBase> [-Item] <ItemBase>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1a60b-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1a60b-108">DESCRIPTION</span></span>
<span data-ttu-id="1a60b-109">O cmdlet **Enable-AzureRmRecoveryServicesBackupProtection** define a política de proteção de backup do Azure em um item.</span><span class="sxs-lookup"><span data-stu-id="1a60b-109">The **Enable-AzureRmRecoveryServicesBackupProtection** cmdlet sets Azure Backup protection policy on an item.</span></span>

<span data-ttu-id="1a60b-110">Defina o contexto do cofre usando o cmdlet Set-AzureRmRecoveryServicesVaultContext antes de usar o cmdlet atual.</span><span class="sxs-lookup"><span data-stu-id="1a60b-110">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="1a60b-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1a60b-111">EXAMPLES</span></span>

### <span data-ttu-id="1a60b-112">Exemplo 1: habilitar a proteção de backup para um item</span><span class="sxs-lookup"><span data-stu-id="1a60b-112">Example 1: Enable Backup protection for an item</span></span>
```
PS C:\> $Pol = Get-AzureRmRecoveryServicesBackupProtectionPolicy -Name "DefaultPolicy"
PS C:\> Enable-AzureRmRecoveryServicesBackupProtection -Policy $Pol -Name "V2VM" -ResourceGroupName "RGName1"
WorkloadName    Operation        Status          StartTime                  EndTime
------------    ---------        ------          ---------                  -------
co03-vm         ConfigureBackup  Completed       11-Apr-16 12:19:49 PM      11-Apr-16 12:19:54 PM
```

<span data-ttu-id="1a60b-113">O primeiro cmdlet obtém um objeto de política padrão e, em seguida, armazena-o na variável $Pol.</span><span class="sxs-lookup"><span data-stu-id="1a60b-113">The first cmdlet gets a default policy object, and then stores it in the $Pol variable.</span></span>

<span data-ttu-id="1a60b-114">O segundo cmdlet define a política de proteção de backup para a máquina virtual ARM chamada V2VM usando a política em $Pol.</span><span class="sxs-lookup"><span data-stu-id="1a60b-114">The second cmdlet sets the Backup protection policy for the ARM virtual machine named V2VM using the policy in $Pol.</span></span>

## <span data-ttu-id="1a60b-115">OS</span><span class="sxs-lookup"><span data-stu-id="1a60b-115">PARAMETERS</span></span>

### <span data-ttu-id="1a60b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a60b-116">-DefaultProfile</span></span>
<span data-ttu-id="1a60b-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1a60b-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1a60b-118">-Item</span><span class="sxs-lookup"><span data-stu-id="1a60b-118">-Item</span></span>
<span data-ttu-id="1a60b-119">Especifica o item de backup para o qual esse cmdlet habilita a proteção.</span><span class="sxs-lookup"><span data-stu-id="1a60b-119">Specifies the Backup item for which this cmdlet enables protection.</span></span>
<span data-ttu-id="1a60b-120">Para obter um **AzureRmRecoveryServicesBackupItem** , use o cmdlet Get-AzureRmRecoveryServicesBackupItem.</span><span class="sxs-lookup"><span data-stu-id="1a60b-120">To obtain an **AzureRmRecoveryServicesBackupItem** , use the Get-AzureRmRecoveryServicesBackupItem cmdlet.</span></span>

```yaml
Type: ItemBase
Parameter Sets: ModifyProtection
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1a60b-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="1a60b-121">-Name</span></span>
<span data-ttu-id="1a60b-122">Especifica o nome do item de backup.</span><span class="sxs-lookup"><span data-stu-id="1a60b-122">Specifies the name of the Backup item.</span></span>

```yaml
Type: String
Parameter Sets: AzureVMComputeEnableProtection, AzureVMClassicComputeEnableProtection
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a60b-123">-Política</span><span class="sxs-lookup"><span data-stu-id="1a60b-123">-Policy</span></span>
<span data-ttu-id="1a60b-124">Especifica a política de proteção que este cmdlet associa a um item.</span><span class="sxs-lookup"><span data-stu-id="1a60b-124">Specifies protection policy that this cmdlet associates with an item.</span></span>
<span data-ttu-id="1a60b-125">Para obter um objeto **AzureRmRecoveryServicesBackupProtectionPolicy** , use o cmdlet Get-AzureRmRecoveryServicesBackupProtectionPolicy.</span><span class="sxs-lookup"><span data-stu-id="1a60b-125">To obtain an **AzureRmRecoveryServicesBackupProtectionPolicy** object, use the Get-AzureRmRecoveryServicesBackupProtectionPolicy cmdlet.</span></span>

```yaml
Type: PolicyBase
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a60b-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1a60b-126">-ResourceGroupName</span></span>
<span data-ttu-id="1a60b-127">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="1a60b-127">Specifies the name of the resource group.</span></span>
<span data-ttu-id="1a60b-128">Especifique esse parâmetro somente para máquinas virtuais ARM.</span><span class="sxs-lookup"><span data-stu-id="1a60b-128">Specify this parameter only for ARM virtual machines.</span></span>

```yaml
Type: String
Parameter Sets: AzureVMComputeEnableProtection
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a60b-129">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="1a60b-129">-ServiceName</span></span>
<span data-ttu-id="1a60b-130">Especifica o nome do serviço.</span><span class="sxs-lookup"><span data-stu-id="1a60b-130">Specifies the service name.</span></span>
<span data-ttu-id="1a60b-131">Especifique esse parâmetro somente para máquinas virtuais ASM.</span><span class="sxs-lookup"><span data-stu-id="1a60b-131">Specify this parameter only for ASM virtual machines.</span></span>

```yaml
Type: String
Parameter Sets: AzureVMClassicComputeEnableProtection
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a60b-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="1a60b-132">-Confirm</span></span>
<span data-ttu-id="1a60b-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1a60b-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a60b-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1a60b-134">-WhatIf</span></span>
<span data-ttu-id="1a60b-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="1a60b-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1a60b-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1a60b-136">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a60b-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a60b-137">CommonParameters</span></span>
<span data-ttu-id="1a60b-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1a60b-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a60b-139">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1a60b-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a60b-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1a60b-140">INPUTS</span></span>

### <span data-ttu-id="1a60b-141">Dobase</span><span class="sxs-lookup"><span data-stu-id="1a60b-141">ItemBase</span></span>
<span data-ttu-id="1a60b-142">O parâmetro ' item ' aceita o valor do tipo ' database ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="1a60b-142">Parameter 'Item' accepts value of type 'ItemBase' from the pipeline</span></span>

## <span data-ttu-id="1a60b-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1a60b-143">OUTPUTS</span></span>

### <span data-ttu-id="1a60b-144">Microsoft. Azure. Commands. Recoveryservices. backup. cmdlets. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="1a60b-144">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="1a60b-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1a60b-145">NOTES</span></span>

## <span data-ttu-id="1a60b-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1a60b-146">RELATED LINKS</span></span>

[<span data-ttu-id="1a60b-147">Disable-AzureRmRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="1a60b-147">Disable-AzureRmRecoveryServicesBackupProtection</span></span>](./Disable-AzureRmRecoveryServicesBackupProtection.md)

[<span data-ttu-id="1a60b-148">Get-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="1a60b-148">Get-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzureRmRecoveryServicesBackupProtectionPolicy.md)


