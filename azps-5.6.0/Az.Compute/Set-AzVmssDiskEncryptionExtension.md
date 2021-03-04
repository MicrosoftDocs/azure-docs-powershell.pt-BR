---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/set-azvmssdiskencryptionextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssDiskEncryptionExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssDiskEncryptionExtension.md
ms.openlocfilehash: 7f163a80efe4e10f0107298351c59a72bfaaceb0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891862"
---
# <span data-ttu-id="d4ac7-101">Set-AzVmssDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="d4ac7-101">Set-AzVmssDiskEncryptionExtension</span></span>

## <span data-ttu-id="d4ac7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d4ac7-102">SYNOPSIS</span></span>
<span data-ttu-id="d4ac7-103">Habilita a criptografia de disco em um conjunto de escala de VM.</span><span class="sxs-lookup"><span data-stu-id="d4ac7-103">Enables disk encryption on a VM scale set.</span></span>

## <span data-ttu-id="d4ac7-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="d4ac7-104">SYNTAX</span></span>

```
Set-AzVmssDiskEncryptionExtension [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-DiskEncryptionKeyVaultUrl] <String> [-DiskEncryptionKeyVaultId] <String> [-KeyEncryptionKeyUrl <String>]
 [-KeyEncryptionKeyVaultId <String>] [-KeyEncryptionAlgorithm <String>] [-VolumeType <String>] [-ForceUpdate]
 [-TypeHandlerVersion <String>] [-ExtensionName <String>] [-Passphrase <String>] [-Force]
 [-DisableAutoUpgradeMinorVersion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d4ac7-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="d4ac7-105">DESCRIPTION</span></span>
<span data-ttu-id="d4ac7-106">O cmdlet **Set-AzVmssDiskEncryptionExtension** habilita a criptografia em um conjunto de escala de VM.</span><span class="sxs-lookup"><span data-stu-id="d4ac7-106">The **Set-AzVmssDiskEncryptionExtension** cmdlet enables encryption on a VM scale set.</span></span> <span data-ttu-id="d4ac7-107">Esse cmdlet habilita a criptografia instalando a extensão de criptografia de disco no conjunto de escala de VM.</span><span class="sxs-lookup"><span data-stu-id="d4ac7-107">This cmdlet enables encryption by installing the disk encryption extension on the VM scale set.</span></span>

<span data-ttu-id="d4ac7-108">Para máquinas virtuais Linux, o parâmetro *VolumeType* deve estar presente e deve ser definido como "Dados"</span><span class="sxs-lookup"><span data-stu-id="d4ac7-108">For Linux virtual machines, the *VolumeType* parameter must be present and must be set to "Data"</span></span>

## <span data-ttu-id="d4ac7-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d4ac7-109">EXAMPLES</span></span>

### <span data-ttu-id="d4ac7-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d4ac7-110">Example 1</span></span>
```
$RGName = "MyResourceGroup"
$VmssName = "MyTestVmss"
$VaultName= "MyKeyVault"
$KeyVault = Get-AzKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId

PS C:\> Set-AzVmssDiskEncryptionExtension -ResourceGroupName $RGName -VMScaleSetName $VmssName -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId
```

<span data-ttu-id="d4ac7-111">Esse comando habilita a criptografia em todos os discos de todas as VMs do Windows em um conjunto de escala de VM.</span><span class="sxs-lookup"><span data-stu-id="d4ac7-111">This command enables encryption on all disks of all Windows VMs in a VM scale set.</span></span>

### <span data-ttu-id="d4ac7-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="d4ac7-112">Example 2</span></span>
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

<span data-ttu-id="d4ac7-113">Esse comando habilita a criptografia nos discos de dados de todas as VMs Linux em um conjunto de escala de VM.</span><span class="sxs-lookup"><span data-stu-id="d4ac7-113">This command enables encryption on the data disks of all Linux VMs in a VM scale set.</span></span>

## <span data-ttu-id="d4ac7-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="d4ac7-114">PARAMETERS</span></span>

### <span data-ttu-id="d4ac7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4ac7-115">-DefaultProfile</span></span>
<span data-ttu-id="d4ac7-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="d4ac7-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d4ac7-117">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="d4ac7-117">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="d4ac7-118">Desabilitar a atualização automática da versão secundária</span><span class="sxs-lookup"><span data-stu-id="d4ac7-118">Disable auto-upgrade of minor version</span></span>

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

### <span data-ttu-id="d4ac7-119">-DiskEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="d4ac7-119">-DiskEncryptionKeyVaultId</span></span>
<span data-ttu-id="d4ac7-120">ResourceID da ChaveVault onde a chave de criptografia gerada será colocada para</span><span class="sxs-lookup"><span data-stu-id="d4ac7-120">ResourceID of the KeyVault where generated encryption key will be placed to</span></span>

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

### <span data-ttu-id="d4ac7-121">-DiskEncryptionKeyVaultUrl</span><span class="sxs-lookup"><span data-stu-id="d4ac7-121">-DiskEncryptionKeyVaultUrl</span></span>
<span data-ttu-id="d4ac7-122">URL da ChaveVault na qual a chave de criptografia gerada será colocada para</span><span class="sxs-lookup"><span data-stu-id="d4ac7-122">URL of the KeyVault where generated encryption key will be placed to</span></span>

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

### <span data-ttu-id="d4ac7-123">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="d4ac7-123">-ExtensionName</span></span>
<span data-ttu-id="d4ac7-124">O nome da extensão.</span><span class="sxs-lookup"><span data-stu-id="d4ac7-124">The extension name.</span></span>
<span data-ttu-id="d4ac7-125">Se esse parâmetro não for especificado, os valores padrão usados serão AzureDiskEncryption para VMs windows e AzureDiskEncryptionForLinux para VMs Linux</span><span class="sxs-lookup"><span data-stu-id="d4ac7-125">If this parameter is not specified, default values used are AzureDiskEncryption for windows VMs and AzureDiskEncryptionForLinux for Linux VMs</span></span>

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

### <span data-ttu-id="d4ac7-126">-Force</span><span class="sxs-lookup"><span data-stu-id="d4ac7-126">-Force</span></span>
<span data-ttu-id="d4ac7-127">Para forçar a habilitação da criptografia no conjunto de escala de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="d4ac7-127">To force enabling encryption on the virtual machine scale set.</span></span>

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

### <span data-ttu-id="d4ac7-128">-ForceUpdate</span><span class="sxs-lookup"><span data-stu-id="d4ac7-128">-ForceUpdate</span></span>
<span data-ttu-id="d4ac7-129">Gere uma marca para atualização de força.</span><span class="sxs-lookup"><span data-stu-id="d4ac7-129">Generate a tag for force update.</span></span>  <span data-ttu-id="d4ac7-130">Isso deve ser dado para executar operações de criptografia repetidas na mesma VM.</span><span class="sxs-lookup"><span data-stu-id="d4ac7-130">This should be given to perform repeated encryption operations on the same VM.</span></span>

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

### <span data-ttu-id="d4ac7-131">-KeyEncryptionAlgorithm</span><span class="sxs-lookup"><span data-stu-id="d4ac7-131">-KeyEncryptionAlgorithm</span></span>
<span data-ttu-id="d4ac7-132">Algoritmo keyEncryption usado para criptografar a chave de criptografia de volume</span><span class="sxs-lookup"><span data-stu-id="d4ac7-132">KeyEncryption Algorithm used to encrypt the volume encryption key</span></span>

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

### <span data-ttu-id="d4ac7-133">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="d4ac7-133">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="d4ac7-134">URL de KeyVault com versão da KeyEncryptionKey usada para criptografar a chave de criptografia de disco</span><span class="sxs-lookup"><span data-stu-id="d4ac7-134">Versioned KeyVault URL of the KeyEncryptionKey used to encrypt the disk encryption key</span></span>

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

### <span data-ttu-id="d4ac7-135">-KeyEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="d4ac7-135">-KeyEncryptionKeyVaultId</span></span>
<span data-ttu-id="d4ac7-136">ResourceID do KeyVault que contém o KeyEncryptionKey usado para criptografar a chave de criptografia de disco</span><span class="sxs-lookup"><span data-stu-id="d4ac7-136">ResourceID of the KeyVault containing the KeyEncryptionKey used to encrypt the disk encryption key</span></span>

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

### <span data-ttu-id="d4ac7-137">-Senha</span><span class="sxs-lookup"><span data-stu-id="d4ac7-137">-Passphrase</span></span>
<span data-ttu-id="d4ac7-138">A senha especificada nos parâmetros.</span><span class="sxs-lookup"><span data-stu-id="d4ac7-138">The passphrase specified in parameters.</span></span>
<span data-ttu-id="d4ac7-139">Esse parâmetro só funciona para VM Linux.</span><span class="sxs-lookup"><span data-stu-id="d4ac7-139">This parameter only works for Linux VM.</span></span>

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

### <span data-ttu-id="d4ac7-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4ac7-140">-ResourceGroupName</span></span>
<span data-ttu-id="d4ac7-141">O nome do grupo de recursos ao qual o Conjunto de Escala de VM pertence</span><span class="sxs-lookup"><span data-stu-id="d4ac7-141">The resource group name to which the VM Scale Set belongs to</span></span>

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

### <span data-ttu-id="d4ac7-142">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="d4ac7-142">-TypeHandlerVersion</span></span>
<span data-ttu-id="d4ac7-143">A versão do manipulador de tipos.</span><span class="sxs-lookup"><span data-stu-id="d4ac7-143">The type handler version.</span></span>

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

### <span data-ttu-id="d4ac7-144">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="d4ac7-144">-VMScaleSetName</span></span>
<span data-ttu-id="d4ac7-145">Nome do conjunto de escala de máquina virtual</span><span class="sxs-lookup"><span data-stu-id="d4ac7-145">Name of the virtual machine scale set</span></span>

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

### <span data-ttu-id="d4ac7-146">-VolumeType</span><span class="sxs-lookup"><span data-stu-id="d4ac7-146">-VolumeType</span></span>
<span data-ttu-id="d4ac7-147">Especifica o tipo de volumes de máquina virtual nos quais executar a operação de criptografia: OS, Data ou All.</span><span class="sxs-lookup"><span data-stu-id="d4ac7-147">Specifies the type of virtual machine volumes on which to perform encryption operation: OS, Data, or All.</span></span> 

<span data-ttu-id="d4ac7-148">Linux: o **parâmetro VolumeType** deve estar presente e deve ser definido como Data.</span><span class="sxs-lookup"><span data-stu-id="d4ac7-148">Linux: The **VolumeType** parameter must be present and must be set to Data.</span></span> 

<span data-ttu-id="d4ac7-149">Windows: o **parâmetro VolumeType,** se presente, deve ser definido como All ou SO.</span><span class="sxs-lookup"><span data-stu-id="d4ac7-149">Windows: The **VolumeType** parameter, if present, must be set to either All or OS.</span></span> <span data-ttu-id="d4ac7-150">Se o **parâmetro VolumeType** for omitido, ele será o padrão para "All".</span><span class="sxs-lookup"><span data-stu-id="d4ac7-150">If the **VolumeType** parameter is omitted it defaults to "All".</span></span>


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

### <span data-ttu-id="d4ac7-151">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d4ac7-151">-Confirm</span></span>
<span data-ttu-id="d4ac7-152">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d4ac7-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d4ac7-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d4ac7-153">-WhatIf</span></span>
<span data-ttu-id="d4ac7-154">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d4ac7-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d4ac7-155">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d4ac7-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d4ac7-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4ac7-156">CommonParameters</span></span>
<span data-ttu-id="d4ac7-157">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4ac7-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4ac7-158">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d4ac7-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4ac7-159">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d4ac7-159">INPUTS</span></span>

### <span data-ttu-id="d4ac7-160">System.String</span><span class="sxs-lookup"><span data-stu-id="d4ac7-160">System.String</span></span>

### <span data-ttu-id="d4ac7-161">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="d4ac7-161">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="d4ac7-162">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="d4ac7-162">OUTPUTS</span></span>

### <span data-ttu-id="d4ac7-163">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineScaleSetExtension</span><span class="sxs-lookup"><span data-stu-id="d4ac7-163">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineScaleSetExtension</span></span>

## <span data-ttu-id="d4ac7-164">NOTES</span><span class="sxs-lookup"><span data-stu-id="d4ac7-164">NOTES</span></span>

## <span data-ttu-id="d4ac7-165">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d4ac7-165">RELATED LINKS</span></span>
