---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/new-azservicefabriccluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricCluster.md
ms.openlocfilehash: 0c3fe2ffc9e5ce74c991e182ef1112629f05b88a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93773191"
---
# <span data-ttu-id="9f846-101">New-AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="9f846-101">New-AzServiceFabricCluster</span></span>

## <span data-ttu-id="9f846-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9f846-102">SYNOPSIS</span></span>
<span data-ttu-id="9f846-103">Esse comando usa certificados que você fornece ou certificados autoassinados gerados pelo sistema para configurar um novo cluster de Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="9f846-103">This command uses certificates that you provide or system generated self-signed certificates to set up a new service fabric cluster.</span></span> <span data-ttu-id="9f846-104">Ele pode usar um modelo padrão ou um modelo personalizado fornecido por você.</span><span class="sxs-lookup"><span data-stu-id="9f846-104">It can use a default template or a custom template that you provide.</span></span> <span data-ttu-id="9f846-105">Você tem a opção de especificar uma pasta para exportar os certificados autoassinados ou para extraí-los mais tarde do cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="9f846-105">You have the option of specifying a folder to export the self-signed certificates to or fetching them later from the key vault.</span></span> 

## <span data-ttu-id="9f846-106">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9f846-106">SYNTAX</span></span>

### <span data-ttu-id="9f846-107">ByDefaultArmTemplate (padrão)</span><span class="sxs-lookup"><span data-stu-id="9f846-107">ByDefaultArmTemplate (Default)</span></span>
```
New-AzServiceFabricCluster [-ResourceGroupName] <String> [-CertificateOutputFolder <String>]
 [-CertificatePassword <SecureString>] [-KeyVaultResourceGroupName <String>] [-KeyVaultName <String>]
 -Location <String> [-Name <String>] [-VmUserName <String>] [-ClusterSize <Int32>]
 [-CertificateSubjectName <String>] -VmPassword <SecureString> [-OS <OperatingSystem>] [-VmSku <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9f846-108">ByExistingKeyVault</span><span class="sxs-lookup"><span data-stu-id="9f846-108">ByExistingKeyVault</span></span>
```
New-AzServiceFabricCluster [-ResourceGroupName] <String> -TemplateFile <String> -ParameterFile <String>
 [-CertificateCommonName <String>] [-CertificateIssuerThumbprint <String>] [-VmPassword <SecureString>]
 -SecretIdentifier <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9f846-109">ByNewPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="9f846-109">ByNewPfxAndVaultName</span></span>
```
New-AzServiceFabricCluster [-ResourceGroupName] <String> -TemplateFile <String> -ParameterFile <String>
 [-CertificateOutputFolder <String>] [-CertificatePassword <SecureString>]
 [-KeyVaultResourceGroupName <String>] [-KeyVaultName <String>] [-CertificateSubjectName <String>]
 [-VmPassword <SecureString>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9f846-110">ByExistingPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="9f846-110">ByExistingPfxAndVaultName</span></span>
```
New-AzServiceFabricCluster [-ResourceGroupName] <String> -TemplateFile <String> -ParameterFile <String>
 -CertificateFile <String> [-CertificatePassword <SecureString>] [-SecondaryCertificateFile <String>]
 [-SecondaryCertificatePassword <SecureString>] [-KeyVaultResourceGroupName <String>] [-KeyVaultName <String>]
 [-CertificateCommonName <String>] [-CertificateIssuerThumbprint <String>] [-VmPassword <SecureString>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9f846-111">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9f846-111">DESCRIPTION</span></span>
<span data-ttu-id="9f846-112">O comando **New-AzServiceFabricCluster** usa certificados que você fornece ou certificados autoassinados gerados pelo sistema para configurar um novo cluster do Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="9f846-112">The **New-AzServiceFabricCluster** command uses certificates that you provide or system generated self-signed certificates to set up a new service fabric cluster.</span></span> <span data-ttu-id="9f846-113">O modelo usado pode ser um modelo padrão ou um modelo personalizado fornecido por você.</span><span class="sxs-lookup"><span data-stu-id="9f846-113">The template used can be a default template or a custom template that you provide.</span></span> <span data-ttu-id="9f846-114">Você tem a opção de especificar uma pasta para exportar os certificados autoassinados ou para obtê-los mais tarde do cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="9f846-114">You have the option of specifying a folder to export the self-signed certificates or fetching them later from the key vault.</span></span>
<span data-ttu-id="9f846-115">Se você estiver especificando um arquivo de modelo e de modelo personalizado, não será necessário fornecer as informações de certificado no arquivo de parâmetro, o sistema preencherá esses parâmetros.</span><span class="sxs-lookup"><span data-stu-id="9f846-115">If you are specifying a custom template and parameter file, you don't need to provide the certificate information in the parameter file, the system will populate these parameters.</span></span>
<span data-ttu-id="9f846-116">As quatro opções são detalhadas abaixo.</span><span class="sxs-lookup"><span data-stu-id="9f846-116">The four options are detailed below.</span></span> <span data-ttu-id="9f846-117">Role a tela para baixo para obter explicações de cada um dos parâmetros.</span><span class="sxs-lookup"><span data-stu-id="9f846-117">Scroll down for explanations of each of the parameters.</span></span>

## <span data-ttu-id="9f846-118">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9f846-118">EXAMPLES</span></span>

### <span data-ttu-id="9f846-119">Exemplo 1: especifique apenas o tamanho do cluster, o nome do requerente do certificado e o sistema operacional para implantar um cluster.</span><span class="sxs-lookup"><span data-stu-id="9f846-119">Example 1: Specify only the cluster size, the cert subject name, and the OS to deploy a cluster.</span></span>
```
$pass="Password#1234" | ConvertTo-SecureString -AsPlainText -Force
$RGname="test01"
$clusterloc="SouthCentralUS"
$subname="{0}.{1}.cloudapp.azure.com" -f $RGname, $clusterloc
$pfxfolder="c:\certs"

Write-Output "Create cluster in '$clusterloc' with cert subject name '$subname' and cert output path '$pfxfolder'"

New-AzServiceFabricCluster -ResourceGroupName $RGname -Location $clusterloc -ClusterSize 5 -VmPassword $pass -CertificateSubjectName $subname -CertificateOutputFolder $pfxfolder -CertificatePassword $pass -OS WindowsServer2016Datacenter
```

<span data-ttu-id="9f846-120">Esse comando especifica somente o tamanho do cluster, o nome do requerente do certificado e o sistema operacional para implantar um cluster.</span><span class="sxs-lookup"><span data-stu-id="9f846-120">This command specifies only the cluster size, the cert subject name, and the OS to deploy a cluster.</span></span>

### <span data-ttu-id="9f846-121">Exemplo 2: especificar um recurso de certificado existente em um cofre de chaves e um modelo personalizado para implantar um cluster</span><span class="sxs-lookup"><span data-stu-id="9f846-121">Example 2: Specify an existing Certificate resource in a key vault and a custom template to deploy a cluster</span></span>
```
$RGname="test20"
$templateParmfile="C:\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploytest.parameters.json"
$templateFile="C:\azure-quickstart-templates\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploy.json"
$secretId="https://test1.vault.azure.net:443/secrets/testcertificate4/56ec774dc61a462bbc645ffc9b4b225f"

New-AzServiceFabricCluster -ResourceGroupName $RGname -TemplateFile $templateFile -ParameterFile $templateParmfile -SecretIdentifier $secretId
```

<span data-ttu-id="9f846-122">Esse comando especifica um recurso de certificado existente em um cofre de chaves e um modelo personalizado para implantar um cluster.</span><span class="sxs-lookup"><span data-stu-id="9f846-122">This command specifies an existing Certificate resource in a key vault and a custom template to deploy a cluster.</span></span>

### <span data-ttu-id="9f846-123">Exemplo 3: criar um novo cluster usando um modelo personalizado.</span><span class="sxs-lookup"><span data-stu-id="9f846-123">Example 3: Create a new cluster using a custom template.</span></span> <span data-ttu-id="9f846-124">Especificar um nome de grupo de recursos diferente para o cofre de chaves e fazer com que o sistema carregue um novo certificado</span><span class="sxs-lookup"><span data-stu-id="9f846-124">Specify a different resource group name for the key vault and have the system upload a new certificate to it</span></span>
```
$pass="Password#1234" | ConvertTo-SecureString -AsPlainText -Force
$RGname="test20"
$keyVaultRG="test20kvrg"
$keyVault="test20kv"
$clusterloc="SouthCentralUS"
$subname="{0}.{1}.$clusterloc.cloudapp.azure.com" -f $RGName, $clusterloc
$pfxfolder="~\Documents"
$templateParmfile="C:\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploytest.parameters.json"
$templateFile="C:\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploy.json"

New-AzServiceFabricCluster -ResourceGroupName $RGname -TemplateFile $templateFile -ParameterFile $templateParmfile -CertificateOutputFolder $pfxfolder -CertificatePassword $pass -KeyVaultResourceGroupName $keyVaultRG  -KeyVaultName $keyVault -CertificateSubjectName $subname
```

<span data-ttu-id="9f846-125">Esse comando cria um novo cluster usando um modelo personalizado.</span><span class="sxs-lookup"><span data-stu-id="9f846-125">This command creates a new cluster using a custom template.</span></span> <span data-ttu-id="9f846-126">Especificar um nome de grupo de recursos diferente para o cofre de chaves e fazer com que o sistema carregue um novo certificado</span><span class="sxs-lookup"><span data-stu-id="9f846-126">Specify a different resource group name for the key vault and have the system upload a new certificate to it</span></span>

### <span data-ttu-id="9f846-127">Exemplo 4: Traga seu próprio certificado e modelo personalizado e crie um novo cluster</span><span class="sxs-lookup"><span data-stu-id="9f846-127">Example 4: Bring your own Certificate and custom template and create a new cluster</span></span>
```
$pass="Password#1234" | ConvertTo-SecureString -AsPlainText -Force
$RGname="test20"
$keyVaultRG="test20kvrg"
$keyVault="test20kv"
$pfxsourcefile="c:\Mycertificates\my2017Prodcert.pfx"
$templateParmfile="~\Documents\GitHub\azure-quickstart-templates-parms\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploytest.parameters.json"
$templateFile="~\GitHub\azure-quickstart-templates\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploy.json"

New-AzServiceFabricCluster -ResourceGroupName $RGname -TemplateFile $templateFile -ParameterFile $templateParmfile -CertificateFile $pfxsourcefile -CertificatePassword $pass -KeyVaultResourceGroupName $keyVaultRG -KeyVaultName $keyVault
```

<span data-ttu-id="9f846-128">Este comando permitirá que você traga seu próprio certificado e modelo personalizado e crie um novo cluster.</span><span class="sxs-lookup"><span data-stu-id="9f846-128">This command will let you bring your own Certificate and custom template and create a new cluster.</span></span>

## <span data-ttu-id="9f846-129">OS</span><span class="sxs-lookup"><span data-stu-id="9f846-129">PARAMETERS</span></span>

### <span data-ttu-id="9f846-130">-CertificateCommonName</span><span class="sxs-lookup"><span data-stu-id="9f846-130">-CertificateCommonName</span></span>
<span data-ttu-id="9f846-131">Nome comum do certificado</span><span class="sxs-lookup"><span data-stu-id="9f846-131">Certificate common name</span></span>

```yaml
Type: System.String
Parameter Sets: ByExistingKeyVault, ByExistingPfxAndVaultName
Aliases: CertCommonName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f846-132">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="9f846-132">-CertificateFile</span></span>
<span data-ttu-id="9f846-133">O caminho do arquivo de certificado existente para o certificado de cluster primário</span><span class="sxs-lookup"><span data-stu-id="9f846-133">The existing certificate file path for the primary cluster certificate</span></span>

```yaml
Type: System.String
Parameter Sets: ByExistingPfxAndVaultName
Aliases: Source

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9f846-134">-CertificateIssuerThumbprint</span><span class="sxs-lookup"><span data-stu-id="9f846-134">-CertificateIssuerThumbprint</span></span>
<span data-ttu-id="9f846-135">Impressão digital do emissor do certificado, separada por vírgulas, se mais de um</span><span class="sxs-lookup"><span data-stu-id="9f846-135">Certificate issuer thumbprint, separated by commas if more than one</span></span>

```yaml
Type: System.String
Parameter Sets: ByExistingKeyVault, ByExistingPfxAndVaultName
Aliases: CertIssuerThumbprint

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f846-136">-CertificateOutputFolder</span><span class="sxs-lookup"><span data-stu-id="9f846-136">-CertificateOutputFolder</span></span>
<span data-ttu-id="9f846-137">A pasta do novo arquivo de certificado a ser criado</span><span class="sxs-lookup"><span data-stu-id="9f846-137">The folder of the new certificate file to be created</span></span>

```yaml
Type: System.String
Parameter Sets: ByDefaultArmTemplate, ByNewPfxAndVaultName
Aliases: Destination

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9f846-138">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="9f846-138">-CertificatePassword</span></span>
<span data-ttu-id="9f846-139">A senha do arquivo de certificado</span><span class="sxs-lookup"><span data-stu-id="9f846-139">The password of the certificate file</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: ByDefaultArmTemplate, ByNewPfxAndVaultName, ByExistingPfxAndVaultName
Aliases: CertPassword

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9f846-140">-CertificateSubjectName</span><span class="sxs-lookup"><span data-stu-id="9f846-140">-CertificateSubjectName</span></span>
<span data-ttu-id="9f846-141">O nome do requerente do certificado a ser criado</span><span class="sxs-lookup"><span data-stu-id="9f846-141">The subject name of the certificate to be created</span></span>

```yaml
Type: System.String
Parameter Sets: ByDefaultArmTemplate, ByNewPfxAndVaultName
Aliases: Subject

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9f846-142">-ClusterSize</span><span class="sxs-lookup"><span data-stu-id="9f846-142">-ClusterSize</span></span>
<span data-ttu-id="9f846-143">O número de nós no cluster.</span><span class="sxs-lookup"><span data-stu-id="9f846-143">The number of nodes in the cluster.</span></span>
<span data-ttu-id="9f846-144">Padrão são 5 nós</span><span class="sxs-lookup"><span data-stu-id="9f846-144">Default are 5 nodes</span></span>

```yaml
Type: System.Int32
Parameter Sets: ByDefaultArmTemplate
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9f846-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f846-145">-DefaultProfile</span></span>
<span data-ttu-id="9f846-146">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9f846-146">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9f846-147">-Keyvaultname</span><span class="sxs-lookup"><span data-stu-id="9f846-147">-KeyVaultName</span></span>
<span data-ttu-id="9f846-148">Nome do cofre de chave do Azure, se não for fornecido, será definido como padrão para o nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="9f846-148">Azure key vault name, if not given it will be defaulted to the resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: ByDefaultArmTemplate, ByNewPfxAndVaultName, ByExistingPfxAndVaultName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9f846-149">-KeyVaultResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f846-149">-KeyVaultResourceGroupName</span></span>
<span data-ttu-id="9f846-150">Nome do grupo de recursos do cofre de chaves do Azure, se não for fornecido padrão para o nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="9f846-150">Azure key vault resource group name, if not given it will be defaulted to resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: ByDefaultArmTemplate, ByNewPfxAndVaultName, ByExistingPfxAndVaultName
Aliases: KeyVaultResouceGroupName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9f846-151">-Local</span><span class="sxs-lookup"><span data-stu-id="9f846-151">-Location</span></span>
<span data-ttu-id="9f846-152">O local do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="9f846-152">The resource group location</span></span>

```yaml
Type: System.String
Parameter Sets: ByDefaultArmTemplate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9f846-153">-Nome</span><span class="sxs-lookup"><span data-stu-id="9f846-153">-Name</span></span>
<span data-ttu-id="9f846-154">Especifique o nome do cluster, se não for fornecido como nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="9f846-154">Specify the name of the cluster, if not given it will be same as resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: ByDefaultArmTemplate
Aliases: ClusterName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9f846-155">-OS</span><span class="sxs-lookup"><span data-stu-id="9f846-155">-OS</span></span>
<span data-ttu-id="9f846-156">O sistema operacional das VMs que compõem o cluster.</span><span class="sxs-lookup"><span data-stu-id="9f846-156">The Operating System of the VMs that make up the cluster.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.OperatingSystem
Parameter Sets: ByDefaultArmTemplate
Aliases: VmImage
Accepted values: WindowsServer2012R2Datacenter, WindowsServer2016Datacenter, WindowsServer2016DatacenterwithContainers, UbuntuServer1604

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f846-157">-Parameterfile</span><span class="sxs-lookup"><span data-stu-id="9f846-157">-ParameterFile</span></span>
<span data-ttu-id="9f846-158">O caminho para o arquivo de parâmetro do modelo.</span><span class="sxs-lookup"><span data-stu-id="9f846-158">The path to the template parameter file.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExistingKeyVault, ByNewPfxAndVaultName, ByExistingPfxAndVaultName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9f846-159">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f846-159">-ResourceGroupName</span></span>
<span data-ttu-id="9f846-160">Especifique o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="9f846-160">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="9f846-161">-SecondaryCertificateFile</span><span class="sxs-lookup"><span data-stu-id="9f846-161">-SecondaryCertificateFile</span></span>
<span data-ttu-id="9f846-162">O caminho do arquivo de certificado existente para o certificado de cluster secundário</span><span class="sxs-lookup"><span data-stu-id="9f846-162">The existing certificate file path for the secondary cluster certificate</span></span>

```yaml
Type: System.String
Parameter Sets: ByExistingPfxAndVaultName
Aliases: SecSource

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9f846-163">-SecondaryCertificatePassword</span><span class="sxs-lookup"><span data-stu-id="9f846-163">-SecondaryCertificatePassword</span></span>
<span data-ttu-id="9f846-164">A senha do arquivo de certificado</span><span class="sxs-lookup"><span data-stu-id="9f846-164">The password of the certificate file</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: ByExistingPfxAndVaultName
Aliases: SecCertPassword

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9f846-165">-SecretIdentifier</span><span class="sxs-lookup"><span data-stu-id="9f846-165">-SecretIdentifier</span></span>
<span data-ttu-id="9f846-166">A URL do segredo do Azure Key Vault existente, por exemplo ' https://mykv.vault.azure.net:443/secrets/mysecrets/55ec7c4dc61a462bbc645ffc9b4b225f '</span><span class="sxs-lookup"><span data-stu-id="9f846-166">The existing Azure key vault secret URL, for example 'https://mykv.vault.azure.net:443/secrets/mysecrets/55ec7c4dc61a462bbc645ffc9b4b225f'</span></span>

```yaml
Type: System.String
Parameter Sets: ByExistingKeyVault
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9f846-167">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="9f846-167">-TemplateFile</span></span>
<span data-ttu-id="9f846-168">O caminho para o arquivo de modelo.</span><span class="sxs-lookup"><span data-stu-id="9f846-168">The path to the template file.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExistingKeyVault, ByNewPfxAndVaultName, ByExistingPfxAndVaultName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9f846-169">-VmPassword</span><span class="sxs-lookup"><span data-stu-id="9f846-169">-VmPassword</span></span>
<span data-ttu-id="9f846-170">A senha da VM.</span><span class="sxs-lookup"><span data-stu-id="9f846-170">The password of the Vm.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: ByDefaultArmTemplate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Security.SecureString
Parameter Sets: ByExistingKeyVault, ByNewPfxAndVaultName, ByExistingPfxAndVaultName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f846-171">-VmSku</span><span class="sxs-lookup"><span data-stu-id="9f846-171">-VmSku</span></span>
<span data-ttu-id="9f846-172">A SKU da VM</span><span class="sxs-lookup"><span data-stu-id="9f846-172">The Vm Sku</span></span>

```yaml
Type: System.String
Parameter Sets: ByDefaultArmTemplate
Aliases: Sku

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f846-173">-VmUserName</span><span class="sxs-lookup"><span data-stu-id="9f846-173">-VmUserName</span></span>
<span data-ttu-id="9f846-174">O nome de usuário para fazer logon na VM</span><span class="sxs-lookup"><span data-stu-id="9f846-174">The user name for logging to Vm</span></span>

```yaml
Type: System.String
Parameter Sets: ByDefaultArmTemplate
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9f846-175">-Confirme</span><span class="sxs-lookup"><span data-stu-id="9f846-175">-Confirm</span></span>
<span data-ttu-id="9f846-176">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9f846-176">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9f846-177">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9f846-177">-WhatIf</span></span>
<span data-ttu-id="9f846-178">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="9f846-178">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9f846-179">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9f846-179">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9f846-180">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f846-180">CommonParameters</span></span>
<span data-ttu-id="9f846-181">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9f846-181">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f846-182">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9f846-182">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f846-183">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9f846-183">INPUTS</span></span>

### <span data-ttu-id="9f846-184">System. String</span><span class="sxs-lookup"><span data-stu-id="9f846-184">System.String</span></span>

### <span data-ttu-id="9f846-185">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="9f846-185">System.Security.SecureString</span></span>

### <span data-ttu-id="9f846-186">System. Int32</span><span class="sxs-lookup"><span data-stu-id="9f846-186">System.Int32</span></span>

### <span data-ttu-id="9f846-187">Microsoft. Azure. Commands. imfabric. Models. OperatingSystem</span><span class="sxs-lookup"><span data-stu-id="9f846-187">Microsoft.Azure.Commands.ServiceFabric.Models.OperatingSystem</span></span>

## <span data-ttu-id="9f846-188">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9f846-188">OUTPUTS</span></span>

### <span data-ttu-id="9f846-189">Microsoft.Azure.Commands.ServiceFabric.Models.PSDeploymentResult</span><span class="sxs-lookup"><span data-stu-id="9f846-189">Microsoft.Azure.Commands.ServiceFabric.Models.PSDeploymentResult</span></span>

## <span data-ttu-id="9f846-190">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9f846-190">NOTES</span></span>

## <span data-ttu-id="9f846-191">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9f846-191">RELATED LINKS</span></span>
