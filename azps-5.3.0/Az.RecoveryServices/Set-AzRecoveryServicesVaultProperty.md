---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: C2A7F37B-5713-4430-B83F-C6745692396D
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesvaultproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesVaultProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesVaultProperty.md
ms.openlocfilehash: e6bd0284d9ce5b5cb6973fce6aae5e16a4c06883
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98428834"
---
# <span data-ttu-id="00d0c-101">Set-AzRecoveryServicesVaultProperty</span><span class="sxs-lookup"><span data-stu-id="00d0c-101">Set-AzRecoveryServicesVaultProperty</span></span>

## <span data-ttu-id="00d0c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="00d0c-102">SYNOPSIS</span></span>
<span data-ttu-id="00d0c-103">Atualiza as propriedades de um cofre.</span><span class="sxs-lookup"><span data-stu-id="00d0c-103">Updates properties of a Vault.</span></span>

## <span data-ttu-id="00d0c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="00d0c-104">SYNTAX</span></span>

### <span data-ttu-id="00d0c-105">AzureRSVaultSoftDelteParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="00d0c-105">AzureRSVaultSoftDelteParameterSet (Default)</span></span>
```
Set-AzRecoveryServicesVaultProperty -SoftDeleteFeatureState <String> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="00d0c-106">AzureRSVaultCMKParameterSet</span><span class="sxs-lookup"><span data-stu-id="00d0c-106">AzureRSVaultCMKParameterSet</span></span>
```
Set-AzRecoveryServicesVaultProperty -EncryptionKeyId <string> -KeyVaultSubscriptionId <string> [-InfrastructureEncryption] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="00d0c-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="00d0c-107">DESCRIPTION</span></span>
<span data-ttu-id="00d0c-108">O cmdlet **set-AzRecoveryServicesVaultProperty** atualiza as propriedades de um cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="00d0c-108">The **Set-AzRecoveryServicesVaultProperty** cmdlet updates properties of a Recovery services vault.</span></span> <span data-ttu-id="00d0c-109">Este cmdlet pode ser usado para habilitar/desabilitar a exclusão reversível ou definir a criptografia CMK para um cofre com dois conjuntos de parâmetros diferentes.</span><span class="sxs-lookup"><span data-stu-id="00d0c-109">This cmdlet can be used to enable/disable soft delete or set CMK encryption for a vault with two different parameter sets.</span></span> 
<span data-ttu-id="00d0c-110">A propriedade **SoftDeleteFeatureState** de um cofre pode ser desabilitada somente se não houver recipientes registrados no cofre.</span><span class="sxs-lookup"><span data-stu-id="00d0c-110">**SoftDeleteFeatureState** property of a vault can be disabled only if there are no registered containers in the vault.</span></span> <span data-ttu-id="00d0c-111">InfrastructurEncryption só pode ser definido na primeira vez que um usuário atualizar o cofre do CMK.</span><span class="sxs-lookup"><span data-stu-id="00d0c-111">InfrastructurEncryption can only be set the first time a user updates the CMK vault.</span></span>

## <span data-ttu-id="00d0c-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="00d0c-112">EXAMPLES</span></span>

### <span data-ttu-id="00d0c-113">Exemplo 1: atualizar SoftDeleteFeatureState de um cofre</span><span class="sxs-lookup"><span data-stu-id="00d0c-113">Example 1: Update SoftDeleteFeatureState of a vault</span></span>
```
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "rgName" -Name "vaultName"
PS C:\> $props = Set-AzRecoveryServicesVaultProperty -VaultId $vault.Id -SoftDeleteFeatureState Enable
```

<span data-ttu-id="00d0c-114">O primeiro comando obtém um objeto de cofre e, em seguida, armazena-o na variável $vault.</span><span class="sxs-lookup"><span data-stu-id="00d0c-114">The first command gets a Vault object and then stores it in the $vault variable.</span></span>
<span data-ttu-id="00d0c-115">O segundo comando atualiza a propriedade SoftDeleteFeatureState do cofre para o estado "habilitado".</span><span class="sxs-lookup"><span data-stu-id="00d0c-115">The second command Updates the SoftDeleteFeatureState property of the vault to "Enabled" state.</span></span>

### <span data-ttu-id="00d0c-116">Exemplo 2: atualizar a criptografia CMK de um cofre</span><span class="sxs-lookup"><span data-stu-id="00d0c-116">Example 2: Update CMK encryption of a vault</span></span>

```
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "rgName" -Name "vaultName"
PS C:\> $keyVault = Get-AzKeyVault -VaultName "keyVaultName" -ResourceGroupName "RGName" 
PS C:\> $key = Get-AzKeyVaultKey -VaultName "keyVaultName" -Name "keyName" 
PS C:\> Set-AzRecoveryServicesVaultProperty -EncryptionKeyId $key.ID -KeyVaultSubscriptionId "f870818k-5h28-4t48-8961-37458592348r" -InfrastructureEncryption -VaultId $vault.ID
```

<span data-ttu-id="00d0c-117">Primeiro cmdlet obtém o RSVault para atualizar as propriedades de criptografia.</span><span class="sxs-lookup"><span data-stu-id="00d0c-117">First cmdlet gets the RSVault to update encryption properties.</span></span> <span data-ttu-id="00d0c-118">O segundo cmdlet obtém o cofre de chaves do Azure.</span><span class="sxs-lookup"><span data-stu-id="00d0c-118">Second cmdlet gets the azure key vault.</span></span> <span data-ttu-id="00d0c-119">Terceiro cmdlet obtenha a chave do cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="00d0c-119">Third cmdlet get the key from the key vault.</span></span>
<span data-ttu-id="00d0c-120">O quarto cmdlet atualiza a chave de criptografia gerenciada pelo cliente no RSVault.</span><span class="sxs-lookup"><span data-stu-id="00d0c-120">Fourth cmdlet updates the customer managed encryption key within the RSVault.</span></span> <span data-ttu-id="00d0c-121">Use o parâmetro-InfrastructureEncryption para habilitar a criptografia de infraestrutura pela primeira vez em que atualizar.</span><span class="sxs-lookup"><span data-stu-id="00d0c-121">Use -InfrastructureEncryption param to enable infrastructure encryption for the first time update.</span></span> 

## <span data-ttu-id="00d0c-122">OS</span><span class="sxs-lookup"><span data-stu-id="00d0c-122">PARAMETERS</span></span>

### <span data-ttu-id="00d0c-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00d0c-123">-DefaultProfile</span></span>
<span data-ttu-id="00d0c-124">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="00d0c-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="00d0c-125">-SoftDeleteFeatureState</span><span class="sxs-lookup"><span data-stu-id="00d0c-125">-SoftDeleteFeatureState</span></span>
<span data-ttu-id="00d0c-126">SoftDeleteFeatureState do cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="00d0c-126">SoftDeleteFeatureState of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="00d0c-127">-EncryptionKeyId</span><span class="sxs-lookup"><span data-stu-id="00d0c-127">-EncryptionKeyId</span></span>
<span data-ttu-id="00d0c-128">KeyId da chave de criptografia a ser usada para CMK.</span><span class="sxs-lookup"><span data-stu-id="00d0c-128">KeyId of the encryption key to be used for CMK.</span></span>

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

### <span data-ttu-id="00d0c-129">-KeyVaultSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="00d0c-129">-KeyVaultSubscriptionId</span></span>
<span data-ttu-id="00d0c-130">ID da assinatura do cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="00d0c-130">Subscription Id of the Key Vault.</span></span>

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

### <span data-ttu-id="00d0c-131">-InfrastructureEncryption</span><span class="sxs-lookup"><span data-stu-id="00d0c-131">-InfrastructureEncryption</span></span>
<span data-ttu-id="00d0c-132">Habilita a criptografia de infraestrutura neste cofre.</span><span class="sxs-lookup"><span data-stu-id="00d0c-132">Enables infrastructure encryption on this vault.</span></span> <span data-ttu-id="00d0c-133">A criptografia de infraestrutura deve ser habilitada durante a configuração de criptografia.</span><span class="sxs-lookup"><span data-stu-id="00d0c-133">Infrastructure encryption must be enabled when configuring encryption.</span></span>

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

### <span data-ttu-id="00d0c-134">-Cofreid</span><span class="sxs-lookup"><span data-stu-id="00d0c-134">-VaultId</span></span>
<span data-ttu-id="00d0c-135">ID do braço do cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="00d0c-135">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="00d0c-136">-Confirme</span><span class="sxs-lookup"><span data-stu-id="00d0c-136">-Confirm</span></span>
<span data-ttu-id="00d0c-137">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="00d0c-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="00d0c-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="00d0c-138">-WhatIf</span></span>
<span data-ttu-id="00d0c-139">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="00d0c-139">Shows what would happen if the cmdlet runs.</span></span>

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

### <span data-ttu-id="00d0c-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00d0c-140">CommonParameters</span></span>
<span data-ttu-id="00d0c-141">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="00d0c-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00d0c-142">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="00d0c-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00d0c-143">SENSORES</span><span class="sxs-lookup"><span data-stu-id="00d0c-143">INPUTS</span></span>

### <span data-ttu-id="00d0c-144">System. String</span><span class="sxs-lookup"><span data-stu-id="00d0c-144">System.String</span></span>

### <span data-ttu-id="00d0c-145">Microsoft. Azure. Commands. Recoveryservices. backup. cmdlets. Models. VaultSoftDeleteFeatureState</span><span class="sxs-lookup"><span data-stu-id="00d0c-145">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.VaultSoftDeleteFeatureState</span></span>

## <span data-ttu-id="00d0c-146">EXIBE</span><span class="sxs-lookup"><span data-stu-id="00d0c-146">OUTPUTS</span></span>

### <span data-ttu-id="00d0c-147">Microsoft. Azure. Management. Recoveryservices. backup. Models. BackupResourceVaultConfigResource</span><span class="sxs-lookup"><span data-stu-id="00d0c-147">Microsoft.Azure.Management.RecoveryServices.Backup.Models.BackupResourceVaultConfigResource</span></span>

## <span data-ttu-id="00d0c-148">INFORMA</span><span class="sxs-lookup"><span data-stu-id="00d0c-148">NOTES</span></span>

## <span data-ttu-id="00d0c-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="00d0c-149">RELATED LINKS</span></span>

[<span data-ttu-id="00d0c-150">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="00d0c-150">Get-AzRecoveryServicesVault</span></span>](./Get-AzRecoveryServicesVault.md)

[<span data-ttu-id="00d0c-151">Get-AzRecoveryServicesVaultProperty</span><span class="sxs-lookup"><span data-stu-id="00d0c-151">Get-AzRecoveryServicesVaultProperty</span></span>](./Get-AzRecoveryServicesVaultProperty.md)
