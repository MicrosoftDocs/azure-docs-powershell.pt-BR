---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/add-azservicefabricclustercertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricClusterCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricClusterCertificate.md
ms.openlocfilehash: bf96b4a21e12e41ce067d669b50c05831a162a8b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93599125"
---
# <span data-ttu-id="b04a3-101">Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="b04a3-101">Add-AzServiceFabricClusterCertificate</span></span>

## <span data-ttu-id="b04a3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b04a3-102">SYNOPSIS</span></span>
<span data-ttu-id="b04a3-103">Adicione um certificado de cluster secundário ao cluster.</span><span class="sxs-lookup"><span data-stu-id="b04a3-103">Add a secondary cluster certificate to the cluster.</span></span>

## <span data-ttu-id="b04a3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b04a3-104">SYNTAX</span></span>

### <span data-ttu-id="b04a3-105">ByExistingKeyVault</span><span class="sxs-lookup"><span data-stu-id="b04a3-105">ByExistingKeyVault</span></span>
```
Add-AzServiceFabricClusterCertificate [-ResourceGroupName] <String> [-Name] <String> -SecretIdentifier <String>
 [-CertificateCommonName <String>] [-CertificateIssuerThumbprint <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b04a3-106">ByNewPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="b04a3-106">ByNewPfxAndVaultName</span></span>
```
Add-AzServiceFabricClusterCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-KeyVaultResouceGroupName <String>] [-KeyVaultName <String>] [-CertificateOutputFolder <String>]
 [-CertificatePassword <SecureString>] -CertificateSubjectName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b04a3-107">ByExistingPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="b04a3-107">ByExistingPfxAndVaultName</span></span>
```
Add-AzServiceFabricClusterCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-KeyVaultResouceGroupName <String>] [-KeyVaultName <String>] -CertificateFile <String>
 [-CertificatePassword <SecureString>] [-CertificateCommonName <String>]
 [-CertificateIssuerThumbprint <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b04a3-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b04a3-108">DESCRIPTION</span></span>
<span data-ttu-id="b04a3-109">Use **Add-AzServiceFabricClusterCertificate** para adicionar um certificado de cluster secundário, seja de um cofre de chaves do Azure existente ou criando um novo cofre de chaves do Azure usando um certificado existente fornecido ou a partir de um novo certificado auto-assinado criado.</span><span class="sxs-lookup"><span data-stu-id="b04a3-109">Use **Add-AzServiceFabricClusterCertificate** to add a secondary cluster certificate, either from an existing Azure key vault or creating a new Azure key vault using an existing certificate provided or from a new self-signed certificate created.</span></span> <span data-ttu-id="b04a3-110">Ele substituirá o cluster secundário, se houver.</span><span class="sxs-lookup"><span data-stu-id="b04a3-110">It will override the secondary cluster if there is any.</span></span>

## <span data-ttu-id="b04a3-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b04a3-111">EXAMPLES</span></span>

### <span data-ttu-id="b04a3-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b04a3-112">Example 1</span></span>
```
Add-AzServiceFabricClusterCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' 
-SecretIdentifier 'https://contoso03vault.vault.azure.net/secrets/contoso03vaultrg/7f7de9131c034172b9df37ccc549524f'
```

<span data-ttu-id="b04a3-113">Esse comando adicionará um certificado no cofre de chaves do Azure existente como um certificado de cluster secundário.</span><span class="sxs-lookup"><span data-stu-id="b04a3-113">This command will add a certificate in the existing Azure key vault as a secondary cluster certificate.</span></span>

### <span data-ttu-id="b04a3-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="b04a3-114">Example 2</span></span>
```
PS c:\> $pwd = ConvertTo-SecureString -String "123" -AsPlainText -Force
PS c:\> add-AzServiceFabricClusterCertificate -ResourceGroupName 'Group2' -Name 'Contoso02SFCluster'  -CertificateSubjectName 'Contoso.com' 
-CertificateOutputFolder 'c:\test' -CertificatePassword $pwd
```

<span data-ttu-id="b04a3-115">Esse comando criará um certificado auto-assinado no cofre de chaves do Azure e atualizará o cluster para usá-lo como um certificado de cluster secundário.</span><span class="sxs-lookup"><span data-stu-id="b04a3-115">This command will create a self-signed certificate in the Azure key vault and upgrade the cluster to use it as a secondary cluster certificate.</span></span>

## <span data-ttu-id="b04a3-116">OS</span><span class="sxs-lookup"><span data-stu-id="b04a3-116">PARAMETERS</span></span>

### <span data-ttu-id="b04a3-117">-CertificateCommonName</span><span class="sxs-lookup"><span data-stu-id="b04a3-117">-CertificateCommonName</span></span>
<span data-ttu-id="b04a3-118">Nome comum do certificado</span><span class="sxs-lookup"><span data-stu-id="b04a3-118">Certificate common name</span></span>

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

### <span data-ttu-id="b04a3-119">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="b04a3-119">-CertificateFile</span></span>
<span data-ttu-id="b04a3-120">O caminho do arquivo de certificado existente.</span><span class="sxs-lookup"><span data-stu-id="b04a3-120">The existing certificate file path.</span></span>

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

### <span data-ttu-id="b04a3-121">-CertificateIssuerThumbprint</span><span class="sxs-lookup"><span data-stu-id="b04a3-121">-CertificateIssuerThumbprint</span></span>
<span data-ttu-id="b04a3-122">Impressão digital do emissor do certificado, separada por vírgulas, se mais de um</span><span class="sxs-lookup"><span data-stu-id="b04a3-122">Certificate issuer thumbprint, separated by commas if more than one</span></span>

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

### <span data-ttu-id="b04a3-123">-CertificateOutputFolder</span><span class="sxs-lookup"><span data-stu-id="b04a3-123">-CertificateOutputFolder</span></span>
<span data-ttu-id="b04a3-124">A pasta do novo certificado a ser criado.</span><span class="sxs-lookup"><span data-stu-id="b04a3-124">The folder of the new certificate to be created.</span></span>

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

### <span data-ttu-id="b04a3-125">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="b04a3-125">-CertificatePassword</span></span>
<span data-ttu-id="b04a3-126">A senha do arquivo de certificado.</span><span class="sxs-lookup"><span data-stu-id="b04a3-126">The password of the certificate file.</span></span>

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

### <span data-ttu-id="b04a3-127">-CertificateSubjectName</span><span class="sxs-lookup"><span data-stu-id="b04a3-127">-CertificateSubjectName</span></span>
<span data-ttu-id="b04a3-128">O nome DNS do certificado a ser criado.</span><span class="sxs-lookup"><span data-stu-id="b04a3-128">The Dns name of the certificate to be created.</span></span>

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

### <span data-ttu-id="b04a3-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b04a3-129">-DefaultProfile</span></span>
<span data-ttu-id="b04a3-130">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b04a3-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b04a3-131">-Keyvaultname</span><span class="sxs-lookup"><span data-stu-id="b04a3-131">-KeyVaultName</span></span>
<span data-ttu-id="b04a3-132">Nome do cofre de chave do Azure.</span><span class="sxs-lookup"><span data-stu-id="b04a3-132">Azure key vault name.</span></span>

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

### <span data-ttu-id="b04a3-133">-KeyVaultResouceGroupName</span><span class="sxs-lookup"><span data-stu-id="b04a3-133">-KeyVaultResouceGroupName</span></span>
<span data-ttu-id="b04a3-134">Nome do grupo de recursos do cofre de chaves do Azure.</span><span class="sxs-lookup"><span data-stu-id="b04a3-134">Azure key vault resource group name.</span></span>

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

### <span data-ttu-id="b04a3-135">-Nome</span><span class="sxs-lookup"><span data-stu-id="b04a3-135">-Name</span></span>
<span data-ttu-id="b04a3-136">Especifique o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="b04a3-136">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="b04a3-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b04a3-137">-ResourceGroupName</span></span>
<span data-ttu-id="b04a3-138">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b04a3-138">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="b04a3-139">-SecretIdentifier</span><span class="sxs-lookup"><span data-stu-id="b04a3-139">-SecretIdentifier</span></span>
<span data-ttu-id="b04a3-140">A URL secreta existente do Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="b04a3-140">The existing Azure key vault secret Url.</span></span>

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

### <span data-ttu-id="b04a3-141">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b04a3-141">-Confirm</span></span>
<span data-ttu-id="b04a3-142">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b04a3-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b04a3-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b04a3-143">-WhatIf</span></span>
<span data-ttu-id="b04a3-144">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b04a3-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b04a3-145">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b04a3-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b04a3-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b04a3-146">CommonParameters</span></span>
<span data-ttu-id="b04a3-147">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b04a3-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b04a3-148">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b04a3-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b04a3-149">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b04a3-149">INPUTS</span></span>

### <span data-ttu-id="b04a3-150">System. String</span><span class="sxs-lookup"><span data-stu-id="b04a3-150">System.String</span></span>

### <span data-ttu-id="b04a3-151">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="b04a3-151">System.Security.SecureString</span></span>

## <span data-ttu-id="b04a3-152">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b04a3-152">OUTPUTS</span></span>

### <span data-ttu-id="b04a3-153">Microsoft. Azure. Commands. imfabric. Models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="b04a3-153">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="b04a3-154">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b04a3-154">NOTES</span></span>

## <span data-ttu-id="b04a3-155">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b04a3-155">RELATED LINKS</span></span>

[<span data-ttu-id="b04a3-156">Remove-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="b04a3-156">Remove-AzServiceFabricClusterCertificate</span></span>](./Remove-AzServiceFabricClusterCertificate.md)

[<span data-ttu-id="b04a3-157">New-AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="b04a3-157">New-AzServiceFabricCluster</span></span>](./New-AzServiceFabricCluster.md)

[<span data-ttu-id="b04a3-158">Add-AzServiceFabricApplicationCertificate</span><span class="sxs-lookup"><span data-stu-id="b04a3-158">Add-AzServiceFabricApplicationCertificate</span></span>](./Add-AzServiceFabricApplicationCertificate.md)
