---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/add-azservicefabricmanagedclusterclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricManagedClusterClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricManagedClusterClientCertificate.md
ms.openlocfilehash: e948acb179a0ae6a338fa02f01d1cb7d6efbd4fe
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98260819"
---
# <span data-ttu-id="a02ff-101">Add-AzServiceFabricManagedClusterClientCertificate</span><span class="sxs-lookup"><span data-stu-id="a02ff-101">Add-AzServiceFabricManagedClusterClientCertificate</span></span>

## <span data-ttu-id="a02ff-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a02ff-102">SYNOPSIS</span></span>
<span data-ttu-id="a02ff-103">Adicione o nome comum ou a impressão digital do certificado ao cluster.</span><span class="sxs-lookup"><span data-stu-id="a02ff-103">Add certificate common name or thumbprint to the cluster.</span></span> <span data-ttu-id="a02ff-104">Isso registrará o certificado novamente no cluster para fins de autenticação de cliente.</span><span class="sxs-lookup"><span data-stu-id="a02ff-104">This will register the certificate agains the cluster for client authentication purposes.</span></span>

## <span data-ttu-id="a02ff-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a02ff-105">SYNTAX</span></span>

### <span data-ttu-id="a02ff-106">ClientCertByTpByObj (padrão)</span><span class="sxs-lookup"><span data-stu-id="a02ff-106">ClientCertByTpByObj (Default)</span></span>
```
Add-AzServiceFabricManagedClusterClientCertificate [-InputObject] <PSManagedCluster> [-Admin]
 -Thumbprint <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a02ff-107">ClientCertByTpByName</span><span class="sxs-lookup"><span data-stu-id="a02ff-107">ClientCertByTpByName</span></span>
```
Add-AzServiceFabricManagedClusterClientCertificate [-ResourceGroupName] <String> [-Name] <String> [-Admin]
 -Thumbprint <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a02ff-108">ClientCertByCnByName</span><span class="sxs-lookup"><span data-stu-id="a02ff-108">ClientCertByCnByName</span></span>
```
Add-AzServiceFabricManagedClusterClientCertificate [-ResourceGroupName] <String> [-Name] <String> [-Admin]
 -CommonName <String> [-IssuerThumbprint <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a02ff-109">ClientCertByCnByObj</span><span class="sxs-lookup"><span data-stu-id="a02ff-109">ClientCertByCnByObj</span></span>
```
Add-AzServiceFabricManagedClusterClientCertificate [-InputObject] <PSManagedCluster> [-Admin]
 -CommonName <String> [-IssuerThumbprint <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a02ff-110">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a02ff-110">DESCRIPTION</span></span>
<span data-ttu-id="a02ff-111">Adicione o nome comum ou a impressão digital do certificado ao cluster.</span><span class="sxs-lookup"><span data-stu-id="a02ff-111">Add certificate common name or thumbprint to the cluster.</span></span> <span data-ttu-id="a02ff-112">Isso registrará o certificado novamente no cluster para fins de autenticação de cliente.</span><span class="sxs-lookup"><span data-stu-id="a02ff-112">This will register the certificate agains the cluster for client authentication purposes.</span></span>

## <span data-ttu-id="a02ff-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a02ff-113">EXAMPLES</span></span>

### <span data-ttu-id="a02ff-114">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a02ff-114">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
Add-AzServiceFabricManagedClusterClientCertificate -ResourceGroupName $rgName -ClusterName $clusterName -Thumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A -Admin
```

<span data-ttu-id="a02ff-115">Esse comando adicionará o certificado com a impressão digital ' 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A ' ao cluster, portanto, o cliente poderá usar o certificado como administrador para se comunicar com o cluster.</span><span class="sxs-lookup"><span data-stu-id="a02ff-115">This command will add the certificate with thumbprint '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A' to the cluster, so the client can use the certificate as admin to communicate with the cluster.</span></span>

### <span data-ttu-id="a02ff-116">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="a02ff-116">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
Add-AzServiceFabricManagedClusterClientCertificate -ResourceGroupName $rgName -ClusterName $clusterName -CommonName 'Contoso.com' -IssuerThumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A, 5F3660C715EBBDA31DB1FFDCF508302348DE8E7B
```

<span data-ttu-id="a02ff-117">Esse comando adicionará um certificado de cliente somente leitura com o nome comum ' Contoso.com ' e dois emissores.</span><span class="sxs-lookup"><span data-stu-id="a02ff-117">This command will add a read only client certificate with common name 'Contoso.com' and 2 issuers.</span></span>

### <span data-ttu-id="a02ff-118">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="a02ff-118">Example 3</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$cluster = Get-AzServiceFabricManagedCluster -ResourceGroupName $rgName -Name $clusterName
$cluster | Add-AzServiceFabricManagedClusterClientCertificate -CommonName 'Contoso.com' -IssuerThumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A, 5F3660C715EBBDA31DB1FFDCF508302348DE8E7B
```

<span data-ttu-id="a02ff-119">Esse comando adicionará um certificado de cliente somente leitura com nome comum ' Contoso.com ' e 2 emissores, com tubulação.</span><span class="sxs-lookup"><span data-stu-id="a02ff-119">This command will add a read only client certificate with common name 'Contoso.com' and 2 issuers, with piping.</span></span>

## <span data-ttu-id="a02ff-120">OS</span><span class="sxs-lookup"><span data-stu-id="a02ff-120">PARAMETERS</span></span>

### <span data-ttu-id="a02ff-121">-Administrador</span><span class="sxs-lookup"><span data-stu-id="a02ff-121">-Admin</span></span>
<span data-ttu-id="a02ff-122">Use para especificar se o certificado do cliente tem nível de administrador.</span><span class="sxs-lookup"><span data-stu-id="a02ff-122">Use to specify if the client certificate has administrator level.</span></span>

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

### <span data-ttu-id="a02ff-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a02ff-123">-AsJob</span></span>
<span data-ttu-id="a02ff-124">Execute o cmdlet em segundo plano e retorne um trabalho para acompanhar o progresso.</span><span class="sxs-lookup"><span data-stu-id="a02ff-124">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="a02ff-125">-CommonName</span><span class="sxs-lookup"><span data-stu-id="a02ff-125">-CommonName</span></span>
<span data-ttu-id="a02ff-126">Nome comum do certificado do cliente.</span><span class="sxs-lookup"><span data-stu-id="a02ff-126">Client certificate common name.</span></span>

```yaml
Type: System.String
Parameter Sets: ClientCertByCnByName, ClientCertByCnByObj
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a02ff-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a02ff-127">-DefaultProfile</span></span>
<span data-ttu-id="a02ff-128">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a02ff-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a02ff-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a02ff-129">-InputObject</span></span>
<span data-ttu-id="a02ff-130">Recurso de cluster gerenciado</span><span class="sxs-lookup"><span data-stu-id="a02ff-130">Managed cluster resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster
Parameter Sets: ClientCertByTpByObj, ClientCertByCnByObj
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a02ff-131">-IssuerThumbprint</span><span class="sxs-lookup"><span data-stu-id="a02ff-131">-IssuerThumbprint</span></span>
<span data-ttu-id="a02ff-132">Lista de impressões digitais do emissor para o certificado do cliente.</span><span class="sxs-lookup"><span data-stu-id="a02ff-132">List of Issuer thumbprints for the client certificate.</span></span>
<span data-ttu-id="a02ff-133">Use somente em combinação com CommonName.</span><span class="sxs-lookup"><span data-stu-id="a02ff-133">Only use in combination with CommonName.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ClientCertByCnByName, ClientCertByCnByObj
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a02ff-134">-Nome</span><span class="sxs-lookup"><span data-stu-id="a02ff-134">-Name</span></span>
<span data-ttu-id="a02ff-135">Especifique o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="a02ff-135">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: ClientCertByTpByName, ClientCertByCnByName
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a02ff-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a02ff-136">-ResourceGroupName</span></span>
<span data-ttu-id="a02ff-137">Especifique o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a02ff-137">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ClientCertByTpByName, ClientCertByCnByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a02ff-138">-Impressão digital</span><span class="sxs-lookup"><span data-stu-id="a02ff-138">-Thumbprint</span></span>
<span data-ttu-id="a02ff-139">Impressão digital do certificado do cliente.</span><span class="sxs-lookup"><span data-stu-id="a02ff-139">Client certificate thumbprint.</span></span>

```yaml
Type: System.String
Parameter Sets: ClientCertByTpByObj, ClientCertByTpByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a02ff-140">-Confirme</span><span class="sxs-lookup"><span data-stu-id="a02ff-140">-Confirm</span></span>
<span data-ttu-id="a02ff-141">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a02ff-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a02ff-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a02ff-142">-WhatIf</span></span>
<span data-ttu-id="a02ff-143">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a02ff-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a02ff-144">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a02ff-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a02ff-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a02ff-145">CommonParameters</span></span>
<span data-ttu-id="a02ff-146">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a02ff-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a02ff-147">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a02ff-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a02ff-148">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a02ff-148">INPUTS</span></span>

### <span data-ttu-id="a02ff-149">System. String</span><span class="sxs-lookup"><span data-stu-id="a02ff-149">System.String</span></span>

## <span data-ttu-id="a02ff-150">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a02ff-150">OUTPUTS</span></span>

### <span data-ttu-id="a02ff-151">Microsoft. Azure. Commands. imfabric. Models. PSManagedCluster</span><span class="sxs-lookup"><span data-stu-id="a02ff-151">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster</span></span>

## <span data-ttu-id="a02ff-152">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a02ff-152">NOTES</span></span>

## <span data-ttu-id="a02ff-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a02ff-153">RELATED LINKS</span></span>
