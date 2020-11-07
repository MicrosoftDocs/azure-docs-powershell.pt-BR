---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/add-azservicefabricapplicationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricApplicationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricApplicationCertificate.md
ms.openlocfilehash: 62298a5747a8bb5b4f01458cac611f5e86869ee7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93773206"
---
# <span data-ttu-id="57fa9-101">Add-AzServiceFabricApplicationCertificate</span><span class="sxs-lookup"><span data-stu-id="57fa9-101">Add-AzServiceFabricApplicationCertificate</span></span>

## <span data-ttu-id="57fa9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="57fa9-102">SYNOPSIS</span></span>
<span data-ttu-id="57fa9-103">Adicione um novo certificado ao (s) conjunto (s) de escala da máquina virtual que compõe o cluster.</span><span class="sxs-lookup"><span data-stu-id="57fa9-103">Add a new certificate to the Virtual Machine Scale Set(s) that make up the cluster.</span></span> <span data-ttu-id="57fa9-104">O certificado deve ser usado como um certificado de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="57fa9-104">The certificate is intended to be used as an application certificate.</span></span>

## <span data-ttu-id="57fa9-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="57fa9-105">SYNTAX</span></span>

### <span data-ttu-id="57fa9-106">ByExistingKeyVault</span><span class="sxs-lookup"><span data-stu-id="57fa9-106">ByExistingKeyVault</span></span>
```
Add-AzServiceFabricApplicationCertificate [-ResourceGroupName] <String> [-Name] <String>
 -SecretIdentifier <String> [-CertificateCommonName <String>] [-CertificateIssuerThumbprint <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="57fa9-107">ByNewPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="57fa9-107">ByNewPfxAndVaultName</span></span>
```
Add-AzServiceFabricApplicationCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-KeyVaultResourceGroupName <String>] [-KeyVaultName <String>] [-CertificateOutputFolder <String>]
 [-CertificatePassword <SecureString>] -CertificateSubjectName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="57fa9-108">ByExistingPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="57fa9-108">ByExistingPfxAndVaultName</span></span>
```
Add-AzServiceFabricApplicationCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-KeyVaultResourceGroupName <String>] [-KeyVaultName <String>] -CertificateFile <String>
 [-CertificatePassword <SecureString>] [-CertificateCommonName <String>]
 [-CertificateIssuerThumbprint <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="57fa9-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="57fa9-109">DESCRIPTION</span></span>
<span data-ttu-id="57fa9-110">Use **Add-AzServiceFabricApplicationCertificate** para instalar um certificado em todos os nós do cluster.</span><span class="sxs-lookup"><span data-stu-id="57fa9-110">Use **Add-AzServiceFabricApplicationCertificate** to install a certificate to all nodes in the cluster.</span></span> <span data-ttu-id="57fa9-111">Você pode especificar um certificado que você já tem ou ter o sistema gera um novo para você e carregá-lo em um cofre de chaves do Azure novo ou existente.</span><span class="sxs-lookup"><span data-stu-id="57fa9-111">You can specify a certificate you already have or have the system generate a new one for you, and upload it to a new or existing Azure key vault.</span></span>

## <span data-ttu-id="57fa9-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="57fa9-112">EXAMPLES</span></span>

### <span data-ttu-id="57fa9-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="57fa9-113">Example 1</span></span>
```powershell
PS c:> Add-AzServiceFabricApplicationCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -SecretIdentifier 'https://contoso03vault.vault.azure.net/secrets/contoso03vaultrg/7f7de9131c034172b9df37ccc549524f'
```

<span data-ttu-id="57fa9-114">Esse comando adicionará um certificado do cofre de chaves do Azure existente a todos os tipos de nó do cluster.</span><span class="sxs-lookup"><span data-stu-id="57fa9-114">This command will add a certificate from existing Azure key vault to all node types of the cluster.</span></span>

### <span data-ttu-id="57fa9-115">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="57fa9-115">Example 2</span></span>
```
PS c:\> $pwd = ConvertTo-SecureString -String '123' -AsPlainText -Force
PS C:\> Add-AzServiceFabricApplicationCertificate -ResourceGroupName 'Group2' -Name 'Contoso02SFCluster' -KeyVaultName 'Contoso02Vault' -KeyVaultResouceGroupName 'Contoso02VaultRg'
        -CertificateSubjectName 'cn=Contoso.com' -CertificateOutputFolder 'c:\test' -CertificatePassword $pwd
```

<span data-ttu-id="57fa9-116">Esse comando criará um certificado auto-assinado no cofre de chaves do Azure com o nome do grupo de recursos do cofre de chaves e o nome do cofre de chaves, será instalado em todos os tipos de nó do cluster e baixará o certificado na pasta ' c:\test '.</span><span class="sxs-lookup"><span data-stu-id="57fa9-116">This command will create a self-signed certificate in the Azure key vault with the key vault resource group name and key vault Name, installs to all node types of the cluster, and downloads the certificate under folder 'c:\test'.</span></span> <span data-ttu-id="57fa9-117">O nome do certificado baixado é igual ao nome do certificado do cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="57fa9-117">The name of the certificate downloaded is same as the name of key vault certificate.</span></span>

## <span data-ttu-id="57fa9-118">OS</span><span class="sxs-lookup"><span data-stu-id="57fa9-118">PARAMETERS</span></span>

### <span data-ttu-id="57fa9-119">-CertificateCommonName</span><span class="sxs-lookup"><span data-stu-id="57fa9-119">-CertificateCommonName</span></span>
<span data-ttu-id="57fa9-120">Nome comum do certificado</span><span class="sxs-lookup"><span data-stu-id="57fa9-120">Certificate common name</span></span>

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

### <span data-ttu-id="57fa9-121">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="57fa9-121">-CertificateFile</span></span>
<span data-ttu-id="57fa9-122">O caminho para o certificado existente</span><span class="sxs-lookup"><span data-stu-id="57fa9-122">The path to the existing certificate</span></span>

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

### <span data-ttu-id="57fa9-123">-CertificateIssuerThumbprint</span><span class="sxs-lookup"><span data-stu-id="57fa9-123">-CertificateIssuerThumbprint</span></span>
<span data-ttu-id="57fa9-124">Impressão digital do emissor do certificado, separada por vírgulas, se mais de um</span><span class="sxs-lookup"><span data-stu-id="57fa9-124">Certificate issuer thumbprint, separated by commas if more than one</span></span>

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

### <span data-ttu-id="57fa9-125">-CertificateOutputFolder</span><span class="sxs-lookup"><span data-stu-id="57fa9-125">-CertificateOutputFolder</span></span>
<span data-ttu-id="57fa9-126">A pasta onde o novo certificado precisa ser baixado.</span><span class="sxs-lookup"><span data-stu-id="57fa9-126">The folder where the new certificate needs to be downloaded.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNewPfxAndVaultName
Aliases: Destination

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="57fa9-127">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="57fa9-127">-CertificatePassword</span></span>
<span data-ttu-id="57fa9-128">A senha do certificado</span><span class="sxs-lookup"><span data-stu-id="57fa9-128">The password of the certificate</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: ByNewPfxAndVaultName, ByExistingPfxAndVaultName
Aliases: CertPassword

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="57fa9-129">-CertificateSubjectName</span><span class="sxs-lookup"><span data-stu-id="57fa9-129">-CertificateSubjectName</span></span>
<span data-ttu-id="57fa9-130">O nome do requerente do certificado</span><span class="sxs-lookup"><span data-stu-id="57fa9-130">The subject name of the certificate</span></span>

```yaml
Type: System.String
Parameter Sets: ByNewPfxAndVaultName
Aliases: Subject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="57fa9-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57fa9-131">-DefaultProfile</span></span>
<span data-ttu-id="57fa9-132">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="57fa9-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="57fa9-133">-Keyvaultname</span><span class="sxs-lookup"><span data-stu-id="57fa9-133">-KeyVaultName</span></span>
<span data-ttu-id="57fa9-134">Nome do cofre de chave do Azure, se não for fornecido, será definido como padrão para o nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="57fa9-134">Azure key vault name, if not given it will be defaulted to the resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: ByNewPfxAndVaultName, ByExistingPfxAndVaultName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="57fa9-135">-KeyVaultResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57fa9-135">-KeyVaultResourceGroupName</span></span>
<span data-ttu-id="57fa9-136">Nome do grupo de recursos do cofre de chaves do Azure, se não for fornecido padrão para o nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="57fa9-136">Azure key vault resource group name, if not given it will be defaulted to resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: ByNewPfxAndVaultName, ByExistingPfxAndVaultName
Aliases: KeyVaultResouceGroupName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="57fa9-137">-Nome</span><span class="sxs-lookup"><span data-stu-id="57fa9-137">-Name</span></span>
<span data-ttu-id="57fa9-138">Especificar o nome do cluster</span><span class="sxs-lookup"><span data-stu-id="57fa9-138">Specify the name of the cluster</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57fa9-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57fa9-139">-ResourceGroupName</span></span>
<span data-ttu-id="57fa9-140">Especifique o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="57fa9-140">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="57fa9-141">-SecretIdentifier</span><span class="sxs-lookup"><span data-stu-id="57fa9-141">-SecretIdentifier</span></span>
<span data-ttu-id="57fa9-142">A URL do segredo do Azure Key Vault existente, por exemplo ' https://mykv.vault.azure.net:443/secrets/mysecrets/55ec7c4dc61a462bbc645ffc9b4b225f '</span><span class="sxs-lookup"><span data-stu-id="57fa9-142">The existing Azure key vault secret URL, for example 'https://mykv.vault.azure.net:443/secrets/mysecrets/55ec7c4dc61a462bbc645ffc9b4b225f'</span></span>

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

### <span data-ttu-id="57fa9-143">-Confirme</span><span class="sxs-lookup"><span data-stu-id="57fa9-143">-Confirm</span></span>
<span data-ttu-id="57fa9-144">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="57fa9-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="57fa9-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="57fa9-145">-WhatIf</span></span>
<span data-ttu-id="57fa9-146">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="57fa9-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="57fa9-147">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="57fa9-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="57fa9-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57fa9-148">CommonParameters</span></span>
<span data-ttu-id="57fa9-149">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57fa9-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57fa9-150">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="57fa9-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57fa9-151">SENSORES</span><span class="sxs-lookup"><span data-stu-id="57fa9-151">INPUTS</span></span>

### <span data-ttu-id="57fa9-152">System. String</span><span class="sxs-lookup"><span data-stu-id="57fa9-152">System.String</span></span>

### <span data-ttu-id="57fa9-153">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="57fa9-153">System.Security.SecureString</span></span>

## <span data-ttu-id="57fa9-154">EXIBE</span><span class="sxs-lookup"><span data-stu-id="57fa9-154">OUTPUTS</span></span>

### <span data-ttu-id="57fa9-155">Microsoft. Azure. Commands. imfabric. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="57fa9-155">Microsoft.Azure.Commands.ServiceFabric.Models.PSKeyVault</span></span>

## <span data-ttu-id="57fa9-156">INFORMA</span><span class="sxs-lookup"><span data-stu-id="57fa9-156">NOTES</span></span>

## <span data-ttu-id="57fa9-157">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="57fa9-157">RELATED LINKS</span></span>

[<span data-ttu-id="57fa9-158">Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="57fa9-158">Add-AzServiceFabricClusterCertificate</span></span>](./Add-AzServiceFabricClusterCertificate.md)

[<span data-ttu-id="57fa9-159">New-AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="57fa9-159">New-AzServiceFabricCluster</span></span>](./New-AzServiceFabricCluster.md)
