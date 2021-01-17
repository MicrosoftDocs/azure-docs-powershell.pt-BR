---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/add-azservicefabricmanagednodetypevmsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricManagedNodeTypeVMSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricManagedNodeTypeVMSecret.md
ms.openlocfilehash: 36ed679066d1850851ff0e90f39eb6f9ef8ffa1a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98433071"
---
# <span data-ttu-id="e35d2-101">Add-AzServiceFabricManagedNodeTypeVMSecret</span><span class="sxs-lookup"><span data-stu-id="e35d2-101">Add-AzServiceFabricManagedNodeTypeVMSecret</span></span>

## <span data-ttu-id="e35d2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e35d2-102">SYNOPSIS</span></span>
<span data-ttu-id="e35d2-103">Adicione o segredo do certificado ao tipo de nó.</span><span class="sxs-lookup"><span data-stu-id="e35d2-103">Add certificate secret to the node type.</span></span>

## <span data-ttu-id="e35d2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e35d2-104">SYNTAX</span></span>

### <span data-ttu-id="e35d2-105">ByObj (padrão)</span><span class="sxs-lookup"><span data-stu-id="e35d2-105">ByObj (Default)</span></span>
```
Add-AzServiceFabricManagedNodeTypeVMSecret [-InputObject] <PSManagedNodeType> -SourceVaultId <String>
 -CertificateUrl <String> -CertificateStore <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e35d2-106">ByName</span><span class="sxs-lookup"><span data-stu-id="e35d2-106">ByName</span></span>
```
Add-AzServiceFabricManagedNodeTypeVMSecret [-ResourceGroupName] <String> [-ClusterName] <String>
 [-Name] <String> -SourceVaultId <String> -CertificateUrl <String> -CertificateStore <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e35d2-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e35d2-107">DESCRIPTION</span></span>
<span data-ttu-id="e35d2-108">Adicione o segredo do certificado ao tipo de nó.</span><span class="sxs-lookup"><span data-stu-id="e35d2-108">Add certificate secret to the node type.</span></span> <span data-ttu-id="e35d2-109">O segredo deve ser armazenado em um cofre de chaves do Azure.</span><span class="sxs-lookup"><span data-stu-id="e35d2-109">The secret must be stored in an Azure Key Vault.</span></span> <span data-ttu-id="e35d2-110">Para obter mais informações sobre o Key Vault, consulte o que é o cofre de chave do Azure?</span><span class="sxs-lookup"><span data-stu-id="e35d2-110">For more information relating to Key Vault, see What is Azure Key Vault?</span></span> <span data-ttu-id="e35d2-111">(https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/).</span><span class="sxs-lookup"><span data-stu-id="e35d2-111">(https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/).</span></span> <span data-ttu-id="e35d2-112">Para obter mais informações sobre os cmdlets, consulte cmdlets do compartimento de chave do Azure ( https://msdn.microsoft.com/library/azure/dn868052.aspx) na biblioteca Microsoft Developer Network ou o cmdlet Set-AzKeyVaultSecret.</span><span class="sxs-lookup"><span data-stu-id="e35d2-112">For more information about the cmdlets, see Azure Key Vault Cmdlets (https://msdn.microsoft.com/library/azure/dn868052.aspx) in the Microsoft Developer Network library or the Set-AzKeyVaultSecret cmdlet.</span></span>

## <span data-ttu-id="e35d2-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e35d2-113">EXAMPLES</span></span>

### <span data-ttu-id="e35d2-114">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e35d2-114">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
Add-AzServiceFabricManagedNodeTypeVMSecret -ResourceGroupName $rgName -ClusterName $clusterName -NodeTypeName $NodeTypeName -SourceVaultId /subscriptions/XXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/testRG/providers/Microsoft.KeyVault/vaults/testkv -CertificateUrl https://testskv.vault.azure.net:443/secrets/TestCert/xxxxxxxxxxxxxxxxxxxxxxxx -CertificateStore My -Verbose
```

<span data-ttu-id="e35d2-115">Essa vírgula adiciona um segredo de certificado do keyvault e do identificador de segredo especificado.</span><span class="sxs-lookup"><span data-stu-id="e35d2-115">This commad adds a certificate secret from the keyvault and secret identifier specified.</span></span>

### <span data-ttu-id="e35d2-116">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="e35d2-116">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
$nodeType = Get-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -Name $NodeTypeName

$nodeType | Add-AzServiceFabricManagedNodeTypeVMSecret -SourceVaultId /subscriptions/XXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/testRG/providers/Microsoft.KeyVault/vaults/testkv -CertificateUrl https://testskv.vault.azure.net:443/secrets/TestCert/xxxxxxxxxxxxxxxxxxxxxxxx -CertificateStore My -Verbose
```

<span data-ttu-id="e35d2-117">Essa vírgula adiciona um segredo de certificado do keyvault e do identificador de segredo especificado com tubulação.</span><span class="sxs-lookup"><span data-stu-id="e35d2-117">This commad adds a certificate secret from the keyvault and secret identifier specified, with piping.</span></span>

## <span data-ttu-id="e35d2-118">OS</span><span class="sxs-lookup"><span data-stu-id="e35d2-118">PARAMETERS</span></span>

### <span data-ttu-id="e35d2-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e35d2-119">-AsJob</span></span>
<span data-ttu-id="e35d2-120">Execute o cmdlet em segundo plano e retorne um trabalho para acompanhar o progresso.</span><span class="sxs-lookup"><span data-stu-id="e35d2-120">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e35d2-121">-CertificateStore</span><span class="sxs-lookup"><span data-stu-id="e35d2-121">-CertificateStore</span></span>
<span data-ttu-id="e35d2-122">Especifica o repositório de certificados na máquina virtual à qual o certificado deve ser adicionado.</span><span class="sxs-lookup"><span data-stu-id="e35d2-122">Specifies the certificate store on the Virtual Machine to which the certificate should be added.</span></span>
<span data-ttu-id="e35d2-123">O repositório de certificados especificado está implicitamente na conta LocalMachine.</span><span class="sxs-lookup"><span data-stu-id="e35d2-123">The specified certificate store is implicitly in the LocalMachine account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e35d2-124">-CertificateUrl</span><span class="sxs-lookup"><span data-stu-id="e35d2-124">-CertificateUrl</span></span>
<span data-ttu-id="e35d2-125">Esta é a URL de um certificado que foi carregado no cofre de chaves como um segredo.</span><span class="sxs-lookup"><span data-stu-id="e35d2-125">This is the URL of a certificate that has been uploaded to Key Vault as a secret.</span></span>
<span data-ttu-id="e35d2-126">Para adicionar um segredo ao cofre de chaves, consulte \[ Adicionar uma chave ou um segredo ao cofre de chaves \] ( https://docs.microsoft.com/azure/key-vault/key-vault-get-started/#add) .</span><span class="sxs-lookup"><span data-stu-id="e35d2-126">For adding a secret to the Key Vault, see \[Add a key or secret to the key vault\](https://docs.microsoft.com/azure/key-vault/key-vault-get-started/#add).</span></span>
<span data-ttu-id="e35d2-127">Nesse caso, o certificado precisa ser a codificação base64 do objeto JSON a seguir, que é codificada em UTF-8: \<br\> \<br\> { \<br\> "dados": " \<Base64-encoded-certificate\> ", \<br\> "DataType": "pfx", \<br\> "senha": " \<pfx-file-password\> " \<br\> }/</span><span class="sxs-lookup"><span data-stu-id="e35d2-127">In this case, your certificate needs to be It is the Base64 encoding of the following JSON Object which is encoded in UTF-8: \<br\>\<br\> {\<br\>  "data":"\<Base64-encoded-certificate\>",\<br\>  "dataType":"pfx",\<br\>  "password":"\<pfx-file-password\>"\<br\>}/</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e35d2-128">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="e35d2-128">-ClusterName</span></span>
<span data-ttu-id="e35d2-129">Especifique o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="e35d2-129">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e35d2-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e35d2-130">-DefaultProfile</span></span>
<span data-ttu-id="e35d2-131">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e35d2-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e35d2-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e35d2-132">-InputObject</span></span>
<span data-ttu-id="e35d2-133">Recurso de tipo de nó</span><span class="sxs-lookup"><span data-stu-id="e35d2-133">Node Type resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType
Parameter Sets: ByObj
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e35d2-134">-Nome</span><span class="sxs-lookup"><span data-stu-id="e35d2-134">-Name</span></span>
<span data-ttu-id="e35d2-135">Especifique o nome do tipo de nó.</span><span class="sxs-lookup"><span data-stu-id="e35d2-135">Specify the name of the node type.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: NodeTypeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e35d2-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e35d2-136">-ResourceGroupName</span></span>
<span data-ttu-id="e35d2-137">Especifique o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e35d2-137">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e35d2-138">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="e35d2-138">-SourceVaultId</span></span>
<span data-ttu-id="e35d2-139">ID do recurso do cofre de chaves que contém os certificados.</span><span class="sxs-lookup"><span data-stu-id="e35d2-139">Key Vault resource id containing the certificates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e35d2-140">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e35d2-140">-Confirm</span></span>
<span data-ttu-id="e35d2-141">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e35d2-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e35d2-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e35d2-142">-WhatIf</span></span>
<span data-ttu-id="e35d2-143">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e35d2-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e35d2-144">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e35d2-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e35d2-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e35d2-145">CommonParameters</span></span>
<span data-ttu-id="e35d2-146">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e35d2-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e35d2-147">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e35d2-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e35d2-148">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e35d2-148">INPUTS</span></span>

### <span data-ttu-id="e35d2-149">System. String</span><span class="sxs-lookup"><span data-stu-id="e35d2-149">System.String</span></span>

## <span data-ttu-id="e35d2-150">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e35d2-150">OUTPUTS</span></span>

### <span data-ttu-id="e35d2-151">Microsoft. Azure. Commands. imfabric. Models. PSManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="e35d2-151">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType</span></span>

## <span data-ttu-id="e35d2-152">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e35d2-152">NOTES</span></span>

## <span data-ttu-id="e35d2-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e35d2-153">RELATED LINKS</span></span>
