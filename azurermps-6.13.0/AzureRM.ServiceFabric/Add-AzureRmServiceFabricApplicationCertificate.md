---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric/add-azurermservicefabricapplicationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Add-AzureRmServiceFabricApplicationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Add-AzureRmServiceFabricApplicationCertificate.md
ms.openlocfilehash: 982eb6bf8c579d3f6ef9a5c6b74299ecf1114eb6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429328"
---
# <span data-ttu-id="6a812-101">Add-AzureRmServiceFabricApplicationCertificate</span><span class="sxs-lookup"><span data-stu-id="6a812-101">Add-AzureRmServiceFabricApplicationCertificate</span></span>

## <span data-ttu-id="6a812-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6a812-102">SYNOPSIS</span></span>
<span data-ttu-id="6a812-103">Adicione um novo certificado ao (s) conjunto (s) de escala da máquina virtual que compõe o cluster.</span><span class="sxs-lookup"><span data-stu-id="6a812-103">Add a new certificate to the Virtual Machine Scale Set(s) that make up the cluster.</span></span> <span data-ttu-id="6a812-104">O certificado deve ser usado como um certificado de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6a812-104">The certificate is intended to be used as an application certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6a812-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6a812-105">SYNTAX</span></span>

### <span data-ttu-id="6a812-106">ByExistingKeyVault</span><span class="sxs-lookup"><span data-stu-id="6a812-106">ByExistingKeyVault</span></span>
```
Add-AzureRmServiceFabricApplicationCertificate [-ResourceGroupName] <String> [-Name] <String>
 -SecretIdentifier <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6a812-107">ByNewPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="6a812-107">ByNewPfxAndVaultName</span></span>
```
Add-AzureRmServiceFabricApplicationCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-KeyVaultResouceGroupName <String>] [-KeyVaultName <String>] [-CertificateOutputFolder <String>]
 [-CertificatePassword <SecureString>] -CertificateSubjectName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6a812-108">ByExistingPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="6a812-108">ByExistingPfxAndVaultName</span></span>
```
Add-AzureRmServiceFabricApplicationCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-KeyVaultResouceGroupName <String>] [-KeyVaultName <String>] -CertificateFile <String>
 [-CertificatePassword <SecureString>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6a812-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6a812-109">DESCRIPTION</span></span>
<span data-ttu-id="6a812-110">Use **Add-AzureRmServiceFabricApplicationCertificate** para instalar um certificado em todos os nós do cluster.</span><span class="sxs-lookup"><span data-stu-id="6a812-110">Use **Add-AzureRmServiceFabricApplicationCertificate** to install a certificate to all nodes in the cluster.</span></span> <span data-ttu-id="6a812-111">Você pode especificar um certificado que você já tem ou ter o sistema gera um novo para você e carregá-lo em um cofre de chaves do Azure novo ou existente.</span><span class="sxs-lookup"><span data-stu-id="6a812-111">You can specify a certificate you already have or have the system generate a new one for you, and upload it to a new or existing Azure key vault.</span></span>

## <span data-ttu-id="6a812-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6a812-112">EXAMPLES</span></span>

### <span data-ttu-id="6a812-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="6a812-113">Example 1</span></span>
```
PS c:> Add-AzureRmServiceFabricApplicationCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -SecretIdentifier 'https://contoso03vault.vault.azure.net/secrets/contoso03vaultrg/7f7de9131c034172b9df37ccc549524f'
```

<span data-ttu-id="6a812-114">Esse comando adicionará um certificado do cofre de chaves do Azure existente a todos os tipos de nó do cluster.</span><span class="sxs-lookup"><span data-stu-id="6a812-114">This command will add a certificate from existing Azure key vault to all node types of the cluster.</span></span>

### <span data-ttu-id="6a812-115">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="6a812-115">Example 2</span></span>
```
PS c:\> $pwd = ConvertTo-SecureString -String '123' -AsPlainText -Force
PS C:\> Add-AzureRmServiceFabricApplicationCertificate -ResourceGroupName 'Group2' -Name 'Contoso02SFCluster' -KeyVaultName 'Contoso02Vault' -KeyVaultResouceGroupName 'Contoso02VaultRg'
        -CertificateSubjectName 'cn=Contoso.com' -CertificateOutputFolder 'c:\test' -CertificatePassword $pwd
```

<span data-ttu-id="6a812-116">Esse comando criará um certificado auto-assinado no cofre de chaves do Azure com o nome do grupo de recursos do cofre de chaves e o nome do cofre de chaves, será instalado em todos os tipos de nó do cluster e baixará o certificado na pasta ' c:\test '.</span><span class="sxs-lookup"><span data-stu-id="6a812-116">This command will create a self-signed certificate in the Azure key vault with the key vault resource group name and key vault Name, installs to all node types of the cluster, and downloads the certificate under folder 'c:\test'.</span></span> <span data-ttu-id="6a812-117">O nome do certificado baixado é igual ao nome do certificado do cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="6a812-117">The name of the certificate downloaded is same as the name of key vault certificate.</span></span>

## <span data-ttu-id="6a812-118">OS</span><span class="sxs-lookup"><span data-stu-id="6a812-118">PARAMETERS</span></span>

### <span data-ttu-id="6a812-119">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="6a812-119">-CertificateFile</span></span>
<span data-ttu-id="6a812-120">O caminho do arquivo de certificado existente.</span><span class="sxs-lookup"><span data-stu-id="6a812-120">The existing certificate file path.</span></span>

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

### <span data-ttu-id="6a812-121">-CertificateOutputFolder</span><span class="sxs-lookup"><span data-stu-id="6a812-121">-CertificateOutputFolder</span></span>
<span data-ttu-id="6a812-122">O caminho da pasta do novo certificado a ser criado.</span><span class="sxs-lookup"><span data-stu-id="6a812-122">The folder path of the new certificate to be created.</span></span>

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

### <span data-ttu-id="6a812-123">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="6a812-123">-CertificatePassword</span></span>
<span data-ttu-id="6a812-124">A senha do arquivo PFX.</span><span class="sxs-lookup"><span data-stu-id="6a812-124">The password of the pfx file.</span></span>

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

### <span data-ttu-id="6a812-125">-CertificateSubjectName</span><span class="sxs-lookup"><span data-stu-id="6a812-125">-CertificateSubjectName</span></span>
<span data-ttu-id="6a812-126">O nome DNS do certificado a ser criado.</span><span class="sxs-lookup"><span data-stu-id="6a812-126">The Dns name of the certificate to be created.</span></span>

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

### <span data-ttu-id="6a812-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a812-127">-DefaultProfile</span></span>
<span data-ttu-id="6a812-128">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6a812-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6a812-129">-Keyvaultname</span><span class="sxs-lookup"><span data-stu-id="6a812-129">-KeyVaultName</span></span>
<span data-ttu-id="6a812-130">Nome do cofre de chave do Azure.</span><span class="sxs-lookup"><span data-stu-id="6a812-130">Azure key vault name.</span></span>

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

### <span data-ttu-id="6a812-131">-KeyVaultResouceGroupName</span><span class="sxs-lookup"><span data-stu-id="6a812-131">-KeyVaultResouceGroupName</span></span>
<span data-ttu-id="6a812-132">Nome do grupo de recursos do cofre de chaves do Azure.</span><span class="sxs-lookup"><span data-stu-id="6a812-132">Azure key vault resource group name.</span></span>

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

### <span data-ttu-id="6a812-133">-Nome</span><span class="sxs-lookup"><span data-stu-id="6a812-133">-Name</span></span>
<span data-ttu-id="6a812-134">Especifique o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="6a812-134">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="6a812-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6a812-135">-ResourceGroupName</span></span>
<span data-ttu-id="6a812-136">Especifique o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="6a812-136">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="6a812-137">-SecretIdentifier</span><span class="sxs-lookup"><span data-stu-id="6a812-137">-SecretIdentifier</span></span>
<span data-ttu-id="6a812-138">O URI do segredo do cofre de chaves do Azure existente.</span><span class="sxs-lookup"><span data-stu-id="6a812-138">The existing Azure key vault secret uri.</span></span>

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

### <span data-ttu-id="6a812-139">-Confirme</span><span class="sxs-lookup"><span data-stu-id="6a812-139">-Confirm</span></span>
<span data-ttu-id="6a812-140">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6a812-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6a812-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6a812-141">-WhatIf</span></span>
<span data-ttu-id="6a812-142">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="6a812-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6a812-143">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6a812-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6a812-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a812-144">CommonParameters</span></span>
<span data-ttu-id="6a812-145">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a812-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a812-146">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6a812-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a812-147">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6a812-147">INPUTS</span></span>

### <span data-ttu-id="6a812-148">System. String</span><span class="sxs-lookup"><span data-stu-id="6a812-148">System.String</span></span>
<span data-ttu-id="6a812-149">Parâmetros: CertificateFile (ByValue), CertificateOutputFolder (ByValue), CertificateSubjectName (ByValue), keyvaultname (ByValue), KeyVaultResouceGroupName (ByValue), SecretIdentifier (ByValue)</span><span class="sxs-lookup"><span data-stu-id="6a812-149">Parameters: CertificateFile (ByValue), CertificateOutputFolder (ByValue), CertificateSubjectName (ByValue), KeyVaultName (ByValue), KeyVaultResouceGroupName (ByValue), SecretIdentifier (ByValue)</span></span>

### <span data-ttu-id="6a812-150">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="6a812-150">System.Security.SecureString</span></span>
<span data-ttu-id="6a812-151">Parâmetros: CertificatePassword (ByValue)</span><span class="sxs-lookup"><span data-stu-id="6a812-151">Parameters: CertificatePassword (ByValue)</span></span>

## <span data-ttu-id="6a812-152">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6a812-152">OUTPUTS</span></span>

### <span data-ttu-id="6a812-153">Microsoft. Azure. Commands. imfabric. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="6a812-153">Microsoft.Azure.Commands.ServiceFabric.Models.PSKeyVault</span></span>

## <span data-ttu-id="6a812-154">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6a812-154">NOTES</span></span>

## <span data-ttu-id="6a812-155">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6a812-155">RELATED LINKS</span></span>

[<span data-ttu-id="6a812-156">Add-AzureRmServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="6a812-156">Add-AzureRmServiceFabricClusterCertificate</span></span>](./Add-AzureRmServiceFabricClusterCertificate.md)

[<span data-ttu-id="6a812-157">New-AzureRmServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="6a812-157">New-AzureRmServiceFabricCluster</span></span>](./New-AzureRmServiceFabricCluster.md)
