---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/add-azservicefabricmanagedclusterclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricManagedClusterClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricManagedClusterClientCertificate.md
ms.openlocfilehash: 11534ff7102295cd312410c5ecbae932fd9459e5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887616"
---
# <span data-ttu-id="2b537-101">Add-AzServiceFabricManagedClusterClientCertificate</span><span class="sxs-lookup"><span data-stu-id="2b537-101">Add-AzServiceFabricManagedClusterClientCertificate</span></span>

## <span data-ttu-id="2b537-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2b537-102">SYNOPSIS</span></span>
<span data-ttu-id="2b537-103">Adicione o nome comum do certificado ou a impressão digital ao cluster.</span><span class="sxs-lookup"><span data-stu-id="2b537-103">Add certificate common name or thumbprint to the cluster.</span></span> <span data-ttu-id="2b537-104">Isso registrará novamente o certificado para fins de autenticação do cliente.</span><span class="sxs-lookup"><span data-stu-id="2b537-104">This will register the certificate agains the cluster for client authentication purposes.</span></span>

## <span data-ttu-id="2b537-105">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="2b537-105">SYNTAX</span></span>

### <span data-ttu-id="2b537-106">ClientCertByTpByObj (Padrão)</span><span class="sxs-lookup"><span data-stu-id="2b537-106">ClientCertByTpByObj (Default)</span></span>
```
Add-AzServiceFabricManagedClusterClientCertificate [-InputObject] <PSManagedCluster> [-Admin]
 -Thumbprint <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2b537-107">ClientCertByTpByName</span><span class="sxs-lookup"><span data-stu-id="2b537-107">ClientCertByTpByName</span></span>
```
Add-AzServiceFabricManagedClusterClientCertificate [-ResourceGroupName] <String> [-Name] <String> [-Admin]
 -Thumbprint <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2b537-108">ClientCertByCnByName</span><span class="sxs-lookup"><span data-stu-id="2b537-108">ClientCertByCnByName</span></span>
```
Add-AzServiceFabricManagedClusterClientCertificate [-ResourceGroupName] <String> [-Name] <String> [-Admin]
 -CommonName <String> [-IssuerThumbprint <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2b537-109">ClientCertByCnByObj</span><span class="sxs-lookup"><span data-stu-id="2b537-109">ClientCertByCnByObj</span></span>
```
Add-AzServiceFabricManagedClusterClientCertificate [-InputObject] <PSManagedCluster> [-Admin]
 -CommonName <String> [-IssuerThumbprint <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2b537-110">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="2b537-110">DESCRIPTION</span></span>
<span data-ttu-id="2b537-111">Adicione o nome comum do certificado ou a impressão digital ao cluster.</span><span class="sxs-lookup"><span data-stu-id="2b537-111">Add certificate common name or thumbprint to the cluster.</span></span> <span data-ttu-id="2b537-112">Isso registrará novamente o certificado para fins de autenticação do cliente.</span><span class="sxs-lookup"><span data-stu-id="2b537-112">This will register the certificate agains the cluster for client authentication purposes.</span></span>

## <span data-ttu-id="2b537-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2b537-113">EXAMPLES</span></span>

### <span data-ttu-id="2b537-114">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="2b537-114">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
Add-AzServiceFabricManagedClusterClientCertificate -ResourceGroupName $rgName -ClusterName $clusterName -Thumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A -Admin
```

<span data-ttu-id="2b537-115">Este comando adicionará o certificado com a impressão digital '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A' ao cluster, para que o cliente possa usar o certificado como administrador para se comunicar com o cluster.</span><span class="sxs-lookup"><span data-stu-id="2b537-115">This command will add the certificate with thumbprint '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A' to the cluster, so the client can use the certificate as admin to communicate with the cluster.</span></span>

### <span data-ttu-id="2b537-116">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="2b537-116">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
Add-AzServiceFabricManagedClusterClientCertificate -ResourceGroupName $rgName -ClusterName $clusterName -CommonName 'Contoso.com' -IssuerThumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A, 5F3660C715EBBDA31DB1FFDCF508302348DE8E7B
```

<span data-ttu-id="2b537-117">Este comando adicionará um certificado de cliente somente leitura com o nome comum "Contoso.com" e dois emissores.</span><span class="sxs-lookup"><span data-stu-id="2b537-117">This command will add a read only client certificate with common name 'Contoso.com' and 2 issuers.</span></span>

### <span data-ttu-id="2b537-118">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="2b537-118">Example 3</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$cluster = Get-AzServiceFabricManagedCluster -ResourceGroupName $rgName -Name $clusterName
$cluster | Add-AzServiceFabricManagedClusterClientCertificate -CommonName 'Contoso.com' -IssuerThumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A, 5F3660C715EBBDA31DB1FFDCF508302348DE8E7B
```

<span data-ttu-id="2b537-119">Este comando adicionará um certificado de cliente somente leitura com o nome comum "Contoso.com" e dois emissores, com canalização.</span><span class="sxs-lookup"><span data-stu-id="2b537-119">This command will add a read only client certificate with common name 'Contoso.com' and 2 issuers, with piping.</span></span>

## <span data-ttu-id="2b537-120">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="2b537-120">PARAMETERS</span></span>

### <span data-ttu-id="2b537-121">-Admin</span><span class="sxs-lookup"><span data-stu-id="2b537-121">-Admin</span></span>
<span data-ttu-id="2b537-122">Use para especificar se o certificado do cliente tem nível de administrador.</span><span class="sxs-lookup"><span data-stu-id="2b537-122">Use to specify if the client certificate has administrator level.</span></span>

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

### <span data-ttu-id="2b537-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2b537-123">-AsJob</span></span>
<span data-ttu-id="2b537-124">Execute o cmdlet em segundo plano e retorne um Trabalho para controlar o progresso.</span><span class="sxs-lookup"><span data-stu-id="2b537-124">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="2b537-125">-CommonName</span><span class="sxs-lookup"><span data-stu-id="2b537-125">-CommonName</span></span>
<span data-ttu-id="2b537-126">Nome comum do certificado do cliente.</span><span class="sxs-lookup"><span data-stu-id="2b537-126">Client certificate common name.</span></span>

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

### <span data-ttu-id="2b537-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b537-127">-DefaultProfile</span></span>
<span data-ttu-id="2b537-128">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2b537-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2b537-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2b537-129">-InputObject</span></span>
<span data-ttu-id="2b537-130">Recurso de cluster gerenciado</span><span class="sxs-lookup"><span data-stu-id="2b537-130">Managed cluster resource</span></span>

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

### <span data-ttu-id="2b537-131">-IssuerThumbprint</span><span class="sxs-lookup"><span data-stu-id="2b537-131">-IssuerThumbprint</span></span>
<span data-ttu-id="2b537-132">Lista de impressões digitais do emissor para o certificado do cliente.</span><span class="sxs-lookup"><span data-stu-id="2b537-132">List of Issuer thumbprints for the client certificate.</span></span>
<span data-ttu-id="2b537-133">Use somente em combinação com CommonName.</span><span class="sxs-lookup"><span data-stu-id="2b537-133">Only use in combination with CommonName.</span></span>

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

### <span data-ttu-id="2b537-134">-Name</span><span class="sxs-lookup"><span data-stu-id="2b537-134">-Name</span></span>
<span data-ttu-id="2b537-135">Especifique o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="2b537-135">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="2b537-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b537-136">-ResourceGroupName</span></span>
<span data-ttu-id="2b537-137">Especifique o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="2b537-137">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="2b537-138">-Thumbprint</span><span class="sxs-lookup"><span data-stu-id="2b537-138">-Thumbprint</span></span>
<span data-ttu-id="2b537-139">Impressão digital do certificado do cliente.</span><span class="sxs-lookup"><span data-stu-id="2b537-139">Client certificate thumbprint.</span></span>

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

### <span data-ttu-id="2b537-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2b537-140">-Confirm</span></span>
<span data-ttu-id="2b537-141">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2b537-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2b537-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2b537-142">-WhatIf</span></span>
<span data-ttu-id="2b537-143">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="2b537-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2b537-144">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2b537-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2b537-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b537-145">CommonParameters</span></span>
<span data-ttu-id="2b537-146">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2b537-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b537-147">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2b537-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b537-148">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2b537-148">INPUTS</span></span>

### <span data-ttu-id="2b537-149">System.String</span><span class="sxs-lookup"><span data-stu-id="2b537-149">System.String</span></span>

## <span data-ttu-id="2b537-150">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="2b537-150">OUTPUTS</span></span>

### <span data-ttu-id="2b537-151">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster</span><span class="sxs-lookup"><span data-stu-id="2b537-151">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster</span></span>

## <span data-ttu-id="2b537-152">NOTES</span><span class="sxs-lookup"><span data-stu-id="2b537-152">NOTES</span></span>

## <span data-ttu-id="2b537-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2b537-153">RELATED LINKS</span></span>
