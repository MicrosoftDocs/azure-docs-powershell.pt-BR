---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 6BCB36BC-F5E6-4EDD-983C-8BDE7A9B004D
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmdiskencryptionextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMDiskEncryptionExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMDiskEncryptionExtension.md
ms.openlocfilehash: da50845ff5012d466eed0c68103cdbd0baea4e7f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93771108"
---
# <span data-ttu-id="c356c-101">Set-AzVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="c356c-101">Set-AzVMDiskEncryptionExtension</span></span>

## <span data-ttu-id="c356c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c356c-102">SYNOPSIS</span></span>
<span data-ttu-id="c356c-103">Habilita a criptografia em uma máquina virtual IaaS em execução no Azure.</span><span class="sxs-lookup"><span data-stu-id="c356c-103">Enables encryption on a running IaaS virtual machine in Azure.</span></span>

## <span data-ttu-id="c356c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c356c-104">SYNTAX</span></span>

### <span data-ttu-id="c356c-105">SinglePassParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="c356c-105">SinglePassParameterSet (Default)</span></span>
```
Set-AzVMDiskEncryptionExtension [-ResourceGroupName] <String> [-VMName] <String>
 [-DiskEncryptionKeyVaultUrl] <String> [-DiskEncryptionKeyVaultId] <String> [[-KeyEncryptionKeyUrl] <String>]
 [[-KeyEncryptionKeyVaultId] <String>] [[-KeyEncryptionAlgorithm] <String>] [[-VolumeType] <String>]
 [[-SequenceVersion] <String>] [[-TypeHandlerVersion] <String>] [[-Name] <String>] [[-Passphrase] <String>]
 [-Force] [-DisableAutoUpgradeMinorVersion] [-SkipVmBackup] [-ExtensionType <String>]
 [-ExtensionPublisherName <String>] [-EncryptFormatAll] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c356c-106">AADClientSecretParameterSet</span><span class="sxs-lookup"><span data-stu-id="c356c-106">AADClientSecretParameterSet</span></span>
```
Set-AzVMDiskEncryptionExtension [-ResourceGroupName] <String> [-VMName] <String> [-AadClientID] <String>
 [-AadClientSecret] <String> [-DiskEncryptionKeyVaultUrl] <String> [-DiskEncryptionKeyVaultId] <String>
 [[-KeyEncryptionKeyUrl] <String>] [[-KeyEncryptionKeyVaultId] <String>] [[-KeyEncryptionAlgorithm] <String>]
 [[-VolumeType] <String>] [[-SequenceVersion] <String>] [[-TypeHandlerVersion] <String>] [[-Name] <String>]
 [[-Passphrase] <String>] [-Force] [-DisableAutoUpgradeMinorVersion] [-SkipVmBackup] [-ExtensionType <String>]
 [-ExtensionPublisherName <String>] [-EncryptFormatAll] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c356c-107">AADClientCertParameterSet</span><span class="sxs-lookup"><span data-stu-id="c356c-107">AADClientCertParameterSet</span></span>
```
Set-AzVMDiskEncryptionExtension [-ResourceGroupName] <String> [-VMName] <String> [-AadClientID] <String>
 [-AadClientCertThumbprint] <String> [-DiskEncryptionKeyVaultUrl] <String> [-DiskEncryptionKeyVaultId] <String>
 [[-KeyEncryptionKeyUrl] <String>] [[-KeyEncryptionKeyVaultId] <String>] [[-KeyEncryptionAlgorithm] <String>]
 [[-VolumeType] <String>] [[-SequenceVersion] <String>] [[-TypeHandlerVersion] <String>] [[-Name] <String>]
 [[-Passphrase] <String>] [-Force] [-DisableAutoUpgradeMinorVersion] [-SkipVmBackup] [-ExtensionType <String>]
 [-ExtensionPublisherName <String>] [-EncryptFormatAll] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c356c-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c356c-108">DESCRIPTION</span></span>
<span data-ttu-id="c356c-109">O cmdlet **set-AzVMDiskEncryptionExtension** habilita a criptografia em uma máquina virtual de serviço (IaaS) de infraestrutura em execução no Azure.</span><span class="sxs-lookup"><span data-stu-id="c356c-109">The **Set-AzVMDiskEncryptionExtension** cmdlet enables encryption on a running infrastructure as a service (IaaS) virtual machine in Azure.</span></span>
<span data-ttu-id="c356c-110">Esse cmdlet habilita a criptografia instalando a extensão de criptografia de disco na máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="c356c-110">This cmdlet enables encryption by installing the disk encryption extension on the virtual machine.</span></span>
<span data-ttu-id="c356c-111">Se nenhum parâmetro *Name* for especificado, será instalada uma extensão com o nome padrão AzureDiskEncryption para máquinas virtuais que executam o sistema operacional Windows ou AzureDiskEncryptionForLinux para máquinas virtuais Linux.</span><span class="sxs-lookup"><span data-stu-id="c356c-111">If no *Name* parameter is specified, an extension with the default name AzureDiskEncryption for virtual machines that run the Windows operating system or AzureDiskEncryptionForLinux for Linux virtual machines are installed.</span></span>
<span data-ttu-id="c356c-112">Esse cmdlet requer confirmação dos usuários como uma das etapas para habilitar a criptografia requer uma reinicialização da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="c356c-112">This cmdlet requires confirmation from the users as one of the steps to enable encryption requires a restart of the virtual machine.</span></span>
<span data-ttu-id="c356c-113">É recomendável que você salve o trabalho na máquina virtual antes de executar esse cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c356c-113">It is advised that you save your work on the virtual machine before you run this cmdlet.</span></span>

## <span data-ttu-id="c356c-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c356c-114">EXAMPLES</span></span>

### <span data-ttu-id="c356c-115">Exemplo 1: habilitar a criptografia</span><span class="sxs-lookup"><span data-stu-id="c356c-115">Example 1: Enable encryption</span></span>
```
$RGName = "MyResourceGroup"
$VMName = "MyTestVM"
$VaultName= "MyKeyVault"
$KeyVault = Get-AzKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId
Set-AzVMDiskEncryptionExtension -ResourceGroupName $RGName -VMName $VMName -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId
```

<span data-ttu-id="c356c-116">Este exemplo demonstra a habilitação da criptografia sem a especificação de credenciais do anúncio.</span><span class="sxs-lookup"><span data-stu-id="c356c-116">This example demonstrates enabling encryption without specifying AD credentials.</span></span>   

### <span data-ttu-id="c356c-117">Exemplo 2: habilitar a criptografia com entrada em pipeline</span><span class="sxs-lookup"><span data-stu-id="c356c-117">Example 2: Enable encryption with pipelined input</span></span>
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

<span data-ttu-id="c356c-118">Este exemplo demonstra o envio de parâmetros usando entrada em pipeline para habilitar a criptografia sem especificar credenciais do anúncio.</span><span class="sxs-lookup"><span data-stu-id="c356c-118">This example demonstrates sending parameters using pipelined input to enable encryption without specifying AD credentials.</span></span>  

### <span data-ttu-id="c356c-119">Exemplo 3: habilitar a criptografia usando o ID de cliente do Azure AD e o segredo do cliente</span><span class="sxs-lookup"><span data-stu-id="c356c-119">Example 3: Enable encryption using Azure AD Client ID and Client Secret</span></span>
```
$RGName = "MyResourceGroup"
$VMName = "MyTestVM"
$AADClientID = "<clientID of your Azure AD app>"
$AADClientSecret = "<clientSecret of your Azure AD app>"
$VaultName= "MyKeyVault"
$KeyVault = Get-AzKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId
Set-AzVMDiskEncryptionExtension -ResourceGroupName $RGName -VMName $VMName -AadClientID $AADClientID -AadClientSecret $AADClientSecret -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId
```

<span data-ttu-id="c356c-120">Este exemplo ativa a criptografia usando o ID de cliente do Azure AD e o segredo do cliente.</span><span class="sxs-lookup"><span data-stu-id="c356c-120">This example enables encryption using Azure AD client ID, and client secret.</span></span>

### <span data-ttu-id="c356c-121">Exemplo 4: habilitar a criptografia usando a ID de cliente do Azure AD e a impressão digital de certificação do cliente</span><span class="sxs-lookup"><span data-stu-id="c356c-121">Example 4: Enable encryption using Azure AD client ID and client certification thumbprint</span></span>
```
$RGName = "MyResourceGroup"
$VMName = "MyTestVM"
#The KeyVault must have enabledForDiskEncryption property set on it
$VaultName= "MyKeyVault"
$KeyVault = Get-AzKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId

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
Set-AzVMDiskEncryptionExtension -ResourceGroupName $RGName -VMName $VMName -AadClientID $AADClientID -AadClientCertThumbprint $AADClientCertThumbprint -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId
```

<span data-ttu-id="c356c-122">Este exemplo habilita a criptografia usando a ID de cliente do Azure AD e as impressões de certificação do cliente.</span><span class="sxs-lookup"><span data-stu-id="c356c-122">This example enables encryption using Azure AD client ID and client certification thumbprints.</span></span>

### <span data-ttu-id="c356c-123">Exemplo 5: habilitar a criptografia usando a identificação de cliente do Azure AD, o segredo do cliente e a chave de criptografia do disco decodificada usando chave de criptografia de chave</span><span class="sxs-lookup"><span data-stu-id="c356c-123">Example 5: Enable encryption using Azure AD client ID, client secret, and wrap disk encryption key by using key encryption key</span></span>
```
$RGName = "MyResourceGroup"
$VMName = "MyTestVM"

$AADClientID = "<clientID of your Azure AD app>"
$AADClientSecret = "<clientSecret of your Azure AD app>"

$VaultName= "MyKeyVault"
$KeyVault = Get-AzKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId

$KEKName = "MyKeyEncryptionKey"
$KEK = Add-AzKeyVaultKey -VaultName $VaultName -Name $KEKName -Destination "Software"
$KeyEncryptionKeyUrl = $KEK.Key.kid

Set-AzVMDiskEncryptionExtension -ResourceGroupName $RGName -VMName $VMName -AadClientID $AADClientID -AadClientSecret $AADClientSecret -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId -KeyEncryptionKeyUrl $KeyEncryptionKeyUrl -KeyEncryptionKeyVaultId $KeyVaultResourceId
```

<span data-ttu-id="c356c-124">Este exemplo habilita a criptografia usando a ID de cliente do Azure AD, o segredo do cliente e a chave de criptografia do disco de quebra de linha usando a chave de criptografia de chave.</span><span class="sxs-lookup"><span data-stu-id="c356c-124">This example enables encryption using Azure AD client ID, client secret, and wrap disk encryption key by using the key encryption key.</span></span>

### <span data-ttu-id="c356c-125">Exemplo 6: habilitar a criptografia usando a ID de cliente do Azure AD, a impressão digital de certificado de cliente e quebrar o disco EncryptionKey usando chave de criptografia de chave</span><span class="sxs-lookup"><span data-stu-id="c356c-125">Example 6: Enable encryption using Azure AD client ID, client cert thumbprint, and wrap disk encryptionkey by using key encryption key</span></span>
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
Set-AzVMDiskEncryptionExtension -ResourceGroupName $RGname -VMName $VMName -AadClientID $AADClientID -AadClientCertThumbprint $AADClientCertThumbprint -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId -KeyEncryptionKeyUrl $KeyEncryptionKeyUrl -KeyEncryptionKeyVaultId $KeyVaultResourceId
```

<span data-ttu-id="c356c-126">Este exemplo habilita a criptografia usando a ID de cliente do Azure AD, a impressão digital de certificado de cliente e a chave de criptografia de disco decodificada usando chave de criptografia.</span><span class="sxs-lookup"><span data-stu-id="c356c-126">This example enables encryption using Azure AD client ID, client cert thumbprint, and wrap disk encryption key by using key encryption key.</span></span>

## <span data-ttu-id="c356c-127">OS</span><span class="sxs-lookup"><span data-stu-id="c356c-127">PARAMETERS</span></span>

### <span data-ttu-id="c356c-128">-AadClientCertThumbprint</span><span class="sxs-lookup"><span data-stu-id="c356c-128">-AadClientCertThumbprint</span></span>
<span data-ttu-id="c356c-129">Especifica a impressão digital do certificado de cliente do aplicativo AzureActive Directory (Azure AD) que tem permissões para gravar segredos no **keyvault**.</span><span class="sxs-lookup"><span data-stu-id="c356c-129">Specifies the thumbprint of the AzureActive Directory (Azure AD) application client certificate that has permissions to write secrets to **KeyVault**.</span></span>
<span data-ttu-id="c356c-130">Como pré-requisito, o certificado de cliente do Azure AD deve ser implantado anteriormente no repositório de certificados do computador local da máquina virtual `my` .</span><span class="sxs-lookup"><span data-stu-id="c356c-130">As a prerequisite, the Azure AD client certificate must be previously deployed to the virtual machine's local computer `my` certificate store.</span></span>
<span data-ttu-id="c356c-131">O cmdlet Add-AzVMSecret pode ser usado para implantar um certificado em uma máquina virtual no Azure.</span><span class="sxs-lookup"><span data-stu-id="c356c-131">The Add-AzVMSecret cmdlet can be used to deploy a certificate to a virtual machine in Azure.</span></span>
<span data-ttu-id="c356c-132">Para obter mais detalhes, consulte a ajuda do cmdlet **Add-AzVMSecret** .</span><span class="sxs-lookup"><span data-stu-id="c356c-132">For more details, see the **Add-AzVMSecret** cmdlet help.</span></span>
<span data-ttu-id="c356c-133">O certificado deve ser implantado anteriormente no computador local da máquina virtual meu repositório de certificados.</span><span class="sxs-lookup"><span data-stu-id="c356c-133">The certificate must be previously deployed to the virtual machine local computer my certificate store.</span></span>

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

### <span data-ttu-id="c356c-134">-AadClientID</span><span class="sxs-lookup"><span data-stu-id="c356c-134">-AadClientID</span></span>
<span data-ttu-id="c356c-135">Especifica a ID do cliente do aplicativo Azure AD que tem permissões para gravar segredos no **keyvault**.</span><span class="sxs-lookup"><span data-stu-id="c356c-135">Specifies the client ID of the Azure AD application that has permissions to write secrets to **KeyVault**.</span></span>

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

### <span data-ttu-id="c356c-136">-AadClientSecret</span><span class="sxs-lookup"><span data-stu-id="c356c-136">-AadClientSecret</span></span>
<span data-ttu-id="c356c-137">Especifica o segredo do cliente do aplicativo Azure AD que tem permissões para gravar segredos no **keyvault**.</span><span class="sxs-lookup"><span data-stu-id="c356c-137">Specifies the client secret of the Azure AD application that has permissions to write secrets to **KeyVault**.</span></span>

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

### <span data-ttu-id="c356c-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c356c-138">-DefaultProfile</span></span>
<span data-ttu-id="c356c-139">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c356c-139">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c356c-140">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="c356c-140">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="c356c-141">Indica que esse cmdlet desabilita a atualização automática da versão secundária da extensão.</span><span class="sxs-lookup"><span data-stu-id="c356c-141">Indicates that this cmdlet disables auto-upgrade of the minor version of the extension.</span></span>

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

### <span data-ttu-id="c356c-142">-DiskEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="c356c-142">-DiskEncryptionKeyVaultId</span></span>
<span data-ttu-id="c356c-143">Especifica a ID do recurso do **cofre** para o qual as chaves de criptografia da máquina virtual devem ser carregadas.</span><span class="sxs-lookup"><span data-stu-id="c356c-143">Specifies the resource ID of the **KeyVault** to which the virtual machine encryption keys should be uploaded.</span></span>

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

### <span data-ttu-id="c356c-144">-DiskEncryptionKeyVaultUrl</span><span class="sxs-lookup"><span data-stu-id="c356c-144">-DiskEncryptionKeyVaultUrl</span></span>
<span data-ttu-id="c356c-145">Especifica a URL do **keyvault** para a qual as chaves de criptografia da máquina virtual devem ser carregadas.</span><span class="sxs-lookup"><span data-stu-id="c356c-145">Specifies the **KeyVault** URL to which the virtual machine encryption keys should be uploaded.</span></span>

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

### <span data-ttu-id="c356c-146">-EncryptFormatAll</span><span class="sxs-lookup"><span data-stu-id="c356c-146">-EncryptFormatAll</span></span>
<span data-ttu-id="c356c-147">Encrypt-Format todas as unidades de dados que ainda não estão criptografadas</span><span class="sxs-lookup"><span data-stu-id="c356c-147">Encrypt-Format all data drives that are not already encrypted</span></span>

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

### <span data-ttu-id="c356c-148">-ExtensionPublisherName</span><span class="sxs-lookup"><span data-stu-id="c356c-148">-ExtensionPublisherName</span></span>
<span data-ttu-id="c356c-149">O nome do fornecedor da extensão.</span><span class="sxs-lookup"><span data-stu-id="c356c-149">The extension publisher name.</span></span> <span data-ttu-id="c356c-150">Especifique esse parâmetro somente para substituir o valor padrão de "Microsoft. Azure. Security".</span><span class="sxs-lookup"><span data-stu-id="c356c-150">Specify this parameter only to override the default value of "Microsoft.Azure.Security".</span></span>

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

### <span data-ttu-id="c356c-151">-ExtensionType</span><span class="sxs-lookup"><span data-stu-id="c356c-151">-ExtensionType</span></span>
<span data-ttu-id="c356c-152">O tipo de extensão.</span><span class="sxs-lookup"><span data-stu-id="c356c-152">The extension type.</span></span> <span data-ttu-id="c356c-153">Especifique esse parâmetro para substituir o valor padrão de "AzureDiskEncryption" para VMs do Windows e "AzureDiskEncryptionForLinux" para VMs Linux.</span><span class="sxs-lookup"><span data-stu-id="c356c-153">Specify this parameter to override its default value of "AzureDiskEncryption" for Windows VMs and "AzureDiskEncryptionForLinux" for Linux VMs.</span></span>

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

### <span data-ttu-id="c356c-154">-Force</span><span class="sxs-lookup"><span data-stu-id="c356c-154">-Force</span></span>
<span data-ttu-id="c356c-155">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="c356c-155">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c356c-156">-KeyEncryptionAlgorithm</span><span class="sxs-lookup"><span data-stu-id="c356c-156">-KeyEncryptionAlgorithm</span></span>
<span data-ttu-id="c356c-157">Especifica o algoritmo que é usado para quebrar e desencapsular a chave de criptografia da chave da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="c356c-157">Specifies the algorithm that is used to wrap and unwrap the key encryption key of the virtual machine.</span></span>
<span data-ttu-id="c356c-158">O valor padrão é RSA-OAEP.</span><span class="sxs-lookup"><span data-stu-id="c356c-158">The default value is RSA-OAEP.</span></span>

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

### <span data-ttu-id="c356c-159">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="c356c-159">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="c356c-160">Especifica a URL da chave de criptografia da chave que é usada para encapsular e descodificar a chave de criptografia da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="c356c-160">Specifies the URL of the key encryption key that is used to wrap and unwrap the virtual machine encryption key.</span></span>
<span data-ttu-id="c356c-161">Deve ser a URL completa com versão.</span><span class="sxs-lookup"><span data-stu-id="c356c-161">This must be the full versioned URL.</span></span>

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

### <span data-ttu-id="c356c-162">-KeyEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="c356c-162">-KeyEncryptionKeyVaultId</span></span>
<span data-ttu-id="c356c-163">Especifica a ID do **recurso que contém a chave** de criptografia de chave que é usada para encapsular e desencapsular a chave de criptografia da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="c356c-163">Specifies the resource ID of the **KeyVault** that contains key encryption key that is used to wrap and unwrap the virtual machine encryption key.</span></span>
<span data-ttu-id="c356c-164">Deve ser uma URL completa com versão.</span><span class="sxs-lookup"><span data-stu-id="c356c-164">This must be a full versioned URL.</span></span>

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

### <span data-ttu-id="c356c-165">-Nome</span><span class="sxs-lookup"><span data-stu-id="c356c-165">-Name</span></span>
<span data-ttu-id="c356c-166">Especifica o nome do recurso do Gerenciador de recursos do Azure que representa a extensão.</span><span class="sxs-lookup"><span data-stu-id="c356c-166">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span>
<span data-ttu-id="c356c-167">O valor padrão é AzureDiskEncryption para máquinas virtuais que executam o sistema operacional Windows ou o AzureDiskEncryptionForLinux para máquinas virtuais Linux.</span><span class="sxs-lookup"><span data-stu-id="c356c-167">The default value is AzureDiskEncryption for virtual machines that run the Windows operating system or AzureDiskEncryptionForLinux for Linux virtual machines.</span></span>

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

### <span data-ttu-id="c356c-168">-Senha</span><span class="sxs-lookup"><span data-stu-id="c356c-168">-Passphrase</span></span>
<span data-ttu-id="c356c-169">Especifica a senha usada para criptografar apenas máquinas virtuais Linux.</span><span class="sxs-lookup"><span data-stu-id="c356c-169">Specifies the passphrase used for encrypting Linux virtual machines only.</span></span>
<span data-ttu-id="c356c-170">Esse parâmetro não é usado para máquinas virtuais que executam o sistema operacional Windows.</span><span class="sxs-lookup"><span data-stu-id="c356c-170">This parameter is not used for virtual machines that run the Windows operating system.</span></span>

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

### <span data-ttu-id="c356c-171">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c356c-171">-ResourceGroupName</span></span>
<span data-ttu-id="c356c-172">Especifica o nome do grupo de recursos da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="c356c-172">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="c356c-173">-SequenceVersion</span><span class="sxs-lookup"><span data-stu-id="c356c-173">-SequenceVersion</span></span>
<span data-ttu-id="c356c-174">Especifica o número de sequência das operações de criptografia para uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="c356c-174">Specifies the sequence number of the encryption operations for a virtual machine.</span></span>
<span data-ttu-id="c356c-175">Isso é exclusivo por cada operação de criptografia executada na mesma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="c356c-175">This is unique per each encryption operation performed on the same virtual machine.</span></span>
<span data-ttu-id="c356c-176">O cmdlet Get-AzVMExtension pode ser usado para recuperar o número de sequência anterior que foi usado.</span><span class="sxs-lookup"><span data-stu-id="c356c-176">The Get-AzVMExtension cmdlet can be used to retrieve the previous sequence number that was used.</span></span>

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

### <span data-ttu-id="c356c-177">-SkipVmBackup</span><span class="sxs-lookup"><span data-stu-id="c356c-177">-SkipVmBackup</span></span>
<span data-ttu-id="c356c-178">Ignorar a criação de backup para VMs Linux</span><span class="sxs-lookup"><span data-stu-id="c356c-178">Skip backup creation for Linux VMs</span></span>

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

### <span data-ttu-id="c356c-179">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="c356c-179">-TypeHandlerVersion</span></span>
<span data-ttu-id="c356c-180">Especifica a versão da extensão de criptografia.</span><span class="sxs-lookup"><span data-stu-id="c356c-180">Specifies the version of the encryption extension.</span></span>

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

### <span data-ttu-id="c356c-181">-VMName</span><span class="sxs-lookup"><span data-stu-id="c356c-181">-VMName</span></span>
<span data-ttu-id="c356c-182">Especifica o nome da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="c356c-182">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="c356c-183">-Volumetype</span><span class="sxs-lookup"><span data-stu-id="c356c-183">-VolumeType</span></span>
<span data-ttu-id="c356c-184">Especifica o tipo de volumes da máquina virtual para executar a operação de criptografia.</span><span class="sxs-lookup"><span data-stu-id="c356c-184">Specifies the type of virtual machine volumes to perform the encryption operation.</span></span>
<span data-ttu-id="c356c-185">Os valores permitidos para máquinas virtuais que executam o sistema operacional Windows são os seguintes: ALL, so e data.</span><span class="sxs-lookup"><span data-stu-id="c356c-185">Allowed values for virtual machines that run the Windows operating system are as follows: All, OS, and Data.</span></span>
<span data-ttu-id="c356c-186">Os valores permitidos para máquinas virtuais Linux são os seguintes: somente dados.</span><span class="sxs-lookup"><span data-stu-id="c356c-186">The allowed values for Linux virtual machines are as follows: Data only.</span></span>

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

### <span data-ttu-id="c356c-187">-Confirme</span><span class="sxs-lookup"><span data-stu-id="c356c-187">-Confirm</span></span>
<span data-ttu-id="c356c-188">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c356c-188">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c356c-189">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c356c-189">-WhatIf</span></span>
<span data-ttu-id="c356c-190">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c356c-190">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c356c-191">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c356c-191">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c356c-192">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c356c-192">CommonParameters</span></span>
<span data-ttu-id="c356c-193">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c356c-193">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c356c-194">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c356c-194">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c356c-195">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c356c-195">INPUTS</span></span>

### <span data-ttu-id="c356c-196">System. String</span><span class="sxs-lookup"><span data-stu-id="c356c-196">System.String</span></span>

### <span data-ttu-id="c356c-197">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="c356c-197">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="c356c-198">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c356c-198">OUTPUTS</span></span>

### <span data-ttu-id="c356c-199">Microsoft. Azure. Commands. COMPUTE. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="c356c-199">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="c356c-200">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c356c-200">NOTES</span></span>

## <span data-ttu-id="c356c-201">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c356c-201">RELATED LINKS</span></span>

[<span data-ttu-id="c356c-202">Add-AzVMSecret</span><span class="sxs-lookup"><span data-stu-id="c356c-202">Add-AzVMSecret</span></span>](./Add-AzVMSecret.md)

[<span data-ttu-id="c356c-203">Get-AzVMDiskEncryptionStatus</span><span class="sxs-lookup"><span data-stu-id="c356c-203">Get-AzVMDiskEncryptionStatus</span></span>](./Get-AzVMDiskEncryptionStatus.md)

[<span data-ttu-id="c356c-204">Remove-AzVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="c356c-204">Remove-AzVMDiskEncryptionExtension</span></span>](./Remove-AzVMDiskEncryptionExtension.md)


