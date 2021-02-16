---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 6BCB36BC-F5E6-4EDD-983C-8BDE7A9B004D
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmdiskencryptionextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMDiskEncryptionExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMDiskEncryptionExtension.md
ms.openlocfilehash: 1c69d79e148eae92307855ecfe308f5208a2f455
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117818"
---
# <span data-ttu-id="33bcc-101">Set-AzVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="33bcc-101">Set-AzVMDiskEncryptionExtension</span></span>

## <span data-ttu-id="33bcc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="33bcc-102">SYNOPSIS</span></span>
<span data-ttu-id="33bcc-103">Habilita a criptografia em uma máquina virtual IaaS em execução no Azure.</span><span class="sxs-lookup"><span data-stu-id="33bcc-103">Enables encryption on a running IaaS virtual machine in Azure.</span></span>

## <span data-ttu-id="33bcc-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="33bcc-104">SYNTAX</span></span>

### <span data-ttu-id="33bcc-105">SinglePassParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="33bcc-105">SinglePassParameterSet (Default)</span></span>
```
Set-AzVMDiskEncryptionExtension [-ResourceGroupName] <String> [-VMName] <String>
 [-DiskEncryptionKeyVaultUrl] <String> [-DiskEncryptionKeyVaultId] <String> [[-KeyEncryptionKeyUrl] <String>]
 [[-KeyEncryptionKeyVaultId] <String>] [[-KeyEncryptionAlgorithm] <String>] [[-VolumeType] <String>]
 [[-SequenceVersion] <String>] [[-TypeHandlerVersion] <String>] [[-Name] <String>] [[-Passphrase] <String>]
 [-Force] [-DisableAutoUpgradeMinorVersion] [-SkipVmBackup] [-ExtensionType <String>]
 [-ExtensionPublisherName <String>] [-EncryptFormatAll] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="33bcc-106">AADClientSecibleParameterSet</span><span class="sxs-lookup"><span data-stu-id="33bcc-106">AADClientSecretParameterSet</span></span>
```
Set-AzVMDiskEncryptionExtension [-ResourceGroupName] <String> [-VMName] <String> [-AadClientID] <String>
 [-AadClientSecret] <String> [-DiskEncryptionKeyVaultUrl] <String> [-DiskEncryptionKeyVaultId] <String>
 [[-KeyEncryptionKeyUrl] <String>] [[-KeyEncryptionKeyVaultId] <String>] [[-KeyEncryptionAlgorithm] <String>]
 [[-VolumeType] <String>] [[-SequenceVersion] <String>] [[-TypeHandlerVersion] <String>] [[-Name] <String>]
 [[-Passphrase] <String>] [-Force] [-DisableAutoUpgradeMinorVersion] [-SkipVmBackup] [-ExtensionType <String>]
 [-ExtensionPublisherName <String>] [-EncryptFormatAll] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="33bcc-107">AADClientCertParameterSet</span><span class="sxs-lookup"><span data-stu-id="33bcc-107">AADClientCertParameterSet</span></span>
```
Set-AzVMDiskEncryptionExtension [-ResourceGroupName] <String> [-VMName] <String> [-AadClientID] <String>
 [-AadClientCertThumbprint] <String> [-DiskEncryptionKeyVaultUrl] <String> [-DiskEncryptionKeyVaultId] <String>
 [[-KeyEncryptionKeyUrl] <String>] [[-KeyEncryptionKeyVaultId] <String>] [[-KeyEncryptionAlgorithm] <String>]
 [[-VolumeType] <String>] [[-SequenceVersion] <String>] [[-TypeHandlerVersion] <String>] [[-Name] <String>]
 [[-Passphrase] <String>] [-Force] [-DisableAutoUpgradeMinorVersion] [-SkipVmBackup] [-ExtensionType <String>]
 [-ExtensionPublisherName <String>] [-EncryptFormatAll] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="33bcc-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="33bcc-108">DESCRIPTION</span></span>
<span data-ttu-id="33bcc-109">O cmdlet **Set-AzVMDiskEncryptionExtension** habilita a criptografia em uma infraestrutura de execução como um computador virtual de serviço (IaaS) no Azure.</span><span class="sxs-lookup"><span data-stu-id="33bcc-109">The **Set-AzVMDiskEncryptionExtension** cmdlet enables encryption on a running infrastructure as a service (IaaS) virtual machine in Azure.</span></span>  <span data-ttu-id="33bcc-110">Ele habilita a criptografia instalando a extensão de criptografia de disco na máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="33bcc-110">It enables encryption by installing the disk encryption extension on the virtual machine.</span></span> 

<span data-ttu-id="33bcc-111">Esse cmdlet requer confirmação dos usuários, pois uma das etapas para habilitar a criptografia requer uma reinicialização da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="33bcc-111">This cmdlet requires confirmation from the users as one of the steps to enable encryption requires a restart of the virtual machine.</span></span>

<span data-ttu-id="33bcc-112">É aconselhável que você salve seu trabalho na máquina virtual antes de executar este cmdlet.</span><span class="sxs-lookup"><span data-stu-id="33bcc-112">It is advised that you save your work on the virtual machine before you run this cmdlet.</span></span>

<span data-ttu-id="33bcc-113">Linux: o parâmetro **VolumeType** é necessário ao criptografar máquinas virtuais do Linux e deve ser definido como um valor ("Os", "Dados" ou "Todos") com suporte na distribuição do Linux.</span><span class="sxs-lookup"><span data-stu-id="33bcc-113">Linux: The **VolumeType** parameter is required when encrypting Linux virtual machines, and must be set to a value ("Os", "Data", or "All") supported by the Linux distribution.</span></span> 

<span data-ttu-id="33bcc-114">Windows: O parâmetro **VolumeType** pode ser omitido; nesse caso, a operação é padrão para Todos; se o parâmetro VolumeType estiver presente para uma máquina virtual do Windows, ele deverá ser definido como All ou OS.</span><span class="sxs-lookup"><span data-stu-id="33bcc-114">Windows: The **VolumeType** parameter may be omitted, in which case the operation defaults to All; if the VolumeType parameter is present for a Windows virtual machine, it must be set to either All or OS.</span></span>

## <span data-ttu-id="33bcc-115">Exemplos</span><span class="sxs-lookup"><span data-stu-id="33bcc-115">EXAMPLES</span></span>

### <span data-ttu-id="33bcc-116">Exemplo 1: Habilitar criptografia</span><span class="sxs-lookup"><span data-stu-id="33bcc-116">Example 1: Enable encryption</span></span>
```
$RGName = "MyResourceGroup"
$VMName = "MyTestVM"
$VaultName= "MyKeyVault"
$KeyVault = Get-AzKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId
$VolumeType = "All"
Set-AzVMDiskEncryptionExtension -ResourceGroupName $RGName -VMName $VMName -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId -VolumeType $VolumeType
```

<span data-ttu-id="33bcc-117">Este exemplo habilita a criptografia em um VM sem especificar credenciais AD.</span><span class="sxs-lookup"><span data-stu-id="33bcc-117">This example enables encryption on a VM without specifying AD credentials.</span></span>

### <span data-ttu-id="33bcc-118">Exemplo 2: Habilitar a criptografia com entrada de pipeline</span><span class="sxs-lookup"><span data-stu-id="33bcc-118">Example 2: Enable encryption with pipelined input</span></span>
```
$params = New-Object PSObject -Property @{
    ResourceGroupName = "[resource-group-name]"
    VMName = "[vm-name]"
    DiskEncryptionKeyVaultId = "/subscriptions/[subscription-id-guid]/resourceGroups/[resource-group-name]/providers/Microsoft.KeyVault/vaults/[keyvault-name]"
    DiskEncryptionKeyVaultUrl = "https://[keyvault-name].vault.azure.net"
    KeyEncryptionKeyVaultId = "/subscriptions/[subscription-id-guid]/resourceGroups/[resource-group-name]/providers/Microsoft.KeyVault/vaults/[keyvault-name]"
    KeyEncryptionKeyUrl = "https://[keyvault-name].vault.azure.net/keys/[kekname]/[kek-unique-id]"
    VolumeType = "All"
}

$params | Set-AzVmDiskEncryptionExtension
```

<span data-ttu-id="33bcc-119">Este exemplo envia parâmetros usando a entrada de pipeline para habilitar a criptografia em um VM, sem especificar credenciais AD.</span><span class="sxs-lookup"><span data-stu-id="33bcc-119">This example sends parameters using pipelined input to enable encryption on a VM, without specifying AD credentials.</span></span>

### <span data-ttu-id="33bcc-120">Exemplo 3: Habilitar a criptografia usando Azure AD Client ID e Client Secret</span><span class="sxs-lookup"><span data-stu-id="33bcc-120">Example 3: Enable encryption using Azure AD Client ID and Client Secret</span></span>
```
$RGName = "MyResourceGroup"
$VMName = "MyTestVM"
$AADClientID = "<clientID of your Azure AD app>"
$AADClientSecret = "<clientSecret of your Azure AD app>"
$VaultName= "MyKeyVault"
$KeyVault = Get-AzKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId
$VolumeType = "All"
Set-AzVMDiskEncryptionExtension -ResourceGroupName $RGName -VMName $VMName -AadClientID $AADClientID -AadClientSecret $AADClientSecret -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId -VolumeType $VolumeType
```

<span data-ttu-id="33bcc-121">Este exemplo usa a ID do cliente Azure AD e o segredo do cliente para habilitar a criptografia em um VM.</span><span class="sxs-lookup"><span data-stu-id="33bcc-121">This example uses Azure AD client ID and client secret to enable encryption on a VM.</span></span>

### <span data-ttu-id="33bcc-122">Exemplo 4: Habilitar a criptografia usando Azure AD client ID e client certification thumbprint</span><span class="sxs-lookup"><span data-stu-id="33bcc-122">Example 4: Enable encryption using Azure AD client ID and client certification thumbprint</span></span>
```
$RGName = "MyResourceGroup"
$VMName = "MyTestVM"
#The KeyVault must have enabledForDiskEncryption property set on it
$VaultName= "MyKeyVault"
$KeyVault = Get-AzKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId
$VolumeType = "All"

# create Azure AD application and associate the certificate
$CertPath = "C:\certificates\examplecert.pfx"
$CertPassword = "Password"
$Cert = New-Object System.Security.Cryptography.X509Certificates.X509Certificate2($CertPath, $CertPassword)
$CertValue = [System.Convert]::ToBase64String($cert.GetRawCertData())
$AzureAdApplication = New-AzADApplication -DisplayName "<Your Application Display Name>" -HomePage "<https://YourApplicationHomePage>" -IdentifierUris "<https://YouApplicationUri>" -CertValue $CertValue 
$ServicePrincipal = New-AzADServicePrincipal -ApplicationId $AzureAdApplication.ApplicationId

$AADClientID = $AzureAdApplication.ApplicationId
$aadClientCertThumbprint= $cert.Thumbprint

#Upload pfx to KeyVault 
$KeyVaultSecretName = "MyAADCert"
$FileContentBytes = get-content $CertPath -Encoding Byte
$FileContentEncoded = [System.Convert]::ToBase64String($fileContentBytes)
$JSONObject = @"
    { 
        "data" : "$filecontentencoded", 
        "dataType" : "pfx", 
        "password" : "$CertPassword" 
    } 
"@
$JSONObjectBytes = [System.Text.Encoding]::UTF8.GetBytes($jsonObject)
$JSONEncoded = [System.Convert]::ToBase64String($jsonObjectBytes)

$Secret = ConvertTo-SecureString -String $JSONEncoded -AsPlainText -Force
Set-AzKeyVaultSecret -VaultName $VaultName -Name $KeyVaultSecretName -SecretValue $Secret
Set-AzKeyVaultAccessPolicy -VaultName $VaultName -ResourceGroupName $RGName -EnabledForDeployment

#deploy cert to VM
$CertUrl = (Get-AzKeyVaultSecret -VaultName $VaultName -Name $KeyVaultSecretName).Id
$SourceVaultId = (Get-AzKeyVault -VaultName $VaultName -ResourceGroupName $RGName).ResourceId
$VM = Get-AzVM -ResourceGroupName $RGName -Name $VMName 
$VM = Add-AzVMSecret -VM $VM -SourceVaultId $SourceVaultId -CertificateStore "My" -CertificateUrl $CertUrl
Update-AzVM -VM $VM -ResourceGroupName $RGName 

#Enable encryption on the virtual machine using Azure AD client ID and client cert thumbprint
Set-AzVMDiskEncryptionExtension -ResourceGroupName $RGName -VMName $VMName -AadClientID $AADClientID -AadClientCertThumbprint $AADClientCertThumbprint -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId -VolumeType $VolumeType
```

<span data-ttu-id="33bcc-123">Este exemplo usa a ID do cliente Azure AD e as miniaturas de certificação do cliente para habilitar a criptografia em um VM.</span><span class="sxs-lookup"><span data-stu-id="33bcc-123">This example uses Azure AD client ID and client certification thumbprints to enable encryption on a VM.</span></span>

### <span data-ttu-id="33bcc-124">Exemplo 5: Habilitar a criptografia usando a ID do cliente Azure AD, o segredo do cliente e quebrar a chave de criptografia de disco usando a chave de criptografia</span><span class="sxs-lookup"><span data-stu-id="33bcc-124">Example 5: Enable encryption using Azure AD client ID, client secret, and wrap disk encryption key by using key encryption key</span></span>
```
$RGName = "MyResourceGroup"
$VMName = "MyTestVM"

$AADClientID = "<clientID of your Azure AD app>"
$AADClientSecret = "<clientSecret of your Azure AD app>"

$VaultName= "MyKeyVault"
$KeyVault = Get-AzKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId
$VolumeType = "All"

$KEKName = "MyKeyEncryptionKey"
$KEK = Add-AzKeyVaultKey -VaultName $VaultName -Name $KEKName -Destination "Software"
$KeyEncryptionKeyUrl = $KEK.Key.kid

Set-AzVMDiskEncryptionExtension -ResourceGroupName $RGName -VMName $VMName -AadClientID $AADClientID -AadClientSecret $AADClientSecret -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId -KeyEncryptionKeyUrl $KeyEncryptionKeyUrl -KeyEncryptionKeyVaultId $KeyVaultResourceId -VolumeType $VolumeType
```

<span data-ttu-id="33bcc-125">Este exemplo usa a ID do cliente Azure AD e o segredo do cliente para habilitar a criptografia em um VM e quebra a chave de criptografia de disco usando uma chave de criptografia.</span><span class="sxs-lookup"><span data-stu-id="33bcc-125">This example uses Azure AD client ID and client secret to enable encryption on a VM, and wraps the disk encryption key using a key encryption key.</span></span>

### <span data-ttu-id="33bcc-126">Exemplo 6: Habilitar a criptografia usando Azure AD client ID, client cert thumbprint e wrap disk encryptionkey by using key encryption key</span><span class="sxs-lookup"><span data-stu-id="33bcc-126">Example 6: Enable encryption using Azure AD client ID, client cert thumbprint, and wrap disk encryptionkey by using key encryption key</span></span>
```
$RGName = "MyResourceGroup"
$VMName = "MyTestVM"
#The KeyVault must have enabledForDiskEncryption property set on it
$VaultName= "MyKeyVault"
$KeyVault = Get-AzKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId
$KEKName = "MyKeyEncryptionKey"
$KEK = Add-AzKeyVaultKey -VaultName $VaultName -Name $KEKName -Destination "Software"
$KeyEncryptionKeyUrl = $KEK.Key.kid
$VolumeType = "All"

# create Azure AD application and associate the certificate
$CertPath = "C:\certificates\examplecert.pfx"
$CertPassword = "Password"
$Cert = New-Object System.Security.Cryptography.X509Certificates.X509Certificate2($CertPath, $CertPassword)
$CertValue = [System.Convert]::ToBase64String($cert.GetRawCertData())
$AzureAdApplication = New-AzADApplication -DisplayName "<Your Application Display Name>" -HomePage "<https://YourApplicationHomePage>" -IdentifierUris "<https://YouApplicationUri>" -CertValue $CertValue
$ServicePrincipal = New-AzADServicePrincipal -ApplicationId $AzureAdApplication.ApplicationId

$AADClientID = $AzureAdApplication.ApplicationId
$AADClientCertThumbprint= $Cert.Thumbprint

#Upload pfx to KeyVault 
$KeyVaultSecretName = "MyAADCert"
$FileContentBytes = get-content $CertPath -Encoding Byte
$FileContentEncoded = [System.Convert]::ToBase64String($FileContentBytes)
$JSONObject = @"
    { 
        "data" : "$filecontentencoded", 
        "dataType" : "pfx", 
        "password" : "$CertPassword" 
    } 
"@
$JSONObjectBytes = [System.Text.Encoding]::UTF8.GetBytes($JSONObject)
$JsonEncoded = [System.Convert]::ToBase64String($JSONObjectBytes)
$Secret = ConvertTo-SecureString -String $JSONEncoded -AsPlainText -Force
Set-AzKeyVaultSecret -VaultName $VaultName-Name $KeyVaultSecretName -SecretValue $Secret
Set-AzKeyVaultAccessPolicy -VaultName $VaultName -ResourceGroupName $RGName -EnabledForDeployment

#deploy cert to VM
$CertUrl = (Get-AzKeyVaultSecret -VaultName $VaultName -Name $KeyVaultSecretName).Id
$SourceVaultId = (Get-AzKeyVault -VaultName $VaultName -ResourceGroupName $RGName).ResourceId
$VM = Get-AzVM -ResourceGroupName $RGName -Name $VMName 
$VM = Add-AzVMSecret -VM $VM -SourceVaultId $SourceVaultId -CertificateStore "My" -CertificateUrl $CertUrl 
Update-AzVM -VM $VM -ResourceGroupName $RGName 

#Enable encryption on the virtual machine using Azure AD client ID and client cert thumbprint
Set-AzVMDiskEncryptionExtension -ResourceGroupName $RGname -VMName $VMName -AadClientID $AADClientID -AadClientCertThumbprint $AADClientCertThumbprint -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId -KeyEncryptionKeyUrl $KeyEncryptionKeyUrl -KeyEncryptionKeyVaultId $KeyVaultResourceId -VolumeType $VolumeType
```

<span data-ttu-id="33bcc-127">Este exemplo usa Azure AD client ID e client cert thumbprint to enable encryption on a VM, and wraps the disk encryption key using a key encryption key.</span><span class="sxs-lookup"><span data-stu-id="33bcc-127">This example uses Azure AD client ID and client cert thumbprint to enable encryption on a VM, and wraps the disk encryption key using a key encryption key.</span></span>

## <span data-ttu-id="33bcc-128">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="33bcc-128">PARAMETERS</span></span>

### <span data-ttu-id="33bcc-129">-AadClientCertThumbprint</span><span class="sxs-lookup"><span data-stu-id="33bcc-129">-AadClientCertThumbprint</span></span>
<span data-ttu-id="33bcc-130">Especifica a impressão digital do certificado do cliente do aplicativo AzureActive Directory (Azure AD) que tem permissões para escrever segredos para **o KeyVault.**</span><span class="sxs-lookup"><span data-stu-id="33bcc-130">Specifies the thumbprint of the AzureActive Directory (Azure AD) application client certificate that has permissions to write secrets to **KeyVault**.</span></span>
<span data-ttu-id="33bcc-131">Como um pré-requisito, o certificado do cliente Azure AD deve ser implantado anteriormente no armazenamento de certificados de computador local da máquina `my` virtual.</span><span class="sxs-lookup"><span data-stu-id="33bcc-131">As a prerequisite, the Azure AD client certificate must be previously deployed to the virtual machine's local computer `my` certificate store.</span></span>
<span data-ttu-id="33bcc-132">O Add-AzVMSecret cmdlet pode ser usado para implantar um certificado em uma máquina virtual no Azure.</span><span class="sxs-lookup"><span data-stu-id="33bcc-132">The Add-AzVMSecret cmdlet can be used to deploy a certificate to a virtual machine in Azure.</span></span>
<span data-ttu-id="33bcc-133">Para obter mais detalhes, consulte a ajuda do **cmdlet Add-AzVMSec ltd.**</span><span class="sxs-lookup"><span data-stu-id="33bcc-133">For more details, see the **Add-AzVMSecret** cmdlet help.</span></span>
<span data-ttu-id="33bcc-134">O certificado deve ser implantado anteriormente no computador virtual local do meu armazenamento de certificados.</span><span class="sxs-lookup"><span data-stu-id="33bcc-134">The certificate must be previously deployed to the virtual machine local computer my certificate store.</span></span>

```yaml
Type: System.String
Parameter Sets: AADClientCertParameterSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33bcc-135">-AadClientID</span><span class="sxs-lookup"><span data-stu-id="33bcc-135">-AadClientID</span></span>
<span data-ttu-id="33bcc-136">Especifica a ID do cliente do aplicativo Azure AD que tem permissões para escrever segredos **para KeyVault.**</span><span class="sxs-lookup"><span data-stu-id="33bcc-136">Specifies the client ID of the Azure AD application that has permissions to write secrets to **KeyVault**.</span></span>

```yaml
Type: System.String
Parameter Sets: AADClientSecretParameterSet, AADClientCertParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33bcc-137">-AadClientSecsec</span><span class="sxs-lookup"><span data-stu-id="33bcc-137">-AadClientSecret</span></span>
<span data-ttu-id="33bcc-138">Especifica o segredo do cliente do aplicativo Azure AD que tem permissões para escrever segredos para **KeyVault.**</span><span class="sxs-lookup"><span data-stu-id="33bcc-138">Specifies the client secret of the Azure AD application that has permissions to write secrets to **KeyVault**.</span></span>

```yaml
Type: System.String
Parameter Sets: AADClientSecretParameterSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33bcc-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33bcc-139">-DefaultProfile</span></span>
<span data-ttu-id="33bcc-140">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="33bcc-140">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="33bcc-141">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="33bcc-141">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="33bcc-142">Indica que esse cmdlet desabilita a atualização automática da versão secundária da extensão.</span><span class="sxs-lookup"><span data-stu-id="33bcc-142">Indicates that this cmdlet disables auto-upgrade of the minor version of the extension.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 14
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33bcc-143">-DiskEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="33bcc-143">-DiskEncryptionKeyVaultId</span></span>
<span data-ttu-id="33bcc-144">Especifica a ID de recurso **do KeyVault** para o qual as chaves de criptografia de computador virtual devem ser carregadas.</span><span class="sxs-lookup"><span data-stu-id="33bcc-144">Specifies the resource ID of the **KeyVault** to which the virtual machine encryption keys should be uploaded.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33bcc-145">-DiskEncryptionKeyVaultUrl</span><span class="sxs-lookup"><span data-stu-id="33bcc-145">-DiskEncryptionKeyVaultUrl</span></span>
<span data-ttu-id="33bcc-146">Especifica a URL **do KeyVault** para a qual as chaves de criptografia de computador virtual devem ser carregadas.</span><span class="sxs-lookup"><span data-stu-id="33bcc-146">Specifies the **KeyVault** URL to which the virtual machine encryption keys should be uploaded.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33bcc-147">-EncryptFormatAll</span><span class="sxs-lookup"><span data-stu-id="33bcc-147">-EncryptFormatAll</span></span>
<span data-ttu-id="33bcc-148">Encrypt-Format todas as unidades de dados que ainda não estão criptografadas</span><span class="sxs-lookup"><span data-stu-id="33bcc-148">Encrypt-Format all data drives that are not already encrypted</span></span>

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

### <span data-ttu-id="33bcc-149">-ExtensionPublisherName</span><span class="sxs-lookup"><span data-stu-id="33bcc-149">-ExtensionPublisherName</span></span>
<span data-ttu-id="33bcc-150">O nome do editor de extensão.</span><span class="sxs-lookup"><span data-stu-id="33bcc-150">The extension publisher name.</span></span> <span data-ttu-id="33bcc-151">Especifique esse parâmetro apenas para substituir o valor padrão de "Microsoft.Azure.Security".</span><span class="sxs-lookup"><span data-stu-id="33bcc-151">Specify this parameter only to override the default value of "Microsoft.Azure.Security".</span></span>

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

### <span data-ttu-id="33bcc-152">-ExtensionType</span><span class="sxs-lookup"><span data-stu-id="33bcc-152">-ExtensionType</span></span>
<span data-ttu-id="33bcc-153">O tipo de extensão.</span><span class="sxs-lookup"><span data-stu-id="33bcc-153">The extension type.</span></span> <span data-ttu-id="33bcc-154">Especifique este parâmetro para substituir seu valor padrão de "AzureDiskEncryption" para VMs do Windows e "AzureDiskEncryptionForLinux" para VMs do Linux.</span><span class="sxs-lookup"><span data-stu-id="33bcc-154">Specify this parameter to override its default value of "AzureDiskEncryption" for Windows VMs and "AzureDiskEncryptionForLinux" for Linux VMs.</span></span>

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

### <span data-ttu-id="33bcc-155">-Forçar</span><span class="sxs-lookup"><span data-stu-id="33bcc-155">-Force</span></span>
<span data-ttu-id="33bcc-156">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="33bcc-156">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="33bcc-157">-KeyEncryptionAlgorithm</span><span class="sxs-lookup"><span data-stu-id="33bcc-157">-KeyEncryptionAlgorithm</span></span>
<span data-ttu-id="33bcc-158">Especifica o algoritmo usado para quebrar e desembrulhar a chave de criptografia da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="33bcc-158">Specifies the algorithm that is used to wrap and unwrap the key encryption key of the virtual machine.</span></span>
<span data-ttu-id="33bcc-159">O valor padrão é RSA-OAEP.</span><span class="sxs-lookup"><span data-stu-id="33bcc-159">The default value is RSA-OAEP.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: RSA-OAEP, RSA1_5

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33bcc-160">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="33bcc-160">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="33bcc-161">Especifica a URL da chave de criptografia usada para quebrar e desembrulhar a chave de criptografia de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="33bcc-161">Specifies the URL of the key encryption key that is used to wrap and unwrap the virtual machine encryption key.</span></span>
<span data-ttu-id="33bcc-162">Essa deve ser a URL com versão completa.</span><span class="sxs-lookup"><span data-stu-id="33bcc-162">This must be the full versioned URL.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33bcc-163">-KeyEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="33bcc-163">-KeyEncryptionKeyVaultId</span></span>
<span data-ttu-id="33bcc-164">Especifica a ID de recurso do **KeyVault** que contém a chave de criptografia usada para quebrar e desembrulhar a chave de criptografia de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="33bcc-164">Specifies the resource ID of the **KeyVault** that contains key encryption key that is used to wrap and unwrap the virtual machine encryption key.</span></span>
<span data-ttu-id="33bcc-165">Essa deve ser uma URL com versão completa.</span><span class="sxs-lookup"><span data-stu-id="33bcc-165">This must be a full versioned URL.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33bcc-166">-Nome</span><span class="sxs-lookup"><span data-stu-id="33bcc-166">-Name</span></span>
<span data-ttu-id="33bcc-167">Especifica o nome do recurso gerenciador de recursos do Azure que representa a extensão.</span><span class="sxs-lookup"><span data-stu-id="33bcc-167">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span> <span data-ttu-id="33bcc-168">Se  o parâmetro Nome for omitido, a extensão instalada será nomeada AzureDiskEncryption em máquinas virtuais do Windows e AzureDiskEncryptionForLinux em máquinas virtuais do Linux.</span><span class="sxs-lookup"><span data-stu-id="33bcc-168">If the *Name* parameter is omitted, the installed extension will be named AzureDiskEncryption on Windows virtual machines and AzureDiskEncryptionForLinux on Linux virtual machines.</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 12
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33bcc-169">-Frase-senha</span><span class="sxs-lookup"><span data-stu-id="33bcc-169">-Passphrase</span></span>
<span data-ttu-id="33bcc-170">Especifica a frase de senha usada apenas para criptografar máquinas virtuais do Linux.</span><span class="sxs-lookup"><span data-stu-id="33bcc-170">Specifies the passphrase used for encrypting Linux virtual machines only.</span></span>
<span data-ttu-id="33bcc-171">Esse parâmetro não é usado para máquinas virtuais que executem o sistema operacional Windows.</span><span class="sxs-lookup"><span data-stu-id="33bcc-171">This parameter is not used for virtual machines that run the Windows operating system.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 13
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33bcc-172">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="33bcc-172">-ResourceGroupName</span></span>
<span data-ttu-id="33bcc-173">Especifica o nome do grupo de recursos da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="33bcc-173">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="33bcc-174">-SequenceVersion</span><span class="sxs-lookup"><span data-stu-id="33bcc-174">-SequenceVersion</span></span>
<span data-ttu-id="33bcc-175">Especifica o número da sequência das operações de criptografia para uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="33bcc-175">Specifies the sequence number of the encryption operations for a virtual machine.</span></span>
<span data-ttu-id="33bcc-176">Isso é exclusivo para cada operação de criptografia executada na mesma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="33bcc-176">This is unique per each encryption operation performed on the same virtual machine.</span></span>
<span data-ttu-id="33bcc-177">O Get-AzVMExtension cmdlet pode ser usado para recuperar o número da sequência anterior que foi usado.</span><span class="sxs-lookup"><span data-stu-id="33bcc-177">The Get-AzVMExtension cmdlet can be used to retrieve the previous sequence number that was used.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33bcc-178">-SkipVmBackup</span><span class="sxs-lookup"><span data-stu-id="33bcc-178">-SkipVmBackup</span></span>
<span data-ttu-id="33bcc-179">Ignorar a criação de backup para VMs do Linux</span><span class="sxs-lookup"><span data-stu-id="33bcc-179">Skip backup creation for Linux VMs</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 15
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33bcc-180">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="33bcc-180">-TypeHandlerVersion</span></span>
<span data-ttu-id="33bcc-181">Especifica a versão da extensão de criptografia.</span><span class="sxs-lookup"><span data-stu-id="33bcc-181">Specifies the version of the encryption extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: 11
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33bcc-182">-VMName</span><span class="sxs-lookup"><span data-stu-id="33bcc-182">-VMName</span></span>
<span data-ttu-id="33bcc-183">Especifica o nome da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="33bcc-183">Specifies the name of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33bcc-184">-VolumeType</span><span class="sxs-lookup"><span data-stu-id="33bcc-184">-VolumeType</span></span>
<span data-ttu-id="33bcc-185">Especifica o tipo de volumes de máquina virtual no qual executar a operação de criptografia: SO, Dados ou Tudo.</span><span class="sxs-lookup"><span data-stu-id="33bcc-185">Specifies the type of virtual machine volumes on which to perform encryption operation: OS, Data, or All.</span></span> 

<span data-ttu-id="33bcc-186">Linux: o parâmetro **VolumeType** é necessário ao criptografar máquinas virtuais do Linux e deve ser definido como um valor ("Os", "Dados" ou "Todos") com suporte na distribuição do Linux.</span><span class="sxs-lookup"><span data-stu-id="33bcc-186">Linux: The **VolumeType** parameter is required when encrypting Linux virtual machines, and must be set to a value ("Os", "Data", or "All") supported by the Linux distribution.</span></span> 

<span data-ttu-id="33bcc-187">Windows: O parâmetro **VolumeType** pode ser omitido; nesse caso, a operação é padrão para Todos; se o parâmetro VolumeType estiver presente para uma máquina virtual do Windows, ele deverá ser definido como All ou OS.</span><span class="sxs-lookup"><span data-stu-id="33bcc-187">Windows: The **VolumeType** parameter may be omitted, in which case the operation defaults to All; if the VolumeType parameter is present for a Windows virtual machine, it must be set to either All or OS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: OS, Data, All

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33bcc-188">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="33bcc-188">-Confirm</span></span>
<span data-ttu-id="33bcc-189">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="33bcc-189">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="33bcc-190">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="33bcc-190">-WhatIf</span></span>
<span data-ttu-id="33bcc-191">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="33bcc-191">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="33bcc-192">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="33bcc-192">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="33bcc-193">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33bcc-193">CommonParameters</span></span>
<span data-ttu-id="33bcc-194">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="33bcc-194">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33bcc-195">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="33bcc-195">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33bcc-196">Entradas</span><span class="sxs-lookup"><span data-stu-id="33bcc-196">INPUTS</span></span>

### <span data-ttu-id="33bcc-197">System.String</span><span class="sxs-lookup"><span data-stu-id="33bcc-197">System.String</span></span>

### <span data-ttu-id="33bcc-198">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="33bcc-198">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="33bcc-199">Saídas</span><span class="sxs-lookup"><span data-stu-id="33bcc-199">OUTPUTS</span></span>

### <span data-ttu-id="33bcc-200">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="33bcc-200">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="33bcc-201">Notas</span><span class="sxs-lookup"><span data-stu-id="33bcc-201">NOTES</span></span>

## <span data-ttu-id="33bcc-202">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="33bcc-202">RELATED LINKS</span></span>

[<span data-ttu-id="33bcc-203">Add-AzVMSecsecsec</span><span class="sxs-lookup"><span data-stu-id="33bcc-203">Add-AzVMSecret</span></span>](./Add-AzVMSecret.md)

[<span data-ttu-id="33bcc-204">Get-AzVMDiskEncryptionStatus</span><span class="sxs-lookup"><span data-stu-id="33bcc-204">Get-AzVMDiskEncryptionStatus</span></span>](./Get-AzVMDiskEncryptionStatus.md)

[<span data-ttu-id="33bcc-205">Remove-AzVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="33bcc-205">Remove-AzVMDiskEncryptionExtension</span></span>](./Remove-AzVMDiskEncryptionExtension.md)


