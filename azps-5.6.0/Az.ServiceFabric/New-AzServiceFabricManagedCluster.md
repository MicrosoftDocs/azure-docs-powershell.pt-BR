---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/new-azservicefabricmanagedcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricManagedCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricManagedCluster.md
ms.openlocfilehash: b6f948de5c5e1eea666086b839d314ace6394e98
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887674"
---
# <span data-ttu-id="bc2f6-101">New-AzServiceFabricManagedCluster</span><span class="sxs-lookup"><span data-stu-id="bc2f6-101">New-AzServiceFabricManagedCluster</span></span>

## <span data-ttu-id="bc2f6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bc2f6-102">SYNOPSIS</span></span>
<span data-ttu-id="bc2f6-103">Criar novo cluster gerenciado.</span><span class="sxs-lookup"><span data-stu-id="bc2f6-103">Create new managed cluster.</span></span>

## <span data-ttu-id="bc2f6-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="bc2f6-104">SYNTAX</span></span>

### <span data-ttu-id="bc2f6-105">ClientCertByTp (Padrão)</span><span class="sxs-lookup"><span data-stu-id="bc2f6-105">ClientCertByTp (Default)</span></span>
```
New-AzServiceFabricManagedCluster [-ResourceGroupName] <String> [-Name] <String> -Location <String>
 [-UpgradeMode <ClusterUpgradeMode>] [-CodeVersion <String>] [-ClientCertIsAdmin]
 -ClientCertThumbprint <String> -AdminPassword <SecureString> [-AdminUserName <String>]
 [-HttpGatewayConnectionPort <Int32>] [-ClientConnectionPort <Int32>] [-DnsName <String>]
 [-ReverseProxyEndpointPort <Int32>] [-Sku <ManagedClusterSku>] [-UseTestExtension] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bc2f6-106">ClientCertByCn</span><span class="sxs-lookup"><span data-stu-id="bc2f6-106">ClientCertByCn</span></span>
```
New-AzServiceFabricManagedCluster [-ResourceGroupName] <String> [-Name] <String> -Location <String>
 [-UpgradeMode <ClusterUpgradeMode>] [-CodeVersion <String>] [-ClientCertIsAdmin]
 -ClientCertCommonName <String> [-ClientCertIssuerThumbprint <String[]>] -AdminPassword <SecureString>
 [-AdminUserName <String>] [-HttpGatewayConnectionPort <Int32>] [-ClientConnectionPort <Int32>]
 [-DnsName <String>] [-ReverseProxyEndpointPort <Int32>] [-Sku <ManagedClusterSku>] [-UseTestExtension]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bc2f6-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="bc2f6-107">DESCRIPTION</span></span>
<span data-ttu-id="bc2f6-108">Este cmdlet criará um recurso de cluster gerenciado sem tipos de nó.</span><span class="sxs-lookup"><span data-stu-id="bc2f6-108">This cmdlet will create a managed cluster resource without node types.</span></span> <span data-ttu-id="bc2f6-109">Para inicializar o cluster Um tipo de nó principal precisa ser adicionado use [New-AzServiceFabricManagedNodeType](./New-AzServiceFabricManagedNodeType.md).</span><span class="sxs-lookup"><span data-stu-id="bc2f6-109">To bootstrap the cluster A primary node type needs to be added use [New-AzServiceFabricManagedNodeType](./New-AzServiceFabricManagedNodeType.md).</span></span>

## <span data-ttu-id="bc2f6-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bc2f6-110">EXAMPLES</span></span>

### <span data-ttu-id="bc2f6-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="bc2f6-111">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$password = ConvertTo-SecureString -AsPlainText -Force "testpass1234!@#$"
New-AzServiceFabricManagedCluster -ResourceGroupName $rgName -Location centraluseuap -ClusterName $clusterName -AdminPassword $password -Verbose
```

<span data-ttu-id="bc2f6-112">Este comando cria um recurso de cluster com sku básico padrão.</span><span class="sxs-lookup"><span data-stu-id="bc2f6-112">This command creates a cluster resource with default basic sku.</span></span>

### <span data-ttu-id="bc2f6-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="bc2f6-113">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$password = ConvertTo-SecureString -AsPlainText -Force "testpass1234!@#$"
New-AzServiceFabricManagedCluster -ResourceGroupName $rgName -Location centraluseuap -ClusterName $clusterName -ClientCertThumbprint XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX -ClientCertIsAdmin -AdminPassword $password -Sku Standard -Verbose
```

<span data-ttu-id="bc2f6-114">Este comando cria um recurso de cluster em centraluseuap com um certificado de cliente de administrador inicial e sku padrão.</span><span class="sxs-lookup"><span data-stu-id="bc2f6-114">This command creates a cluster resource in centraluseuap with an initial admin client certificate and standard sku.</span></span>

## <span data-ttu-id="bc2f6-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="bc2f6-115">PARAMETERS</span></span>

### <span data-ttu-id="bc2f6-116">-AdminPassword</span><span class="sxs-lookup"><span data-stu-id="bc2f6-116">-AdminPassword</span></span>
<span data-ttu-id="bc2f6-117">Senha de administrador usada para as máquinas virtuais.</span><span class="sxs-lookup"><span data-stu-id="bc2f6-117">Admin password used for the virtual machines.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc2f6-118">-AdminUserName</span><span class="sxs-lookup"><span data-stu-id="bc2f6-118">-AdminUserName</span></span>
<span data-ttu-id="bc2f6-119">Senha de administrador usada para as máquinas virtuais.</span><span class="sxs-lookup"><span data-stu-id="bc2f6-119">Admin password used for the virtual machines.</span></span>
<span data-ttu-id="bc2f6-120">Padrão: vmadmin.</span><span class="sxs-lookup"><span data-stu-id="bc2f6-120">Default: vmadmin.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: "vmadmin"
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc2f6-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bc2f6-121">-AsJob</span></span>
<span data-ttu-id="bc2f6-122">Execute o cmdlet em segundo plano e retorne um Trabalho para controlar o progresso.</span><span class="sxs-lookup"><span data-stu-id="bc2f6-122">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="bc2f6-123">-ClientCertCommonName</span><span class="sxs-lookup"><span data-stu-id="bc2f6-123">-ClientCertCommonName</span></span>
<span data-ttu-id="bc2f6-124">Nome comum do certificado do cliente.</span><span class="sxs-lookup"><span data-stu-id="bc2f6-124">Client certificate common name.</span></span>

```yaml
Type: System.String
Parameter Sets: ClientCertByCn
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc2f6-125">-ClientCertIsAdmin</span><span class="sxs-lookup"><span data-stu-id="bc2f6-125">-ClientCertIsAdmin</span></span>
<span data-ttu-id="bc2f6-126">Use para especificar se o certificado do cliente tem nível de administrador.</span><span class="sxs-lookup"><span data-stu-id="bc2f6-126">Use to specify if the client certificate has administrator level.</span></span>

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

### <span data-ttu-id="bc2f6-127">-ClientCertIssuerThumbprint</span><span class="sxs-lookup"><span data-stu-id="bc2f6-127">-ClientCertIssuerThumbprint</span></span>
<span data-ttu-id="bc2f6-128">Lista de impressões digitais do emissor para o certificado do cliente.</span><span class="sxs-lookup"><span data-stu-id="bc2f6-128">List of Issuer thumbprints for the client certificate.</span></span>
<span data-ttu-id="bc2f6-129">Use somente em combinação com ClientCertCommonName.</span><span class="sxs-lookup"><span data-stu-id="bc2f6-129">Only use in combination with ClientCertCommonName.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ClientCertByCn
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc2f6-130">-ClientCertThumbprint</span><span class="sxs-lookup"><span data-stu-id="bc2f6-130">-ClientCertThumbprint</span></span>
<span data-ttu-id="bc2f6-131">Impressão digital do certificado do cliente.</span><span class="sxs-lookup"><span data-stu-id="bc2f6-131">Client certificate thumbprint.</span></span>

```yaml
Type: System.String
Parameter Sets: ClientCertByTp
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc2f6-132">-ClientConnectionPort</span><span class="sxs-lookup"><span data-stu-id="bc2f6-132">-ClientConnectionPort</span></span>
<span data-ttu-id="bc2f6-133">Porta usada para conexões do cliente com o cluster.</span><span class="sxs-lookup"><span data-stu-id="bc2f6-133">Port used for client connections to the cluster.</span></span>
<span data-ttu-id="bc2f6-134">Padrão: 19000.</span><span class="sxs-lookup"><span data-stu-id="bc2f6-134">Default: 19000.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 19000
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc2f6-135">-CodeVersion</span><span class="sxs-lookup"><span data-stu-id="bc2f6-135">-CodeVersion</span></span>
<span data-ttu-id="bc2f6-136">Versão do código de malha de serviço de cluster.</span><span class="sxs-lookup"><span data-stu-id="bc2f6-136">Cluster service fabric code version.</span></span>
<span data-ttu-id="bc2f6-137">Use somente se o modo de atualização for Manual.</span><span class="sxs-lookup"><span data-stu-id="bc2f6-137">Only use if upgrade mode is Manual.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc2f6-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc2f6-138">-DefaultProfile</span></span>
<span data-ttu-id="bc2f6-139">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="bc2f6-139">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bc2f6-140">-DnsName</span><span class="sxs-lookup"><span data-stu-id="bc2f6-140">-DnsName</span></span>
<span data-ttu-id="bc2f6-141">Nome dns do cluster.</span><span class="sxs-lookup"><span data-stu-id="bc2f6-141">Cluster's dns name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc2f6-142">-HttpGatewayConnectionPort</span><span class="sxs-lookup"><span data-stu-id="bc2f6-142">-HttpGatewayConnectionPort</span></span>
<span data-ttu-id="bc2f6-143">Porta usada para conexões http com o cluster.</span><span class="sxs-lookup"><span data-stu-id="bc2f6-143">Port used for http connections to the cluster.</span></span>
<span data-ttu-id="bc2f6-144">Padrão: 19080.</span><span class="sxs-lookup"><span data-stu-id="bc2f6-144">Default: 19080.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 19080
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc2f6-145">-Location</span><span class="sxs-lookup"><span data-stu-id="bc2f6-145">-Location</span></span>
<span data-ttu-id="bc2f6-146">O local do recurso</span><span class="sxs-lookup"><span data-stu-id="bc2f6-146">The resource location</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bc2f6-147">-Name</span><span class="sxs-lookup"><span data-stu-id="bc2f6-147">-Name</span></span>
<span data-ttu-id="bc2f6-148">Especifique o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="bc2f6-148">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="bc2f6-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bc2f6-149">-ResourceGroupName</span></span>
<span data-ttu-id="bc2f6-150">Especifique o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="bc2f6-150">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="bc2f6-151">-ReverseProxyEndpointPort</span><span class="sxs-lookup"><span data-stu-id="bc2f6-151">-ReverseProxyEndpointPort</span></span>
<span data-ttu-id="bc2f6-152">Ponto de extremidade usado pelo proxy reverso.</span><span class="sxs-lookup"><span data-stu-id="bc2f6-152">Endpoint used by reverse proxy.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc2f6-153">-Sku</span><span class="sxs-lookup"><span data-stu-id="bc2f6-153">-Sku</span></span>
<span data-ttu-id="bc2f6-154">Sku do cluster, as opções são Básicas: ele terá no mínimo 3 nós de semente e permite apenas 1 tipo de nó e Standard: ele terá no mínimo 5 nós de semente e permitirá vários tipos de nó.</span><span class="sxs-lookup"><span data-stu-id="bc2f6-154">Cluster's Sku, the options are Basic: it will have a minimum of 3 seed nodes and only allows 1 node type and Standard: it will have a minimum of 5 seed nodes and allows multiple node types.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.ManagedClusterSku
Parameter Sets: (All)
Aliases:
Accepted values: Basic, Standard

Required: False
Position: Named
Default value: Basic
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc2f6-155">-UpgradeMode</span><span class="sxs-lookup"><span data-stu-id="bc2f6-155">-UpgradeMode</span></span>
<span data-ttu-id="bc2f6-156">Modo de atualização de versão do código de malha de serviço de cluster.</span><span class="sxs-lookup"><span data-stu-id="bc2f6-156">Cluster service fabric code version upgrade mode.</span></span>
<span data-ttu-id="bc2f6-157">Automático ou Manual.</span><span class="sxs-lookup"><span data-stu-id="bc2f6-157">Automatic or Manual.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.ClusterUpgradeMode
Parameter Sets: (All)
Aliases:
Accepted values: Automatic, Manual

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc2f6-158">-UseTestExtension</span><span class="sxs-lookup"><span data-stu-id="bc2f6-158">-UseTestExtension</span></span>
<span data-ttu-id="bc2f6-159">Se Especificar O cluster será engradado com a extensão vmss de teste de serviço.</span><span class="sxs-lookup"><span data-stu-id="bc2f6-159">If Specify The cluster will be crated with service test vmss extension.</span></span>

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

### <span data-ttu-id="bc2f6-160">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bc2f6-160">-Confirm</span></span>
<span data-ttu-id="bc2f6-161">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bc2f6-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bc2f6-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bc2f6-162">-WhatIf</span></span>
<span data-ttu-id="bc2f6-163">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="bc2f6-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bc2f6-164">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="bc2f6-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bc2f6-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc2f6-165">CommonParameters</span></span>
<span data-ttu-id="bc2f6-166">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bc2f6-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc2f6-167">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bc2f6-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc2f6-168">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bc2f6-168">INPUTS</span></span>

### <span data-ttu-id="bc2f6-169">System.String</span><span class="sxs-lookup"><span data-stu-id="bc2f6-169">System.String</span></span>

## <span data-ttu-id="bc2f6-170">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="bc2f6-170">OUTPUTS</span></span>

### <span data-ttu-id="bc2f6-171">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster</span><span class="sxs-lookup"><span data-stu-id="bc2f6-171">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster</span></span>

## <span data-ttu-id="bc2f6-172">NOTES</span><span class="sxs-lookup"><span data-stu-id="bc2f6-172">NOTES</span></span>

## <span data-ttu-id="bc2f6-173">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bc2f6-173">RELATED LINKS</span></span>

[<span data-ttu-id="bc2f6-174">New-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="bc2f6-174">New-AzServiceFabricManagedNodeType</span></span>](./New-AzServiceFabricManagedNodeType.md)