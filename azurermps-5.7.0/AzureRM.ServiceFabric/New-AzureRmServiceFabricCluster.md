---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric/new-azurermservicefabriccluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/New-AzureRmServiceFabricCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/New-AzureRmServiceFabricCluster.md
ms.openlocfilehash: 5da8d1f48a50cafc970278d59b99750f283a9414
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432396"
---
# <span data-ttu-id="68efc-101">New-AzureRmServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="68efc-101">New-AzureRmServiceFabricCluster</span></span>

## <span data-ttu-id="68efc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="68efc-102">SYNOPSIS</span></span>
<span data-ttu-id="68efc-103">Esse comando usa certificados que você fornece ou certificados autoassinados gerados pelo sistema para configurar um novo cluster de Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="68efc-103">This command uses certificates that you provide or system generated self-signed certificates to set up a new service fabric cluster.</span></span> <span data-ttu-id="68efc-104">Ele pode usar um modelo padrão ou um modelo personalizado fornecido por você.</span><span class="sxs-lookup"><span data-stu-id="68efc-104">It can use a default template or a custom template that you provide.</span></span> <span data-ttu-id="68efc-105">Você tem a opção de especificar uma pasta para exportar os certificados autoassinados ou para extraí-los mais tarde do cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="68efc-105">You have the option of specifying a folder to export the self-signed certificates to or fetching them later from the key vault.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="68efc-106">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="68efc-106">SYNTAX</span></span>

### <span data-ttu-id="68efc-107">ByDefaultArmTemplate (padrão)</span><span class="sxs-lookup"><span data-stu-id="68efc-107">ByDefaultArmTemplate (Default)</span></span>
```
New-AzureRmServiceFabricCluster [-ResourceGroupName] <String> [-CertificateOutputFolder <String>]
 [-CertificatePassword <SecureString>] [-KeyVaultResouceGroupName <String>] [-KeyVaultName <String>]
 -Location <String> [-Name <String>] [-VmUserName <String>] [-ClusterSize <Int32>]
 [-CertificateSubjectName <String>] -VmPassword <SecureString> [-OS <OperatingSystem>] [-VmSku <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="68efc-108">ByExistingKeyVault</span><span class="sxs-lookup"><span data-stu-id="68efc-108">ByExistingKeyVault</span></span>
```
New-AzureRmServiceFabricCluster [-ResourceGroupName] <String> -TemplateFile <String> -ParameterFile <String>
 [-VmPassword <SecureString>] -SecretIdentifier <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="68efc-109">ByNewPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="68efc-109">ByNewPfxAndVaultName</span></span>
```
New-AzureRmServiceFabricCluster [-ResourceGroupName] <String> -TemplateFile <String> -ParameterFile <String>
 [-CertificateOutputFolder <String>] [-CertificatePassword <SecureString>] [-KeyVaultResouceGroupName <String>]
 [-KeyVaultName <String>] [-CertificateSubjectName <String>] [-VmPassword <SecureString>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="68efc-110">ByExistingPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="68efc-110">ByExistingPfxAndVaultName</span></span>
```
New-AzureRmServiceFabricCluster [-ResourceGroupName] <String> -TemplateFile <String> -ParameterFile <String>
 -CertificateFile <String> [-CertificatePassword <SecureString>] [-SecondaryCertificateFile <String>]
 [-SecondaryCertificatePassword <SecureString>] [-KeyVaultResouceGroupName <String>] [-KeyVaultName <String>]
 [-VmPassword <SecureString>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="68efc-111">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="68efc-111">DESCRIPTION</span></span>
<span data-ttu-id="68efc-112">O comando **New-AzureRmServiceFabricCluster** usa certificados que você fornece ou certificados autoassinados gerados pelo sistema para configurar um novo cluster do Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="68efc-112">The **New-AzureRmServiceFabricCluster** command uses certificates that you provide or system generated self-signed certificates to set up a new service fabric cluster.</span></span> <span data-ttu-id="68efc-113">O modelo usado pode ser um modelo padrão ou um modelo personalizado fornecido por você.</span><span class="sxs-lookup"><span data-stu-id="68efc-113">The template used can be a default template or a custom template that you provide.</span></span> <span data-ttu-id="68efc-114">Você tem a opção de especificar uma pasta para exportar os certificados autoassinados ou para obtê-los mais tarde do cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="68efc-114">You have the option of specifying a folder to export the self-signed certificates or fetching them later from the key vault.</span></span>

<span data-ttu-id="68efc-115">Se você estiver especificando um arquivo de modelo e de modelo personalizado, não será necessário fornecer as informações de certificado no arquivo de parâmetro, o sistema preencherá esses parâmetros.</span><span class="sxs-lookup"><span data-stu-id="68efc-115">If you are specifying a custom template and parameter file, you don't need to provide the certificate information in the parameter file, the system will populate these parameters.</span></span>

<span data-ttu-id="68efc-116">As quatro opções são detalhadas abaixo.</span><span class="sxs-lookup"><span data-stu-id="68efc-116">The four options are detailed below.</span></span> <span data-ttu-id="68efc-117">Role a tela para baixo para obter explicações de cada um dos parâmetros.</span><span class="sxs-lookup"><span data-stu-id="68efc-117">Scroll down for explanations of each of the parameters.</span></span>

## <span data-ttu-id="68efc-118">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="68efc-118">EXAMPLES</span></span>

### <span data-ttu-id="68efc-119">Exemplo 1: especifique apenas o tamanho do cluster, o nome do requerente do certificado e o sistema operacional para implantar um cluster.</span><span class="sxs-lookup"><span data-stu-id="68efc-119">Example 1: Specify only the cluster size, the cert subject name, and the OS to deploy a cluster.</span></span>
```
$pass="Password#1234" | ConvertTo-SecureString -AsPlainText -Force
$RGname="test01"
$clusterloc="SouthCentralUS"
$subname="{0}.{1}.cloudapp.azure.com" -f $RGname, $clusterloc
$pfxfolder="~\Documents"

Write-Output "Create cluster in '$clusterloc' with cert subject name '$subname' and cert output path '$pfxfolder'"

New-AzureRmServiceFabricCluster -ResourceGroupName $RGname -Location $clusterloc -ClusterSize 3 -VmPassword $pass -CertificateSubjectName $subname -CertificateOutputFolder $pfxfolder -CertificatePassword $pass -OS WindowsServer2016Datacenter
```

<span data-ttu-id="68efc-120">Esse comando especifica somente o tamanho do cluster, o nome do requerente do certificado e o sistema operacional para implantar um cluster.</span><span class="sxs-lookup"><span data-stu-id="68efc-120">This command specifies only the cluster size, the cert subject name, and the OS to deploy a cluster.</span></span>

### <span data-ttu-id="68efc-121">Exemplo 2: especificar um recurso de certificado existente em um cofre de chaves e um modelo personalizado para implantar um cluster</span><span class="sxs-lookup"><span data-stu-id="68efc-121">Example 2: Specify an existing Certificate resource in a key vault and a custom template to deploy a cluster</span></span>
```
$RGname="test20"
$templateParmfile="C:\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploytest.parameters.json"
$templateFile="C:\azure-quickstart-templates\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploy.json"
$secretId="https://test1.vault.azure.net:443/secrets/testcertificate4/56ec774dc61a462bbc645ffc9b4b225f"

New-AzureRmServiceFabricCluster -ResourceGroupName $RGname -TemplateFile $templateFile -ParameterFile $templateParmfile -SecretIdentifier $secretId
```

<span data-ttu-id="68efc-122">Esse comando especifica um recurso de certificado existente em um cofre de chaves e um modelo personalizado para implantar um cluster.</span><span class="sxs-lookup"><span data-stu-id="68efc-122">This command specifies an existing Certificate resource in a key vault and a custom template to deploy a cluster.</span></span>

### <span data-ttu-id="68efc-123">Exemplo 3: criar um novo cluster usando um modelo personalizado.</span><span class="sxs-lookup"><span data-stu-id="68efc-123">Example 3: Create a new cluster using a custom template.</span></span> <span data-ttu-id="68efc-124">Especificar um nome de grupo de recursos diferente para o cofre de chaves e fazer com que o sistema carregue um novo certificado</span><span class="sxs-lookup"><span data-stu-id="68efc-124">Specify a different resource group name for the key vault and have the system upload a new certificate to it</span></span>
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

New-AzureRmServiceFabricCluster -ResourceGroupName $RGname -TemplateFile $templateFile -ParameterFile $templateParmfile -CertificateOutputFolder $pfxfolder -CertificatePassword $pass -KeyVaultResouceGroupName $keyVaultRG  -KeyVaultName $keyVault -CertificateSubjectName $subname
```

<span data-ttu-id="68efc-125">Esse comando cria um novo cluster usando um modelo personalizado.</span><span class="sxs-lookup"><span data-stu-id="68efc-125">This command creates a new cluster using a custom template.</span></span> <span data-ttu-id="68efc-126">Especificar um nome de grupo de recursos diferente para o cofre de chaves e fazer com que o sistema carregue um novo certificado</span><span class="sxs-lookup"><span data-stu-id="68efc-126">Specify a different resource group name for the key vault and have the system upload a new certificate to it</span></span>

### <span data-ttu-id="68efc-127">Exemplo 4: Traga seu próprio certificado e modelo personalizado e crie um novo cluster</span><span class="sxs-lookup"><span data-stu-id="68efc-127">Example 4: Bring your own Certificate and custom template and create a new cluster</span></span>
```
$pass="Password#1234" | ConvertTo-SecureString -AsPlainText -Force
$RGname="test20"
$keyVaultRG="test20kvrg"
$keyVault="test20kv"
$pfxsourcefile="c:\Mycertificates\my2017Prodcert.pfx"
$templateParmfile="~\Documents\GitHub\azure-quickstart-templates-parms\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploytest.parameters.json"
$templateFile="~\GitHub\azure-quickstart-templates\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploy.json"

New-AzureRmServiceFabricCluster -ResourceGroupName $RGname -TemplateFile $templateFile -ParameterFile $templateParmfile -CertificateFile $pfxsourcefile -CertificatePassword $pass -KeyVaultResouceGroupName $keyVaultRG -KeyVaultName $keyVault
```

<span data-ttu-id="68efc-128">Este comando permitirá que você traga seu próprio certificado e modelo personalizado e crie um novo cluster.</span><span class="sxs-lookup"><span data-stu-id="68efc-128">This command will let you bring your own Certificate and custom template and create a new cluster.</span></span>

## <span data-ttu-id="68efc-129">OS</span><span class="sxs-lookup"><span data-stu-id="68efc-129">PARAMETERS</span></span>

### <span data-ttu-id="68efc-130">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="68efc-130">-CertificateFile</span></span>
<span data-ttu-id="68efc-131">O caminho do arquivo de certificado existente para o certificado de cluster primário.</span><span class="sxs-lookup"><span data-stu-id="68efc-131">The existing certificate file path for the primary cluster certificate.</span></span>

```yaml
Type: String
Parameter Sets: ByExistingPfxAndVaultName
Aliases: Source

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="68efc-132">-CertificateOutputFolder</span><span class="sxs-lookup"><span data-stu-id="68efc-132">-CertificateOutputFolder</span></span>
<span data-ttu-id="68efc-133">A pasta do novo arquivo de certificado a ser criado.</span><span class="sxs-lookup"><span data-stu-id="68efc-133">The folder of the new certificate file to be created.</span></span>

```yaml
Type: String
Parameter Sets: ByDefaultArmTemplate, ByNewPfxAndVaultName
Aliases: Destination

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="68efc-134">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="68efc-134">-CertificatePassword</span></span>
<span data-ttu-id="68efc-135">A senha do arquivo de certificado.</span><span class="sxs-lookup"><span data-stu-id="68efc-135">The password of the certificate file.</span></span>

```yaml
Type: SecureString
Parameter Sets: ByDefaultArmTemplate, ByNewPfxAndVaultName, ByExistingPfxAndVaultName
Aliases: CertPassword

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="68efc-136">-CertificateSubjectName</span><span class="sxs-lookup"><span data-stu-id="68efc-136">-CertificateSubjectName</span></span>
<span data-ttu-id="68efc-137">O nome do requerente do certificado a ser criado.</span><span class="sxs-lookup"><span data-stu-id="68efc-137">The subject name of the certificate to be created.</span></span>

```yaml
Type: String
Parameter Sets: ByDefaultArmTemplate, ByNewPfxAndVaultName
Aliases: Subject

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="68efc-138">-ClusterSize</span><span class="sxs-lookup"><span data-stu-id="68efc-138">-ClusterSize</span></span>
<span data-ttu-id="68efc-139">O número de nós no cluster.</span><span class="sxs-lookup"><span data-stu-id="68efc-139">The number of nodes in the cluster.</span></span> <span data-ttu-id="68efc-140">Padrão são 5 nós.</span><span class="sxs-lookup"><span data-stu-id="68efc-140">Default are 5 nodes.</span></span>

```yaml
Type: Int32
Parameter Sets: ByDefaultArmTemplate
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="68efc-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68efc-141">-DefaultProfile</span></span>
<span data-ttu-id="68efc-142">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="68efc-142">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="68efc-143">-Keyvaultname</span><span class="sxs-lookup"><span data-stu-id="68efc-143">-KeyVaultName</span></span>
<span data-ttu-id="68efc-144">Nome do cofre de chave do Azure.</span><span class="sxs-lookup"><span data-stu-id="68efc-144">Azure key vault name.</span></span> <span data-ttu-id="68efc-145">Se não for especificado, o nome do grupo de recursos será definido como padrão.</span><span class="sxs-lookup"><span data-stu-id="68efc-145">If not given, it will be defaulted to the resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByDefaultArmTemplate, ByNewPfxAndVaultName, ByExistingPfxAndVaultName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="68efc-146">-KeyVaultResouceGroupName</span><span class="sxs-lookup"><span data-stu-id="68efc-146">-KeyVaultResouceGroupName</span></span>
<span data-ttu-id="68efc-147">Nome do grupo de recursos do cofre de chaves do Azure.</span><span class="sxs-lookup"><span data-stu-id="68efc-147">Azure key vault resource group name.</span></span> <span data-ttu-id="68efc-148">Se não for especificado, o nome do grupo de recursos será definido como padrão.</span><span class="sxs-lookup"><span data-stu-id="68efc-148">If not given, it will be defaulted to resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByDefaultArmTemplate, ByNewPfxAndVaultName, ByExistingPfxAndVaultName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="68efc-149">-Local</span><span class="sxs-lookup"><span data-stu-id="68efc-149">-Location</span></span>
<span data-ttu-id="68efc-150">O local do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="68efc-150">The resource group location.</span></span>

```yaml
Type: String
Parameter Sets: ByDefaultArmTemplate
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="68efc-151">-Nome</span><span class="sxs-lookup"><span data-stu-id="68efc-151">-Name</span></span>
<span data-ttu-id="68efc-152">Especifique o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="68efc-152">Specify the name of the cluster.</span></span> <span data-ttu-id="68efc-153">Se não for especificado, ele será igual ao nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="68efc-153">If not given, it will be same as resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByDefaultArmTemplate
Aliases: ClusterName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="68efc-154">-OS</span><span class="sxs-lookup"><span data-stu-id="68efc-154">-OS</span></span>
<span data-ttu-id="68efc-155">O sistema operacional das VMs que compõem o cluster.</span><span class="sxs-lookup"><span data-stu-id="68efc-155">The Operating System of the VMs that make up the cluster.</span></span>

```yaml
Type: OperatingSystem
Parameter Sets: ByDefaultArmTemplate
Aliases: VmImage
Accepted values: WindowsServer2012R2Datacenter, WindowsServer2016Datacenter, WindowsServer2016DatacenterwithContainers, UbuntuServer1604

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68efc-156">-Parameterfile</span><span class="sxs-lookup"><span data-stu-id="68efc-156">-ParameterFile</span></span>
<span data-ttu-id="68efc-157">O caminho para o arquivo de parâmetro do modelo.</span><span class="sxs-lookup"><span data-stu-id="68efc-157">The path to the template parameter file.</span></span>

```yaml
Type: String
Parameter Sets: ByExistingKeyVault, ByNewPfxAndVaultName, ByExistingPfxAndVaultName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="68efc-158">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68efc-158">-ResourceGroupName</span></span>
<span data-ttu-id="68efc-159">Especifique o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="68efc-159">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="68efc-160">-SecondaryCertificateFile</span><span class="sxs-lookup"><span data-stu-id="68efc-160">-SecondaryCertificateFile</span></span>
<span data-ttu-id="68efc-161">O caminho do arquivo de certificado existente para o certificado de cluster secundário.</span><span class="sxs-lookup"><span data-stu-id="68efc-161">The existing certificate file path for the secondary cluster certificate.</span></span>

```yaml
Type: String
Parameter Sets: ByExistingPfxAndVaultName
Aliases: SecSource

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="68efc-162">-SecondaryCertificatePassword</span><span class="sxs-lookup"><span data-stu-id="68efc-162">-SecondaryCertificatePassword</span></span>
<span data-ttu-id="68efc-163">A senha do arquivo de certificado.</span><span class="sxs-lookup"><span data-stu-id="68efc-163">The password of the certificate file.</span></span>

```yaml
Type: SecureString
Parameter Sets: ByExistingPfxAndVaultName
Aliases: SecCertPassword

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="68efc-164">-SecretIdentifier</span><span class="sxs-lookup"><span data-stu-id="68efc-164">-SecretIdentifier</span></span>
<span data-ttu-id="68efc-165">A URL do segredo do Azure Key Vault existente, por exemplo: ' https://mykv.vault.azure.net:443/secrets/mysecrets/55ec7c4dc61a462bbc645ffc9b4b225f '.</span><span class="sxs-lookup"><span data-stu-id="68efc-165">The existing Azure key vault secret URL, for example: 'https://mykv.vault.azure.net:443/secrets/mysecrets/55ec7c4dc61a462bbc645ffc9b4b225f'.</span></span>

```yaml
Type: String
Parameter Sets: ByExistingKeyVault
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="68efc-166">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="68efc-166">-TemplateFile</span></span>
<span data-ttu-id="68efc-167">O caminho para o arquivo de modelo.</span><span class="sxs-lookup"><span data-stu-id="68efc-167">The path to the template file.</span></span>

```yaml
Type: String
Parameter Sets: ByExistingKeyVault, ByNewPfxAndVaultName, ByExistingPfxAndVaultName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="68efc-168">-VmPassword</span><span class="sxs-lookup"><span data-stu-id="68efc-168">-VmPassword</span></span>
<span data-ttu-id="68efc-169">A senha da VM.</span><span class="sxs-lookup"><span data-stu-id="68efc-169">The password of the Vm.</span></span>

```yaml
Type: SecureString
Parameter Sets: ByDefaultArmTemplate
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: SecureString
Parameter Sets: ByExistingKeyVault, ByNewPfxAndVaultName, ByExistingPfxAndVaultName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68efc-170">-VmSku</span><span class="sxs-lookup"><span data-stu-id="68efc-170">-VmSku</span></span>
<span data-ttu-id="68efc-171">A SKU da VM.</span><span class="sxs-lookup"><span data-stu-id="68efc-171">The Vm Sku.</span></span>

```yaml
Type: String
Parameter Sets: ByDefaultArmTemplate
Aliases: Sku

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68efc-172">-VmUserName</span><span class="sxs-lookup"><span data-stu-id="68efc-172">-VmUserName</span></span>
<span data-ttu-id="68efc-173">O nome de usuário para fazer logon na VM.</span><span class="sxs-lookup"><span data-stu-id="68efc-173">The user name for logging to Vm.</span></span>

```yaml
Type: String
Parameter Sets: ByDefaultArmTemplate
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="68efc-174">-Confirme</span><span class="sxs-lookup"><span data-stu-id="68efc-174">-Confirm</span></span>
<span data-ttu-id="68efc-175">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="68efc-175">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68efc-176">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="68efc-176">-WhatIf</span></span>
<span data-ttu-id="68efc-177">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="68efc-177">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="68efc-178">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="68efc-178">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68efc-179">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68efc-179">CommonParameters</span></span>
<span data-ttu-id="68efc-180">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="68efc-180">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68efc-181">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="68efc-181">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68efc-182">SENSORES</span><span class="sxs-lookup"><span data-stu-id="68efc-182">INPUTS</span></span>

### <span data-ttu-id="68efc-183">System. String</span><span class="sxs-lookup"><span data-stu-id="68efc-183">System.String</span></span>
<span data-ttu-id="68efc-184">System. Security. SecureString System. Int32 Microsoft. Azure. Commands. Fabric. Models. OperatingSystem</span><span class="sxs-lookup"><span data-stu-id="68efc-184">System.Security.SecureString System.Int32 Microsoft.Azure.Commands.ServiceFabric.Models.OperatingSystem</span></span>

## <span data-ttu-id="68efc-185">EXIBE</span><span class="sxs-lookup"><span data-stu-id="68efc-185">OUTPUTS</span></span>

### <span data-ttu-id="68efc-186">Microsoft.Azure.Commands.ServiceFabric.Models.PSDeploymentResult</span><span class="sxs-lookup"><span data-stu-id="68efc-186">Microsoft.Azure.Commands.ServiceFabric.Models.PSDeploymentResult</span></span>

## <span data-ttu-id="68efc-187">INFORMA</span><span class="sxs-lookup"><span data-stu-id="68efc-187">NOTES</span></span>

## <span data-ttu-id="68efc-188">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="68efc-188">RELATED LINKS</span></span>

