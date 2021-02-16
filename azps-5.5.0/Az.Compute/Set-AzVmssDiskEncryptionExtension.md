---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmssdiskencryptionextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssDiskEncryptionExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssDiskEncryptionExtension.md
ms.openlocfilehash: a18e91a147e60ddc54caacccd8c63f3568bfe2eb
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117807"
---
# <span data-ttu-id="3e469-101">Set-AzVmssDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="3e469-101">Set-AzVmssDiskEncryptionExtension</span></span>

## <span data-ttu-id="3e469-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3e469-102">SYNOPSIS</span></span>
<span data-ttu-id="3e469-103">Habilita a criptografia de disco em um conjunto de escala de VM.</span><span class="sxs-lookup"><span data-stu-id="3e469-103">Enables disk encryption on a VM scale set.</span></span>

## <span data-ttu-id="3e469-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3e469-104">SYNTAX</span></span>

```
Set-AzVmssDiskEncryptionExtension [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-DiskEncryptionKeyVaultUrl] <String> [-DiskEncryptionKeyVaultId] <String> [-KeyEncryptionKeyUrl <String>]
 [-KeyEncryptionKeyVaultId <String>] [-KeyEncryptionAlgorithm <String>] [-VolumeType <String>] [-ForceUpdate]
 [-TypeHandlerVersion <String>] [-ExtensionName <String>] [-Passphrase <String>] [-Force]
 [-DisableAutoUpgradeMinorVersion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3e469-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="3e469-105">DESCRIPTION</span></span>
<span data-ttu-id="3e469-106">O **cmdlet Set-AzVmssDiskEncryptionExtension** habilita a criptografia em um conjunto de escala VM.</span><span class="sxs-lookup"><span data-stu-id="3e469-106">The **Set-AzVmssDiskEncryptionExtension** cmdlet enables encryption on a VM scale set.</span></span> <span data-ttu-id="3e469-107">Esse cmdlet habilita a criptografia instalando a extensão de criptografia de disco no conjunto de escala de VM.</span><span class="sxs-lookup"><span data-stu-id="3e469-107">This cmdlet enables encryption by installing the disk encryption extension on the VM scale set.</span></span>

<span data-ttu-id="3e469-108">Para máquinas virtuais do Linux, o parâmetro *VolumeType* deve estar presente e deve ser definido como "Dados"</span><span class="sxs-lookup"><span data-stu-id="3e469-108">For Linux virtual machines, the *VolumeType* parameter must be present and must be set to "Data"</span></span>

## <span data-ttu-id="3e469-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="3e469-109">EXAMPLES</span></span>

### <span data-ttu-id="3e469-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="3e469-110">Example 1</span></span>
```
$RGName = "MyResourceGroup"
$VmssName = "MyTestVmss"
$VaultName= "MyKeyVault"
$KeyVault = Get-AzKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId

PS C:\> Set-AzVmssDiskEncryptionExtension -ResourceGroupName $RGName -VMScaleSetName $VmssName -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId
```

<span data-ttu-id="3e469-111">Esse comando habilita a criptografia em todos os discos de todas as VMs do Windows em um conjunto de escala de VM.</span><span class="sxs-lookup"><span data-stu-id="3e469-111">This command enables encryption on all disks of all Windows VMs in a VM scale set.</span></span>

### <span data-ttu-id="3e469-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="3e469-112">Example 2</span></span>
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

<span data-ttu-id="3e469-113">Esse comando habilita a criptografia nos discos de dados de todas as VMs do Linux em um conjunto de escala de VM.</span><span class="sxs-lookup"><span data-stu-id="3e469-113">This command enables encryption on the data disks of all Linux VMs in a VM scale set.</span></span>

## <span data-ttu-id="3e469-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3e469-114">PARAMETERS</span></span>

### <span data-ttu-id="3e469-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e469-115">-DefaultProfile</span></span>
<span data-ttu-id="3e469-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="3e469-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3e469-117">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="3e469-117">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="3e469-118">Desabilitar a atualização automática da versão secundária</span><span class="sxs-lookup"><span data-stu-id="3e469-118">Disable auto-upgrade of minor version</span></span>

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

### <span data-ttu-id="3e469-119">-DiskEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="3e469-119">-DiskEncryptionKeyVaultId</span></span>
<span data-ttu-id="3e469-120">ResourceID da KeyVault onde a chave de criptografia gerada será colocada em</span><span class="sxs-lookup"><span data-stu-id="3e469-120">ResourceID of the KeyVault where generated encryption key will be placed to</span></span>

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

### <span data-ttu-id="3e469-121">-DiskEncryptionKeyVaultUrl</span><span class="sxs-lookup"><span data-stu-id="3e469-121">-DiskEncryptionKeyVaultUrl</span></span>
<span data-ttu-id="3e469-122">URL da KeyVault onde a chave de criptografia gerada será colocada em</span><span class="sxs-lookup"><span data-stu-id="3e469-122">URL of the KeyVault where generated encryption key will be placed to</span></span>

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

### <span data-ttu-id="3e469-123">-Nomeda Extensão</span><span class="sxs-lookup"><span data-stu-id="3e469-123">-ExtensionName</span></span>
<span data-ttu-id="3e469-124">O nome da extensão.</span><span class="sxs-lookup"><span data-stu-id="3e469-124">The extension name.</span></span>
<span data-ttu-id="3e469-125">Se esse parâmetro não for especificado, os valores padrão usados serão VMs do AzureDiskEncryption para windows e VMs do AzureDiskEncryptionForLinux para Linux</span><span class="sxs-lookup"><span data-stu-id="3e469-125">If this parameter is not specified, default values used are AzureDiskEncryption for windows VMs and AzureDiskEncryptionForLinux for Linux VMs</span></span>

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

### <span data-ttu-id="3e469-126">-Forçar</span><span class="sxs-lookup"><span data-stu-id="3e469-126">-Force</span></span>
<span data-ttu-id="3e469-127">Para forçar a habilitação da criptografia no conjunto de escala de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="3e469-127">To force enabling encryption on the virtual machine scale set.</span></span>

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

### <span data-ttu-id="3e469-128">-ForceUpdate</span><span class="sxs-lookup"><span data-stu-id="3e469-128">-ForceUpdate</span></span>
<span data-ttu-id="3e469-129">Gere uma marca para forçar a atualização.</span><span class="sxs-lookup"><span data-stu-id="3e469-129">Generate a tag for force update.</span></span>  <span data-ttu-id="3e469-130">Isso deve ser dado para executar operações de criptografia repetidas no mesmo VM.</span><span class="sxs-lookup"><span data-stu-id="3e469-130">This should be given to perform repeated encryption operations on the same VM.</span></span>

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

### <span data-ttu-id="3e469-131">-KeyEncryptionAlgorithm</span><span class="sxs-lookup"><span data-stu-id="3e469-131">-KeyEncryptionAlgorithm</span></span>
<span data-ttu-id="3e469-132">Algoritmo de Criptografia de Chave usado para criptografar a chave de criptografia por volume</span><span class="sxs-lookup"><span data-stu-id="3e469-132">KeyEncryption Algorithm used to encrypt the volume encryption key</span></span>

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

### <span data-ttu-id="3e469-133">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="3e469-133">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="3e469-134">URL do KeyVault de versão da KeyEncryptionKey usada para criptografar a chave de criptografia de disco</span><span class="sxs-lookup"><span data-stu-id="3e469-134">Versioned KeyVault URL of the KeyEncryptionKey used to encrypt the disk encryption key</span></span>

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

### <span data-ttu-id="3e469-135">-KeyEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="3e469-135">-KeyEncryptionKeyVaultId</span></span>
<span data-ttu-id="3e469-136">ResourceID do KeyVault que contém o KeyEncryptionKey usado para criptografar a chave de criptografia de disco</span><span class="sxs-lookup"><span data-stu-id="3e469-136">ResourceID of the KeyVault containing the KeyEncryptionKey used to encrypt the disk encryption key</span></span>

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

### <span data-ttu-id="3e469-137">-Frase-senha</span><span class="sxs-lookup"><span data-stu-id="3e469-137">-Passphrase</span></span>
<span data-ttu-id="3e469-138">A frase de senha especificada nos parâmetros.</span><span class="sxs-lookup"><span data-stu-id="3e469-138">The passphrase specified in parameters.</span></span>
<span data-ttu-id="3e469-139">Esse parâmetro só funciona para VM do Linux.</span><span class="sxs-lookup"><span data-stu-id="3e469-139">This parameter only works for Linux VM.</span></span>

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

### <span data-ttu-id="3e469-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e469-140">-ResourceGroupName</span></span>
<span data-ttu-id="3e469-141">O nome do grupo de recursos ao qual o Conjunto de Escala de VM pertence</span><span class="sxs-lookup"><span data-stu-id="3e469-141">The resource group name to which the VM Scale Set belongs to</span></span>

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

### <span data-ttu-id="3e469-142">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="3e469-142">-TypeHandlerVersion</span></span>
<span data-ttu-id="3e469-143">A versão do manipulador de tipo.</span><span class="sxs-lookup"><span data-stu-id="3e469-143">The type handler version.</span></span>

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

### <span data-ttu-id="3e469-144">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="3e469-144">-VMScaleSetName</span></span>
<span data-ttu-id="3e469-145">Nome do conjunto de escala de máquina virtual</span><span class="sxs-lookup"><span data-stu-id="3e469-145">Name of the virtual machine scale set</span></span>

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

### <span data-ttu-id="3e469-146">-VolumeType</span><span class="sxs-lookup"><span data-stu-id="3e469-146">-VolumeType</span></span>
<span data-ttu-id="3e469-147">Especifica o tipo de volumes de máquina virtual no qual executar a operação de criptografia: SO, Dados ou Tudo.</span><span class="sxs-lookup"><span data-stu-id="3e469-147">Specifies the type of virtual machine volumes on which to perform encryption operation: OS, Data, or All.</span></span> 

<span data-ttu-id="3e469-148">Linux: o parâmetro **VolumeType** deve estar presente e deve ser definido como Dados.</span><span class="sxs-lookup"><span data-stu-id="3e469-148">Linux: The **VolumeType** parameter must be present and must be set to Data.</span></span> 

<span data-ttu-id="3e469-149">Windows: O parâmetro **VolumeType,** se presente, deve ser definido como Todo ou SO.</span><span class="sxs-lookup"><span data-stu-id="3e469-149">Windows: The **VolumeType** parameter, if present, must be set to either All or OS.</span></span> <span data-ttu-id="3e469-150">Se o **parâmetro VolumeType** for omitido, ele será padrão para "Tudo".</span><span class="sxs-lookup"><span data-stu-id="3e469-150">If the **VolumeType** parameter is omitted it defaults to "All".</span></span>


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

### <span data-ttu-id="3e469-151">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="3e469-151">-Confirm</span></span>
<span data-ttu-id="3e469-152">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3e469-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3e469-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3e469-153">-WhatIf</span></span>
<span data-ttu-id="3e469-154">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="3e469-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3e469-155">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3e469-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3e469-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e469-156">CommonParameters</span></span>
<span data-ttu-id="3e469-157">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e469-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e469-158">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3e469-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e469-159">Entradas</span><span class="sxs-lookup"><span data-stu-id="3e469-159">INPUTS</span></span>

### <span data-ttu-id="3e469-160">System.String</span><span class="sxs-lookup"><span data-stu-id="3e469-160">System.String</span></span>

### <span data-ttu-id="3e469-161">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="3e469-161">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="3e469-162">Saídas</span><span class="sxs-lookup"><span data-stu-id="3e469-162">OUTPUTS</span></span>

### <span data-ttu-id="3e469-163">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineScaleSetExtension</span><span class="sxs-lookup"><span data-stu-id="3e469-163">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineScaleSetExtension</span></span>

## <span data-ttu-id="3e469-164">Notas</span><span class="sxs-lookup"><span data-stu-id="3e469-164">NOTES</span></span>

## <span data-ttu-id="3e469-165">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3e469-165">RELATED LINKS</span></span>
