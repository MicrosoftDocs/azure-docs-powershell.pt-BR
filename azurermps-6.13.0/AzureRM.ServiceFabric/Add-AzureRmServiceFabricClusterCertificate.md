---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric/add-azurermservicefabricclustercertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Add-AzureRmServiceFabricClusterCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Add-AzureRmServiceFabricClusterCertificate.md
ms.openlocfilehash: fa357a4f5b8e599858ce5aff3e0aa11121833ba1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430850"
---
# <span data-ttu-id="10c3e-101">Add-AzureRmServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="10c3e-101">Add-AzureRmServiceFabricClusterCertificate</span></span>

## <span data-ttu-id="10c3e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="10c3e-102">SYNOPSIS</span></span>
<span data-ttu-id="10c3e-103">Adicione um certificado de cluster secundário ao cluster.</span><span class="sxs-lookup"><span data-stu-id="10c3e-103">Add a secondary cluster certificate to the cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="10c3e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="10c3e-104">SYNTAX</span></span>

### <span data-ttu-id="10c3e-105">ByExistingKeyVault</span><span class="sxs-lookup"><span data-stu-id="10c3e-105">ByExistingKeyVault</span></span>
```
Add-AzureRmServiceFabricClusterCertificate [-ResourceGroupName] <String> [-Name] <String>
 -SecretIdentifier <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="10c3e-106">ByNewPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="10c3e-106">ByNewPfxAndVaultName</span></span>
```
Add-AzureRmServiceFabricClusterCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-KeyVaultResouceGroupName <String>] [-KeyVaultName <String>] [-CertificateOutputFolder <String>]
 [-CertificatePassword <SecureString>] -CertificateSubjectName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="10c3e-107">ByExistingPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="10c3e-107">ByExistingPfxAndVaultName</span></span>
```
Add-AzureRmServiceFabricClusterCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-KeyVaultResouceGroupName <String>] [-KeyVaultName <String>] -CertificateFile <String>
 [-CertificatePassword <SecureString>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="10c3e-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="10c3e-108">DESCRIPTION</span></span>
<span data-ttu-id="10c3e-109">Use **Add-AzureRmServiceFabricClusterCertificate** para adicionar um certificado de cluster secundário, seja de um cofre de chaves do Azure existente ou criando um novo cofre de chaves do Azure usando um certificado existente fornecido ou a partir de um novo certificado auto-assinado criado.</span><span class="sxs-lookup"><span data-stu-id="10c3e-109">Use **Add-AzureRmServiceFabricClusterCertificate** to add a secondary cluster certificate, either from an existing Azure key vault or creating a new Azure key vault using an existing certificate provided or from a new self-signed certificate created.</span></span> <span data-ttu-id="10c3e-110">Ele substituirá o cluster secundário, se houver.</span><span class="sxs-lookup"><span data-stu-id="10c3e-110">It will override the secondary cluster if there is any.</span></span>

## <span data-ttu-id="10c3e-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="10c3e-111">EXAMPLES</span></span>

### <span data-ttu-id="10c3e-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="10c3e-112">Example 1</span></span>
```
Add-AzureRmServiceFabricClusterCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' 
-SecretIdentifier 'https://contoso03vault.vault.azure.net/secrets/contoso03vaultrg/7f7de9131c034172b9df37ccc549524f'
```

<span data-ttu-id="10c3e-113">Esse comando adicionará um certificado no cofre de chaves do Azure existente como um certificado de cluster secundário.</span><span class="sxs-lookup"><span data-stu-id="10c3e-113">This command will add a certificate in the existing Azure key vault as a secondary cluster certificate.</span></span>

### <span data-ttu-id="10c3e-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="10c3e-114">Example 2</span></span>
```
PS c:\> $pwd = ConvertTo-SecureString -String "123" -AsPlainText -Force
PS c:\> add-AzureRmServiceFabricClusterCertificate -ResourceGroupName 'Group2' -Name 'Contoso02SFCluster'  -CertificateSubjectName 'Contoso.com' 
-CertificateOutputFolder 'c:\test' -CertificatePassword $pwd
```

<span data-ttu-id="10c3e-115">Esse comando criará um certificado auto-assinado no cofre de chaves do Azure e atualizará o cluster para usá-lo como um certificado de cluster secundário.</span><span class="sxs-lookup"><span data-stu-id="10c3e-115">This command will create a self-signed certificate in the Azure key vault and upgrade the cluster to use it as a secondary cluster certificate.</span></span>

## <span data-ttu-id="10c3e-116">OS</span><span class="sxs-lookup"><span data-stu-id="10c3e-116">PARAMETERS</span></span>

### <span data-ttu-id="10c3e-117">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="10c3e-117">-CertificateFile</span></span>
<span data-ttu-id="10c3e-118">O caminho do arquivo de certificado existente.</span><span class="sxs-lookup"><span data-stu-id="10c3e-118">The existing certificate file path.</span></span>

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

### <span data-ttu-id="10c3e-119">-CertificateOutputFolder</span><span class="sxs-lookup"><span data-stu-id="10c3e-119">-CertificateOutputFolder</span></span>
<span data-ttu-id="10c3e-120">A pasta do novo certificado a ser criado.</span><span class="sxs-lookup"><span data-stu-id="10c3e-120">The folder of the new certificate to be created.</span></span>

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

### <span data-ttu-id="10c3e-121">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="10c3e-121">-CertificatePassword</span></span>
<span data-ttu-id="10c3e-122">A senha do arquivo de certificado.</span><span class="sxs-lookup"><span data-stu-id="10c3e-122">The password of the certificate file.</span></span>

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

### <span data-ttu-id="10c3e-123">-CertificateSubjectName</span><span class="sxs-lookup"><span data-stu-id="10c3e-123">-CertificateSubjectName</span></span>
<span data-ttu-id="10c3e-124">O nome DNS do certificado a ser criado.</span><span class="sxs-lookup"><span data-stu-id="10c3e-124">The Dns name of the certificate to be created.</span></span>

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

### <span data-ttu-id="10c3e-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10c3e-125">-DefaultProfile</span></span>
<span data-ttu-id="10c3e-126">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="10c3e-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="10c3e-127">-Keyvaultname</span><span class="sxs-lookup"><span data-stu-id="10c3e-127">-KeyVaultName</span></span>
<span data-ttu-id="10c3e-128">Nome do cofre de chave do Azure.</span><span class="sxs-lookup"><span data-stu-id="10c3e-128">Azure key vault name.</span></span>

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

### <span data-ttu-id="10c3e-129">-KeyVaultResouceGroupName</span><span class="sxs-lookup"><span data-stu-id="10c3e-129">-KeyVaultResouceGroupName</span></span>
<span data-ttu-id="10c3e-130">Nome do grupo de recursos do cofre de chaves do Azure.</span><span class="sxs-lookup"><span data-stu-id="10c3e-130">Azure key vault resource group name.</span></span>

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

### <span data-ttu-id="10c3e-131">-Nome</span><span class="sxs-lookup"><span data-stu-id="10c3e-131">-Name</span></span>
<span data-ttu-id="10c3e-132">Especifique o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="10c3e-132">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="10c3e-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10c3e-133">-ResourceGroupName</span></span>
<span data-ttu-id="10c3e-134">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="10c3e-134">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="10c3e-135">-SecretIdentifier</span><span class="sxs-lookup"><span data-stu-id="10c3e-135">-SecretIdentifier</span></span>
<span data-ttu-id="10c3e-136">A URL secreta existente do Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="10c3e-136">The existing Azure key vault secret Url.</span></span>

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

### <span data-ttu-id="10c3e-137">-Confirme</span><span class="sxs-lookup"><span data-stu-id="10c3e-137">-Confirm</span></span>
<span data-ttu-id="10c3e-138">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="10c3e-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="10c3e-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="10c3e-139">-WhatIf</span></span>
<span data-ttu-id="10c3e-140">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="10c3e-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="10c3e-141">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="10c3e-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="10c3e-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10c3e-142">CommonParameters</span></span>
<span data-ttu-id="10c3e-143">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10c3e-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10c3e-144">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="10c3e-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10c3e-145">SENSORES</span><span class="sxs-lookup"><span data-stu-id="10c3e-145">INPUTS</span></span>

### <span data-ttu-id="10c3e-146">System. String</span><span class="sxs-lookup"><span data-stu-id="10c3e-146">System.String</span></span>
<span data-ttu-id="10c3e-147">Parâmetros: CertificateFile (ByValue), CertificateOutputFolder (ByValue), CertificateSubjectName (ByValue), keyvaultname (ByValue), KeyVaultResouceGroupName (ByValue), SecretIdentifier (ByValue)</span><span class="sxs-lookup"><span data-stu-id="10c3e-147">Parameters: CertificateFile (ByValue), CertificateOutputFolder (ByValue), CertificateSubjectName (ByValue), KeyVaultName (ByValue), KeyVaultResouceGroupName (ByValue), SecretIdentifier (ByValue)</span></span>

### <span data-ttu-id="10c3e-148">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="10c3e-148">System.Security.SecureString</span></span>
<span data-ttu-id="10c3e-149">Parâmetros: CertificatePassword (ByValue)</span><span class="sxs-lookup"><span data-stu-id="10c3e-149">Parameters: CertificatePassword (ByValue)</span></span>

## <span data-ttu-id="10c3e-150">EXIBE</span><span class="sxs-lookup"><span data-stu-id="10c3e-150">OUTPUTS</span></span>

### <span data-ttu-id="10c3e-151">Microsoft. Azure. Commands. imfabric. Models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="10c3e-151">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="10c3e-152">INFORMA</span><span class="sxs-lookup"><span data-stu-id="10c3e-152">NOTES</span></span>

## <span data-ttu-id="10c3e-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="10c3e-153">RELATED LINKS</span></span>

[<span data-ttu-id="10c3e-154">Remove-AzureRmServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="10c3e-154">Remove-AzureRmServiceFabricClusterCertificate</span></span>](./Remove-AzureRmServiceFabricClusterCertificate.md)

[<span data-ttu-id="10c3e-155">New-AzureRmServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="10c3e-155">New-AzureRmServiceFabricCluster</span></span>](./New-AzureRmServiceFabricCluster.md)

[<span data-ttu-id="10c3e-156">Add-AzureRmServiceFabricApplicationCertificate</span><span class="sxs-lookup"><span data-stu-id="10c3e-156">Add-AzureRmServiceFabricApplicationCertificate</span></span>](./Add-AzureRmServiceFabricApplicationCertificate.md)
