---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/add-azservicefabricclustercertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricClusterCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricClusterCertificate.md
ms.openlocfilehash: 379bd710413fee83a2fdb6b10dc7fb42f0f207bf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887620"
---
# <span data-ttu-id="df272-101">Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="df272-101">Add-AzServiceFabricClusterCertificate</span></span>

## <span data-ttu-id="df272-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="df272-102">SYNOPSIS</span></span>
<span data-ttu-id="df272-103">Adicione um certificado de cluster secundário ao cluster.</span><span class="sxs-lookup"><span data-stu-id="df272-103">Add a secondary cluster certificate to the cluster.</span></span>

## <span data-ttu-id="df272-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="df272-104">SYNTAX</span></span>

### <span data-ttu-id="df272-105">ByExistingKeyVault</span><span class="sxs-lookup"><span data-stu-id="df272-105">ByExistingKeyVault</span></span>
```
Add-AzServiceFabricClusterCertificate [-ResourceGroupName] <String> [-Name] <String> -SecretIdentifier <String>
 [-Thumbprint <String>] [-CertificateCommonName <String>] [-CertificateIssuerThumbprint <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="df272-106">ByNewPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="df272-106">ByNewPfxAndVaultName</span></span>
```
Add-AzServiceFabricClusterCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-KeyVaultResourceGroupName <String>] [-KeyVaultName <String>] [-CertificateOutputFolder <String>]
 [-CertificatePassword <SecureString>] -CertificateSubjectName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="df272-107">ByExistingPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="df272-107">ByExistingPfxAndVaultName</span></span>
```
Add-AzServiceFabricClusterCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-KeyVaultResourceGroupName <String>] [-KeyVaultName <String>] -CertificateFile <String>
 [-CertificatePassword <SecureString>] [-CertificateCommonName <String>]
 [-CertificateIssuerThumbprint <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="df272-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="df272-108">DESCRIPTION</span></span>
<span data-ttu-id="df272-109">Use **Add-AzServiceFabricClusterCertificate** para adicionar um certificado de cluster secundário, de um cofre de chaves do Azure existente ou criar um novo cofre de chaves do Azure usando um certificado existente fornecido ou a partir de um novo certificado auto-assinado criado.</span><span class="sxs-lookup"><span data-stu-id="df272-109">Use **Add-AzServiceFabricClusterCertificate** to add a secondary cluster certificate, either from an existing Azure key vault or creating a new Azure key vault using an existing certificate provided or from a new self-signed certificate created.</span></span> <span data-ttu-id="df272-110">Ele substituirá o cluster secundário se houver algum.</span><span class="sxs-lookup"><span data-stu-id="df272-110">It will override the secondary cluster if there is any.</span></span>

## <span data-ttu-id="df272-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="df272-111">EXAMPLES</span></span>

### <span data-ttu-id="df272-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="df272-112">Example 1</span></span>
```powershell
Add-AzServiceFabricClusterCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' 
-SecretIdentifier 'https://contoso03vault.vault.azure.net/secrets/contoso03vaultrg/7f7de9131c034172b9df37ccc549524f'
```

<span data-ttu-id="df272-113">Este comando adicionará um certificado no cofre de chaves do Azure existente como um certificado de cluster secundário.</span><span class="sxs-lookup"><span data-stu-id="df272-113">This command will add a certificate in the existing Azure key vault as a secondary cluster certificate.</span></span>

### <span data-ttu-id="df272-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="df272-114">Example 2</span></span>
```
PS c:\> $pwd = ConvertTo-SecureString -String "123" -AsPlainText -Force
PS c:\> add-AzServiceFabricClusterCertificate -ResourceGroupName 'Group2' -Name 'Contoso02SFCluster'  -CertificateSubjectName 'Contoso.com' 
-CertificateOutputFolder 'c:\test' -CertificatePassword $pwd
```

<span data-ttu-id="df272-115">Este comando criará um certificado auto-assinado no cofre de chaves do Azure e atualizará o cluster para usá-lo como um certificado de cluster secundário.</span><span class="sxs-lookup"><span data-stu-id="df272-115">This command will create a self-signed certificate in the Azure key vault and upgrade the cluster to use it as a secondary cluster certificate.</span></span>

## <span data-ttu-id="df272-116">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="df272-116">PARAMETERS</span></span>

### <span data-ttu-id="df272-117">-CertificateCommonName</span><span class="sxs-lookup"><span data-stu-id="df272-117">-CertificateCommonName</span></span>
<span data-ttu-id="df272-118">Nome comum do certificado</span><span class="sxs-lookup"><span data-stu-id="df272-118">Certificate common name</span></span>

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

### <span data-ttu-id="df272-119">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="df272-119">-CertificateFile</span></span>
<span data-ttu-id="df272-120">O caminho para o certificado existente</span><span class="sxs-lookup"><span data-stu-id="df272-120">The path to the existing certificate</span></span>

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

### <span data-ttu-id="df272-121">-CertificateIssuerThumbprint</span><span class="sxs-lookup"><span data-stu-id="df272-121">-CertificateIssuerThumbprint</span></span>
<span data-ttu-id="df272-122">Impressão digital do emissor de certificado, separada por vírgulas, se mais de uma</span><span class="sxs-lookup"><span data-stu-id="df272-122">Certificate issuer thumbprint, separated by commas if more than one</span></span>

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

### <span data-ttu-id="df272-123">-CertificateOutputFolder</span><span class="sxs-lookup"><span data-stu-id="df272-123">-CertificateOutputFolder</span></span>
<span data-ttu-id="df272-124">A pasta onde o novo certificado precisa ser baixado.</span><span class="sxs-lookup"><span data-stu-id="df272-124">The folder where the new certificate needs to be downloaded.</span></span>

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

### <span data-ttu-id="df272-125">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="df272-125">-CertificatePassword</span></span>
<span data-ttu-id="df272-126">A senha do certificado</span><span class="sxs-lookup"><span data-stu-id="df272-126">The password of the certificate</span></span>

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

### <span data-ttu-id="df272-127">-CertificateSubjectName</span><span class="sxs-lookup"><span data-stu-id="df272-127">-CertificateSubjectName</span></span>
<span data-ttu-id="df272-128">O nome do assunto do certificado</span><span class="sxs-lookup"><span data-stu-id="df272-128">The subject name of the certificate</span></span>

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

### <span data-ttu-id="df272-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df272-129">-DefaultProfile</span></span>
<span data-ttu-id="df272-130">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="df272-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="df272-131">-KeyVaultName</span><span class="sxs-lookup"><span data-stu-id="df272-131">-KeyVaultName</span></span>
<span data-ttu-id="df272-132">O nome do cofre de chaves do Azure, se não for dado, será padrão para o nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="df272-132">Azure key vault name, if not given it will be defaulted to the resource group name</span></span>

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

### <span data-ttu-id="df272-133">-KeyVaultResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df272-133">-KeyVaultResourceGroupName</span></span>
<span data-ttu-id="df272-134">Nome do grupo de recursos do cofre de chaves do Azure, se não for dado, ele será padrão para o nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="df272-134">Azure key vault resource group name, if not given it will be defaulted to resource group name</span></span>

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

### <span data-ttu-id="df272-135">-Name</span><span class="sxs-lookup"><span data-stu-id="df272-135">-Name</span></span>
<span data-ttu-id="df272-136">Especificar o nome do cluster</span><span class="sxs-lookup"><span data-stu-id="df272-136">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="df272-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df272-137">-ResourceGroupName</span></span>
<span data-ttu-id="df272-138">Especifique o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="df272-138">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="df272-139">-SecretIdentifier</span><span class="sxs-lookup"><span data-stu-id="df272-139">-SecretIdentifier</span></span>
<span data-ttu-id="df272-140">A URL secreta do cofre de chaves do Azure existente, por exemplo ' https://mykv.vault.azure.net:443/secrets/mysecrets/55ec7c4dc61a462bbc645ffc9b4b225f '</span><span class="sxs-lookup"><span data-stu-id="df272-140">The existing Azure key vault secret URL, for example 'https://mykv.vault.azure.net:443/secrets/mysecrets/55ec7c4dc61a462bbc645ffc9b4b225f'</span></span>

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

### <span data-ttu-id="df272-141">-Thumbprint</span><span class="sxs-lookup"><span data-stu-id="df272-141">-Thumbprint</span></span>
<span data-ttu-id="df272-142">A impressão digital do certificado correspoinding para SecretIdentifier.</span><span class="sxs-lookup"><span data-stu-id="df272-142">The thumbprint for the certificate correspoinding to the SecretIdentifier.</span></span> <span data-ttu-id="df272-143">Use isso se o certificado não for gerenciado, pois o cofre de chaves só terá o certificado armazenado como segredo e o cmdlet não poderá retrear a impressão digital.</span><span class="sxs-lookup"><span data-stu-id="df272-143">Use this if the certificate is not managed as the key vault would only have the certificate stored as a secret and the cmdlet is unable to retreive the thumbprint.</span></span>

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

### <span data-ttu-id="df272-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="df272-144">-Confirm</span></span>
<span data-ttu-id="df272-145">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="df272-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="df272-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="df272-146">-WhatIf</span></span>
<span data-ttu-id="df272-147">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="df272-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="df272-148">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="df272-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="df272-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df272-149">CommonParameters</span></span>
<span data-ttu-id="df272-150">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df272-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df272-151">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="df272-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df272-152">INPUTS</span><span class="sxs-lookup"><span data-stu-id="df272-152">INPUTS</span></span>

### <span data-ttu-id="df272-153">System.String</span><span class="sxs-lookup"><span data-stu-id="df272-153">System.String</span></span>

### <span data-ttu-id="df272-154">System.Security.SecureString</span><span class="sxs-lookup"><span data-stu-id="df272-154">System.Security.SecureString</span></span>

## <span data-ttu-id="df272-155">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="df272-155">OUTPUTS</span></span>

### <span data-ttu-id="df272-156">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span><span class="sxs-lookup"><span data-stu-id="df272-156">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="df272-157">NOTES</span><span class="sxs-lookup"><span data-stu-id="df272-157">NOTES</span></span>

## <span data-ttu-id="df272-158">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="df272-158">RELATED LINKS</span></span>

[<span data-ttu-id="df272-159">Remove-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="df272-159">Remove-AzServiceFabricClusterCertificate</span></span>](./Remove-AzServiceFabricClusterCertificate.md)

[<span data-ttu-id="df272-160">New-AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="df272-160">New-AzServiceFabricCluster</span></span>](./New-AzServiceFabricCluster.md)
