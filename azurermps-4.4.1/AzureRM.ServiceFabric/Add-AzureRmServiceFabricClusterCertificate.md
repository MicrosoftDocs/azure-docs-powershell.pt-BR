---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Add-AzureRmServiceFabricClusterCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Add-AzureRmServiceFabricClusterCertificate.md
ms.openlocfilehash: 498b09867436e6aa272abd8796b41f159cd388f8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440175"
---
# <span data-ttu-id="f6709-101">Add-AzureRmServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="f6709-101">Add-AzureRmServiceFabricClusterCertificate</span></span>

## <span data-ttu-id="f6709-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f6709-102">SYNOPSIS</span></span>
<span data-ttu-id="f6709-103">Adicione um certificado de cluster secundário ao cluster.</span><span class="sxs-lookup"><span data-stu-id="f6709-103">Add a secondary cluster certificate to the cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f6709-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f6709-104">SYNTAX</span></span>

### <span data-ttu-id="f6709-105">ByExistingKeyVault</span><span class="sxs-lookup"><span data-stu-id="f6709-105">ByExistingKeyVault</span></span>
```
Add-AzureRmServiceFabricClusterCertificate [-ResourceGroupName] <String> [-Name] <String>
 -SecretIdentifier <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f6709-106">ByNewPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="f6709-106">ByNewPfxAndVaultName</span></span>
```
Add-AzureRmServiceFabricClusterCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-KeyVaultResouceGroupName <String>] [-KeyVaultName <String>] [-CertificateOutputFolder <String>]
 [-CertificatePassword <SecureString>] -CertificateSubjectName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f6709-107">ByExistingPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="f6709-107">ByExistingPfxAndVaultName</span></span>
```
Add-AzureRmServiceFabricClusterCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-KeyVaultResouceGroupName <String>] [-KeyVaultName <String>] -CertificateFile <String>
 [-CertificatePassword <SecureString>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f6709-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f6709-108">DESCRIPTION</span></span>
<span data-ttu-id="f6709-109">Use **Add-AzureRmServiceFabricClusterCertificate** para adicionar um certificado de cluster secundário, seja de um cofre de chaves do Azure existente ou criando um novo cofre de chaves do Azure usando um certificado existente fornecido ou a partir de um novo certificado auto-assinado criado.</span><span class="sxs-lookup"><span data-stu-id="f6709-109">Use **Add-AzureRmServiceFabricClusterCertificate** to add a secondary cluster certificate, either from an existing Azure key vault or creating a new Azure key vault using an existing certificate provided or from a new self-signed certificate created.</span></span> <span data-ttu-id="f6709-110">Ele substituirá o cluster secundário, se houver.</span><span class="sxs-lookup"><span data-stu-id="f6709-110">It will override the secondary cluster if there is any.</span></span>

## <span data-ttu-id="f6709-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f6709-111">EXAMPLES</span></span>

### <span data-ttu-id="f6709-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f6709-112">Example 1</span></span>
```
Add-AzureRmServiceFabricClusterCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' 
-SecretIdentifier 'https://contoso03vault.vault.azure.net/secrets/contoso03vaultrg/7f7de9131c034172b9df37ccc549524f'
```

<span data-ttu-id="f6709-113">Esse comando adicionará um certificado no cofre de chaves do Azure existente como um certificado de cluster secundário.</span><span class="sxs-lookup"><span data-stu-id="f6709-113">This command will add a certificate in the existing Azure key vault as a secondary cluster certificate.</span></span>

### <span data-ttu-id="f6709-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="f6709-114">Example 2</span></span>
```
PS c:\> $pwd = ConvertTo-SecureString -String "123" -AsPlainText -Force
PS c:\> add-AzureRmServiceFabricClusterCertificate -ResourceGroupName 'Group2' -Name 'Contoso02SFCluster'  -CertificateSubjectName 'Contoso.com' 
-CertificateOutputFolder 'c:\test' -CertificatePassword $pwd
```

<span data-ttu-id="f6709-115">Esse comando criará um certificado auto-assinado no cofre de chaves do Azure e atualizará o cluster para usá-lo como um certificado de cluster secundário.</span><span class="sxs-lookup"><span data-stu-id="f6709-115">This command will create a self-signed certificate in the Azure key vault and upgrade the cluster to use it as a secondary cluster certificate.</span></span>

## <span data-ttu-id="f6709-116">OS</span><span class="sxs-lookup"><span data-stu-id="f6709-116">PARAMETERS</span></span>

### <span data-ttu-id="f6709-117">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="f6709-117">-CertificateFile</span></span>
<span data-ttu-id="f6709-118">O caminho do arquivo de certificado existente.</span><span class="sxs-lookup"><span data-stu-id="f6709-118">The existing certificate file path.</span></span>

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

### <span data-ttu-id="f6709-119">-CertificateOutputFolder</span><span class="sxs-lookup"><span data-stu-id="f6709-119">-CertificateOutputFolder</span></span>
<span data-ttu-id="f6709-120">A pasta do novo certificado a ser criado.</span><span class="sxs-lookup"><span data-stu-id="f6709-120">The folder of the new certificate to be created.</span></span>

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

### <span data-ttu-id="f6709-121">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="f6709-121">-CertificatePassword</span></span>
<span data-ttu-id="f6709-122">A senha do arquivo de certificado.</span><span class="sxs-lookup"><span data-stu-id="f6709-122">The password of the certificate file.</span></span>

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

### <span data-ttu-id="f6709-123">-CertificateSubjectName</span><span class="sxs-lookup"><span data-stu-id="f6709-123">-CertificateSubjectName</span></span>
<span data-ttu-id="f6709-124">O nome DNS do certificado a ser criado.</span><span class="sxs-lookup"><span data-stu-id="f6709-124">The Dns name of the certificate to be created.</span></span>

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

### <span data-ttu-id="f6709-125">-Keyvaultname</span><span class="sxs-lookup"><span data-stu-id="f6709-125">-KeyVaultName</span></span>
<span data-ttu-id="f6709-126">Nome do cofre de chave do Azure.</span><span class="sxs-lookup"><span data-stu-id="f6709-126">Azure key vault name.</span></span>

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

### <span data-ttu-id="f6709-127">-KeyVaultResouceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6709-127">-KeyVaultResouceGroupName</span></span>
<span data-ttu-id="f6709-128">Nome do grupo de recursos do cofre de chaves do Azure.</span><span class="sxs-lookup"><span data-stu-id="f6709-128">Azure key vault resource group name.</span></span>

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

### <span data-ttu-id="f6709-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="f6709-129">-Name</span></span>
<span data-ttu-id="f6709-130">Especifique o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="f6709-130">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="f6709-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6709-131">-ResourceGroupName</span></span>
<span data-ttu-id="f6709-132">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f6709-132">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="f6709-133">-SecretIdentifier</span><span class="sxs-lookup"><span data-stu-id="f6709-133">-SecretIdentifier</span></span>
<span data-ttu-id="f6709-134">A URL secreta existente do Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="f6709-134">The existing Azure key vault secret Url.</span></span>

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

### <span data-ttu-id="f6709-135">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f6709-135">-Confirm</span></span>
<span data-ttu-id="f6709-136">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f6709-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f6709-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f6709-137">-WhatIf</span></span>
<span data-ttu-id="f6709-138">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f6709-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f6709-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f6709-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f6709-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6709-140">-DefaultProfile</span></span>
<span data-ttu-id="f6709-141">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f6709-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f6709-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6709-142">CommonParameters</span></span>
<span data-ttu-id="f6709-143">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f6709-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6709-144">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f6709-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6709-145">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f6709-145">INPUTS</span></span>

### <span data-ttu-id="f6709-146">System. String</span><span class="sxs-lookup"><span data-stu-id="f6709-146">System.String</span></span>

## <span data-ttu-id="f6709-147">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f6709-147">OUTPUTS</span></span>

### <span data-ttu-id="f6709-148">Microsoft. Azure. Commands. imfabric. Models. PsCluster</span><span class="sxs-lookup"><span data-stu-id="f6709-148">Microsoft.Azure.Commands.ServiceFabric.Models.PsCluster</span></span>

## <span data-ttu-id="f6709-149">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f6709-149">NOTES</span></span>

## <span data-ttu-id="f6709-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f6709-150">RELATED LINKS</span></span>

[<span data-ttu-id="f6709-151">Remove-AzureRmServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="f6709-151">Remove-AzureRmServiceFabricClusterCertificate</span></span>](./Remove-AzureRmServiceFabricClusterCertificate.md)

[<span data-ttu-id="f6709-152">New-AzureRmServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="f6709-152">New-AzureRmServiceFabricCluster</span></span>](./New-AzureRmServiceFabricCluster.md)

[<span data-ttu-id="f6709-153">Add-AzureRmServiceFabricApplicationCertificate</span><span class="sxs-lookup"><span data-stu-id="f6709-153">Add-AzureRmServiceFabricApplicationCertificate</span></span>](./Add-AzureRmServiceFabricApplicationCertificate.md)
