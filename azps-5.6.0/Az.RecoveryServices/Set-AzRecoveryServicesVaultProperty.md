---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: C2A7F37B-5713-4430-B83F-C6745692396D
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/set-azrecoveryservicesvaultproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesVaultProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesVaultProperty.md
ms.openlocfilehash: a88b137b5735984ce6b5f19389d9035b85b1dfe4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891291"
---
# <span data-ttu-id="24cc0-101">Set-AzRecoveryServicesVaultProperty</span><span class="sxs-lookup"><span data-stu-id="24cc0-101">Set-AzRecoveryServicesVaultProperty</span></span>

## <span data-ttu-id="24cc0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="24cc0-102">SYNOPSIS</span></span>
<span data-ttu-id="24cc0-103">Atualiza as propriedades de um Vault.</span><span class="sxs-lookup"><span data-stu-id="24cc0-103">Updates properties of a Vault.</span></span>

## <span data-ttu-id="24cc0-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="24cc0-104">SYNTAX</span></span>

### <span data-ttu-id="24cc0-105">AzureRSVaultSoftDelteParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="24cc0-105">AzureRSVaultSoftDelteParameterSet (Default)</span></span>
```
Set-AzRecoveryServicesVaultProperty -SoftDeleteFeatureState <String> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="24cc0-106">AzureRSVaultCMKParameterSet</span><span class="sxs-lookup"><span data-stu-id="24cc0-106">AzureRSVaultCMKParameterSet</span></span>
```
Set-AzRecoveryServicesVaultProperty -EncryptionKeyId <string> -KeyVaultSubscriptionId <string> [-InfrastructureEncryption] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="24cc0-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="24cc0-107">DESCRIPTION</span></span>
<span data-ttu-id="24cc0-108">O cmdlet **Set-AzRecoveryServicesVaultProperty** atualiza as propriedades de um cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="24cc0-108">The **Set-AzRecoveryServicesVaultProperty** cmdlet updates properties of a Recovery services vault.</span></span> <span data-ttu-id="24cc0-109">Esse cmdlet pode ser usado para habilitar/desabilitar a exclusão suave ou definir a criptografia CMK para um cofre com dois conjuntos de parâmetros diferentes.</span><span class="sxs-lookup"><span data-stu-id="24cc0-109">This cmdlet can be used to enable/disable soft delete or set CMK encryption for a vault with two different parameter sets.</span></span> 
<span data-ttu-id="24cc0-110">**A propriedade SoftDeleteFeatureState** de um cofre só poderá ser desabilitada se não houver contêineres registrados no cofre.</span><span class="sxs-lookup"><span data-stu-id="24cc0-110">**SoftDeleteFeatureState** property of a vault can be disabled only if there are no registered containers in the vault.</span></span> <span data-ttu-id="24cc0-111">InfrastructurEncryption só pode ser definido na primeira vez que um usuário atualiza o cofre CMK.</span><span class="sxs-lookup"><span data-stu-id="24cc0-111">InfrastructurEncryption can only be set the first time a user updates the CMK vault.</span></span>

## <span data-ttu-id="24cc0-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="24cc0-112">EXAMPLES</span></span>

### <span data-ttu-id="24cc0-113">Exemplo 1: Atualizar SoftDeleteFeatureState de um cofre</span><span class="sxs-lookup"><span data-stu-id="24cc0-113">Example 1: Update SoftDeleteFeatureState of a vault</span></span>
```
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "rgName" -Name "vaultName"
PS C:\> $props = Set-AzRecoveryServicesVaultProperty -VaultId $vault.Id -SoftDeleteFeatureState Enable
```

<span data-ttu-id="24cc0-114">O primeiro comando obtém um objeto Vault e o armazena na $vault variável.</span><span class="sxs-lookup"><span data-stu-id="24cc0-114">The first command gets a Vault object and then stores it in the $vault variable.</span></span>
<span data-ttu-id="24cc0-115">O segundo comando atualiza a propriedade SoftDeleteFeatureState do cofre para o estado "Habilitado".</span><span class="sxs-lookup"><span data-stu-id="24cc0-115">The second command Updates the SoftDeleteFeatureState property of the vault to "Enabled" state.</span></span>

### <span data-ttu-id="24cc0-116">Exemplo 2: Atualizar a criptografia CMK de um cofre</span><span class="sxs-lookup"><span data-stu-id="24cc0-116">Example 2: Update CMK encryption of a vault</span></span>

```
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "rgName" -Name "vaultName"
PS C:\> $keyVault = Get-AzKeyVault -VaultName "keyVaultName" -ResourceGroupName "RGName" 
PS C:\> $key = Get-AzKeyVaultKey -VaultName "keyVaultName" -Name "keyName" 
PS C:\> Set-AzRecoveryServicesVaultProperty -EncryptionKeyId $key.ID -KeyVaultSubscriptionId "f870818k-5h28-4t48-8961-37458592348r" -InfrastructureEncryption -VaultId $vault.ID
```

<span data-ttu-id="24cc0-117">O primeiro cmdlet obtém o RSVault para atualizar as propriedades de criptografia.</span><span class="sxs-lookup"><span data-stu-id="24cc0-117">First cmdlet gets the RSVault to update encryption properties.</span></span> <span data-ttu-id="24cc0-118">O segundo cmdlet obtém o cofre de chaves do azure.</span><span class="sxs-lookup"><span data-stu-id="24cc0-118">Second cmdlet gets the azure key vault.</span></span> <span data-ttu-id="24cc0-119">O terceiro cmdlet obter a chave do cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="24cc0-119">Third cmdlet get the key from the key vault.</span></span>
<span data-ttu-id="24cc0-120">O quarto cmdlet atualiza a chave de criptografia gerenciada pelo cliente no RSVault.</span><span class="sxs-lookup"><span data-stu-id="24cc0-120">Fourth cmdlet updates the customer managed encryption key within the RSVault.</span></span> <span data-ttu-id="24cc0-121">Use -InfrastructureEncryption para habilitar a criptografia de infraestrutura para a primeira atualização.</span><span class="sxs-lookup"><span data-stu-id="24cc0-121">Use -InfrastructureEncryption param to enable infrastructure encryption for the first time update.</span></span> 

## <span data-ttu-id="24cc0-122">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="24cc0-122">PARAMETERS</span></span>

### <span data-ttu-id="24cc0-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24cc0-123">-DefaultProfile</span></span>
<span data-ttu-id="24cc0-124">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="24cc0-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="24cc0-125">-SoftDeleteFeatureState</span><span class="sxs-lookup"><span data-stu-id="24cc0-125">-SoftDeleteFeatureState</span></span>
<span data-ttu-id="24cc0-126">SoftDeleteFeatureState do Recovery Services Vault.</span><span class="sxs-lookup"><span data-stu-id="24cc0-126">SoftDeleteFeatureState of the Recovery Services Vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enable, Disable

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24cc0-127">-EncryptionKeyId</span><span class="sxs-lookup"><span data-stu-id="24cc0-127">-EncryptionKeyId</span></span>
<span data-ttu-id="24cc0-128">KeyId da chave de criptografia a ser usada para CMK.</span><span class="sxs-lookup"><span data-stu-id="24cc0-128">KeyId of the encryption key to be used for CMK.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: KeyID

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24cc0-129">-KeyVaultSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="24cc0-129">-KeyVaultSubscriptionId</span></span>
<span data-ttu-id="24cc0-130">ID de assinatura do Cofre de Chaves.</span><span class="sxs-lookup"><span data-stu-id="24cc0-130">Subscription Id of the Key Vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: SubscriptionID

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24cc0-131">-InfrastructureEncryption</span><span class="sxs-lookup"><span data-stu-id="24cc0-131">-InfrastructureEncryption</span></span>
<span data-ttu-id="24cc0-132">Habilita a criptografia de infraestrutura neste cofre.</span><span class="sxs-lookup"><span data-stu-id="24cc0-132">Enables infrastructure encryption on this vault.</span></span> <span data-ttu-id="24cc0-133">A criptografia de infraestrutura deve ser habilitada ao configurar a criptografia.</span><span class="sxs-lookup"><span data-stu-id="24cc0-133">Infrastructure encryption must be enabled when configuring encryption.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24cc0-134">-VaultId</span><span class="sxs-lookup"><span data-stu-id="24cc0-134">-VaultId</span></span>
<span data-ttu-id="24cc0-135">ARM ID do Cofre de Serviços de Recuperação.</span><span class="sxs-lookup"><span data-stu-id="24cc0-135">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="24cc0-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="24cc0-136">-Confirm</span></span>
<span data-ttu-id="24cc0-137">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="24cc0-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="24cc0-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24cc0-138">-WhatIf</span></span>
<span data-ttu-id="24cc0-139">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="24cc0-139">Shows what would happen if the cmdlet runs.</span></span>

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

### <span data-ttu-id="24cc0-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24cc0-140">CommonParameters</span></span>
<span data-ttu-id="24cc0-141">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24cc0-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24cc0-142">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="24cc0-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24cc0-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="24cc0-143">INPUTS</span></span>

### <span data-ttu-id="24cc0-144">System.String</span><span class="sxs-lookup"><span data-stu-id="24cc0-144">System.String</span></span>

### <span data-ttu-id="24cc0-145">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.VaultSoftDeleteFeatureState</span><span class="sxs-lookup"><span data-stu-id="24cc0-145">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.VaultSoftDeleteFeatureState</span></span>

## <span data-ttu-id="24cc0-146">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="24cc0-146">OUTPUTS</span></span>

### <span data-ttu-id="24cc0-147">Microsoft.Azure.Management.RecoveryServices.Backup.Models.BackupResourceVaultConfigResource</span><span class="sxs-lookup"><span data-stu-id="24cc0-147">Microsoft.Azure.Management.RecoveryServices.Backup.Models.BackupResourceVaultConfigResource</span></span>

## <span data-ttu-id="24cc0-148">NOTES</span><span class="sxs-lookup"><span data-stu-id="24cc0-148">NOTES</span></span>

## <span data-ttu-id="24cc0-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="24cc0-149">RELATED LINKS</span></span>

[<span data-ttu-id="24cc0-150">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="24cc0-150">Get-AzRecoveryServicesVault</span></span>](./Get-AzRecoveryServicesVault.md)

[<span data-ttu-id="24cc0-151">Get-AzRecoveryServicesVaultProperty</span><span class="sxs-lookup"><span data-stu-id="24cc0-151">Get-AzRecoveryServicesVaultProperty</span></span>](./Get-AzRecoveryServicesVaultProperty.md)
