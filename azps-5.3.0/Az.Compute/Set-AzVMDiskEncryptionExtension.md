---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 6BCB36BC-F5E6-4EDD-983C-8BDE7A9B004D
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmdiskencryptionextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMDiskEncryptionExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMDiskEncryptionExtension.md
ms.openlocfilehash: 1c69d79e148eae92307855ecfe308f5208a2f455
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98434186"
---
# <span data-ttu-id="57141-101">Set-AzVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="57141-101">Set-AzVMDiskEncryptionExtension</span></span>

## <span data-ttu-id="57141-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="57141-102">SYNOPSIS</span></span>
<span data-ttu-id="57141-103">Habilita a criptografia em uma máquina virtual IaaS em execução no Azure.</span><span class="sxs-lookup"><span data-stu-id="57141-103">Enables encryption on a running IaaS virtual machine in Azure.</span></span>

## <span data-ttu-id="57141-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="57141-104">SYNTAX</span></span>

### <span data-ttu-id="57141-105">SinglePassParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="57141-105">SinglePassParameterSet (Default)</span></span>
```
Set-AzVMDiskEncryptionExtension [-ResourceGroupName] <String> [-VMName] <String>
 [-DiskEncryptionKeyVaultUrl] <String> [-DiskEncryptionKeyVaultId] <String> [[-KeyEncryptionKeyUrl] <String>]
 [[-KeyEncryptionKeyVaultId] <String>] [[-KeyEncryptionAlgorithm] <String>] [[-VolumeType] <String>]
 [[-SequenceVersion] <String>] [[-TypeHandlerVersion] <String>] [[-Name] <String>] [[-Passphrase] <String>]
 [-Force] [-DisableAutoUpgradeMinorVersion] [-SkipVmBackup] [-ExtensionType <String>]
 [-ExtensionPublisherName <String>] [-EncryptFormatAll] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="57141-106">AADClientSecretParameterSet</span><span class="sxs-lookup"><span data-stu-id="57141-106">AADClientSecretParameterSet</span></span>
```
Set-AzVMDiskEncryptionExtension [-ResourceGroupName] <String> [-VMName] <String> [-AadClientID] <String>
 [-AadClientSecret] <String> [-DiskEncryptionKeyVaultUrl] <String> [-DiskEncryptionKeyVaultId] <String>
 [[-KeyEncryptionKeyUrl] <String>] [[-KeyEncryptionKeyVaultId] <String>] [[-KeyEncryptionAlgorithm] <String>]
 [[-VolumeType] <String>] [[-SequenceVersion] <String>] [[-TypeHandlerVersion] <String>] [[-Name] <String>]
 [[-Passphrase] <String>] [-Force] [-DisableAutoUpgradeMinorVersion] [-SkipVmBackup] [-ExtensionType <String>]
 [-ExtensionPublisherName <String>] [-EncryptFormatAll] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="57141-107">AADClientCertParameterSet</span><span class="sxs-lookup"><span data-stu-id="57141-107">AADClientCertParameterSet</span></span>
```
Set-AzVMDiskEncryptionExtension [-ResourceGroupName] <String> [-VMName] <String> [-AadClientID] <String>
 [-AadClientCertThumbprint] <String> [-DiskEncryptionKeyVaultUrl] <String> [-DiskEncryptionKeyVaultId] <String>
 [[-KeyEncryptionKeyUrl] <String>] [[-KeyEncryptionKeyVaultId] <String>] [[-KeyEncryptionAlgorithm] <String>]
 [[-VolumeType] <String>] [[-SequenceVersion] <String>] [[-TypeHandlerVersion] <String>] [[-Name] <String>]
 [[-Passphrase] <String>] [-Force] [-DisableAutoUpgradeMinorVersion] [-SkipVmBackup] [-ExtensionType <String>]
 [-ExtensionPublisherName <String>] [-EncryptFormatAll] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="57141-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="57141-108">DESCRIPTION</span></span>
<span data-ttu-id="57141-109">O cmdlet **set-AzVMDiskEncryptionExtension** habilita a criptografia em uma máquina virtual de serviço (IaaS) de infraestrutura em execução no Azure.</span><span class="sxs-lookup"><span data-stu-id="57141-109">The **Set-AzVMDiskEncryptionExtension** cmdlet enables encryption on a running infrastructure as a service (IaaS) virtual machine in Azure.</span></span>  <span data-ttu-id="57141-110">Ele permite a criptografia instalando a extensão de criptografia de disco na máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="57141-110">It enables encryption by installing the disk encryption extension on the virtual machine.</span></span> 

<span data-ttu-id="57141-111">Esse cmdlet requer confirmação dos usuários como uma das etapas para habilitar a criptografia requer uma reinicialização da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="57141-111">This cmdlet requires confirmation from the users as one of the steps to enable encryption requires a restart of the virtual machine.</span></span>

<span data-ttu-id="57141-112">É recomendável que você salve o trabalho na máquina virtual antes de executar esse cmdlet.</span><span class="sxs-lookup"><span data-stu-id="57141-112">It is advised that you save your work on the virtual machine before you run this cmdlet.</span></span>

<span data-ttu-id="57141-113">Linux: o parâmetro **volumetype** é necessário ao criptografar máquinas virtuais do Linux e deve ser definido como um valor ("so", "dados" ou "todos") compatível com a distribuição Linux.</span><span class="sxs-lookup"><span data-stu-id="57141-113">Linux: The **VolumeType** parameter is required when encrypting Linux virtual machines, and must be set to a value ("Os", "Data", or "All") supported by the Linux distribution.</span></span> 

<span data-ttu-id="57141-114">Windows: o parâmetro **volumetype** pode ser omitido e, nesse caso, a operação é padrão para All; Se o parâmetro Volumetype estiver presente para um computador virtual do Windows, ele deverá ser definido como All ou o sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="57141-114">Windows: The **VolumeType** parameter may be omitted, in which case the operation defaults to All; if the VolumeType parameter is present for a Windows virtual machine, it must be set to either All or OS.</span></span>

## <span data-ttu-id="57141-115">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="57141-115">EXAMPLES</span></span>

### <span data-ttu-id="57141-116">Exemplo 1: habilitar a criptografia</span><span class="sxs-lookup"><span data-stu-id="57141-116">Example 1: Enable encryption</span></span>
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

<span data-ttu-id="57141-117">Este exemplo habilita a criptografia em uma VM sem especificar credenciais do anúncio.</span><span class="sxs-lookup"><span data-stu-id="57141-117">This example enables encryption on a VM without specifying AD credentials.</span></span>

### <span data-ttu-id="57141-118">Exemplo 2: habilitar a criptografia com entrada em pipeline</span><span class="sxs-lookup"><span data-stu-id="57141-118">Example 2: Enable encryption with pipelined input</span></span>
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

<span data-ttu-id="57141-119">Este exemplo envia parâmetros usando entrada em pipeline para habilitar a criptografia em uma VM, sem especificar as credenciais do anúncio.</span><span class="sxs-lookup"><span data-stu-id="57141-119">This example sends parameters using pipelined input to enable encryption on a VM, without specifying AD credentials.</span></span>

### <span data-ttu-id="57141-120">Exemplo 3: habilitar a criptografia usando o ID de cliente do Azure AD e o segredo do cliente</span><span class="sxs-lookup"><span data-stu-id="57141-120">Example 3: Enable encryption using Azure AD Client ID and Client Secret</span></span>
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

<span data-ttu-id="57141-121">Este exemplo usa o ID de cliente e o segredo do cliente do Azure AD para habilitar a criptografia em uma VM.</span><span class="sxs-lookup"><span data-stu-id="57141-121">This example uses Azure AD client ID and client secret to enable encryption on a VM.</span></span>

### <span data-ttu-id="57141-122">Exemplo 4: habilitar a criptografia usando a ID de cliente do Azure AD e a impressão digital de certificação do cliente</span><span class="sxs-lookup"><span data-stu-id="57141-122">Example 4: Enable encryption using Azure AD client ID and client certification thumbprint</span></span>
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

<span data-ttu-id="57141-123">Este exemplo usa a identificação do cliente do Azure AD e impressões digitais de certificação do cliente para habilitar a criptografia em uma VM.</span><span class="sxs-lookup"><span data-stu-id="57141-123">This example uses Azure AD client ID and client certification thumbprints to enable encryption on a VM.</span></span>

### <span data-ttu-id="57141-124">Exemplo 5: habilitar a criptografia usando a identificação de cliente do Azure AD, o segredo do cliente e a chave de criptografia do disco decodificada usando chave de criptografia de chave</span><span class="sxs-lookup"><span data-stu-id="57141-124">Example 5: Enable encryption using Azure AD client ID, client secret, and wrap disk encryption key by using key encryption key</span></span>
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

<span data-ttu-id="57141-125">Este exemplo usa a ID de cliente e o segredo do cliente do Azure AD para habilitar a criptografia em uma VM e encapsula a chave de criptografia de disco usando uma chave de criptografia de chave.</span><span class="sxs-lookup"><span data-stu-id="57141-125">This example uses Azure AD client ID and client secret to enable encryption on a VM, and wraps the disk encryption key using a key encryption key.</span></span>

### <span data-ttu-id="57141-126">Exemplo 6: habilitar a criptografia usando a ID de cliente do Azure AD, a impressão digital de certificado de cliente e quebrar o disco EncryptionKey usando chave de criptografia de chave</span><span class="sxs-lookup"><span data-stu-id="57141-126">Example 6: Enable encryption using Azure AD client ID, client cert thumbprint, and wrap disk encryptionkey by using key encryption key</span></span>
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

<span data-ttu-id="57141-127">Este exemplo usa a ID de cliente do Azure AD e a impressão digital de certificado de cliente para habilitar a criptografia em uma VM e encapsula a chave de criptografia de disco usando uma chave de criptografia de chave.</span><span class="sxs-lookup"><span data-stu-id="57141-127">This example uses Azure AD client ID and client cert thumbprint to enable encryption on a VM, and wraps the disk encryption key using a key encryption key.</span></span>

## <span data-ttu-id="57141-128">OS</span><span class="sxs-lookup"><span data-stu-id="57141-128">PARAMETERS</span></span>

### <span data-ttu-id="57141-129">-AadClientCertThumbprint</span><span class="sxs-lookup"><span data-stu-id="57141-129">-AadClientCertThumbprint</span></span>
<span data-ttu-id="57141-130">Especifica a impressão digital do certificado de cliente do aplicativo AzureActive Directory (Azure AD) que tem permissões para gravar segredos no **keyvault**.</span><span class="sxs-lookup"><span data-stu-id="57141-130">Specifies the thumbprint of the AzureActive Directory (Azure AD) application client certificate that has permissions to write secrets to **KeyVault**.</span></span>
<span data-ttu-id="57141-131">Como pré-requisito, o certificado de cliente do Azure AD deve ser implantado anteriormente no repositório de certificados do computador local da máquina virtual `my` .</span><span class="sxs-lookup"><span data-stu-id="57141-131">As a prerequisite, the Azure AD client certificate must be previously deployed to the virtual machine's local computer `my` certificate store.</span></span>
<span data-ttu-id="57141-132">O cmdlet Add-AzVMSecret pode ser usado para implantar um certificado em uma máquina virtual no Azure.</span><span class="sxs-lookup"><span data-stu-id="57141-132">The Add-AzVMSecret cmdlet can be used to deploy a certificate to a virtual machine in Azure.</span></span>
<span data-ttu-id="57141-133">Para obter mais detalhes, consulte a ajuda do cmdlet **Add-AzVMSecret** .</span><span class="sxs-lookup"><span data-stu-id="57141-133">For more details, see the **Add-AzVMSecret** cmdlet help.</span></span>
<span data-ttu-id="57141-134">O certificado deve ser implantado anteriormente no computador local da máquina virtual meu repositório de certificados.</span><span class="sxs-lookup"><span data-stu-id="57141-134">The certificate must be previously deployed to the virtual machine local computer my certificate store.</span></span>

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

### <span data-ttu-id="57141-135">-AadClientID</span><span class="sxs-lookup"><span data-stu-id="57141-135">-AadClientID</span></span>
<span data-ttu-id="57141-136">Especifica a ID do cliente do aplicativo Azure AD que tem permissões para gravar segredos no **keyvault**.</span><span class="sxs-lookup"><span data-stu-id="57141-136">Specifies the client ID of the Azure AD application that has permissions to write secrets to **KeyVault**.</span></span>

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

### <span data-ttu-id="57141-137">-AadClientSecret</span><span class="sxs-lookup"><span data-stu-id="57141-137">-AadClientSecret</span></span>
<span data-ttu-id="57141-138">Especifica o segredo do cliente do aplicativo Azure AD que tem permissões para gravar segredos no **keyvault**.</span><span class="sxs-lookup"><span data-stu-id="57141-138">Specifies the client secret of the Azure AD application that has permissions to write secrets to **KeyVault**.</span></span>

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

### <span data-ttu-id="57141-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57141-139">-DefaultProfile</span></span>
<span data-ttu-id="57141-140">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="57141-140">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="57141-141">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="57141-141">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="57141-142">Indica que esse cmdlet desabilita a atualização automática da versão secundária da extensão.</span><span class="sxs-lookup"><span data-stu-id="57141-142">Indicates that this cmdlet disables auto-upgrade of the minor version of the extension.</span></span>

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

### <span data-ttu-id="57141-143">-DiskEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="57141-143">-DiskEncryptionKeyVaultId</span></span>
<span data-ttu-id="57141-144">Especifica a ID do recurso do **cofre** para o qual as chaves de criptografia da máquina virtual devem ser carregadas.</span><span class="sxs-lookup"><span data-stu-id="57141-144">Specifies the resource ID of the **KeyVault** to which the virtual machine encryption keys should be uploaded.</span></span>

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

### <span data-ttu-id="57141-145">-DiskEncryptionKeyVaultUrl</span><span class="sxs-lookup"><span data-stu-id="57141-145">-DiskEncryptionKeyVaultUrl</span></span>
<span data-ttu-id="57141-146">Especifica a URL do **keyvault** para a qual as chaves de criptografia da máquina virtual devem ser carregadas.</span><span class="sxs-lookup"><span data-stu-id="57141-146">Specifies the **KeyVault** URL to which the virtual machine encryption keys should be uploaded.</span></span>

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

### <span data-ttu-id="57141-147">-EncryptFormatAll</span><span class="sxs-lookup"><span data-stu-id="57141-147">-EncryptFormatAll</span></span>
<span data-ttu-id="57141-148">Encrypt-Format todas as unidades de dados que ainda não estão criptografadas</span><span class="sxs-lookup"><span data-stu-id="57141-148">Encrypt-Format all data drives that are not already encrypted</span></span>

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

### <span data-ttu-id="57141-149">-ExtensionPublisherName</span><span class="sxs-lookup"><span data-stu-id="57141-149">-ExtensionPublisherName</span></span>
<span data-ttu-id="57141-150">O nome do fornecedor da extensão.</span><span class="sxs-lookup"><span data-stu-id="57141-150">The extension publisher name.</span></span> <span data-ttu-id="57141-151">Especifique esse parâmetro somente para substituir o valor padrão de "Microsoft. Azure. Security".</span><span class="sxs-lookup"><span data-stu-id="57141-151">Specify this parameter only to override the default value of "Microsoft.Azure.Security".</span></span>

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

### <span data-ttu-id="57141-152">-ExtensionType</span><span class="sxs-lookup"><span data-stu-id="57141-152">-ExtensionType</span></span>
<span data-ttu-id="57141-153">O tipo de extensão.</span><span class="sxs-lookup"><span data-stu-id="57141-153">The extension type.</span></span> <span data-ttu-id="57141-154">Especifique esse parâmetro para substituir o valor padrão de "AzureDiskEncryption" para VMs do Windows e "AzureDiskEncryptionForLinux" para VMs Linux.</span><span class="sxs-lookup"><span data-stu-id="57141-154">Specify this parameter to override its default value of "AzureDiskEncryption" for Windows VMs and "AzureDiskEncryptionForLinux" for Linux VMs.</span></span>

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

### <span data-ttu-id="57141-155">-Force</span><span class="sxs-lookup"><span data-stu-id="57141-155">-Force</span></span>
<span data-ttu-id="57141-156">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="57141-156">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="57141-157">-KeyEncryptionAlgorithm</span><span class="sxs-lookup"><span data-stu-id="57141-157">-KeyEncryptionAlgorithm</span></span>
<span data-ttu-id="57141-158">Especifica o algoritmo que é usado para quebrar e desencapsular a chave de criptografia da chave da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="57141-158">Specifies the algorithm that is used to wrap and unwrap the key encryption key of the virtual machine.</span></span>
<span data-ttu-id="57141-159">O valor padrão é RSA-OAEP.</span><span class="sxs-lookup"><span data-stu-id="57141-159">The default value is RSA-OAEP.</span></span>

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

### <span data-ttu-id="57141-160">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="57141-160">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="57141-161">Especifica a URL da chave de criptografia da chave que é usada para encapsular e descodificar a chave de criptografia da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="57141-161">Specifies the URL of the key encryption key that is used to wrap and unwrap the virtual machine encryption key.</span></span>
<span data-ttu-id="57141-162">Deve ser a URL completa com versão.</span><span class="sxs-lookup"><span data-stu-id="57141-162">This must be the full versioned URL.</span></span>

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

### <span data-ttu-id="57141-163">-KeyEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="57141-163">-KeyEncryptionKeyVaultId</span></span>
<span data-ttu-id="57141-164">Especifica a ID do **recurso que contém a chave** de criptografia de chave que é usada para encapsular e desencapsular a chave de criptografia da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="57141-164">Specifies the resource ID of the **KeyVault** that contains key encryption key that is used to wrap and unwrap the virtual machine encryption key.</span></span>
<span data-ttu-id="57141-165">Deve ser uma URL completa com versão.</span><span class="sxs-lookup"><span data-stu-id="57141-165">This must be a full versioned URL.</span></span>

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

### <span data-ttu-id="57141-166">-Nome</span><span class="sxs-lookup"><span data-stu-id="57141-166">-Name</span></span>
<span data-ttu-id="57141-167">Especifica o nome do recurso do Gerenciador de recursos do Azure que representa a extensão.</span><span class="sxs-lookup"><span data-stu-id="57141-167">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span> <span data-ttu-id="57141-168">Se o parâmetro *Name* for omitido, a extensão instalada será nomeada AzureDiskEncryption nas máquinas virtuais do Windows e AzureDiskEncryptionForLinux em máquinas virtuais Linux.</span><span class="sxs-lookup"><span data-stu-id="57141-168">If the *Name* parameter is omitted, the installed extension will be named AzureDiskEncryption on Windows virtual machines and AzureDiskEncryptionForLinux on Linux virtual machines.</span></span>


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

### <span data-ttu-id="57141-169">-Senha</span><span class="sxs-lookup"><span data-stu-id="57141-169">-Passphrase</span></span>
<span data-ttu-id="57141-170">Especifica a senha usada para criptografar apenas máquinas virtuais Linux.</span><span class="sxs-lookup"><span data-stu-id="57141-170">Specifies the passphrase used for encrypting Linux virtual machines only.</span></span>
<span data-ttu-id="57141-171">Esse parâmetro não é usado para máquinas virtuais que executam o sistema operacional Windows.</span><span class="sxs-lookup"><span data-stu-id="57141-171">This parameter is not used for virtual machines that run the Windows operating system.</span></span>

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

### <span data-ttu-id="57141-172">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57141-172">-ResourceGroupName</span></span>
<span data-ttu-id="57141-173">Especifica o nome do grupo de recursos da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="57141-173">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="57141-174">-SequenceVersion</span><span class="sxs-lookup"><span data-stu-id="57141-174">-SequenceVersion</span></span>
<span data-ttu-id="57141-175">Especifica o número de sequência das operações de criptografia para uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="57141-175">Specifies the sequence number of the encryption operations for a virtual machine.</span></span>
<span data-ttu-id="57141-176">Isso é exclusivo por cada operação de criptografia executada na mesma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="57141-176">This is unique per each encryption operation performed on the same virtual machine.</span></span>
<span data-ttu-id="57141-177">O cmdlet Get-AzVMExtension pode ser usado para recuperar o número de sequência anterior que foi usado.</span><span class="sxs-lookup"><span data-stu-id="57141-177">The Get-AzVMExtension cmdlet can be used to retrieve the previous sequence number that was used.</span></span>

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

### <span data-ttu-id="57141-178">-SkipVmBackup</span><span class="sxs-lookup"><span data-stu-id="57141-178">-SkipVmBackup</span></span>
<span data-ttu-id="57141-179">Ignorar a criação de backup para VMs Linux</span><span class="sxs-lookup"><span data-stu-id="57141-179">Skip backup creation for Linux VMs</span></span>

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

### <span data-ttu-id="57141-180">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="57141-180">-TypeHandlerVersion</span></span>
<span data-ttu-id="57141-181">Especifica a versão da extensão de criptografia.</span><span class="sxs-lookup"><span data-stu-id="57141-181">Specifies the version of the encryption extension.</span></span>

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

### <span data-ttu-id="57141-182">-VMName</span><span class="sxs-lookup"><span data-stu-id="57141-182">-VMName</span></span>
<span data-ttu-id="57141-183">Especifica o nome da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="57141-183">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="57141-184">-Volumetype</span><span class="sxs-lookup"><span data-stu-id="57141-184">-VolumeType</span></span>
<span data-ttu-id="57141-185">Especifica o tipo de volumes de máquina virtual para executar a operação de criptografia: so, dados ou todos.</span><span class="sxs-lookup"><span data-stu-id="57141-185">Specifies the type of virtual machine volumes on which to perform encryption operation: OS, Data, or All.</span></span> 

<span data-ttu-id="57141-186">Linux: o parâmetro **volumetype** é necessário ao criptografar máquinas virtuais do Linux e deve ser definido como um valor ("so", "dados" ou "todos") compatível com a distribuição Linux.</span><span class="sxs-lookup"><span data-stu-id="57141-186">Linux: The **VolumeType** parameter is required when encrypting Linux virtual machines, and must be set to a value ("Os", "Data", or "All") supported by the Linux distribution.</span></span> 

<span data-ttu-id="57141-187">Windows: o parâmetro **volumetype** pode ser omitido e, nesse caso, a operação é padrão para All; Se o parâmetro Volumetype estiver presente para um computador virtual do Windows, ele deverá ser definido como All ou o sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="57141-187">Windows: The **VolumeType** parameter may be omitted, in which case the operation defaults to All; if the VolumeType parameter is present for a Windows virtual machine, it must be set to either All or OS.</span></span>

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

### <span data-ttu-id="57141-188">-Confirme</span><span class="sxs-lookup"><span data-stu-id="57141-188">-Confirm</span></span>
<span data-ttu-id="57141-189">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="57141-189">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="57141-190">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="57141-190">-WhatIf</span></span>
<span data-ttu-id="57141-191">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="57141-191">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="57141-192">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="57141-192">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="57141-193">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57141-193">CommonParameters</span></span>
<span data-ttu-id="57141-194">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57141-194">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57141-195">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="57141-195">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57141-196">SENSORES</span><span class="sxs-lookup"><span data-stu-id="57141-196">INPUTS</span></span>

### <span data-ttu-id="57141-197">System. String</span><span class="sxs-lookup"><span data-stu-id="57141-197">System.String</span></span>

### <span data-ttu-id="57141-198">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="57141-198">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="57141-199">EXIBE</span><span class="sxs-lookup"><span data-stu-id="57141-199">OUTPUTS</span></span>

### <span data-ttu-id="57141-200">Microsoft. Azure. Commands. COMPUTE. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="57141-200">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="57141-201">INFORMA</span><span class="sxs-lookup"><span data-stu-id="57141-201">NOTES</span></span>

## <span data-ttu-id="57141-202">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="57141-202">RELATED LINKS</span></span>

[<span data-ttu-id="57141-203">Add-AzVMSecret</span><span class="sxs-lookup"><span data-stu-id="57141-203">Add-AzVMSecret</span></span>](./Add-AzVMSecret.md)

[<span data-ttu-id="57141-204">Get-AzVMDiskEncryptionStatus</span><span class="sxs-lookup"><span data-stu-id="57141-204">Get-AzVMDiskEncryptionStatus</span></span>](./Get-AzVMDiskEncryptionStatus.md)

[<span data-ttu-id="57141-205">Remove-AzVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="57141-205">Remove-AzVMDiskEncryptionExtension</span></span>](./Remove-AzVMDiskEncryptionExtension.md)


