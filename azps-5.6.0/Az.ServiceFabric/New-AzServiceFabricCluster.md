---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/new-azservicefabriccluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricCluster.md
ms.openlocfilehash: b603087063a763d63f986afa7568160a6623a22b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885963"
---
# <span data-ttu-id="dfdbf-101">New-AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="dfdbf-101">New-AzServiceFabricCluster</span></span>

## <span data-ttu-id="dfdbf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dfdbf-102">SYNOPSIS</span></span>

<span data-ttu-id="dfdbf-103">Este comando usa certificados que você fornece ou certificados auto-assinados gerados pelo sistema para configurar um novo cluster de malha de serviço.</span><span class="sxs-lookup"><span data-stu-id="dfdbf-103">This command uses certificates that you provide or system generated self-signed certificates to set up a new service fabric cluster.</span></span> <span data-ttu-id="dfdbf-104">Ele pode usar um modelo padrão ou um modelo personalizado que você fornece.</span><span class="sxs-lookup"><span data-stu-id="dfdbf-104">It can use a default template or a custom template that you provide.</span></span> <span data-ttu-id="dfdbf-105">Você tem a opção de especificar uma pasta para exportar os certificados auto-assinados ou buscá-los posteriormente do cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="dfdbf-105">You have the option of specifying a folder to export the self-signed certificates to or fetching them later from the key vault.</span></span>

## <span data-ttu-id="dfdbf-106">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="dfdbf-106">SYNTAX</span></span>

### <span data-ttu-id="dfdbf-107">ByDefaultArmTemplate (Padrão)</span><span class="sxs-lookup"><span data-stu-id="dfdbf-107">ByDefaultArmTemplate (Default)</span></span>
```
New-AzServiceFabricCluster [-ResourceGroupName] <String> [-CertificateOutputFolder <String>]
 [-CertificatePassword <SecureString>] [-KeyVaultResourceGroupName <String>] [-KeyVaultName <String>]
 -Location <String> [-Name <String>] [-VmUserName <String>] [-ClusterSize <Int32>]
 [-CertificateSubjectName <String>] -VmPassword <SecureString> [-OS <OperatingSystem>] [-VmSku <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dfdbf-108">ByExistingKeyVault</span><span class="sxs-lookup"><span data-stu-id="dfdbf-108">ByExistingKeyVault</span></span>
```
New-AzServiceFabricCluster [-ResourceGroupName] <String> -TemplateFile <String> -ParameterFile <String>
 [-CertificateCommonName <String>] [-CertificateIssuerThumbprint <String>] [-VmPassword <SecureString>]
 -SecretIdentifier <String> [-Thumbprint <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dfdbf-109">ByNewPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="dfdbf-109">ByNewPfxAndVaultName</span></span>
```
New-AzServiceFabricCluster [-ResourceGroupName] <String> -TemplateFile <String> -ParameterFile <String>
 [-CertificateOutputFolder <String>] [-CertificatePassword <SecureString>]
 [-KeyVaultResourceGroupName <String>] [-KeyVaultName <String>] [-CertificateSubjectName <String>]
 [-VmPassword <SecureString>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="dfdbf-110">ByExistingPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="dfdbf-110">ByExistingPfxAndVaultName</span></span>
```
New-AzServiceFabricCluster [-ResourceGroupName] <String> -TemplateFile <String> -ParameterFile <String>
 -CertificateFile <String> [-CertificatePassword <SecureString>] [-SecondaryCertificateFile <String>]
 [-SecondaryCertificatePassword <SecureString>] [-KeyVaultResourceGroupName <String>] [-KeyVaultName <String>]
 [-CertificateCommonName <String>] [-CertificateIssuerThumbprint <String>] [-VmPassword <SecureString>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dfdbf-111">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="dfdbf-111">DESCRIPTION</span></span>

<span data-ttu-id="dfdbf-112">O **comando New-AzServiceFabricCluster** usa certificados que você fornece ou certificados auto-assinados gerados pelo sistema para configurar um novo cluster de malha de serviço.</span><span class="sxs-lookup"><span data-stu-id="dfdbf-112">The **New-AzServiceFabricCluster** command uses certificates that you provide or system generated self-signed certificates to set up a new service fabric cluster.</span></span> <span data-ttu-id="dfdbf-113">O modelo usado pode ser um modelo padrão ou um modelo personalizado que você fornece.</span><span class="sxs-lookup"><span data-stu-id="dfdbf-113">The template used can be a default template or a custom template that you provide.</span></span> <span data-ttu-id="dfdbf-114">Você tem a opção de especificar uma pasta para exportar os certificados auto-assinados ou buscá-los posteriormente do cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="dfdbf-114">You have the option of specifying a folder to export the self-signed certificates or fetching them later from the key vault.</span></span>
<span data-ttu-id="dfdbf-115">Se você estiver especificando um modelo personalizado e um arquivo de parâmetro, você não precisa fornecer as informações de certificado no arquivo de parâmetros, o sistema preencherá esses parâmetros.</span><span class="sxs-lookup"><span data-stu-id="dfdbf-115">If you are specifying a custom template and parameter file, you don't need to provide the certificate information in the parameter file, the system will populate these parameters.</span></span>
<span data-ttu-id="dfdbf-116">As quatro opções são detalhadas abaixo.</span><span class="sxs-lookup"><span data-stu-id="dfdbf-116">The four options are detailed below.</span></span> <span data-ttu-id="dfdbf-117">Role para baixo para explicações de cada um dos parâmetros.</span><span class="sxs-lookup"><span data-stu-id="dfdbf-117">Scroll down for explanations of each of the parameters.</span></span>

## <span data-ttu-id="dfdbf-118">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="dfdbf-118">EXAMPLES</span></span>

### <span data-ttu-id="dfdbf-119">Exemplo 1: Especifique apenas o tamanho do cluster, o nome do assunto do certificado e o sistema operacional para implantar um cluster</span><span class="sxs-lookup"><span data-stu-id="dfdbf-119">Example 1: Specify only the cluster size, the cert subject name, and the OS to deploy a cluster</span></span>

```powershell
$password = "Password#1234" | ConvertTo-SecureString -AsPlainText -Force
$resourceGroupName = "quickstart-sf-group"
$azureRegion = "southcentralus"
$clusterDnsName = "{0}.{1}.cloudapp.azure.com" -f $resourceGroupName, $azureRegion
$localCertificateFolder = "c:\certs"

Write-Output "Create cluster in '$azureRegion' with cert subject name '$clusterDnsName' and cert output path '$localCertificateFolder'"

New-AzServiceFabricCluster -ResourceGroupName $resourceGroupName -Location $azureRegion -ClusterSize 5 -VmPassword $password -CertificateSubjectName $clusterDnsName -CertificateOutputFolder $localCertificateFolder -CertificatePassword $pass -OS WindowsServer2016Datacenter
```

<span data-ttu-id="dfdbf-120">Este comando especifica apenas o tamanho do cluster, o nome do assunto do certificado e o sistema operacional para implantar um cluster.</span><span class="sxs-lookup"><span data-stu-id="dfdbf-120">This command specifies only the cluster size, the cert subject name, and the OS to deploy a cluster.</span></span>

### <span data-ttu-id="dfdbf-121">Exemplo 2: Especifique um recurso Certificado existente em um cofre de chaves e um modelo personalizado para implantar um cluster</span><span class="sxs-lookup"><span data-stu-id="dfdbf-121">Example 2: Specify an existing Certificate resource in a key vault and a custom template to deploy a cluster</span></span>

```powershell
$resourceGroupName = "test20"
$templateParameterFile = "C:\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploytest.parameters.json"
$templateFile = "C:\azure-quickstart-templates\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploy.json"
$secretId = "https://test1.vault.azure.net:443/secrets/testcertificate4/56ec774dc61a462bbc645ffc9b4b225f"

New-AzServiceFabricCluster -ResourceGroupName $resourceGroupName -TemplateFile $templateFile -ParameterFile $templateParameterFile -SecretIdentifier $secretId
```

<span data-ttu-id="dfdbf-122">Este comando especifica um recurso Certificado existente em um cofre de chaves e um modelo personalizado para implantar um cluster.</span><span class="sxs-lookup"><span data-stu-id="dfdbf-122">This command specifies an existing Certificate resource in a key vault and a custom template to deploy a cluster.</span></span>

### <span data-ttu-id="dfdbf-123">Exemplo 3: Criar um novo cluster usando um modelo personalizado.</span><span class="sxs-lookup"><span data-stu-id="dfdbf-123">Example 3: Create a new cluster using a custom template.</span></span> <span data-ttu-id="dfdbf-124">Especifique um nome de grupo de recursos diferente para o cofre de chaves e faça com que o sistema carregue um novo certificado para ele</span><span class="sxs-lookup"><span data-stu-id="dfdbf-124">Specify a different resource group name for the key vault and have the system upload a new certificate to it</span></span>

```powershell
$password = "Password#1234" | ConvertTo-SecureString -AsPlainText -Force
$resourceGroupName = "quickstart-sf-group"
$keyVaultResourceGroupName = " quickstart-kv-group"
$keyVaultName = "quickstart-kv"
$azureRegion = "southcentralus"
$clusterDnsName = "{0}.{1}.cloudapp.azure.com" -F $resourceGroupName, $azureRegion
$localCertificateFolder = "~\Documents"
$templateParameterFile = "C:\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploytest.parameters.json"
$templateFile = "C:\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploy.json"

New-AzServiceFabricCluster -ResourceGroupName $resourceGroupName -TemplateFile $templateFile -ParameterFile $templateParameterFile -CertificateOutputFolder $localCertificateFolder -CertificatePassword $password -KeyVaultResourceGroupName $keyVaultResourceGroupName  -KeyVaultName $keyVaultName -CertificateSubjectName $clusterDnsName
```

<span data-ttu-id="dfdbf-125">Este comando cria um novo cluster usando um modelo personalizado.</span><span class="sxs-lookup"><span data-stu-id="dfdbf-125">This command creates a new cluster using a custom template.</span></span> <span data-ttu-id="dfdbf-126">Especifique um nome de grupo de recursos diferente para o cofre de chaves e faça com que o sistema carregue um novo certificado para ele</span><span class="sxs-lookup"><span data-stu-id="dfdbf-126">Specify a different resource group name for the key vault and have the system upload a new certificate to it</span></span>

### <span data-ttu-id="dfdbf-127">Exemplo 4: traga seu próprio certificado e modelo personalizado e crie um novo cluster</span><span class="sxs-lookup"><span data-stu-id="dfdbf-127">Example 4: Bring your own Certificate and custom template and create a new cluster</span></span>

```powershell
$password = "Password#1234" | ConvertTo-SecureString -AsPlainText -Force
$resourceGroupName = "test20"
$keyVaultResourceGroupName = "test20kvrg"
$keyVaultName = "test20kv"
$localCertificateFile = "c:\Mycertificates\my2017Prodcert.pfx"
$templateParameterFile = "~\Documents\GitHub\azure-quickstart-templates-parms\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploytest.parameters.json"
$templateFile = "~\GitHub\azure-quickstart-templates\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploy.json"

New-AzServiceFabricCluster -ResourceGroupName $resourceGroupName -TemplateFile $templateFile -ParameterFile $templateParameterFile -CertificateFile $localCertificateFile -CertificatePassword $password -KeyVaultResourceGroupName $keyVaultResourceGroupName -KeyVaultName $keyVaultName
```

<span data-ttu-id="dfdbf-128">Este comando permitirá que você traga seu próprio certificado e modelo personalizado e crie um novo cluster.</span><span class="sxs-lookup"><span data-stu-id="dfdbf-128">This command will let you bring your own Certificate and custom template and create a new cluster.</span></span>

## <span data-ttu-id="dfdbf-129">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="dfdbf-129">PARAMETERS</span></span>

### <span data-ttu-id="dfdbf-130">-CertificateCommonName</span><span class="sxs-lookup"><span data-stu-id="dfdbf-130">-CertificateCommonName</span></span>

<span data-ttu-id="dfdbf-131">Nome comum do certificado</span><span class="sxs-lookup"><span data-stu-id="dfdbf-131">Certificate common name</span></span>

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

### <span data-ttu-id="dfdbf-132">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="dfdbf-132">-CertificateFile</span></span>

<span data-ttu-id="dfdbf-133">O caminho de arquivo de certificado existente para o certificado de cluster principal</span><span class="sxs-lookup"><span data-stu-id="dfdbf-133">The existing certificate file path for the primary cluster certificate</span></span>

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

### <span data-ttu-id="dfdbf-134">-CertificateIssuerThumbprint</span><span class="sxs-lookup"><span data-stu-id="dfdbf-134">-CertificateIssuerThumbprint</span></span>

<span data-ttu-id="dfdbf-135">Impressão digital do emissor de certificado, separada por vírgulas, se mais de uma</span><span class="sxs-lookup"><span data-stu-id="dfdbf-135">Certificate issuer thumbprint, separated by commas if more than one</span></span>

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

### <span data-ttu-id="dfdbf-136">-CertificateOutputFolder</span><span class="sxs-lookup"><span data-stu-id="dfdbf-136">-CertificateOutputFolder</span></span>

<span data-ttu-id="dfdbf-137">A pasta do novo arquivo de certificado a ser criado</span><span class="sxs-lookup"><span data-stu-id="dfdbf-137">The folder of the new certificate file to be created</span></span>

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

### <span data-ttu-id="dfdbf-138">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="dfdbf-138">-CertificatePassword</span></span>

<span data-ttu-id="dfdbf-139">A senha do arquivo de certificado</span><span class="sxs-lookup"><span data-stu-id="dfdbf-139">The password of the certificate file</span></span>

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

### <span data-ttu-id="dfdbf-140">-CertificateSubjectName</span><span class="sxs-lookup"><span data-stu-id="dfdbf-140">-CertificateSubjectName</span></span>

<span data-ttu-id="dfdbf-141">O nome do assunto do certificado a ser criado</span><span class="sxs-lookup"><span data-stu-id="dfdbf-141">The subject name of the certificate to be created</span></span>

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

### <span data-ttu-id="dfdbf-142">-ClusterSize</span><span class="sxs-lookup"><span data-stu-id="dfdbf-142">-ClusterSize</span></span>

<span data-ttu-id="dfdbf-143">O número de nós no cluster.</span><span class="sxs-lookup"><span data-stu-id="dfdbf-143">The number of nodes in the cluster.</span></span>
<span data-ttu-id="dfdbf-144">Padrão são 5 nós</span><span class="sxs-lookup"><span data-stu-id="dfdbf-144">Default are 5 nodes</span></span>

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

### <span data-ttu-id="dfdbf-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dfdbf-145">-DefaultProfile</span></span>

<span data-ttu-id="dfdbf-146">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="dfdbf-146">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dfdbf-147">-KeyVaultName</span><span class="sxs-lookup"><span data-stu-id="dfdbf-147">-KeyVaultName</span></span>

<span data-ttu-id="dfdbf-148">O nome do cofre de chaves do Azure, se não for dado, será padrão para o nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="dfdbf-148">Azure key vault name, if not given it will be defaulted to the resource group name</span></span>

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

### <span data-ttu-id="dfdbf-149">-KeyVaultResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dfdbf-149">-KeyVaultResourceGroupName</span></span>

<span data-ttu-id="dfdbf-150">Nome do grupo de recursos do cofre de chaves do Azure, se não for dado, ele será padrão para o nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="dfdbf-150">Azure key vault resource group name, if not given it will be defaulted to resource group name</span></span>

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

### <span data-ttu-id="dfdbf-151">-Location</span><span class="sxs-lookup"><span data-stu-id="dfdbf-151">-Location</span></span>

<span data-ttu-id="dfdbf-152">O local do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="dfdbf-152">The resource group location</span></span>

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

### <span data-ttu-id="dfdbf-153">-Name</span><span class="sxs-lookup"><span data-stu-id="dfdbf-153">-Name</span></span>

<span data-ttu-id="dfdbf-154">Especifique o nome do cluster, se não for dado, ele será o mesmo que o nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="dfdbf-154">Specify the name of the cluster, if not given it will be same as resource group name</span></span>

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

### <span data-ttu-id="dfdbf-155">-OS</span><span class="sxs-lookup"><span data-stu-id="dfdbf-155">-OS</span></span>

<span data-ttu-id="dfdbf-156">O sistema operacional das VMs que comem o cluster.</span><span class="sxs-lookup"><span data-stu-id="dfdbf-156">The Operating System of the VMs that make up the cluster.</span></span>

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

### <span data-ttu-id="dfdbf-157">-ParameterFile</span><span class="sxs-lookup"><span data-stu-id="dfdbf-157">-ParameterFile</span></span>

<span data-ttu-id="dfdbf-158">O caminho para o arquivo de parâmetro de modelo.</span><span class="sxs-lookup"><span data-stu-id="dfdbf-158">The path to the template parameter file.</span></span>

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

### <span data-ttu-id="dfdbf-159">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dfdbf-159">-ResourceGroupName</span></span>

<span data-ttu-id="dfdbf-160">Especifique o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="dfdbf-160">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="dfdbf-161">-SecondaryCertificateFile</span><span class="sxs-lookup"><span data-stu-id="dfdbf-161">-SecondaryCertificateFile</span></span>

<span data-ttu-id="dfdbf-162">O caminho do arquivo de certificado existente para o certificado de cluster secundário</span><span class="sxs-lookup"><span data-stu-id="dfdbf-162">The existing certificate file path for the secondary cluster certificate</span></span>

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

### <span data-ttu-id="dfdbf-163">-SecondaryCertificatePassword</span><span class="sxs-lookup"><span data-stu-id="dfdbf-163">-SecondaryCertificatePassword</span></span>

<span data-ttu-id="dfdbf-164">A senha do arquivo de certificado</span><span class="sxs-lookup"><span data-stu-id="dfdbf-164">The password of the certificate file</span></span>

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

### <span data-ttu-id="dfdbf-165">-SecretIdentifier</span><span class="sxs-lookup"><span data-stu-id="dfdbf-165">-SecretIdentifier</span></span>

<span data-ttu-id="dfdbf-166">A URL secreta do cofre de chaves do Azure existente, por exemplo ' https://mykv.vault.azure.net:443/secrets/mysecrets/55ec7c4dc61a462bbc645ffc9b4b225f '</span><span class="sxs-lookup"><span data-stu-id="dfdbf-166">The existing Azure key vault secret URL, for example 'https://mykv.vault.azure.net:443/secrets/mysecrets/55ec7c4dc61a462bbc645ffc9b4b225f'</span></span>

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

### <span data-ttu-id="dfdbf-167">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="dfdbf-167">-TemplateFile</span></span>

<span data-ttu-id="dfdbf-168">O caminho para o arquivo de modelo.</span><span class="sxs-lookup"><span data-stu-id="dfdbf-168">The path to the template file.</span></span>

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

### <span data-ttu-id="dfdbf-169">-Thumbprint</span><span class="sxs-lookup"><span data-stu-id="dfdbf-169">-Thumbprint</span></span>
<span data-ttu-id="dfdbf-170">A impressão digital do certificado correspoinding para SecretIdentifier.</span><span class="sxs-lookup"><span data-stu-id="dfdbf-170">The thumbprint for the certificate correspoinding to the SecretIdentifier.</span></span> <span data-ttu-id="dfdbf-171">Use isso se o certificado não for gerenciado, pois o cofre de chaves só terá o certificado armazenado como segredo e o cmdlet não poderá retrear a impressão digital.</span><span class="sxs-lookup"><span data-stu-id="dfdbf-171">Use this if the certificate is not managed as the key vault would only have the certificate stored as a secret and the cmdlet is unable to retreive the thumbprint.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExistingKeyVault
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dfdbf-172">-VmPassword</span><span class="sxs-lookup"><span data-stu-id="dfdbf-172">-VmPassword</span></span>

<span data-ttu-id="dfdbf-173">A senha da Vm.</span><span class="sxs-lookup"><span data-stu-id="dfdbf-173">The password of the Vm.</span></span>

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

### <span data-ttu-id="dfdbf-174">-VmSku</span><span class="sxs-lookup"><span data-stu-id="dfdbf-174">-VmSku</span></span>

<span data-ttu-id="dfdbf-175">O Vm Sku</span><span class="sxs-lookup"><span data-stu-id="dfdbf-175">The Vm Sku</span></span>

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

### <span data-ttu-id="dfdbf-176">-VmUserName</span><span class="sxs-lookup"><span data-stu-id="dfdbf-176">-VmUserName</span></span>

<span data-ttu-id="dfdbf-177">O nome de usuário para o log em Vm</span><span class="sxs-lookup"><span data-stu-id="dfdbf-177">The user name for logging to Vm</span></span>

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

### <span data-ttu-id="dfdbf-178">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dfdbf-178">-Confirm</span></span>

<span data-ttu-id="dfdbf-179">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dfdbf-179">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dfdbf-180">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dfdbf-180">-WhatIf</span></span>

<span data-ttu-id="dfdbf-181">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="dfdbf-181">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dfdbf-182">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="dfdbf-182">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dfdbf-183">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dfdbf-183">CommonParameters</span></span>
<span data-ttu-id="dfdbf-184">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dfdbf-184">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dfdbf-185">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dfdbf-185">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dfdbf-186">INPUTS</span><span class="sxs-lookup"><span data-stu-id="dfdbf-186">INPUTS</span></span>

### <span data-ttu-id="dfdbf-187">System.String</span><span class="sxs-lookup"><span data-stu-id="dfdbf-187">System.String</span></span>

### <span data-ttu-id="dfdbf-188">System.Security.SecureString</span><span class="sxs-lookup"><span data-stu-id="dfdbf-188">System.Security.SecureString</span></span>

### <span data-ttu-id="dfdbf-189">System.Int32</span><span class="sxs-lookup"><span data-stu-id="dfdbf-189">System.Int32</span></span>

### <span data-ttu-id="dfdbf-190">Microsoft.Azure.Commands.ServiceFabric.Models.OperatingSystem</span><span class="sxs-lookup"><span data-stu-id="dfdbf-190">Microsoft.Azure.Commands.ServiceFabric.Models.OperatingSystem</span></span>

## <span data-ttu-id="dfdbf-191">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="dfdbf-191">OUTPUTS</span></span>

### <span data-ttu-id="dfdbf-192">Microsoft.Azure.Commands.ServiceFabric.Models.PSDeploymentResult</span><span class="sxs-lookup"><span data-stu-id="dfdbf-192">Microsoft.Azure.Commands.ServiceFabric.Models.PSDeploymentResult</span></span>

## <span data-ttu-id="dfdbf-193">NOTES</span><span class="sxs-lookup"><span data-stu-id="dfdbf-193">NOTES</span></span>

## <span data-ttu-id="dfdbf-194">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="dfdbf-194">RELATED LINKS</span></span>
