---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Add-AzureRmServiceFabricApplicationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Add-AzureRmServiceFabricApplicationCertificate.md
ms.openlocfilehash: 6d77c795415bca1a8bffbed6d09062f394782e94
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440176"
---
# <span data-ttu-id="a95f5-101">Add-AzureRmServiceFabricApplicationCertificate</span><span class="sxs-lookup"><span data-stu-id="a95f5-101">Add-AzureRmServiceFabricApplicationCertificate</span></span>

## <span data-ttu-id="a95f5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a95f5-102">SYNOPSIS</span></span>
<span data-ttu-id="a95f5-103">Adicione um novo certificado ao (s) conjunto (s) de escala da máquina virtual que compõe o cluster.</span><span class="sxs-lookup"><span data-stu-id="a95f5-103">Add a new certificate to the Virtual Machine Scale Set(s) that make up the cluster.</span></span> <span data-ttu-id="a95f5-104">O certificado deve ser usado como um certificado de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a95f5-104">The certificate is intended to be used as an application certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a95f5-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a95f5-105">SYNTAX</span></span>

### <span data-ttu-id="a95f5-106">ByExistingKeyVault</span><span class="sxs-lookup"><span data-stu-id="a95f5-106">ByExistingKeyVault</span></span>
```
Add-AzureRmServiceFabricApplicationCertificate [-ResourceGroupName] <String> [-Name] <String>
 -SecretIdentifier <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a95f5-107">ByNewPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="a95f5-107">ByNewPfxAndVaultName</span></span>
```
Add-AzureRmServiceFabricApplicationCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-KeyVaultResouceGroupName <String>] [-KeyVaultName <String>] [-CertificateOutputFolder <String>]
 [-CertificatePassword <SecureString>] -CertificateSubjectName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a95f5-108">ByExistingPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="a95f5-108">ByExistingPfxAndVaultName</span></span>
```
Add-AzureRmServiceFabricApplicationCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-KeyVaultResouceGroupName <String>] [-KeyVaultName <String>] -CertificateFile <String>
 [-CertificatePassword <SecureString>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a95f5-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a95f5-109">DESCRIPTION</span></span>
<span data-ttu-id="a95f5-110">Use **Add-AzureRmServiceFabricApplicationCertificate** para instalar um certificado em todos os nós do cluster.</span><span class="sxs-lookup"><span data-stu-id="a95f5-110">Use **Add-AzureRmServiceFabricApplicationCertificate** to install a certificate to all nodes in the cluster.</span></span> <span data-ttu-id="a95f5-111">Você pode especificar um certificado que você já tem ou ter o sistema gera um novo para você e carregá-lo em um cofre de chaves do Azure novo ou existente.</span><span class="sxs-lookup"><span data-stu-id="a95f5-111">You can specify a certificate you already have or have the system generate a new one for you, and upload it to a new or existing Azure key vault.</span></span>

## <span data-ttu-id="a95f5-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a95f5-112">EXAMPLES</span></span>

### <span data-ttu-id="a95f5-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a95f5-113">Example 1</span></span>
```
PS c:> Add-AzureRmServiceFabricApplicationCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -SecretIdentifier 'https://contoso03vault.vault.azure.net/secrets/contoso03vaultrg/7f7de9131c034172b9df37ccc549524f'
```

<span data-ttu-id="a95f5-114">Esse comando adicionará um certificado do cofre de chaves do Azure existente a todos os tipos de nó do cluster.</span><span class="sxs-lookup"><span data-stu-id="a95f5-114">This command will add a certificate from existing Azure key vault to all node types of the cluster.</span></span>

### <span data-ttu-id="a95f5-115">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="a95f5-115">Example 2</span></span>
```
PS c:\> $pwd = ConvertTo-SecureString -String '123' -AsPlainText -Force
PS C:\> Add-AzureRmServiceFabricApplicationCertificate -ResourceGroupName 'Group2' -Name 'Contoso02SFCluster' -KeyVaultName 'Contoso02Vault' -KeyVaultResouceGroupName 'Contoso02VaultRg'
        -CertificateSubjectName 'cn=Contoso.com' -CertificateOutputFolder 'c:\test' -CertificatePassword $pwd
```

<span data-ttu-id="a95f5-116">Esse comando criará um certificado auto-assinado no cofre de chaves do Azure com o nome do grupo de recursos do cofre de chaves e o nome do cofre de chaves, será instalado em todos os tipos de nó do cluster e baixará o certificado na pasta ' c:\test '.</span><span class="sxs-lookup"><span data-stu-id="a95f5-116">This command will create a self-signed certificate in the Azure key vault with the key vault resource group name and key vault Name, installs to all node types of the cluster, and downloads the certificate under folder 'c:\test'.</span></span> <span data-ttu-id="a95f5-117">O nome do certificado baixado é igual ao nome do certificado do cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="a95f5-117">The name of the certificate downloaded is same as the name of key vault certificate.</span></span>

## <span data-ttu-id="a95f5-118">OS</span><span class="sxs-lookup"><span data-stu-id="a95f5-118">PARAMETERS</span></span>

### <span data-ttu-id="a95f5-119">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="a95f5-119">-CertificateFile</span></span>
<span data-ttu-id="a95f5-120">O caminho do arquivo de certificado existente.</span><span class="sxs-lookup"><span data-stu-id="a95f5-120">The existing certificate file path.</span></span>

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

### <span data-ttu-id="a95f5-121">-CertificateOutputFolder</span><span class="sxs-lookup"><span data-stu-id="a95f5-121">-CertificateOutputFolder</span></span>
<span data-ttu-id="a95f5-122">O caminho da pasta do novo certificado a ser criado.</span><span class="sxs-lookup"><span data-stu-id="a95f5-122">The folder path of the new certificate to be created.</span></span>

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

### <span data-ttu-id="a95f5-123">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="a95f5-123">-CertificatePassword</span></span>
<span data-ttu-id="a95f5-124">A senha do arquivo PFX.</span><span class="sxs-lookup"><span data-stu-id="a95f5-124">The password of the pfx file.</span></span>

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

### <span data-ttu-id="a95f5-125">-CertificateSubjectName</span><span class="sxs-lookup"><span data-stu-id="a95f5-125">-CertificateSubjectName</span></span>
<span data-ttu-id="a95f5-126">O nome DNS do certificado a ser criado.</span><span class="sxs-lookup"><span data-stu-id="a95f5-126">The Dns name of the certificate to be created.</span></span>

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

### <span data-ttu-id="a95f5-127">-Keyvaultname</span><span class="sxs-lookup"><span data-stu-id="a95f5-127">-KeyVaultName</span></span>
<span data-ttu-id="a95f5-128">Nome do cofre de chave do Azure.</span><span class="sxs-lookup"><span data-stu-id="a95f5-128">Azure key vault name.</span></span>

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

### <span data-ttu-id="a95f5-129">-KeyVaultResouceGroupName</span><span class="sxs-lookup"><span data-stu-id="a95f5-129">-KeyVaultResouceGroupName</span></span>
<span data-ttu-id="a95f5-130">Nome do grupo de recursos do cofre de chaves do Azure.</span><span class="sxs-lookup"><span data-stu-id="a95f5-130">Azure key vault resource group name.</span></span>

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

### <span data-ttu-id="a95f5-131">-Nome</span><span class="sxs-lookup"><span data-stu-id="a95f5-131">-Name</span></span>
<span data-ttu-id="a95f5-132">Especifique o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="a95f5-132">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="a95f5-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a95f5-133">-ResourceGroupName</span></span>
<span data-ttu-id="a95f5-134">Especifique o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a95f5-134">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="a95f5-135">-SecretIdentifier</span><span class="sxs-lookup"><span data-stu-id="a95f5-135">-SecretIdentifier</span></span>
<span data-ttu-id="a95f5-136">O URI do segredo do cofre de chaves do Azure existente.</span><span class="sxs-lookup"><span data-stu-id="a95f5-136">The existing Azure key vault secret uri.</span></span>

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

### <span data-ttu-id="a95f5-137">-Confirme</span><span class="sxs-lookup"><span data-stu-id="a95f5-137">-Confirm</span></span>
<span data-ttu-id="a95f5-138">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a95f5-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a95f5-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a95f5-139">-WhatIf</span></span>
<span data-ttu-id="a95f5-140">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a95f5-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a95f5-141">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a95f5-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a95f5-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a95f5-142">-DefaultProfile</span></span>
<span data-ttu-id="a95f5-143">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a95f5-143">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a95f5-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a95f5-144">CommonParameters</span></span>
<span data-ttu-id="a95f5-145">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a95f5-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a95f5-146">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a95f5-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a95f5-147">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a95f5-147">INPUTS</span></span>

### <span data-ttu-id="a95f5-148">System. String</span><span class="sxs-lookup"><span data-stu-id="a95f5-148">System.String</span></span>

## <span data-ttu-id="a95f5-149">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a95f5-149">OUTPUTS</span></span>

### <span data-ttu-id="a95f5-150">Microsoft. Azure. Commands. imfabric. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="a95f5-150">Microsoft.Azure.Commands.ServiceFabric.Models.PSKeyVault</span></span>

## <span data-ttu-id="a95f5-151">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a95f5-151">NOTES</span></span>

## <span data-ttu-id="a95f5-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a95f5-152">RELATED LINKS</span></span>

[<span data-ttu-id="a95f5-153">Add-AzureRmServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="a95f5-153">Add-AzureRmServiceFabricClusterCertificate</span></span>](./Add-AzureRmServiceFabricClusterCertificate.md)

[<span data-ttu-id="a95f5-154">New-AzureRmServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="a95f5-154">New-AzureRmServiceFabricCluster</span></span>](./New-AzureRmServiceFabricCluster.md)
