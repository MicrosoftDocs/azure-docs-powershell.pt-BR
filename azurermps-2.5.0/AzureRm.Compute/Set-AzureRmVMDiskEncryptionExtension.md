---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 6BCB36BC-F5E6-4EDD-983C-8BDE7A9B004D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmdiskencryptionextension
schema: 2.0.0
ms.openlocfilehash: 76bdebc68f1fafef127863ef753c28fce7034fe0
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93786125"
---
# <span data-ttu-id="5e238-101">Set-AzureRmVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="5e238-101">Set-AzureRmVMDiskEncryptionExtension</span></span>

## <span data-ttu-id="5e238-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5e238-102">SYNOPSIS</span></span>
<span data-ttu-id="5e238-103">Habilita a criptografia em uma máquina virtual IaaS em execução no Azure.</span><span class="sxs-lookup"><span data-stu-id="5e238-103">Enables encryption on a running IaaS virtual machine in Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5e238-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5e238-104">SYNTAX</span></span>

### <span data-ttu-id="5e238-105">AADClientSecretParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="5e238-105">AADClientSecretParameterSet (Default)</span></span>
```
Set-AzureRmVMDiskEncryptionExtension [-ResourceGroupName] <String> [-VMName] <String> [-AadClientID] <String>
 [-AadClientSecret] <String> [-DiskEncryptionKeyVaultUrl] <String> [-DiskEncryptionKeyVaultId] <String>
 [[-KeyEncryptionKeyUrl] <String>] [[-KeyEncryptionKeyVaultId] <String>] [[-KeyEncryptionAlgorithm] <String>]
 [[-VolumeType] <String>] [[-SequenceVersion] <String>] [[-TypeHandlerVersion] <String>] [[-Name] <String>]
 [[-Passphrase] <String>] [-Force] [-DisableAutoUpgradeMinorVersion] [-SkipVmBackup] [-ExtensionType <String>]
 [-ExtensionPublisherName <String>] [-EncryptFormatAll] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5e238-106">AADClientCertParameterSet</span><span class="sxs-lookup"><span data-stu-id="5e238-106">AADClientCertParameterSet</span></span>
```
Set-AzureRmVMDiskEncryptionExtension [-ResourceGroupName] <String> [-VMName] <String> [-AadClientID] <String>
 [-AadClientCertThumbprint] <String> [-DiskEncryptionKeyVaultUrl] <String> [-DiskEncryptionKeyVaultId] <String>
 [[-KeyEncryptionKeyUrl] <String>] [[-KeyEncryptionKeyVaultId] <String>] [[-KeyEncryptionAlgorithm] <String>]
 [[-VolumeType] <String>] [[-SequenceVersion] <String>] [[-TypeHandlerVersion] <String>] [[-Name] <String>]
 [[-Passphrase] <String>] [-Force] [-DisableAutoUpgradeMinorVersion] [-SkipVmBackup] [-ExtensionType <String>]
 [-ExtensionPublisherName <String>] [-EncryptFormatAll] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5e238-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5e238-107">DESCRIPTION</span></span>
<span data-ttu-id="5e238-108">O cmdlet **set-AzureRmVMDiskEncryptionExtension** habilita a criptografia em uma máquina virtual de serviço (IaaS) de infraestrutura em execução no Azure.</span><span class="sxs-lookup"><span data-stu-id="5e238-108">The **Set-AzureRmVMDiskEncryptionExtension** cmdlet enables encryption on a running infrastructure as a service (IaaS) virtual machine in Azure.</span></span>
<span data-ttu-id="5e238-109">Esse cmdlet habilita a criptografia instalando a extensão de criptografia de disco na máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="5e238-109">This cmdlet enables encryption by installing the disk encryption extension on the virtual machine.</span></span>
<span data-ttu-id="5e238-110">Se nenhum parâmetro *Name* for especificado, será instalada uma extensão com o nome padrão AzureDiskEncryption para máquinas virtuais que executam o sistema operacional Windows ou AzureDiskEncryptionForLinux para máquinas virtuais Linux.</span><span class="sxs-lookup"><span data-stu-id="5e238-110">If no *Name* parameter is specified, an extension with the default name AzureDiskEncryption for virtual machines that run the Windows operating system or AzureDiskEncryptionForLinux for Linux virtual machines are installed.</span></span>
<span data-ttu-id="5e238-111">Esse cmdlet requer confirmação dos usuários como uma das etapas para habilitar a criptografia requer uma reinicialização da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="5e238-111">This cmdlet requires confirmation from the users as one of the steps to enable encryption requires a restart of the virtual machine.</span></span>
<span data-ttu-id="5e238-112">É recomendável que você salve o trabalho na máquina virtual antes de executar esse cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5e238-112">It is advised that you save your work on the virtual machine before you run this cmdlet.</span></span>

## <span data-ttu-id="5e238-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5e238-113">EXAMPLES</span></span>

### <span data-ttu-id="5e238-114">Exemplo 1: habilitar a criptografia usando o ID de cliente do Azure AD e o segredo do cliente</span><span class="sxs-lookup"><span data-stu-id="5e238-114">Example 1: Enable encryption using Azure AD Client ID and Client Secret</span></span>
```
$RGName = "MyResourceGroup"
$VMName = "MyTestVM"
$AADClientID = "<clientID of your Azure AD app>"
$AADClientSecret = "<clientSecret of your Azure AD app>"
$VaultName= "MyKeyVault"
$KeyVault = Get-AzureRmKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId
Set-AzureRmVMDiskEncryptionExtension -ResourceGroupName $RGName -VMName $VMName -AadClientID $AADClientID -AadClientSecret $AADClientSecret -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId
```

<span data-ttu-id="5e238-115">Este exemplo ativa a criptografia usando o ID de cliente do Azure AD e o segredo do cliente.</span><span class="sxs-lookup"><span data-stu-id="5e238-115">This example enables encryption using Azure AD client ID, and client secret.</span></span>

### <span data-ttu-id="5e238-116">Exemplo 2: habilitar a criptografia usando a ID de cliente do Azure AD e a impressão digital de certificação do cliente</span><span class="sxs-lookup"><span data-stu-id="5e238-116">Example 2: Enable encryption using Azure AD client ID and client certification thumbprint</span></span>
```
$RGName = "MyResourceGroup"
$VMName = "MyTestVM"
#The KeyVault must have enabledForDiskEncryption property set on it
$VaultName= "MyKeyVault"
$KeyVault = Get-AzureRmKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId

# create Azure AD application and associate the certificate
$CertPath = "C:\certificates\examplecert.pfx"
$CertPassword = "Password"
$Cert = New-Object System.Security.Cryptography.X509Certificates.X509Certificate2($CertPath, $CertPassword)
$KeyValue = [System.Convert]::ToBase64String($cert.GetRawCertData())
$AzureAdApplication = New-AzureRmADApplication -DisplayName "<Your Application Display Name>" -HomePage "<https://YourApplicationHomePage>" -IdentifierUris "<https://YouApplicationUri>" -KeyValue $KeyValue -KeyType AsymmetricX509Cert 
$ServicePrincipal = New-AzureRmADServicePrincipal -ApplicationId $AzureAdApplication.ApplicationId

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
Set-AzureKeyVaultSecret -VaultName $VaultName -Name $KeyVaultSecretName -SecretValue $Secret
Set-AzureRmKeyVaultAccessPolicy -VaultName $VaultName -ResourceGroupName $RGName -EnabledForDeployment

#deploy cert to VM
$CertUrl = (Get-AzureKeyVaultSecret -VaultName $VaultName -Name $KeyVaultSecretName).Id
$SourceVaultId = (Get-AzureRmKeyVault -VaultName $VaultName -ResourceGroupName $RGName).ResourceId
$VM = Get-AzureRmVM -ResourceGroupName $RGName -Name $VMName 
$VM = Add-AzureRmVMSecret -VM $VM -SourceVaultId $SourceVaultId -CertificateStore "My" -CertificateUrl $CertUrl
Update-AzureRmVM -VM $VM -ResourceGroupName $RGName 

#Enable encryption on the virtual machine using Azure AD client ID and client cert thumbprint
Set-AzureRmVMDiskEncryptionExtension -ResourceGroupName $RGName -VMName $VMName -AadClientID $AADClientID -AadClientCertThumbprint $AADClientCertThumbprint -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId
```

<span data-ttu-id="5e238-117">Este exemplo habilita a criptografia usando a ID de cliente do Azure AD e as impressões de certificação do cliente.</span><span class="sxs-lookup"><span data-stu-id="5e238-117">This example enables encryption using Azure AD client ID and client certification thumbprints.</span></span>

### <span data-ttu-id="5e238-118">Exemplo 3: habilitar a criptografia usando a identificação de cliente do Azure AD, o segredo do cliente e a chave de criptografia do disco decodificada usando chave de criptografia de chave</span><span class="sxs-lookup"><span data-stu-id="5e238-118">Example 3: Enable encryption using Azure AD client ID, client secret, and wrap disk encryption key by using key encryption key</span></span>
```
$RGName = "MyResourceGroup"
$VMName = "MyTestVM"

$AADClientID = "<clientID of your Azure AD app>"
$AADClientSecret = "<clientSecret of your Azure AD app>"

$VaultName= "MyKeyVault"
$KeyVault = Get-AzureRmKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId

$KEK = Add-AzureKeyVaultKey -VaultName $VaultName -Name $KEKName -Destination "Software"
$KeyEncryptionKeyUrl = $KEK.Key.kid

Set-AzureRmVMDiskEncryptionExtension -ResourceGroupName $RGName -VMName $VMName -AadClientID $AADClientID -AadClientSecret $AADClientSecret -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId -KeyEncryptionKeyUrl $KeyEncryptionKeyUrl -KeyEncryptionKeyVaultId $KeyVaultResourceId
```

<span data-ttu-id="5e238-119">Este exemplo habilita a criptografia usando a ID de cliente do Azure AD, o segredo do cliente e a chave de criptografia do disco de quebra de linha usando a chave de criptografia de chave.</span><span class="sxs-lookup"><span data-stu-id="5e238-119">This example enables encryption using Azure AD client ID, client secret, and wrap disk encryption key by using the key encryption key.</span></span>

### <span data-ttu-id="5e238-120">Exemplo 4: habilitar a criptografia usando a ID de cliente do Azure AD, a impressão digital de certificado de cliente e o encapsulamento de disco EncryptionKey usando chave de criptografia de chave</span><span class="sxs-lookup"><span data-stu-id="5e238-120">Example 4: Enable encryption using Azure AD client ID, client cert thumbprint, and wrap disk encryptionkey by using key encryption key</span></span>
```
$RGName = "MyResourceGroup"
$VMName = "MyTestVM"
#The KeyVault must have enabledForDiskEncryption property set on it
$VaultName= "MyKeyVault"
$KeyVault = Get-AzureRmKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId
$KEK = Add-AzureKeyVaultKey -VaultName $VaultName -Name $KEKName -Destination "Software"
$KeyEncryptionKeyUrl = $KEK.Key.kid

# create Azure AD application and associate the certificate
$CertPath = "C:\certificates\examplecert.pfx"
$CertPassword = "Password"
$Cert = New-Object System.Security.Cryptography.X509Certificates.X509Certificate2($CertPath, $CertPassword)
$KeyValue = [System.Convert]::ToBase64String($cert.GetRawCertData())
$AzureAdApplication = New-AzureRmADApplication -DisplayName "<Your Application Display Name>" -HomePage "<https://YourApplicationHomePage>" -IdentifierUris "<https://YouApplicationUri>" -KeyValue $KeyValue -KeyType AsymmetricX509Cert 
$ServicePrincipal = New-AzureRmADServicePrincipal -ApplicationId $AzureAdApplication.ApplicationId

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
Set-AzureKeyVaultSecret -VaultName $VaultName-Name $KeyVaultSecretName -SecretValue $Secret
Set-AzureRmKeyVaultAccessPolicy -VaultName $VaultName -ResourceGroupName $RGName -EnabledForDeployment

#deploy cert to VM
$CertUrl = (Get-AzureKeyVaultSecret -VaultName $VaultName -Name $KeyVaultSecretName).Id
$SourceVaultId = (Get-AzureRmKeyVault -VaultName $VaultName -ResourceGroupName $RGName).ResourceId
$VM = Get-AzureRmVM -ResourceGroupName $RGName -Name $VMName 
$VM = Add-AzureRmVMSecret -VM $VM -SourceVaultId $SourceVaultId -CertificateStore "My" -CertificateUrl $CertUrl 
Update-AzureRmVM -VM $VM -ResourceGroupName $RGName 

#Enable encryption on the virtual machine using Azure AD client ID and client cert thumbprint
Set-AzureRmVMDiskEncryptionExtension -ResourceGroupName $RGname -VMName $VMName -AadClientID $AADClientID -AadClientCertThumbprint $AADClientCertThumbprint -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId
```

<span data-ttu-id="5e238-121">Este exemplo habilita a criptografia usando a ID de cliente do Azure AD, a impressão digital de certificado de cliente e a chave de criptografia de disco decodificada usando chave de criptografia.</span><span class="sxs-lookup"><span data-stu-id="5e238-121">This example enables encryption using Azure AD client ID, client cert thumbprint, and wrap disk encryption key by using key encryption key.</span></span>

## <span data-ttu-id="5e238-122">OS</span><span class="sxs-lookup"><span data-stu-id="5e238-122">PARAMETERS</span></span>

### <span data-ttu-id="5e238-123">-AadClientCertThumbprint</span><span class="sxs-lookup"><span data-stu-id="5e238-123">-AadClientCertThumbprint</span></span>
<span data-ttu-id="5e238-124">Especifica a impressão digital do certificado de cliente do aplicativo AzureActive Directory (Azure AD) que tem permissões para gravar segredos no **keyvault**.</span><span class="sxs-lookup"><span data-stu-id="5e238-124">Specifies the thumbprint of the AzureActive Directory (Azure AD) application client certificate that has permissions to write secrets to **KeyVault**.</span></span>
<span data-ttu-id="5e238-125">Como pré-requisito, o certificado de cliente do Azure AD deve ser implantado anteriormente no repositório de certificados do computador local da máquina virtual `my` .</span><span class="sxs-lookup"><span data-stu-id="5e238-125">As a prerequisite, the Azure AD client certificate must be previously deployed to the virtual machine's local computer `my` certificate store.</span></span>
<span data-ttu-id="5e238-126">O cmdlet Add-AzureRmVMSecret pode ser usado para implantar um certificado em uma máquina virtual no Azure.</span><span class="sxs-lookup"><span data-stu-id="5e238-126">The Add-AzureRmVMSecret cmdlet can be used to deploy a certificate to a virtual machine in Azure.</span></span>
<span data-ttu-id="5e238-127">Para obter mais detalhes, consulte a ajuda do cmdlet **Add-AzureRmVMSecret** .</span><span class="sxs-lookup"><span data-stu-id="5e238-127">For more details, see the **Add-AzureRmVMSecret** cmdlet help.</span></span>
<span data-ttu-id="5e238-128">O certificado deve ser implantado anteriormente no computador local da máquina virtual meu repositório de certificados.</span><span class="sxs-lookup"><span data-stu-id="5e238-128">The certificate must be previously deployed to the virtual machine local computer my certificate store.</span></span>

```yaml
Type: String
Parameter Sets: AADClientCertParameterSet
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e238-129">-AadClientID</span><span class="sxs-lookup"><span data-stu-id="5e238-129">-AadClientID</span></span>
<span data-ttu-id="5e238-130">Especifica a ID do cliente do aplicativo Azure AD que tem permissões para gravar segredos no **keyvault**.</span><span class="sxs-lookup"><span data-stu-id="5e238-130">Specifies the client ID of the Azure AD application that has permissions to write secrets to **KeyVault**.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e238-131">-AadClientSecret</span><span class="sxs-lookup"><span data-stu-id="5e238-131">-AadClientSecret</span></span>
<span data-ttu-id="5e238-132">Especifica o segredo do cliente do aplicativo Azure AD que tem permissões para gravar segredos no **keyvault**.</span><span class="sxs-lookup"><span data-stu-id="5e238-132">Specifies the client secret of the Azure AD application that has permissions to write secrets to **KeyVault**.</span></span>

```yaml
Type: String
Parameter Sets: AADClientSecretParameterSet
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e238-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e238-133">-DefaultProfile</span></span>
<span data-ttu-id="5e238-134">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5e238-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e238-135">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="5e238-135">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="5e238-136">Indica que esse cmdlet desabilita a atualização automática da versão secundária da extensão.</span><span class="sxs-lookup"><span data-stu-id="5e238-136">Indicates that this cmdlet disables auto-upgrade of the minor version of the extension.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 14
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e238-137">-DiskEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="5e238-137">-DiskEncryptionKeyVaultId</span></span>
<span data-ttu-id="5e238-138">Especifica a ID do recurso do **cofre** para o qual as chaves de criptografia da máquina virtual devem ser carregadas.</span><span class="sxs-lookup"><span data-stu-id="5e238-138">Specifies the resource ID of the **KeyVault** to which the virtual machine encryption keys should be uploaded.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e238-139">-DiskEncryptionKeyVaultUrl</span><span class="sxs-lookup"><span data-stu-id="5e238-139">-DiskEncryptionKeyVaultUrl</span></span>
<span data-ttu-id="5e238-140">Especifica a URL do **keyvault** para a qual as chaves de criptografia da máquina virtual devem ser carregadas.</span><span class="sxs-lookup"><span data-stu-id="5e238-140">Specifies the **KeyVault** URL to which the virtual machine encryption keys should be uploaded.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e238-141">-EncryptFormatAll</span><span class="sxs-lookup"><span data-stu-id="5e238-141">-EncryptFormatAll</span></span>
<span data-ttu-id="5e238-142">Encrypt-Format todas as unidades de dados que ainda não estão criptografadas</span><span class="sxs-lookup"><span data-stu-id="5e238-142">Encrypt-Format all data drives that are not already encrypted</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e238-143">-ExtensionPublisherName</span><span class="sxs-lookup"><span data-stu-id="5e238-143">-ExtensionPublisherName</span></span>
<span data-ttu-id="5e238-144">O nome do fornecedor da extensão.</span><span class="sxs-lookup"><span data-stu-id="5e238-144">The extension publisher name.</span></span> <span data-ttu-id="5e238-145">Especifique esse parâmetro somente para substituir o valor padrão de "Microsoft. Azure. Security".</span><span class="sxs-lookup"><span data-stu-id="5e238-145">Specify this parameter only to override the default value of "Microsoft.Azure.Security".</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e238-146">-ExtensionType</span><span class="sxs-lookup"><span data-stu-id="5e238-146">-ExtensionType</span></span>
<span data-ttu-id="5e238-147">O tipo de extensão.</span><span class="sxs-lookup"><span data-stu-id="5e238-147">The extension type.</span></span> <span data-ttu-id="5e238-148">Especifique esse parâmetro para substituir o valor padrão de "AzureDiskEncryption" para VMs do Windows e "AzureDiskEncryptionForLinux" para VMs Linux.</span><span class="sxs-lookup"><span data-stu-id="5e238-148">Specify this parameter to override its default value of "AzureDiskEncryption" for Windows VMs and "AzureDiskEncryptionForLinux" for Linux VMs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e238-149">-Force</span><span class="sxs-lookup"><span data-stu-id="5e238-149">-Force</span></span>
<span data-ttu-id="5e238-150">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="5e238-150">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e238-151">-KeyEncryptionAlgorithm</span><span class="sxs-lookup"><span data-stu-id="5e238-151">-KeyEncryptionAlgorithm</span></span>
<span data-ttu-id="5e238-152">Especifica o algoritmo que é usado para quebrar e desencapsular a chave de criptografia da chave da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="5e238-152">Specifies the algorithm that is used to wrap and unwrap the key encryption key of the virtual machine.</span></span>
<span data-ttu-id="5e238-153">O valor padrão é RSA-OAEP.</span><span class="sxs-lookup"><span data-stu-id="5e238-153">The default value is RSA-OAEP.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: RSA-OAEP, RSA1_5

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e238-154">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="5e238-154">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="5e238-155">Especifica a URL da chave de criptografia da chave que é usada para encapsular e descodificar a chave de criptografia da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="5e238-155">Specifies the URL of the key encryption key that is used to wrap and unwrap the virtual machine encryption key.</span></span>
<span data-ttu-id="5e238-156">Deve ser a URL completa com versão.</span><span class="sxs-lookup"><span data-stu-id="5e238-156">This must be the full versioned URL.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e238-157">-KeyEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="5e238-157">-KeyEncryptionKeyVaultId</span></span>
<span data-ttu-id="5e238-158">Especifica a ID do **recurso que contém a chave** de criptografia de chave que é usada para encapsular e desencapsular a chave de criptografia da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="5e238-158">Specifies the resource ID of the **KeyVault** that contains key encryption key that is used to wrap and unwrap the virtual machine encryption key.</span></span>
<span data-ttu-id="5e238-159">Deve ser uma URL completa com versão.</span><span class="sxs-lookup"><span data-stu-id="5e238-159">This must be a full versioned URL.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e238-160">-Nome</span><span class="sxs-lookup"><span data-stu-id="5e238-160">-Name</span></span>
<span data-ttu-id="5e238-161">Especifica o nome do recurso do Gerenciador de recursos do Azure que representa a extensão.</span><span class="sxs-lookup"><span data-stu-id="5e238-161">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span>
<span data-ttu-id="5e238-162">O valor padrão é AzureDiskEncryption para máquinas virtuais que executam o sistema operacional Windows ou o AzureDiskEncryptionForLinux para máquinas virtuais Linux.</span><span class="sxs-lookup"><span data-stu-id="5e238-162">The default value is AzureDiskEncryption for virtual machines that run the Windows operating system or AzureDiskEncryptionForLinux for Linux virtual machines.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 12
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e238-163">-Senha</span><span class="sxs-lookup"><span data-stu-id="5e238-163">-Passphrase</span></span>
<span data-ttu-id="5e238-164">Especifica a senha usada para criptografar apenas máquinas virtuais Linux.</span><span class="sxs-lookup"><span data-stu-id="5e238-164">Specifies the passphrase used for encrypting Linux virtual machines only.</span></span>
<span data-ttu-id="5e238-165">Esse parâmetro não é usado para máquinas virtuais que executam o sistema operacional Windows.</span><span class="sxs-lookup"><span data-stu-id="5e238-165">This parameter is not used for virtual machines that run the Windows operating system.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 13
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e238-166">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e238-166">-ResourceGroupName</span></span>
<span data-ttu-id="5e238-167">Especifica o nome do grupo de recursos da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="5e238-167">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e238-168">-SequenceVersion</span><span class="sxs-lookup"><span data-stu-id="5e238-168">-SequenceVersion</span></span>
<span data-ttu-id="5e238-169">Especifica o número de sequência das operações de criptografia para uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="5e238-169">Specifies the sequence number of the encryption operations for a virtual machine.</span></span>
<span data-ttu-id="5e238-170">Isso é exclusivo por cada operação de criptografia executada na mesma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="5e238-170">This is unique per each encryption operation performed on the same virtual machine.</span></span>
<span data-ttu-id="5e238-171">O cmdlet Get-AzureRmVMExtension pode ser usado para recuperar o número de sequência anterior que foi usado.</span><span class="sxs-lookup"><span data-stu-id="5e238-171">The Get-AzureRmVMExtension cmdlet can be used to retrieve the previous sequence number that was used.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e238-172">-SkipVmBackup</span><span class="sxs-lookup"><span data-stu-id="5e238-172">-SkipVmBackup</span></span>
<span data-ttu-id="5e238-173">Ignorar a criação de backup para VMs Linux</span><span class="sxs-lookup"><span data-stu-id="5e238-173">Skip backup creation for Linux VMs</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 15
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e238-174">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="5e238-174">-TypeHandlerVersion</span></span>
<span data-ttu-id="5e238-175">Especifica a versão da extensão de criptografia.</span><span class="sxs-lookup"><span data-stu-id="5e238-175">Specifies the version of the encryption extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: 11
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e238-176">-VMName</span><span class="sxs-lookup"><span data-stu-id="5e238-176">-VMName</span></span>
<span data-ttu-id="5e238-177">Especifica o nome da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="5e238-177">Specifies the name of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e238-178">-Volumetype</span><span class="sxs-lookup"><span data-stu-id="5e238-178">-VolumeType</span></span>
<span data-ttu-id="5e238-179">Especifica o tipo de volumes da máquina virtual para executar a operação de criptografia.</span><span class="sxs-lookup"><span data-stu-id="5e238-179">Specifies the type of virtual machine volumes to perform the encryption operation.</span></span>
<span data-ttu-id="5e238-180">Os valores permitidos para máquinas virtuais que executam o sistema operacional Windows são os seguintes: ALL, so e data.</span><span class="sxs-lookup"><span data-stu-id="5e238-180">Allowed values for virtual machines that run the Windows operating system are as follows: All, OS, and Data.</span></span>
<span data-ttu-id="5e238-181">Os valores permitidos para máquinas virtuais Linux são os seguintes: somente dados.</span><span class="sxs-lookup"><span data-stu-id="5e238-181">The allowed values for Linux virtual machines are as follows: Data only.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: OS, Data, All

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e238-182">-Confirme</span><span class="sxs-lookup"><span data-stu-id="5e238-182">-Confirm</span></span>
<span data-ttu-id="5e238-183">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5e238-183">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e238-184">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5e238-184">-WhatIf</span></span>
<span data-ttu-id="5e238-185">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="5e238-185">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="5e238-186">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5e238-186">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e238-187">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e238-187">CommonParameters</span></span>
<span data-ttu-id="5e238-188">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e238-188">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e238-189">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5e238-189">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e238-190">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5e238-190">INPUTS</span></span>

### <span data-ttu-id="5e238-191">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="5e238-191">None</span></span>
<span data-ttu-id="5e238-192">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="5e238-192">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="5e238-193">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5e238-193">OUTPUTS</span></span>

### <span data-ttu-id="5e238-194">Microsoft. Azure. Commands. COMPUTE. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="5e238-194">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="5e238-195">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5e238-195">NOTES</span></span>

## <span data-ttu-id="5e238-196">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5e238-196">RELATED LINKS</span></span>

[<span data-ttu-id="5e238-197">Add-AzureRmVMSecret</span><span class="sxs-lookup"><span data-stu-id="5e238-197">Add-AzureRmVMSecret</span></span>](./Add-AzureRmVMSecret.md)

[<span data-ttu-id="5e238-198">Get-AzureRmVMDiskEncryptionStatus</span><span class="sxs-lookup"><span data-stu-id="5e238-198">Get-AzureRmVMDiskEncryptionStatus</span></span>](./Get-AzureRmVMDiskEncryptionStatus.md)

[<span data-ttu-id="5e238-199">Remove-AzureRmVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="5e238-199">Remove-AzureRmVMDiskEncryptionExtension</span></span>](./Remove-AzureRmVMDiskEncryptionExtension.md)


