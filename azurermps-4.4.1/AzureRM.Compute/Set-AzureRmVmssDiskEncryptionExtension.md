---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVmssDiskEncryptionExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVmssDiskEncryptionExtension.md
ms.openlocfilehash: fe4b965aa859388c2066dc759354a1651cb20123
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431793"
---
# <span data-ttu-id="03325-101">Set-AzureRmVmssDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="03325-101">Set-AzureRmVmssDiskEncryptionExtension</span></span>

## <span data-ttu-id="03325-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="03325-102">SYNOPSIS</span></span>
<span data-ttu-id="03325-103">Habilita a criptografia de disco em um conjunto de escala de VM.</span><span class="sxs-lookup"><span data-stu-id="03325-103">Enables disk encryption on a VM scale set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="03325-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="03325-104">SYNTAX</span></span>

```
Set-AzureRmVmssDiskEncryptionExtension [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-DiskEncryptionKeyVaultUrl] <String> [-DiskEncryptionKeyVaultId] <String> [-KeyEncryptionKeyUrl <String>]
 [-KeyEncryptionKeyVaultId <String>] [-KeyEncryptionAlgorithm <String>] [-VolumeType <String>] [-ForceUpdate]
 [-TypeHandlerVersion <String>] [-ExtensionName <String>] [-Passphrase <String>] [-Force]
 [-DisableAutoUpgradeMinorVersion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="03325-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="03325-105">DESCRIPTION</span></span>
<span data-ttu-id="03325-106">O cmdlet **set-AzureRmVmssDiskEncryptionExtension** habilita a criptografia em um conjunto de escala de VM.</span><span class="sxs-lookup"><span data-stu-id="03325-106">The **Set-AzureRmVmssDiskEncryptionExtension** cmdlet enables encryption on a VM scale set.</span></span>
<span data-ttu-id="03325-107">Esse cmdlet habilita a criptografia instalando a extensão de criptografia de disco no conjunto de escala da VM.</span><span class="sxs-lookup"><span data-stu-id="03325-107">This cmdlet enables encryption by installing the disk encryption extension on the VM scale set.</span></span>
<span data-ttu-id="03325-108">Se nenhum parâmetro *Name* for especificado, será instalada uma extensão com o nome padrão AzureDiskEncryption para máquinas virtuais que executam o sistema operacional Windows ou AzureDiskEncryptionForLinux para máquinas virtuais Linux.</span><span class="sxs-lookup"><span data-stu-id="03325-108">If no *Name* parameter is specified, an extension with the default name AzureDiskEncryption for virtual machines that run the Windows operating system or AzureDiskEncryptionForLinux for Linux virtual machines are installed.</span></span>

## <span data-ttu-id="03325-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="03325-109">EXAMPLES</span></span>

### <span data-ttu-id="03325-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="03325-110">Example 1</span></span>
```
$RGName = "MyResourceGroup"
$VmssName = "MyTestVmss"
$VaultName= "MyKeyVault"
$KeyVault = Get-AzureRmKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId
PS C:\> Set-AzureRmVmssDiskEncryptionExtension -ResourceGroupName $RGName -VMScaleSetName $VmssName -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId
```

<span data-ttu-id="03325-111">Esse comando habilita a criptografia em todos os discos de todas as VMs no conjunto de escala da VM.</span><span class="sxs-lookup"><span data-stu-id="03325-111">This command enables encryption on all disks of all VMs in the VM scale set.</span></span>

## <span data-ttu-id="03325-112">OS</span><span class="sxs-lookup"><span data-stu-id="03325-112">PARAMETERS</span></span>

### <span data-ttu-id="03325-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03325-113">-DefaultProfile</span></span>
<span data-ttu-id="03325-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="03325-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="03325-115">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="03325-115">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="03325-116">Desabilitar a atualização automática da versão secundária</span><span class="sxs-lookup"><span data-stu-id="03325-116">Disable auto-upgrade of minor version</span></span>

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

### <span data-ttu-id="03325-117">-DiskEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="03325-117">-DiskEncryptionKeyVaultId</span></span>
<span data-ttu-id="03325-118">O ResourceId do keyvault onde a chave de criptografia gerada será colocada</span><span class="sxs-lookup"><span data-stu-id="03325-118">ResourceID of the KeyVault where generated encryption key will be placed to</span></span>

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

### <span data-ttu-id="03325-119">-DiskEncryptionKeyVaultUrl</span><span class="sxs-lookup"><span data-stu-id="03325-119">-DiskEncryptionKeyVaultUrl</span></span>
<span data-ttu-id="03325-120">URL do keyvault onde a chave de criptografia gerada será colocada em</span><span class="sxs-lookup"><span data-stu-id="03325-120">URL of the KeyVault where generated encryption key will be placed to</span></span>

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

### <span data-ttu-id="03325-121">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="03325-121">-ExtensionName</span></span>
<span data-ttu-id="03325-122">O nome da extensão.</span><span class="sxs-lookup"><span data-stu-id="03325-122">The extension name.</span></span>
<span data-ttu-id="03325-123">Se esse parâmetro não for especificado, os valores padrão usados serão AzureDiskEncryption para VMs do Windows e AzureDiskEncryptionForLinux para VMs Linux</span><span class="sxs-lookup"><span data-stu-id="03325-123">If this parameter is not specified, default values used are AzureDiskEncryption for windows VMs and AzureDiskEncryptionForLinux for Linux VMs</span></span>

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

### <span data-ttu-id="03325-124">-Force</span><span class="sxs-lookup"><span data-stu-id="03325-124">-Force</span></span>
<span data-ttu-id="03325-125">Para forçar a habilitação da criptografia no conjunto de escala da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="03325-125">To force enabling encryption on the virtual machine scale set.</span></span>

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

### <span data-ttu-id="03325-126">-ForceUpdate</span><span class="sxs-lookup"><span data-stu-id="03325-126">-ForceUpdate</span></span>
<span data-ttu-id="03325-127">Gerar uma marca para a atualização de força.</span><span class="sxs-lookup"><span data-stu-id="03325-127">Generate a tag for force update.</span></span>  <span data-ttu-id="03325-128">Isso deve ser fornecido para executar operações de criptografia repetidas na mesma VM.</span><span class="sxs-lookup"><span data-stu-id="03325-128">This should be given to perform repeated encryption operations on the same VM.</span></span>

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

### <span data-ttu-id="03325-129">-KeyEncryptionAlgorithm</span><span class="sxs-lookup"><span data-stu-id="03325-129">-KeyEncryptionAlgorithm</span></span>
<span data-ttu-id="03325-130">Algoritmo de criptografia de chave usado para criptografar a chave de criptografia de volume</span><span class="sxs-lookup"><span data-stu-id="03325-130">KeyEncryption Algorithm used to encrypt the volume encryption key</span></span>

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

### <span data-ttu-id="03325-131">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="03325-131">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="03325-132">URL de compartimento de chave com controle de KeyEncryptionKey usado para criptografar a chave de criptografia de disco</span><span class="sxs-lookup"><span data-stu-id="03325-132">Versioned KeyVault URL of the KeyEncryptionKey used to encrypt the disk encryption key</span></span>

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

### <span data-ttu-id="03325-133">-KeyEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="03325-133">-KeyEncryptionKeyVaultId</span></span>
<span data-ttu-id="03325-134">ResourceId do keyvault que contém o KeyEncryptionKey usado para criptografar a chave de criptografia do disco</span><span class="sxs-lookup"><span data-stu-id="03325-134">ResourceID of the KeyVault containing the KeyEncryptionKey used to encrypt the disk encryption key</span></span>

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

### <span data-ttu-id="03325-135">-Senha</span><span class="sxs-lookup"><span data-stu-id="03325-135">-Passphrase</span></span>
<span data-ttu-id="03325-136">A senha especificada em parâmetros.</span><span class="sxs-lookup"><span data-stu-id="03325-136">The passphrase specified in parameters.</span></span>
<span data-ttu-id="03325-137">Esse parâmetro funciona somente para VM Linux.</span><span class="sxs-lookup"><span data-stu-id="03325-137">This parameter only works for Linux VM.</span></span>

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

### <span data-ttu-id="03325-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03325-138">-ResourceGroupName</span></span>
<span data-ttu-id="03325-139">O nome do grupo de recursos ao qual o conjunto de escala da VM pertence</span><span class="sxs-lookup"><span data-stu-id="03325-139">The resource group name to which the VM Scale Set belongs to</span></span>

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

### <span data-ttu-id="03325-140">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="03325-140">-TypeHandlerVersion</span></span>
<span data-ttu-id="03325-141">A versão do manipulador de tipos.</span><span class="sxs-lookup"><span data-stu-id="03325-141">The type handler version.</span></span>

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

### <span data-ttu-id="03325-142">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="03325-142">-VMScaleSetName</span></span>
<span data-ttu-id="03325-143">Nome do conjunto de escala da máquina virtual</span><span class="sxs-lookup"><span data-stu-id="03325-143">Name of the virtual machine scale set</span></span>

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

### <span data-ttu-id="03325-144">-Volumetype</span><span class="sxs-lookup"><span data-stu-id="03325-144">-VolumeType</span></span>
<span data-ttu-id="03325-145">Tipo do volume (so ou dados) para executar a operação de criptografia</span><span class="sxs-lookup"><span data-stu-id="03325-145">Type of the volume (OS or Data) to perform encryption operation</span></span>

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

### <span data-ttu-id="03325-146">-Confirme</span><span class="sxs-lookup"><span data-stu-id="03325-146">-Confirm</span></span>
<span data-ttu-id="03325-147">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="03325-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="03325-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="03325-148">-WhatIf</span></span>
<span data-ttu-id="03325-149">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="03325-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="03325-150">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="03325-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="03325-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03325-151">CommonParameters</span></span>
<span data-ttu-id="03325-152">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03325-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03325-153">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03325-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03325-154">SENSORES</span><span class="sxs-lookup"><span data-stu-id="03325-154">INPUTS</span></span>

### <span data-ttu-id="03325-155">System. String</span><span class="sxs-lookup"><span data-stu-id="03325-155">System.String</span></span>
<span data-ttu-id="03325-156">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="03325-156">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="03325-157">EXIBE</span><span class="sxs-lookup"><span data-stu-id="03325-157">OUTPUTS</span></span>

### <span data-ttu-id="03325-158">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachineScaleSetExtension</span><span class="sxs-lookup"><span data-stu-id="03325-158">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineScaleSetExtension</span></span>

## <span data-ttu-id="03325-159">INFORMA</span><span class="sxs-lookup"><span data-stu-id="03325-159">NOTES</span></span>

## <span data-ttu-id="03325-160">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="03325-160">RELATED LINKS</span></span>
