---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/new-azservicefabricmanagedcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricManagedCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricManagedCluster.md
ms.openlocfilehash: 9dd54f0f1ca56a8bedf3550e238a4308b519925d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94116539"
---
# <span data-ttu-id="3d8ce-101">New-AzServiceFabricManagedCluster</span><span class="sxs-lookup"><span data-stu-id="3d8ce-101">New-AzServiceFabricManagedCluster</span></span>

## <span data-ttu-id="3d8ce-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3d8ce-102">SYNOPSIS</span></span>
<span data-ttu-id="3d8ce-103">Criar novo cluster gerenciado.</span><span class="sxs-lookup"><span data-stu-id="3d8ce-103">Create new managed cluster.</span></span>

## <span data-ttu-id="3d8ce-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3d8ce-104">SYNTAX</span></span>

### <span data-ttu-id="3d8ce-105">ClientCertByTp (padrão)</span><span class="sxs-lookup"><span data-stu-id="3d8ce-105">ClientCertByTp (Default)</span></span>
```
New-AzServiceFabricManagedCluster [-ResourceGroupName] <String> [-Name] <String> -Location <String>
 [-UpgradeMode <ClusterUpgradeMode>] [-CodeVersion <String>] [-ClientCertIsAdmin]
 -ClientCertThumbprint <String> -AdminPassword <SecureString> [-AdminUserName <String>]
 [-HttpGatewayConnectionPort <Int32>] [-ClientConnectionPort <Int32>] [-DnsName <String>]
 [-ReverseProxyEndpointPort <Int32>] [-Sku <ManagedClusterSku>] [-UseTestExtension] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3d8ce-106">ClientCertByCn</span><span class="sxs-lookup"><span data-stu-id="3d8ce-106">ClientCertByCn</span></span>
```
New-AzServiceFabricManagedCluster [-ResourceGroupName] <String> [-Name] <String> -Location <String>
 [-UpgradeMode <ClusterUpgradeMode>] [-CodeVersion <String>] [-ClientCertIsAdmin]
 -ClientCertCommonName <String> [-ClientCertIssuerThumbprint <String[]>] -AdminPassword <SecureString>
 [-AdminUserName <String>] [-HttpGatewayConnectionPort <Int32>] [-ClientConnectionPort <Int32>]
 [-DnsName <String>] [-ReverseProxyEndpointPort <Int32>] [-Sku <ManagedClusterSku>] [-UseTestExtension]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3d8ce-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3d8ce-107">DESCRIPTION</span></span>
<span data-ttu-id="3d8ce-108">Esse cmdlet criará um recurso de cluster gerenciado sem tipos de nó.</span><span class="sxs-lookup"><span data-stu-id="3d8ce-108">This cmdlet will create a managed cluster resource without node types.</span></span> <span data-ttu-id="3d8ce-109">Para inicializar o cluster, é preciso adicionar um tipo de nó primário use [New-AzServiceFabricManagedNodeType](./New-AzServiceFabricManagedNodeType.md).</span><span class="sxs-lookup"><span data-stu-id="3d8ce-109">To bootstrap the cluster A primary node type needs to be added use [New-AzServiceFabricManagedNodeType](./New-AzServiceFabricManagedNodeType.md).</span></span>

## <span data-ttu-id="3d8ce-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3d8ce-110">EXAMPLES</span></span>

### <span data-ttu-id="3d8ce-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="3d8ce-111">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$password = ConvertTo-SecureString -AsPlainText -Force "testpass1234!@#$"
New-AzServiceFabricManagedCluster -ResourceGroupName $rgName -Location centraluseuap -ClusterName $clusterName -AdminPassword $password -Verbose
```

<span data-ttu-id="3d8ce-112">Esse comando cria um recurso de cluster com a SKU básica padrão.</span><span class="sxs-lookup"><span data-stu-id="3d8ce-112">This command creates a cluster resource with default basic sku.</span></span>

### <span data-ttu-id="3d8ce-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="3d8ce-113">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$password = ConvertTo-SecureString -AsPlainText -Force "testpass1234!@#$"
New-AzServiceFabricManagedCluster -ResourceGroupName $rgName -Location centraluseuap -ClusterName $clusterName -ClientCertThumbprint XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX -ClientCertIsAdmin -AdminPassword $password -Sku Standard -Verbose
```

<span data-ttu-id="3d8ce-114">Esse comando cria um recurso de cluster no centraluseuap com um certificado de cliente de administrador inicial e SKU padrão.</span><span class="sxs-lookup"><span data-stu-id="3d8ce-114">This command creates a cluster resource in centraluseuap with an initial admin client certificate and standard sku.</span></span>

## <span data-ttu-id="3d8ce-115">OS</span><span class="sxs-lookup"><span data-stu-id="3d8ce-115">PARAMETERS</span></span>

### <span data-ttu-id="3d8ce-116">-AdminPassword</span><span class="sxs-lookup"><span data-stu-id="3d8ce-116">-AdminPassword</span></span>
<span data-ttu-id="3d8ce-117">Senha de administrador usada para as máquinas virtuais.</span><span class="sxs-lookup"><span data-stu-id="3d8ce-117">Admin password used for the virtual machines.</span></span>

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

### <span data-ttu-id="3d8ce-118">-AdminUserName</span><span class="sxs-lookup"><span data-stu-id="3d8ce-118">-AdminUserName</span></span>
<span data-ttu-id="3d8ce-119">Senha de administrador usada para as máquinas virtuais.</span><span class="sxs-lookup"><span data-stu-id="3d8ce-119">Admin password used for the virtual machines.</span></span>
<span data-ttu-id="3d8ce-120">Padrão: vmadmin.</span><span class="sxs-lookup"><span data-stu-id="3d8ce-120">Default: vmadmin.</span></span>

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

### <span data-ttu-id="3d8ce-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3d8ce-121">-AsJob</span></span>
<span data-ttu-id="3d8ce-122">Execute o cmdlet em segundo plano e retorne um trabalho para acompanhar o progresso.</span><span class="sxs-lookup"><span data-stu-id="3d8ce-122">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="3d8ce-123">-ClientCertCommonName</span><span class="sxs-lookup"><span data-stu-id="3d8ce-123">-ClientCertCommonName</span></span>
<span data-ttu-id="3d8ce-124">Nome comum do certificado do cliente.</span><span class="sxs-lookup"><span data-stu-id="3d8ce-124">Client certificate common name.</span></span>

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

### <span data-ttu-id="3d8ce-125">-ClientCertIsAdmin</span><span class="sxs-lookup"><span data-stu-id="3d8ce-125">-ClientCertIsAdmin</span></span>
<span data-ttu-id="3d8ce-126">Use para especificar se o certificado do cliente tem nível de administrador.</span><span class="sxs-lookup"><span data-stu-id="3d8ce-126">Use to specify if the client certificate has administrator level.</span></span>

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

### <span data-ttu-id="3d8ce-127">-ClientCertIssuerThumbprint</span><span class="sxs-lookup"><span data-stu-id="3d8ce-127">-ClientCertIssuerThumbprint</span></span>
<span data-ttu-id="3d8ce-128">Lista de impressões digitais do emissor para o certificado do cliente.</span><span class="sxs-lookup"><span data-stu-id="3d8ce-128">List of Issuer thumbprints for the client certificate.</span></span>
<span data-ttu-id="3d8ce-129">Use a combinação somente com o ClientCertCommonName.</span><span class="sxs-lookup"><span data-stu-id="3d8ce-129">Only use in combination with ClientCertCommonName.</span></span>

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

### <span data-ttu-id="3d8ce-130">-ClientCertThumbprint</span><span class="sxs-lookup"><span data-stu-id="3d8ce-130">-ClientCertThumbprint</span></span>
<span data-ttu-id="3d8ce-131">Impressão digital do certificado do cliente.</span><span class="sxs-lookup"><span data-stu-id="3d8ce-131">Client certificate thumbprint.</span></span>

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

### <span data-ttu-id="3d8ce-132">-ClientConnectionPort</span><span class="sxs-lookup"><span data-stu-id="3d8ce-132">-ClientConnectionPort</span></span>
<span data-ttu-id="3d8ce-133">Porta usada para conexões de cliente com o cluster.</span><span class="sxs-lookup"><span data-stu-id="3d8ce-133">Port used for client connections to the cluster.</span></span>
<span data-ttu-id="3d8ce-134">Padrão: 19000.</span><span class="sxs-lookup"><span data-stu-id="3d8ce-134">Default: 19000.</span></span>

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

### <span data-ttu-id="3d8ce-135">-CodeVersion</span><span class="sxs-lookup"><span data-stu-id="3d8ce-135">-CodeVersion</span></span>
<span data-ttu-id="3d8ce-136">Versão do código do Cluster Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="3d8ce-136">Cluster service fabric code version.</span></span>
<span data-ttu-id="3d8ce-137">Use o modo de atualização somente se for manual.</span><span class="sxs-lookup"><span data-stu-id="3d8ce-137">Only use if upgrade mode is Manual.</span></span>

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

### <span data-ttu-id="3d8ce-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d8ce-138">-DefaultProfile</span></span>
<span data-ttu-id="3d8ce-139">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3d8ce-139">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3d8ce-140">-DnsName</span><span class="sxs-lookup"><span data-stu-id="3d8ce-140">-DnsName</span></span>
<span data-ttu-id="3d8ce-141">Nome DNS do cluster.</span><span class="sxs-lookup"><span data-stu-id="3d8ce-141">Cluster's dns name.</span></span>

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

### <span data-ttu-id="3d8ce-142">-HttpGatewayConnectionPort</span><span class="sxs-lookup"><span data-stu-id="3d8ce-142">-HttpGatewayConnectionPort</span></span>
<span data-ttu-id="3d8ce-143">Porta usada para conexões http com o cluster.</span><span class="sxs-lookup"><span data-stu-id="3d8ce-143">Port used for http connections to the cluster.</span></span>
<span data-ttu-id="3d8ce-144">Padrão: 19080.</span><span class="sxs-lookup"><span data-stu-id="3d8ce-144">Default: 19080.</span></span>

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

### <span data-ttu-id="3d8ce-145">-Local</span><span class="sxs-lookup"><span data-stu-id="3d8ce-145">-Location</span></span>
<span data-ttu-id="3d8ce-146">O local do recurso</span><span class="sxs-lookup"><span data-stu-id="3d8ce-146">The resource location</span></span>

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

### <span data-ttu-id="3d8ce-147">-Nome</span><span class="sxs-lookup"><span data-stu-id="3d8ce-147">-Name</span></span>
<span data-ttu-id="3d8ce-148">Especifique o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="3d8ce-148">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="3d8ce-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d8ce-149">-ResourceGroupName</span></span>
<span data-ttu-id="3d8ce-150">Especifique o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="3d8ce-150">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="3d8ce-151">-ReverseProxyEndpointPort</span><span class="sxs-lookup"><span data-stu-id="3d8ce-151">-ReverseProxyEndpointPort</span></span>
<span data-ttu-id="3d8ce-152">Ponto de extremidade usado pelo proxy reverso.</span><span class="sxs-lookup"><span data-stu-id="3d8ce-152">Endpoint used by reverse proxy.</span></span>

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

### <span data-ttu-id="3d8ce-153">-SKU</span><span class="sxs-lookup"><span data-stu-id="3d8ce-153">-Sku</span></span>
<span data-ttu-id="3d8ce-154">SKU do cluster, as opções são básicas: ele terá um mínimo de 3 nós de propagação e só permitirá um tipo e padrão de nó: ele terá um mínimo de 5 nós de propagação e permitir vários tipos de nó.</span><span class="sxs-lookup"><span data-stu-id="3d8ce-154">Cluster's Sku, the options are Basic: it will have a minimum of 3 seed nodes and only allows 1 node type and Standard: it will have a minimum of 5 seed nodes and allows multiple node types.</span></span>

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

### <span data-ttu-id="3d8ce-155">-Upgrademode</span><span class="sxs-lookup"><span data-stu-id="3d8ce-155">-UpgradeMode</span></span>
<span data-ttu-id="3d8ce-156">Modo de atualização de versão do código do Cluster Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="3d8ce-156">Cluster service fabric code version upgrade mode.</span></span>
<span data-ttu-id="3d8ce-157">Automática ou manual.</span><span class="sxs-lookup"><span data-stu-id="3d8ce-157">Automatic or Manual.</span></span>

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

### <span data-ttu-id="3d8ce-158">-UseTestExtension</span><span class="sxs-lookup"><span data-stu-id="3d8ce-158">-UseTestExtension</span></span>
<span data-ttu-id="3d8ce-159">Se especificar o cluster será reportado com a extensão vmss de teste do serviço.</span><span class="sxs-lookup"><span data-stu-id="3d8ce-159">If Specify The cluster will be crated with service test vmss extension.</span></span>

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

### <span data-ttu-id="3d8ce-160">-Confirme</span><span class="sxs-lookup"><span data-stu-id="3d8ce-160">-Confirm</span></span>
<span data-ttu-id="3d8ce-161">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3d8ce-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3d8ce-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3d8ce-162">-WhatIf</span></span>
<span data-ttu-id="3d8ce-163">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="3d8ce-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3d8ce-164">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3d8ce-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3d8ce-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d8ce-165">CommonParameters</span></span>
<span data-ttu-id="3d8ce-166">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d8ce-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d8ce-167">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3d8ce-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d8ce-168">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3d8ce-168">INPUTS</span></span>

### <span data-ttu-id="3d8ce-169">System. String</span><span class="sxs-lookup"><span data-stu-id="3d8ce-169">System.String</span></span>

## <span data-ttu-id="3d8ce-170">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3d8ce-170">OUTPUTS</span></span>

### <span data-ttu-id="3d8ce-171">Microsoft. Azure. Commands. imfabric. Models. PSManagedCluster</span><span class="sxs-lookup"><span data-stu-id="3d8ce-171">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster</span></span>

## <span data-ttu-id="3d8ce-172">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3d8ce-172">NOTES</span></span>

## <span data-ttu-id="3d8ce-173">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3d8ce-173">RELATED LINKS</span></span>

[<span data-ttu-id="3d8ce-174">New-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="3d8ce-174">New-AzServiceFabricManagedNodeType</span></span>](./New-AzServiceFabricManagedNodeType.md)