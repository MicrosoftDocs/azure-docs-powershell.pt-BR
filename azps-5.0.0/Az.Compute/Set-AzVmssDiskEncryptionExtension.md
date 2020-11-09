---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmssdiskencryptionextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssDiskEncryptionExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssDiskEncryptionExtension.md
ms.openlocfilehash: a18e91a147e60ddc54caacccd8c63f3568bfe2eb
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94280373"
---
# <span data-ttu-id="e37a6-101">Set-AzVmssDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="e37a6-101">Set-AzVmssDiskEncryptionExtension</span></span>

## <span data-ttu-id="e37a6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e37a6-102">SYNOPSIS</span></span>
<span data-ttu-id="e37a6-103">Habilita a criptografia de disco em um conjunto de escala de VM.</span><span class="sxs-lookup"><span data-stu-id="e37a6-103">Enables disk encryption on a VM scale set.</span></span>

## <span data-ttu-id="e37a6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e37a6-104">SYNTAX</span></span>

```
Set-AzVmssDiskEncryptionExtension [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-DiskEncryptionKeyVaultUrl] <String> [-DiskEncryptionKeyVaultId] <String> [-KeyEncryptionKeyUrl <String>]
 [-KeyEncryptionKeyVaultId <String>] [-KeyEncryptionAlgorithm <String>] [-VolumeType <String>] [-ForceUpdate]
 [-TypeHandlerVersion <String>] [-ExtensionName <String>] [-Passphrase <String>] [-Force]
 [-DisableAutoUpgradeMinorVersion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e37a6-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e37a6-105">DESCRIPTION</span></span>
<span data-ttu-id="e37a6-106">O cmdlet **set-AzVmssDiskEncryptionExtension** habilita a criptografia em um conjunto de escala de VM.</span><span class="sxs-lookup"><span data-stu-id="e37a6-106">The **Set-AzVmssDiskEncryptionExtension** cmdlet enables encryption on a VM scale set.</span></span> <span data-ttu-id="e37a6-107">Esse cmdlet habilita a criptografia instalando a extensão de criptografia de disco no conjunto de escala da VM.</span><span class="sxs-lookup"><span data-stu-id="e37a6-107">This cmdlet enables encryption by installing the disk encryption extension on the VM scale set.</span></span>

<span data-ttu-id="e37a6-108">Para máquinas virtuais Linux, o parâmetro *volumetype* deve estar presente e deve ser definido como "dados"</span><span class="sxs-lookup"><span data-stu-id="e37a6-108">For Linux virtual machines, the *VolumeType* parameter must be present and must be set to "Data"</span></span>

## <span data-ttu-id="e37a6-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e37a6-109">EXAMPLES</span></span>

### <span data-ttu-id="e37a6-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e37a6-110">Example 1</span></span>
```
$RGName = "MyResourceGroup"
$VmssName = "MyTestVmss"
$VaultName= "MyKeyVault"
$KeyVault = Get-AzKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId

PS C:\> Set-AzVmssDiskEncryptionExtension -ResourceGroupName $RGName -VMScaleSetName $VmssName -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId
```

<span data-ttu-id="e37a6-111">Esse comando habilita a criptografia em todos os discos de todas as VMs do Windows em um conjunto de escala da VM.</span><span class="sxs-lookup"><span data-stu-id="e37a6-111">This command enables encryption on all disks of all Windows VMs in a VM scale set.</span></span>

### <span data-ttu-id="e37a6-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="e37a6-112">Example 2</span></span>
```
$RGName = "MyResourceGroup"
$VmssName = "MyTestVmss"
$VaultName= "MyKeyVault"
$KeyVault = Get-AzKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId
$VolumeType = "Data"

PS C:\> Set-AzVmssDiskEncryptionExtension -ResourceGroupName $RGName -VMScaleSetName $VmssName -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId
 -VolumeType $volumeType
```

<span data-ttu-id="e37a6-113">Esse comando habilita a criptografia nos discos de dados de todas as VMs Linux em um conjunto de escalas de VM.</span><span class="sxs-lookup"><span data-stu-id="e37a6-113">This command enables encryption on the data disks of all Linux VMs in a VM scale set.</span></span>

## <span data-ttu-id="e37a6-114">OS</span><span class="sxs-lookup"><span data-stu-id="e37a6-114">PARAMETERS</span></span>

### <span data-ttu-id="e37a6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e37a6-115">-DefaultProfile</span></span>
<span data-ttu-id="e37a6-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e37a6-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e37a6-117">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="e37a6-117">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="e37a6-118">Desabilitar a atualização automática da versão secundária</span><span class="sxs-lookup"><span data-stu-id="e37a6-118">Disable auto-upgrade of minor version</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e37a6-119">-DiskEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="e37a6-119">-DiskEncryptionKeyVaultId</span></span>
<span data-ttu-id="e37a6-120">O ResourceId do keyvault onde a chave de criptografia gerada será colocada</span><span class="sxs-lookup"><span data-stu-id="e37a6-120">ResourceID of the KeyVault where generated encryption key will be placed to</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e37a6-121">-DiskEncryptionKeyVaultUrl</span><span class="sxs-lookup"><span data-stu-id="e37a6-121">-DiskEncryptionKeyVaultUrl</span></span>
<span data-ttu-id="e37a6-122">URL do keyvault onde a chave de criptografia gerada será colocada em</span><span class="sxs-lookup"><span data-stu-id="e37a6-122">URL of the KeyVault where generated encryption key will be placed to</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e37a6-123">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="e37a6-123">-ExtensionName</span></span>
<span data-ttu-id="e37a6-124">O nome da extensão.</span><span class="sxs-lookup"><span data-stu-id="e37a6-124">The extension name.</span></span>
<span data-ttu-id="e37a6-125">Se esse parâmetro não for especificado, os valores padrão usados serão AzureDiskEncryption para VMs do Windows e AzureDiskEncryptionForLinux para VMs Linux</span><span class="sxs-lookup"><span data-stu-id="e37a6-125">If this parameter is not specified, default values used are AzureDiskEncryption for windows VMs and AzureDiskEncryptionForLinux for Linux VMs</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e37a6-126">-Force</span><span class="sxs-lookup"><span data-stu-id="e37a6-126">-Force</span></span>
<span data-ttu-id="e37a6-127">Para forçar a habilitação da criptografia no conjunto de escala da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="e37a6-127">To force enabling encryption on the virtual machine scale set.</span></span>

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

### <span data-ttu-id="e37a6-128">-ForceUpdate</span><span class="sxs-lookup"><span data-stu-id="e37a6-128">-ForceUpdate</span></span>
<span data-ttu-id="e37a6-129">Gerar uma marca para a atualização de força.</span><span class="sxs-lookup"><span data-stu-id="e37a6-129">Generate a tag for force update.</span></span>  <span data-ttu-id="e37a6-130">Isso deve ser fornecido para executar operações de criptografia repetidas na mesma VM.</span><span class="sxs-lookup"><span data-stu-id="e37a6-130">This should be given to perform repeated encryption operations on the same VM.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e37a6-131">-KeyEncryptionAlgorithm</span><span class="sxs-lookup"><span data-stu-id="e37a6-131">-KeyEncryptionAlgorithm</span></span>
<span data-ttu-id="e37a6-132">Algoritmo de criptografia de chave usado para criptografar a chave de criptografia de volume</span><span class="sxs-lookup"><span data-stu-id="e37a6-132">KeyEncryption Algorithm used to encrypt the volume encryption key</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: RSA-OAEP, RSA1_5

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e37a6-133">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="e37a6-133">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="e37a6-134">URL de compartimento de chave com controle de KeyEncryptionKey usado para criptografar a chave de criptografia de disco</span><span class="sxs-lookup"><span data-stu-id="e37a6-134">Versioned KeyVault URL of the KeyEncryptionKey used to encrypt the disk encryption key</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e37a6-135">-KeyEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="e37a6-135">-KeyEncryptionKeyVaultId</span></span>
<span data-ttu-id="e37a6-136">ResourceId do keyvault que contém o KeyEncryptionKey usado para criptografar a chave de criptografia do disco</span><span class="sxs-lookup"><span data-stu-id="e37a6-136">ResourceID of the KeyVault containing the KeyEncryptionKey used to encrypt the disk encryption key</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e37a6-137">-Senha</span><span class="sxs-lookup"><span data-stu-id="e37a6-137">-Passphrase</span></span>
<span data-ttu-id="e37a6-138">A senha especificada em parâmetros.</span><span class="sxs-lookup"><span data-stu-id="e37a6-138">The passphrase specified in parameters.</span></span>
<span data-ttu-id="e37a6-139">Esse parâmetro funciona somente para VM Linux.</span><span class="sxs-lookup"><span data-stu-id="e37a6-139">This parameter only works for Linux VM.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e37a6-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e37a6-140">-ResourceGroupName</span></span>
<span data-ttu-id="e37a6-141">O nome do grupo de recursos ao qual o conjunto de escala da VM pertence</span><span class="sxs-lookup"><span data-stu-id="e37a6-141">The resource group name to which the VM Scale Set belongs to</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e37a6-142">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="e37a6-142">-TypeHandlerVersion</span></span>
<span data-ttu-id="e37a6-143">A versão do manipulador de tipos.</span><span class="sxs-lookup"><span data-stu-id="e37a6-143">The type handler version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e37a6-144">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="e37a6-144">-VMScaleSetName</span></span>
<span data-ttu-id="e37a6-145">Nome do conjunto de escala da máquina virtual</span><span class="sxs-lookup"><span data-stu-id="e37a6-145">Name of the virtual machine scale set</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e37a6-146">-Volumetype</span><span class="sxs-lookup"><span data-stu-id="e37a6-146">-VolumeType</span></span>
<span data-ttu-id="e37a6-147">Especifica o tipo de volumes de máquina virtual para executar a operação de criptografia: so, dados ou todos.</span><span class="sxs-lookup"><span data-stu-id="e37a6-147">Specifies the type of virtual machine volumes on which to perform encryption operation: OS, Data, or All.</span></span> 

<span data-ttu-id="e37a6-148">Linux: o parâmetro **volumetype** deve estar presente e deve ser definido como dados.</span><span class="sxs-lookup"><span data-stu-id="e37a6-148">Linux: The **VolumeType** parameter must be present and must be set to Data.</span></span> 

<span data-ttu-id="e37a6-149">Windows: o parâmetro **volumetype** , se presente, deve ser definido como All ou o os.</span><span class="sxs-lookup"><span data-stu-id="e37a6-149">Windows: The **VolumeType** parameter, if present, must be set to either All or OS.</span></span> <span data-ttu-id="e37a6-150">Se o parâmetro **volumetype** for omitido, o padrão será "All".</span><span class="sxs-lookup"><span data-stu-id="e37a6-150">If the **VolumeType** parameter is omitted it defaults to "All".</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: OS, Data, All

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e37a6-151">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e37a6-151">-Confirm</span></span>
<span data-ttu-id="e37a6-152">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e37a6-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e37a6-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e37a6-153">-WhatIf</span></span>
<span data-ttu-id="e37a6-154">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e37a6-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e37a6-155">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e37a6-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e37a6-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e37a6-156">CommonParameters</span></span>
<span data-ttu-id="e37a6-157">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e37a6-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e37a6-158">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e37a6-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e37a6-159">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e37a6-159">INPUTS</span></span>

### <span data-ttu-id="e37a6-160">System. String</span><span class="sxs-lookup"><span data-stu-id="e37a6-160">System.String</span></span>

### <span data-ttu-id="e37a6-161">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="e37a6-161">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="e37a6-162">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e37a6-162">OUTPUTS</span></span>

### <span data-ttu-id="e37a6-163">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachineScaleSetExtension</span><span class="sxs-lookup"><span data-stu-id="e37a6-163">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineScaleSetExtension</span></span>

## <span data-ttu-id="e37a6-164">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e37a6-164">NOTES</span></span>

## <span data-ttu-id="e37a6-165">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e37a6-165">RELATED LINKS</span></span>
