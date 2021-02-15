---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: C2A7F37B-5713-4430-B83F-C6745692396D
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesvaultproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesVaultProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesVaultProperty.md
ms.openlocfilehash: e6bd0284d9ce5b5cb6973fce6aae5e16a4c06883
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114539"
---
# <span data-ttu-id="155fa-101">Set-AzRecoveryServicesVaultProperty</span><span class="sxs-lookup"><span data-stu-id="155fa-101">Set-AzRecoveryServicesVaultProperty</span></span>

## <span data-ttu-id="155fa-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="155fa-102">SYNOPSIS</span></span>
<span data-ttu-id="155fa-103">Atualiza as propriedades de um Cofre.</span><span class="sxs-lookup"><span data-stu-id="155fa-103">Updates properties of a Vault.</span></span>

## <span data-ttu-id="155fa-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="155fa-104">SYNTAX</span></span>

### <span data-ttu-id="155fa-105">AzureRSVaultSoftDelteParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="155fa-105">AzureRSVaultSoftDelteParameterSet (Default)</span></span>
```
Set-AzRecoveryServicesVaultProperty -SoftDeleteFeatureState <String> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="155fa-106">AzureRSVaultCMKParameterSet</span><span class="sxs-lookup"><span data-stu-id="155fa-106">AzureRSVaultCMKParameterSet</span></span>
```
Set-AzRecoveryServicesVaultProperty -EncryptionKeyId <string> -KeyVaultSubscriptionId <string> [-InfrastructureEncryption] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="155fa-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="155fa-107">DESCRIPTION</span></span>
<span data-ttu-id="155fa-108">O **cmdlet Set-AzRecoveryServicesVaultProperty** atualiza as propriedades de um cofre de serviços de Recuperação.</span><span class="sxs-lookup"><span data-stu-id="155fa-108">The **Set-AzRecoveryServicesVaultProperty** cmdlet updates properties of a Recovery services vault.</span></span> <span data-ttu-id="155fa-109">Esse cmdlet pode ser usado para habilitar/desabilitar a exclusão suave ou definir a criptografia CMK para um cofre com dois conjuntos de parâmetros diferentes.</span><span class="sxs-lookup"><span data-stu-id="155fa-109">This cmdlet can be used to enable/disable soft delete or set CMK encryption for a vault with two different parameter sets.</span></span> 
<span data-ttu-id="155fa-110">**A propriedade SoftDeleteFeatureState** de um cofre só poderá ser desabilitada se não houver contêineres registrados no cofre.</span><span class="sxs-lookup"><span data-stu-id="155fa-110">**SoftDeleteFeatureState** property of a vault can be disabled only if there are no registered containers in the vault.</span></span> <span data-ttu-id="155fa-111">O InfrastructurEncryption só pode ser definido na primeira vez que um usuário atualiza o cofre CMK.</span><span class="sxs-lookup"><span data-stu-id="155fa-111">InfrastructurEncryption can only be set the first time a user updates the CMK vault.</span></span>

## <span data-ttu-id="155fa-112">Exemplos</span><span class="sxs-lookup"><span data-stu-id="155fa-112">EXAMPLES</span></span>

### <span data-ttu-id="155fa-113">Exemplo 1: Atualizar SoftDeleteFeatureState de um cofre</span><span class="sxs-lookup"><span data-stu-id="155fa-113">Example 1: Update SoftDeleteFeatureState of a vault</span></span>
```
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "rgName" -Name "vaultName"
PS C:\> $props = Set-AzRecoveryServicesVaultProperty -VaultId $vault.Id -SoftDeleteFeatureState Enable
```

<span data-ttu-id="155fa-114">O primeiro comando obtém um objeto do Cofre e o armazena na variável $vault dados.</span><span class="sxs-lookup"><span data-stu-id="155fa-114">The first command gets a Vault object and then stores it in the $vault variable.</span></span>
<span data-ttu-id="155fa-115">O segundo comando atualiza a propriedade SoftDeleteFeatureState do cofre para o estado "Habilitado".</span><span class="sxs-lookup"><span data-stu-id="155fa-115">The second command Updates the SoftDeleteFeatureState property of the vault to "Enabled" state.</span></span>

### <span data-ttu-id="155fa-116">Exemplo 2: Atualizar a criptografia CMK de um cofre</span><span class="sxs-lookup"><span data-stu-id="155fa-116">Example 2: Update CMK encryption of a vault</span></span>

```
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "rgName" -Name "vaultName"
PS C:\> $keyVault = Get-AzKeyVault -VaultName "keyVaultName" -ResourceGroupName "RGName" 
PS C:\> $key = Get-AzKeyVaultKey -VaultName "keyVaultName" -Name "keyName" 
PS C:\> Set-AzRecoveryServicesVaultProperty -EncryptionKeyId $key.ID -KeyVaultSubscriptionId "f870818k-5h28-4t48-8961-37458592348r" -InfrastructureEncryption -VaultId $vault.ID
```

<span data-ttu-id="155fa-117">O primeiro cmdlet obtém o RSVault para atualizar as propriedades de criptografia.</span><span class="sxs-lookup"><span data-stu-id="155fa-117">First cmdlet gets the RSVault to update encryption properties.</span></span> <span data-ttu-id="155fa-118">O segundo cmdlet obtém o cofre de teclas do Azure.</span><span class="sxs-lookup"><span data-stu-id="155fa-118">Second cmdlet gets the azure key vault.</span></span> <span data-ttu-id="155fa-119">O terceiro cmdlet obterá a chave do cofre de teclas.</span><span class="sxs-lookup"><span data-stu-id="155fa-119">Third cmdlet get the key from the key vault.</span></span>
<span data-ttu-id="155fa-120">O quarto cmdlet atualiza a chave de criptografia gerenciada pelo cliente no RSVault.</span><span class="sxs-lookup"><span data-stu-id="155fa-120">Fourth cmdlet updates the customer managed encryption key within the RSVault.</span></span> <span data-ttu-id="155fa-121">Use o param -InfrastructureEncryption para habilitar a criptografia de infraestrutura pela primeira atualização.</span><span class="sxs-lookup"><span data-stu-id="155fa-121">Use -InfrastructureEncryption param to enable infrastructure encryption for the first time update.</span></span> 

## <span data-ttu-id="155fa-122">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="155fa-122">PARAMETERS</span></span>

### <span data-ttu-id="155fa-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="155fa-123">-DefaultProfile</span></span>
<span data-ttu-id="155fa-124">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="155fa-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="155fa-125">-SoftDeleteFeatureState</span><span class="sxs-lookup"><span data-stu-id="155fa-125">-SoftDeleteFeatureState</span></span>
<span data-ttu-id="155fa-126">SoftDeleteFeatureState do Cofre de Serviços de Recuperação.</span><span class="sxs-lookup"><span data-stu-id="155fa-126">SoftDeleteFeatureState of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="155fa-127">-EncryptionKeyId</span><span class="sxs-lookup"><span data-stu-id="155fa-127">-EncryptionKeyId</span></span>
<span data-ttu-id="155fa-128">KeyId da chave de criptografia a ser usada para CMK.</span><span class="sxs-lookup"><span data-stu-id="155fa-128">KeyId of the encryption key to be used for CMK.</span></span>

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

### <span data-ttu-id="155fa-129">-KeyVaultSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="155fa-129">-KeyVaultSubscriptionId</span></span>
<span data-ttu-id="155fa-130">ID da assinatura do Cofre de Teclas.</span><span class="sxs-lookup"><span data-stu-id="155fa-130">Subscription Id of the Key Vault.</span></span>

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

### <span data-ttu-id="155fa-131">-InfrastructureEncryption</span><span class="sxs-lookup"><span data-stu-id="155fa-131">-InfrastructureEncryption</span></span>
<span data-ttu-id="155fa-132">Habilita a criptografia de infraestrutura neste cofre.</span><span class="sxs-lookup"><span data-stu-id="155fa-132">Enables infrastructure encryption on this vault.</span></span> <span data-ttu-id="155fa-133">A criptografia de infraestrutura deve ser habilitada ao configurar a criptografia.</span><span class="sxs-lookup"><span data-stu-id="155fa-133">Infrastructure encryption must be enabled when configuring encryption.</span></span>

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

### <span data-ttu-id="155fa-134">-VaultId</span><span class="sxs-lookup"><span data-stu-id="155fa-134">-VaultId</span></span>
<span data-ttu-id="155fa-135">ID arm do Cofre de Serviços de Recuperação.</span><span class="sxs-lookup"><span data-stu-id="155fa-135">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="155fa-136">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="155fa-136">-Confirm</span></span>
<span data-ttu-id="155fa-137">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="155fa-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="155fa-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="155fa-138">-WhatIf</span></span>
<span data-ttu-id="155fa-139">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="155fa-139">Shows what would happen if the cmdlet runs.</span></span>

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

### <span data-ttu-id="155fa-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="155fa-140">CommonParameters</span></span>
<span data-ttu-id="155fa-141">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="155fa-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="155fa-142">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="155fa-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="155fa-143">Entradas</span><span class="sxs-lookup"><span data-stu-id="155fa-143">INPUTS</span></span>

### <span data-ttu-id="155fa-144">System.String</span><span class="sxs-lookup"><span data-stu-id="155fa-144">System.String</span></span>

### <span data-ttu-id="155fa-145">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.VaultSoftDeleteFeatureState</span><span class="sxs-lookup"><span data-stu-id="155fa-145">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.VaultSoftDeleteFeatureState</span></span>

## <span data-ttu-id="155fa-146">Saídas</span><span class="sxs-lookup"><span data-stu-id="155fa-146">OUTPUTS</span></span>

### <span data-ttu-id="155fa-147">Microsoft.Azure.Management.RecoveryServices.Backup.Models.BackupResourceVaultConfigResource</span><span class="sxs-lookup"><span data-stu-id="155fa-147">Microsoft.Azure.Management.RecoveryServices.Backup.Models.BackupResourceVaultConfigResource</span></span>

## <span data-ttu-id="155fa-148">Notas</span><span class="sxs-lookup"><span data-stu-id="155fa-148">NOTES</span></span>

## <span data-ttu-id="155fa-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="155fa-149">RELATED LINKS</span></span>

[<span data-ttu-id="155fa-150">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="155fa-150">Get-AzRecoveryServicesVault</span></span>](./Get-AzRecoveryServicesVault.md)

[<span data-ttu-id="155fa-151">Get-AzRecoveryServicesVaultProperty</span><span class="sxs-lookup"><span data-stu-id="155fa-151">Get-AzRecoveryServicesVaultProperty</span></span>](./Get-AzRecoveryServicesVaultProperty.md)
