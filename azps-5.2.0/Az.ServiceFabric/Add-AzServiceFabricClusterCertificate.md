---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/add-azservicefabricclustercertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricClusterCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricClusterCertificate.md
ms.openlocfilehash: c3ddf8373b467b3f7821d9470f67f2b864201949
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98260818"
---
# <span data-ttu-id="d353c-101">Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="d353c-101">Add-AzServiceFabricClusterCertificate</span></span>

## <span data-ttu-id="d353c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d353c-102">SYNOPSIS</span></span>
<span data-ttu-id="d353c-103">Adicione um certificado de cluster secundário ao cluster.</span><span class="sxs-lookup"><span data-stu-id="d353c-103">Add a secondary cluster certificate to the cluster.</span></span>

## <span data-ttu-id="d353c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d353c-104">SYNTAX</span></span>

### <span data-ttu-id="d353c-105">ByExistingKeyVault</span><span class="sxs-lookup"><span data-stu-id="d353c-105">ByExistingKeyVault</span></span>
```
Add-AzServiceFabricClusterCertificate [-ResourceGroupName] <String> [-Name] <String> -SecretIdentifier <String>
 [-Thumbprint <String>] [-CertificateCommonName <String>] [-CertificateIssuerThumbprint <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d353c-106">ByNewPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="d353c-106">ByNewPfxAndVaultName</span></span>
```
Add-AzServiceFabricClusterCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-KeyVaultResourceGroupName <String>] [-KeyVaultName <String>] [-CertificateOutputFolder <String>]
 [-CertificatePassword <SecureString>] -CertificateSubjectName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d353c-107">ByExistingPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="d353c-107">ByExistingPfxAndVaultName</span></span>
```
Add-AzServiceFabricClusterCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-KeyVaultResourceGroupName <String>] [-KeyVaultName <String>] -CertificateFile <String>
 [-CertificatePassword <SecureString>] [-CertificateCommonName <String>]
 [-CertificateIssuerThumbprint <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d353c-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d353c-108">DESCRIPTION</span></span>
<span data-ttu-id="d353c-109">Use **Add-AzServiceFabricClusterCertificate** para adicionar um certificado de cluster secundário, seja de um cofre de chaves do Azure existente ou criando um novo cofre de chaves do Azure usando um certificado existente fornecido ou a partir de um novo certificado auto-assinado criado.</span><span class="sxs-lookup"><span data-stu-id="d353c-109">Use **Add-AzServiceFabricClusterCertificate** to add a secondary cluster certificate, either from an existing Azure key vault or creating a new Azure key vault using an existing certificate provided or from a new self-signed certificate created.</span></span> <span data-ttu-id="d353c-110">Ele substituirá o cluster secundário, se houver.</span><span class="sxs-lookup"><span data-stu-id="d353c-110">It will override the secondary cluster if there is any.</span></span>

## <span data-ttu-id="d353c-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d353c-111">EXAMPLES</span></span>

### <span data-ttu-id="d353c-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d353c-112">Example 1</span></span>
```powershell
Add-AzServiceFabricClusterCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' 
-SecretIdentifier 'https://contoso03vault.vault.azure.net/secrets/contoso03vaultrg/7f7de9131c034172b9df37ccc549524f'
```

<span data-ttu-id="d353c-113">Esse comando adicionará um certificado no cofre de chaves do Azure existente como um certificado de cluster secundário.</span><span class="sxs-lookup"><span data-stu-id="d353c-113">This command will add a certificate in the existing Azure key vault as a secondary cluster certificate.</span></span>

### <span data-ttu-id="d353c-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="d353c-114">Example 2</span></span>
```
PS c:\> $pwd = ConvertTo-SecureString -String "123" -AsPlainText -Force
PS c:\> add-AzServiceFabricClusterCertificate -ResourceGroupName 'Group2' -Name 'Contoso02SFCluster'  -CertificateSubjectName 'Contoso.com' 
-CertificateOutputFolder 'c:\test' -CertificatePassword $pwd
```

<span data-ttu-id="d353c-115">Esse comando criará um certificado auto-assinado no cofre de chaves do Azure e atualizará o cluster para usá-lo como um certificado de cluster secundário.</span><span class="sxs-lookup"><span data-stu-id="d353c-115">This command will create a self-signed certificate in the Azure key vault and upgrade the cluster to use it as a secondary cluster certificate.</span></span>

## <span data-ttu-id="d353c-116">OS</span><span class="sxs-lookup"><span data-stu-id="d353c-116">PARAMETERS</span></span>

### <span data-ttu-id="d353c-117">-CertificateCommonName</span><span class="sxs-lookup"><span data-stu-id="d353c-117">-CertificateCommonName</span></span>
<span data-ttu-id="d353c-118">Nome comum do certificado</span><span class="sxs-lookup"><span data-stu-id="d353c-118">Certificate common name</span></span>

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

### <span data-ttu-id="d353c-119">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="d353c-119">-CertificateFile</span></span>
<span data-ttu-id="d353c-120">O caminho para o certificado existente</span><span class="sxs-lookup"><span data-stu-id="d353c-120">The path to the existing certificate</span></span>

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

### <span data-ttu-id="d353c-121">-CertificateIssuerThumbprint</span><span class="sxs-lookup"><span data-stu-id="d353c-121">-CertificateIssuerThumbprint</span></span>
<span data-ttu-id="d353c-122">Impressão digital do emissor do certificado, separada por vírgulas, se mais de um</span><span class="sxs-lookup"><span data-stu-id="d353c-122">Certificate issuer thumbprint, separated by commas if more than one</span></span>

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

### <span data-ttu-id="d353c-123">-CertificateOutputFolder</span><span class="sxs-lookup"><span data-stu-id="d353c-123">-CertificateOutputFolder</span></span>
<span data-ttu-id="d353c-124">A pasta onde o novo certificado precisa ser baixado.</span><span class="sxs-lookup"><span data-stu-id="d353c-124">The folder where the new certificate needs to be downloaded.</span></span>

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

### <span data-ttu-id="d353c-125">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="d353c-125">-CertificatePassword</span></span>
<span data-ttu-id="d353c-126">A senha do certificado</span><span class="sxs-lookup"><span data-stu-id="d353c-126">The password of the certificate</span></span>

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

### <span data-ttu-id="d353c-127">-CertificateSubjectName</span><span class="sxs-lookup"><span data-stu-id="d353c-127">-CertificateSubjectName</span></span>
<span data-ttu-id="d353c-128">O nome do requerente do certificado</span><span class="sxs-lookup"><span data-stu-id="d353c-128">The subject name of the certificate</span></span>

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

### <span data-ttu-id="d353c-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d353c-129">-DefaultProfile</span></span>
<span data-ttu-id="d353c-130">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d353c-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d353c-131">-Keyvaultname</span><span class="sxs-lookup"><span data-stu-id="d353c-131">-KeyVaultName</span></span>
<span data-ttu-id="d353c-132">Nome do cofre de chave do Azure, se não for fornecido, será definido como padrão para o nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="d353c-132">Azure key vault name, if not given it will be defaulted to the resource group name</span></span>

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

### <span data-ttu-id="d353c-133">-KeyVaultResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d353c-133">-KeyVaultResourceGroupName</span></span>
<span data-ttu-id="d353c-134">Nome do grupo de recursos do cofre de chaves do Azure, se não for fornecido padrão para o nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="d353c-134">Azure key vault resource group name, if not given it will be defaulted to resource group name</span></span>

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

### <span data-ttu-id="d353c-135">-Nome</span><span class="sxs-lookup"><span data-stu-id="d353c-135">-Name</span></span>
<span data-ttu-id="d353c-136">Especificar o nome do cluster</span><span class="sxs-lookup"><span data-stu-id="d353c-136">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="d353c-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d353c-137">-ResourceGroupName</span></span>
<span data-ttu-id="d353c-138">Especifique o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d353c-138">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="d353c-139">-SecretIdentifier</span><span class="sxs-lookup"><span data-stu-id="d353c-139">-SecretIdentifier</span></span>
<span data-ttu-id="d353c-140">A URL do segredo do Azure Key Vault existente, por exemplo ' https://mykv.vault.azure.net:443/secrets/mysecrets/55ec7c4dc61a462bbc645ffc9b4b225f '</span><span class="sxs-lookup"><span data-stu-id="d353c-140">The existing Azure key vault secret URL, for example 'https://mykv.vault.azure.net:443/secrets/mysecrets/55ec7c4dc61a462bbc645ffc9b4b225f'</span></span>

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

### <span data-ttu-id="d353c-141">-Impressão digital</span><span class="sxs-lookup"><span data-stu-id="d353c-141">-Thumbprint</span></span>
<span data-ttu-id="d353c-142">A impressão digital do certificado correspoinding ao SecretIdentifier.</span><span class="sxs-lookup"><span data-stu-id="d353c-142">The thumbprint for the certificate correspoinding to the SecretIdentifier.</span></span> <span data-ttu-id="d353c-143">Use isso se o certificado não for gerenciado como o cofre de chaves só tiver o certificado armazenado como um segredo e o cmdlet não conseguir recuperar a impressão digital.</span><span class="sxs-lookup"><span data-stu-id="d353c-143">Use this if the certificate is not managed as the key vault would only have the certificate stored as a secret and the cmdlet is unable to retreive the thumbprint.</span></span>

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

### <span data-ttu-id="d353c-144">-Confirme</span><span class="sxs-lookup"><span data-stu-id="d353c-144">-Confirm</span></span>
<span data-ttu-id="d353c-145">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d353c-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d353c-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d353c-146">-WhatIf</span></span>
<span data-ttu-id="d353c-147">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d353c-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d353c-148">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d353c-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d353c-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d353c-149">CommonParameters</span></span>
<span data-ttu-id="d353c-150">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d353c-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d353c-151">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d353c-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d353c-152">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d353c-152">INPUTS</span></span>

### <span data-ttu-id="d353c-153">System. String</span><span class="sxs-lookup"><span data-stu-id="d353c-153">System.String</span></span>

### <span data-ttu-id="d353c-154">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="d353c-154">System.Security.SecureString</span></span>

## <span data-ttu-id="d353c-155">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d353c-155">OUTPUTS</span></span>

### <span data-ttu-id="d353c-156">Microsoft. Azure. Commands. imfabric. Models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="d353c-156">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="d353c-157">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d353c-157">NOTES</span></span>

## <span data-ttu-id="d353c-158">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d353c-158">RELATED LINKS</span></span>

[<span data-ttu-id="d353c-159">Remove-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="d353c-159">Remove-AzServiceFabricClusterCertificate</span></span>](./Remove-AzServiceFabricClusterCertificate.md)

[<span data-ttu-id="d353c-160">New-AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="d353c-160">New-AzServiceFabricCluster</span></span>](./New-AzServiceFabricCluster.md)
