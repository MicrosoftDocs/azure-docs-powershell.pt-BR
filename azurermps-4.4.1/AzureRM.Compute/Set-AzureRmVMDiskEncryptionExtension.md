---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 6BCB36BC-F5E6-4EDD-983C-8BDE7A9B004D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMDiskEncryptionExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMDiskEncryptionExtension.md
ms.openlocfilehash: c10b55ae0d1243320171d898058947d4781a7de1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426929"
---
# <span data-ttu-id="023d7-101">Set-AzureRmVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="023d7-101">Set-AzureRmVMDiskEncryptionExtension</span></span>

## <span data-ttu-id="023d7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="023d7-102">SYNOPSIS</span></span>
<span data-ttu-id="023d7-103">Habilita a criptografia em uma máquina virtual IaaS em execução no Azure.</span><span class="sxs-lookup"><span data-stu-id="023d7-103">Enables encryption on a running IaaS virtual machine in Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="023d7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="023d7-104">SYNTAX</span></span>

### <span data-ttu-id="023d7-105">Parâmetros secretos do cliente AAD (padrão)</span><span class="sxs-lookup"><span data-stu-id="023d7-105">AAD Client Secret Parameters (Default)</span></span>
```
Set-AzureRmVMDiskEncryptionExtension [-ResourceGroupName] <String> [-VMName] <String> [-AadClientID] <String>
 [-AadClientSecret] <String> [-DiskEncryptionKeyVaultUrl] <String> [-DiskEncryptionKeyVaultId] <String>
 [[-KeyEncryptionKeyUrl] <String>] [[-KeyEncryptionKeyVaultId] <String>] [[-KeyEncryptionAlgorithm] <String>]
 [[-VolumeType] <String>] [[-SequenceVersion] <String>] [[-TypeHandlerVersion] <String>] [[-Name] <String>]
 [[-Passphrase] <String>] [-Force] [-DisableAutoUpgradeMinorVersion] [-SkipVmBackup]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="023d7-106">Parâmetros de certificado de cliente AAD</span><span class="sxs-lookup"><span data-stu-id="023d7-106">AAD Client Cert Parameters</span></span>
```
Set-AzureRmVMDiskEncryptionExtension [-ResourceGroupName] <String> [-VMName] <String> [-AadClientID] <String>
 [-AadClientCertThumbprint] <String> [-DiskEncryptionKeyVaultUrl] <String> [-DiskEncryptionKeyVaultId] <String>
 [[-KeyEncryptionKeyUrl] <String>] [[-KeyEncryptionKeyVaultId] <String>] [[-KeyEncryptionAlgorithm] <String>]
 [[-VolumeType] <String>] [[-SequenceVersion] <String>] [[-TypeHandlerVersion] <String>] [[-Name] <String>]
 [[-Passphrase] <String>] [-Force] [-DisableAutoUpgradeMinorVersion] [-SkipVmBackup]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="023d7-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="023d7-107">DESCRIPTION</span></span>
<span data-ttu-id="023d7-108">O cmdlet **set-AzureRmVMDiskEncryptionExtension** habilita a criptografia em uma máquina virtual de serviço (IaaS) de infraestrutura em execução no Azure.</span><span class="sxs-lookup"><span data-stu-id="023d7-108">The **Set-AzureRmVMDiskEncryptionExtension** cmdlet enables encryption on a running infrastructure as a service (IaaS) virtual machine in Azure.</span></span>
<span data-ttu-id="023d7-109">Esse cmdlet habilita a criptografia instalando a extensão de criptografia de disco na máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="023d7-109">This cmdlet enables encryption by installing the disk encryption extension on the virtual machine.</span></span>
<span data-ttu-id="023d7-110">Se nenhum parâmetro *Name* for especificado, será instalada uma extensão com o nome padrão AzureDiskEncryption para máquinas virtuais que executam o sistema operacional Windows ou AzureDiskEncryptionForLinux para máquinas virtuais Linux.</span><span class="sxs-lookup"><span data-stu-id="023d7-110">If no *Name* parameter is specified, an extension with the default name AzureDiskEncryption for virtual machines that run the Windows operating system or AzureDiskEncryptionForLinux for Linux virtual machines are installed.</span></span>
<span data-ttu-id="023d7-111">Esse cmdlet requer confirmação dos usuários como uma das etapas para habilitar a criptografia requer uma reinicialização da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="023d7-111">This cmdlet requires confirmation from the users as one of the steps to enable encryption requires a restart of the virtual machine.</span></span>
<span data-ttu-id="023d7-112">É recomendável que você salve o trabalho na máquina virtual antes de executar esse cmdlet.</span><span class="sxs-lookup"><span data-stu-id="023d7-112">It is advised that you save your work on the virtual machine before you run this cmdlet.</span></span>

## <span data-ttu-id="023d7-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="023d7-113">EXAMPLES</span></span>

### <span data-ttu-id="023d7-114">Exemplo 1: habilitar a criptografia usando o ID de cliente do Azure AD e o segredo do cliente</span><span class="sxs-lookup"><span data-stu-id="023d7-114">Example 1: Enable encryption using Azure AD Client ID and Client Secret</span></span>
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

<span data-ttu-id="023d7-115">Este exemplo ativa a criptografia usando o ID de cliente do Azure AD e o segredo do cliente.</span><span class="sxs-lookup"><span data-stu-id="023d7-115">This example enables encryption using Azure AD client ID, and client secret.</span></span>

### <span data-ttu-id="023d7-116">Exemplo 2: habilitar a criptografia usando a ID de cliente do Azure AD e a impressão digital de certificação do cliente</span><span class="sxs-lookup"><span data-stu-id="023d7-116">Example 2: Enable encryption using Azure AD client ID and client certification thumbprint</span></span>
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

<span data-ttu-id="023d7-117">Este exemplo habilita a criptografia usando a ID de cliente do Azure AD e as impressões de certificação do cliente.</span><span class="sxs-lookup"><span data-stu-id="023d7-117">This example enables encryption using Azure AD client ID and client certification thumbprints.</span></span>

### <span data-ttu-id="023d7-118">Exemplo 3: habilitar a criptografia usando a identificação de cliente do Azure AD, o segredo do cliente e a chave de criptografia do disco decodificada usando chave de criptografia de chave</span><span class="sxs-lookup"><span data-stu-id="023d7-118">Example 3: Enable encryption using Azure AD client ID, client secret, and wrap disk encryption key by using key encryption key</span></span>
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

<span data-ttu-id="023d7-119">Este exemplo habilita a criptografia usando a ID de cliente do Azure AD, o segredo do cliente e a chave de criptografia do disco de quebra de linha usando a chave de criptografia de chave.</span><span class="sxs-lookup"><span data-stu-id="023d7-119">This example enables encryption using Azure AD client ID, client secret, and wrap disk encryption key by using the key encryption key.</span></span>

### <span data-ttu-id="023d7-120">Exemplo 4: habilitar a criptografia usando a ID de cliente do Azure AD, a impressão digital de certificado de cliente e o encapsulamento de disco EncryptionKey usando chave de criptografia de chave</span><span class="sxs-lookup"><span data-stu-id="023d7-120">Example 4: Enable encryption using Azure AD client ID, client cert thumbprint, and wrap disk encryptionkey by using key encryption key</span></span>
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

<span data-ttu-id="023d7-121">Este exemplo habilita a criptografia usando a ID de cliente do Azure AD, a impressão digital de certificado de cliente e a chave de criptografia de disco decodificada usando chave de criptografia.</span><span class="sxs-lookup"><span data-stu-id="023d7-121">This example enables encryption using Azure AD client ID, client cert thumbprint, and wrap disk encryption key by using key encryption key.</span></span>

## <span data-ttu-id="023d7-122">OS</span><span class="sxs-lookup"><span data-stu-id="023d7-122">PARAMETERS</span></span>

### <span data-ttu-id="023d7-123">-AadClientCertThumbprint</span><span class="sxs-lookup"><span data-stu-id="023d7-123">-AadClientCertThumbprint</span></span>
<span data-ttu-id="023d7-124">Especifica a impressão digital do certificado de cliente do aplicativo AzureActive Directory (Azure AD) que tem permissões para gravar segredos no **keyvault**.</span><span class="sxs-lookup"><span data-stu-id="023d7-124">Specifies the thumbprint of the AzureActive Directory (Azure AD) application client certificate that has permissions to write secrets to **KeyVault**.</span></span>
<span data-ttu-id="023d7-125">Como pré-requisito, o certificado de cliente do Azure AD deve ser implantado anteriormente no repositório de certificados do computador local da máquina virtual `my` .</span><span class="sxs-lookup"><span data-stu-id="023d7-125">As a prerequisite, the Azure AD client certificate must be previously deployed to the virtual machine's local computer `my` certificate store.</span></span>
<span data-ttu-id="023d7-126">O cmdlet Add-AzureRmVMSecret pode ser usado para implantar um certificado em uma máquina virtual no Azure.</span><span class="sxs-lookup"><span data-stu-id="023d7-126">The Add-AzureRmVMSecret cmdlet can be used to deploy a certificate to a virtual machine in Azure.</span></span>
<span data-ttu-id="023d7-127">Para obter mais detalhes, consulte a ajuda do cmdlet **Add-AzureRmVMSecret** .</span><span class="sxs-lookup"><span data-stu-id="023d7-127">For more details, see the **Add-AzureRmVMSecret** cmdlet help.</span></span>
<span data-ttu-id="023d7-128">O certificado deve ser implantado anteriormente no computador local da máquina virtual meu repositório de certificados.</span><span class="sxs-lookup"><span data-stu-id="023d7-128">The certificate must be previously deployed to the virtual machine local computer my certificate store.</span></span>

```yaml
Type: System.String
Parameter Sets: AAD Client Cert Parameters
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="023d7-129">-AadClientID</span><span class="sxs-lookup"><span data-stu-id="023d7-129">-AadClientID</span></span>
<span data-ttu-id="023d7-130">Especifica a ID do cliente do aplicativo Azure AD que tem permissões para gravar segredos no **keyvault**.</span><span class="sxs-lookup"><span data-stu-id="023d7-130">Specifies the client ID of the Azure AD application that has permissions to write secrets to **KeyVault**.</span></span>

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

### <span data-ttu-id="023d7-131">-AadClientSecret</span><span class="sxs-lookup"><span data-stu-id="023d7-131">-AadClientSecret</span></span>
<span data-ttu-id="023d7-132">Especifica o segredo do cliente do aplicativo Azure AD que tem permissões para gravar segredos no **keyvault**.</span><span class="sxs-lookup"><span data-stu-id="023d7-132">Specifies the client secret of the Azure AD application that has permissions to write secrets to **KeyVault**.</span></span>

```yaml
Type: System.String
Parameter Sets: AAD Client Secret Parameters
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="023d7-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="023d7-133">-DefaultProfile</span></span>
<span data-ttu-id="023d7-134">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="023d7-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="023d7-135">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="023d7-135">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="023d7-136">Indica que esse cmdlet desabilita a atualização automática da versão secundária da extensão.</span><span class="sxs-lookup"><span data-stu-id="023d7-136">Indicates that this cmdlet disables auto-upgrade of the minor version of the extension.</span></span>

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

### <span data-ttu-id="023d7-137">-DiskEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="023d7-137">-DiskEncryptionKeyVaultId</span></span>
<span data-ttu-id="023d7-138">Especifica a ID do recurso do **cofre** para o qual as chaves de criptografia da máquina virtual devem ser carregadas.</span><span class="sxs-lookup"><span data-stu-id="023d7-138">Specifies the resource ID of the **KeyVault** to which the virtual machine encryption keys should be uploaded.</span></span>

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

### <span data-ttu-id="023d7-139">-DiskEncryptionKeyVaultUrl</span><span class="sxs-lookup"><span data-stu-id="023d7-139">-DiskEncryptionKeyVaultUrl</span></span>
<span data-ttu-id="023d7-140">Especifica a URL do **keyvault** para a qual as chaves de criptografia da máquina virtual devem ser carregadas.</span><span class="sxs-lookup"><span data-stu-id="023d7-140">Specifies the **KeyVault** URL to which the virtual machine encryption keys should be uploaded.</span></span>

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

### <span data-ttu-id="023d7-141">-Force</span><span class="sxs-lookup"><span data-stu-id="023d7-141">-Force</span></span>
<span data-ttu-id="023d7-142">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="023d7-142">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="023d7-143">-KeyEncryptionAlgorithm</span><span class="sxs-lookup"><span data-stu-id="023d7-143">-KeyEncryptionAlgorithm</span></span>
<span data-ttu-id="023d7-144">Especifica o algoritmo que é usado para quebrar e desencapsular a chave de criptografia da chave da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="023d7-144">Specifies the algorithm that is used to wrap and unwrap the key encryption key of the virtual machine.</span></span>
<span data-ttu-id="023d7-145">O valor padrão é RSA-OAEP.</span><span class="sxs-lookup"><span data-stu-id="023d7-145">The default value is RSA-OAEP.</span></span>

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

### <span data-ttu-id="023d7-146">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="023d7-146">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="023d7-147">Especifica a URL da chave de criptografia da chave que é usada para encapsular e descodificar a chave de criptografia da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="023d7-147">Specifies the URL of the key encryption key that is used to wrap and unwrap the virtual machine encryption key.</span></span>
<span data-ttu-id="023d7-148">Deve ser a URL completa com versão.</span><span class="sxs-lookup"><span data-stu-id="023d7-148">This must be the full versioned URL.</span></span>

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

### <span data-ttu-id="023d7-149">-KeyEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="023d7-149">-KeyEncryptionKeyVaultId</span></span>
<span data-ttu-id="023d7-150">Especifica a ID do **recurso que contém a chave** de criptografia de chave que é usada para encapsular e desencapsular a chave de criptografia da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="023d7-150">Specifies the resource ID of the **KeyVault** that contains key encryption key that is used to wrap and unwrap the virtual machine encryption key.</span></span>
<span data-ttu-id="023d7-151">Deve ser uma URL completa com versão.</span><span class="sxs-lookup"><span data-stu-id="023d7-151">This must be a full versioned URL.</span></span>

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

### <span data-ttu-id="023d7-152">-Nome</span><span class="sxs-lookup"><span data-stu-id="023d7-152">-Name</span></span>
<span data-ttu-id="023d7-153">Especifica o nome do recurso do Gerenciador de recursos do Azure que representa a extensão.</span><span class="sxs-lookup"><span data-stu-id="023d7-153">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span>
<span data-ttu-id="023d7-154">O valor padrão é AzureDiskEncryption para máquinas virtuais que executam o sistema operacional Windows ou o AzureDiskEncryptionForLinux para máquinas virtuais Linux.</span><span class="sxs-lookup"><span data-stu-id="023d7-154">The default value is AzureDiskEncryption for virtual machines that run the Windows operating system or AzureDiskEncryptionForLinux for Linux virtual machines.</span></span>

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

### <span data-ttu-id="023d7-155">-Senha</span><span class="sxs-lookup"><span data-stu-id="023d7-155">-Passphrase</span></span>
<span data-ttu-id="023d7-156">Especifica a senha usada para criptografar apenas máquinas virtuais Linux.</span><span class="sxs-lookup"><span data-stu-id="023d7-156">Specifies the passphrase used for encrypting Linux virtual machines only.</span></span>
<span data-ttu-id="023d7-157">Esse parâmetro não é usado para máquinas virtuais que executam o sistema operacional Windows.</span><span class="sxs-lookup"><span data-stu-id="023d7-157">This parameter is not used for virtual machines that run the Windows operating system.</span></span>

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

### <span data-ttu-id="023d7-158">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="023d7-158">-ResourceGroupName</span></span>
<span data-ttu-id="023d7-159">Especifica o nome do grupo de recursos da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="023d7-159">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="023d7-160">-SequenceVersion</span><span class="sxs-lookup"><span data-stu-id="023d7-160">-SequenceVersion</span></span>
<span data-ttu-id="023d7-161">Especifica o número de sequência das operações de criptografia para uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="023d7-161">Specifies the sequence number of the encryption operations for a virtual machine.</span></span>
<span data-ttu-id="023d7-162">Isso é exclusivo por cada operação de criptografia executada na mesma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="023d7-162">This is unique per each encryption operation performed on the same virtual machine.</span></span>
<span data-ttu-id="023d7-163">O cmdlet Get-AzureRmVMExtension pode ser usado para recuperar o número de sequência anterior que foi usado.</span><span class="sxs-lookup"><span data-stu-id="023d7-163">The Get-AzureRmVMExtension cmdlet can be used to retrieve the previous sequence number that was used.</span></span>

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

### <span data-ttu-id="023d7-164">-SkipVmBackup</span><span class="sxs-lookup"><span data-stu-id="023d7-164">-SkipVmBackup</span></span>
<span data-ttu-id="023d7-165">Ignorar a criação de backup para VMs Linux</span><span class="sxs-lookup"><span data-stu-id="023d7-165">Skip backup creation for Linux VMs</span></span>

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

### <span data-ttu-id="023d7-166">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="023d7-166">-TypeHandlerVersion</span></span>
<span data-ttu-id="023d7-167">Especifica a versão da extensão de criptografia.</span><span class="sxs-lookup"><span data-stu-id="023d7-167">Specifies the version of the encryption extension.</span></span>

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

### <span data-ttu-id="023d7-168">-VMName</span><span class="sxs-lookup"><span data-stu-id="023d7-168">-VMName</span></span>
<span data-ttu-id="023d7-169">Especifica o nome da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="023d7-169">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="023d7-170">-Volumetype</span><span class="sxs-lookup"><span data-stu-id="023d7-170">-VolumeType</span></span>
<span data-ttu-id="023d7-171">Especifica o tipo de volumes da máquina virtual para executar a operação de criptografia.</span><span class="sxs-lookup"><span data-stu-id="023d7-171">Specifies the type of virtual machine volumes to perform the encryption operation.</span></span>
<span data-ttu-id="023d7-172">Os valores permitidos para máquinas virtuais que executam o sistema operacional Windows são os seguintes: ALL, so e data.</span><span class="sxs-lookup"><span data-stu-id="023d7-172">Allowed values for virtual machines that run the Windows operating system are as follows: All, OS, and Data.</span></span>
<span data-ttu-id="023d7-173">Os valores permitidos para máquinas virtuais Linux são os seguintes: somente dados.</span><span class="sxs-lookup"><span data-stu-id="023d7-173">The allowed values for Linux virtual machines are as follows: Data only.</span></span>

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

### <span data-ttu-id="023d7-174">-Confirme</span><span class="sxs-lookup"><span data-stu-id="023d7-174">-Confirm</span></span>
<span data-ttu-id="023d7-175">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="023d7-175">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="023d7-176">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="023d7-176">-WhatIf</span></span>
<span data-ttu-id="023d7-177">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="023d7-177">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="023d7-178">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="023d7-178">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="023d7-179">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="023d7-179">CommonParameters</span></span>
<span data-ttu-id="023d7-180">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="023d7-180">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="023d7-181">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="023d7-181">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="023d7-182">SENSORES</span><span class="sxs-lookup"><span data-stu-id="023d7-182">INPUTS</span></span>

## <span data-ttu-id="023d7-183">EXIBE</span><span class="sxs-lookup"><span data-stu-id="023d7-183">OUTPUTS</span></span>

## <span data-ttu-id="023d7-184">INFORMA</span><span class="sxs-lookup"><span data-stu-id="023d7-184">NOTES</span></span>

## <span data-ttu-id="023d7-185">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="023d7-185">RELATED LINKS</span></span>

[<span data-ttu-id="023d7-186">Add-AzureRmVMSecret</span><span class="sxs-lookup"><span data-stu-id="023d7-186">Add-AzureRmVMSecret</span></span>](./Add-AzureRmVMSecret.md)

[<span data-ttu-id="023d7-187">Get-AzureRmVMDiskEncryptionStatus</span><span class="sxs-lookup"><span data-stu-id="023d7-187">Get-AzureRmVMDiskEncryptionStatus</span></span>](./Get-AzureRmVMDiskEncryptionStatus.md)

[<span data-ttu-id="023d7-188">Remove-AzureRmVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="023d7-188">Remove-AzureRmVMDiskEncryptionExtension</span></span>](./Remove-AzureRmVMDiskEncryptionExtension.md)


