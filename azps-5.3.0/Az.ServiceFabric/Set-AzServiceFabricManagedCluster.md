---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/set-azservicefabricmanagedcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricManagedCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricManagedCluster.md
ms.openlocfilehash: 4636dc8f8c8efdf9dae5f7d2094fd3432528f043
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98433011"
---
# <span data-ttu-id="3c870-101">Set-AzServiceFabricManagedCluster</span><span class="sxs-lookup"><span data-stu-id="3c870-101">Set-AzServiceFabricManagedCluster</span></span>

## <span data-ttu-id="3c870-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3c870-102">SYNOPSIS</span></span>
<span data-ttu-id="3c870-103">Definir propriedades de recurso de cluster.</span><span class="sxs-lookup"><span data-stu-id="3c870-103">Set cluster resource properties.</span></span>

## <span data-ttu-id="3c870-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3c870-104">SYNTAX</span></span>

### <span data-ttu-id="3c870-105">ByObj (padrão)</span><span class="sxs-lookup"><span data-stu-id="3c870-105">ByObj (Default)</span></span>
```
Set-AzServiceFabricManagedCluster [-InputObject] <PSManagedCluster> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3c870-106">WithPramsByName</span><span class="sxs-lookup"><span data-stu-id="3c870-106">WithPramsByName</span></span>
```
Set-AzServiceFabricManagedCluster [-ResourceGroupName] <String> [-Name] <String>
 [-UpgradeMode <ClusterUpgradeMode>] [-CodeVersion <String>] [-HttpGatewayConnectionPort <Int32>]
 [-ClientConnectionPort <Int32>] [-DnsName <String>] [-ReverseProxyEndpointPort <Int32>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3c870-107">ByNameById</span><span class="sxs-lookup"><span data-stu-id="3c870-107">ByNameById</span></span>
```
Set-AzServiceFabricManagedCluster [-ResourceId] <String> [-UpgradeMode <ClusterUpgradeMode>]
 [-CodeVersion <String>] [-HttpGatewayConnectionPort <Int32>] [-ClientConnectionPort <Int32>]
 [-DnsName <String>] [-ReverseProxyEndpointPort <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3c870-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3c870-108">DESCRIPTION</span></span>
<span data-ttu-id="3c870-109">Definir propriedades de recurso de cluster.</span><span class="sxs-lookup"><span data-stu-id="3c870-109">Set cluster resource properties.</span></span>

## <span data-ttu-id="3c870-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3c870-110">EXAMPLES</span></span>

### <span data-ttu-id="3c870-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="3c870-111">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
Update-AzServiceFabricManagedCluster -ResourceGroupName $rgName -Name $clusterName -DnsName testnewdns -ClientConnectionPort 50000 -Verbose
```

<span data-ttu-id="3c870-112">Atualize a porta de conexão do cliente e o nome DNS para o cluster.</span><span class="sxs-lookup"><span data-stu-id="3c870-112">Update dns name and client connection port for the cluster.</span></span>

### <span data-ttu-id="3c870-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="3c870-113">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$cluster = Get-AzServiceFabricManagedCluster -ResourceGroupName $rgName -Name $clusterName

$cluster.DnsName = "testnewdns"
$cluster.ClientConnectionPort = 50000
$cluster | Set-AzServiceFabricManagedCluster
```

<span data-ttu-id="3c870-114">Atualize o nome DNS e a porta de conexão do cliente para o cluster, com tubulação.</span><span class="sxs-lookup"><span data-stu-id="3c870-114">Update dns name and client connection port for the cluster, with piping.</span></span>

## <span data-ttu-id="3c870-115">OS</span><span class="sxs-lookup"><span data-stu-id="3c870-115">PARAMETERS</span></span>

### <span data-ttu-id="3c870-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3c870-116">-AsJob</span></span>
<span data-ttu-id="3c870-117">Execute o cmdlet em segundo plano e retorne um trabalho para acompanhar o progresso.</span><span class="sxs-lookup"><span data-stu-id="3c870-117">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="3c870-118">-ClientConnectionPort</span><span class="sxs-lookup"><span data-stu-id="3c870-118">-ClientConnectionPort</span></span>
<span data-ttu-id="3c870-119">Porta usada para conexões de cliente com o cluster.</span><span class="sxs-lookup"><span data-stu-id="3c870-119">Port used for client connections to the cluster.</span></span> <span data-ttu-id="3c870-120">Padrão: 19000.</span><span class="sxs-lookup"><span data-stu-id="3c870-120">Default: 19000.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: WithPramsByName, ByNameById
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c870-121">-CodeVersion</span><span class="sxs-lookup"><span data-stu-id="3c870-121">-CodeVersion</span></span>
<span data-ttu-id="3c870-122">Versão do código do cluster.</span><span class="sxs-lookup"><span data-stu-id="3c870-122">Cluster code version.</span></span> <span data-ttu-id="3c870-123">Use o modo de atualização somente se for manual.</span><span class="sxs-lookup"><span data-stu-id="3c870-123">Only use if upgrade mode is Manual.</span></span>

```yaml
Type: System.String
Parameter Sets: WithPramsByName, ByNameById
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c870-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c870-124">-DefaultProfile</span></span>
<span data-ttu-id="3c870-125">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3c870-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3c870-126">-DnsName</span><span class="sxs-lookup"><span data-stu-id="3c870-126">-DnsName</span></span>
<span data-ttu-id="3c870-127">Nome DNS do cluster.</span><span class="sxs-lookup"><span data-stu-id="3c870-127">Cluster's dns name.</span></span>

```yaml
Type: System.String
Parameter Sets: WithPramsByName, ByNameById
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c870-128">-HttpGatewayConnectionPort</span><span class="sxs-lookup"><span data-stu-id="3c870-128">-HttpGatewayConnectionPort</span></span>
<span data-ttu-id="3c870-129">Porta usada para conexões http com o cluster.</span><span class="sxs-lookup"><span data-stu-id="3c870-129">Port used for http connections to the cluster.</span></span> <span data-ttu-id="3c870-130">Padrão: 19080.</span><span class="sxs-lookup"><span data-stu-id="3c870-130">Default: 19080.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: WithPramsByName, ByNameById
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c870-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3c870-131">-InputObject</span></span>
<span data-ttu-id="3c870-132">Recurso de cluster gerenciado</span><span class="sxs-lookup"><span data-stu-id="3c870-132">Managed Cluster resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster
Parameter Sets: ByObj
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3c870-133">-Nome</span><span class="sxs-lookup"><span data-stu-id="3c870-133">-Name</span></span>
<span data-ttu-id="3c870-134">Especifique o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="3c870-134">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: WithPramsByName
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c870-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3c870-135">-ResourceGroupName</span></span>
<span data-ttu-id="3c870-136">Especifique o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="3c870-136">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: WithPramsByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c870-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3c870-137">-ResourceId</span></span>
<span data-ttu-id="3c870-138">ID do recurso de cluster gerenciado</span><span class="sxs-lookup"><span data-stu-id="3c870-138">Managed Cluster resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameById
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3c870-139">-ReverseProxyEndpointPort</span><span class="sxs-lookup"><span data-stu-id="3c870-139">-ReverseProxyEndpointPort</span></span>
<span data-ttu-id="3c870-140">Ponto de extremidade usado pelo proxy reverso.</span><span class="sxs-lookup"><span data-stu-id="3c870-140">Endpoint used by reverse proxy.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: WithPramsByName, ByNameById
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c870-141">-Upgrademode</span><span class="sxs-lookup"><span data-stu-id="3c870-141">-UpgradeMode</span></span>
<span data-ttu-id="3c870-142">Modo de atualização de versão do código do cluster.</span><span class="sxs-lookup"><span data-stu-id="3c870-142">Cluster code version upgrade mode.</span></span> <span data-ttu-id="3c870-143">Automática ou manual.</span><span class="sxs-lookup"><span data-stu-id="3c870-143">Automatic or Manual.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ServiceFabric.Models.ClusterUpgradeMode]
Parameter Sets: WithPramsByName, ByNameById
Aliases:
Accepted values: Automatic, Manual

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c870-144">-Confirme</span><span class="sxs-lookup"><span data-stu-id="3c870-144">-Confirm</span></span>
<span data-ttu-id="3c870-145">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3c870-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3c870-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3c870-146">-WhatIf</span></span>
<span data-ttu-id="3c870-147">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="3c870-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3c870-148">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3c870-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3c870-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c870-149">CommonParameters</span></span>
<span data-ttu-id="3c870-150">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3c870-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c870-151">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3c870-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c870-152">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3c870-152">INPUTS</span></span>

### <span data-ttu-id="3c870-153">System. String</span><span class="sxs-lookup"><span data-stu-id="3c870-153">System.String</span></span>

## <span data-ttu-id="3c870-154">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3c870-154">OUTPUTS</span></span>

### <span data-ttu-id="3c870-155">Microsoft. Azure. Commands. imfabric. Models. PSManagedCluster</span><span class="sxs-lookup"><span data-stu-id="3c870-155">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster</span></span>

## <span data-ttu-id="3c870-156">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3c870-156">NOTES</span></span>

## <span data-ttu-id="3c870-157">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3c870-157">RELATED LINKS</span></span>
