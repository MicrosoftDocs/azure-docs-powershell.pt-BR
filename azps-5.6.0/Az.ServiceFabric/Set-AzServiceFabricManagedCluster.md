---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/set-azservicefabricmanagedcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricManagedCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricManagedCluster.md
ms.openlocfilehash: 8a3ca4ed215dccbcc3cbfb541d7e023871bf6490
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892322"
---
# <span data-ttu-id="5e23a-101">Set-AzServiceFabricManagedCluster</span><span class="sxs-lookup"><span data-stu-id="5e23a-101">Set-AzServiceFabricManagedCluster</span></span>

## <span data-ttu-id="5e23a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5e23a-102">SYNOPSIS</span></span>
<span data-ttu-id="5e23a-103">Definir propriedades de recurso de cluster.</span><span class="sxs-lookup"><span data-stu-id="5e23a-103">Set cluster resource properties.</span></span>

## <span data-ttu-id="5e23a-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="5e23a-104">SYNTAX</span></span>

### <span data-ttu-id="5e23a-105">ByObj (Padrão)</span><span class="sxs-lookup"><span data-stu-id="5e23a-105">ByObj (Default)</span></span>
```
Set-AzServiceFabricManagedCluster [-InputObject] <PSManagedCluster> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5e23a-106">WithPramsByName</span><span class="sxs-lookup"><span data-stu-id="5e23a-106">WithPramsByName</span></span>
```
Set-AzServiceFabricManagedCluster [-ResourceGroupName] <String> [-Name] <String>
 [-UpgradeMode <ClusterUpgradeMode>] [-CodeVersion <String>] [-HttpGatewayConnectionPort <Int32>]
 [-ClientConnectionPort <Int32>] [-DnsName <String>] [-ReverseProxyEndpointPort <Int32>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5e23a-107">ByNameById</span><span class="sxs-lookup"><span data-stu-id="5e23a-107">ByNameById</span></span>
```
Set-AzServiceFabricManagedCluster [-ResourceId] <String> [-UpgradeMode <ClusterUpgradeMode>]
 [-CodeVersion <String>] [-HttpGatewayConnectionPort <Int32>] [-ClientConnectionPort <Int32>]
 [-DnsName <String>] [-ReverseProxyEndpointPort <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5e23a-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="5e23a-108">DESCRIPTION</span></span>
<span data-ttu-id="5e23a-109">Definir propriedades de recurso de cluster.</span><span class="sxs-lookup"><span data-stu-id="5e23a-109">Set cluster resource properties.</span></span>

## <span data-ttu-id="5e23a-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5e23a-110">EXAMPLES</span></span>

### <span data-ttu-id="5e23a-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="5e23a-111">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
Update-AzServiceFabricManagedCluster -ResourceGroupName $rgName -Name $clusterName -DnsName testnewdns -ClientConnectionPort 50000 -Verbose
```

<span data-ttu-id="5e23a-112">Atualize o nome dns e a porta de conexão do cliente para o cluster.</span><span class="sxs-lookup"><span data-stu-id="5e23a-112">Update dns name and client connection port for the cluster.</span></span>

### <span data-ttu-id="5e23a-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="5e23a-113">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$cluster = Get-AzServiceFabricManagedCluster -ResourceGroupName $rgName -Name $clusterName

$cluster.DnsName = "testnewdns"
$cluster.ClientConnectionPort = 50000
$cluster | Set-AzServiceFabricManagedCluster
```

<span data-ttu-id="5e23a-114">Atualize o nome dns e a porta de conexão do cliente para o cluster, com canalização.</span><span class="sxs-lookup"><span data-stu-id="5e23a-114">Update dns name and client connection port for the cluster, with piping.</span></span>

## <span data-ttu-id="5e23a-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="5e23a-115">PARAMETERS</span></span>

### <span data-ttu-id="5e23a-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5e23a-116">-AsJob</span></span>
<span data-ttu-id="5e23a-117">Execute o cmdlet em segundo plano e retorne um Trabalho para controlar o progresso.</span><span class="sxs-lookup"><span data-stu-id="5e23a-117">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="5e23a-118">-ClientConnectionPort</span><span class="sxs-lookup"><span data-stu-id="5e23a-118">-ClientConnectionPort</span></span>
<span data-ttu-id="5e23a-119">Porta usada para conexões do cliente com o cluster.</span><span class="sxs-lookup"><span data-stu-id="5e23a-119">Port used for client connections to the cluster.</span></span> <span data-ttu-id="5e23a-120">Padrão: 19000.</span><span class="sxs-lookup"><span data-stu-id="5e23a-120">Default: 19000.</span></span>

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

### <span data-ttu-id="5e23a-121">-CodeVersion</span><span class="sxs-lookup"><span data-stu-id="5e23a-121">-CodeVersion</span></span>
<span data-ttu-id="5e23a-122">Versão de código de cluster.</span><span class="sxs-lookup"><span data-stu-id="5e23a-122">Cluster code version.</span></span> <span data-ttu-id="5e23a-123">Use somente se o modo de atualização for Manual.</span><span class="sxs-lookup"><span data-stu-id="5e23a-123">Only use if upgrade mode is Manual.</span></span>

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

### <span data-ttu-id="5e23a-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e23a-124">-DefaultProfile</span></span>
<span data-ttu-id="5e23a-125">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5e23a-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5e23a-126">-DnsName</span><span class="sxs-lookup"><span data-stu-id="5e23a-126">-DnsName</span></span>
<span data-ttu-id="5e23a-127">Nome dns do cluster.</span><span class="sxs-lookup"><span data-stu-id="5e23a-127">Cluster's dns name.</span></span>

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

### <span data-ttu-id="5e23a-128">-HttpGatewayConnectionPort</span><span class="sxs-lookup"><span data-stu-id="5e23a-128">-HttpGatewayConnectionPort</span></span>
<span data-ttu-id="5e23a-129">Porta usada para conexões http com o cluster.</span><span class="sxs-lookup"><span data-stu-id="5e23a-129">Port used for http connections to the cluster.</span></span> <span data-ttu-id="5e23a-130">Padrão: 19080.</span><span class="sxs-lookup"><span data-stu-id="5e23a-130">Default: 19080.</span></span>

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

### <span data-ttu-id="5e23a-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5e23a-131">-InputObject</span></span>
<span data-ttu-id="5e23a-132">Recurso cluster gerenciado</span><span class="sxs-lookup"><span data-stu-id="5e23a-132">Managed Cluster resource</span></span>

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

### <span data-ttu-id="5e23a-133">-Name</span><span class="sxs-lookup"><span data-stu-id="5e23a-133">-Name</span></span>
<span data-ttu-id="5e23a-134">Especifique o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="5e23a-134">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="5e23a-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e23a-135">-ResourceGroupName</span></span>
<span data-ttu-id="5e23a-136">Especifique o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="5e23a-136">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="5e23a-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5e23a-137">-ResourceId</span></span>
<span data-ttu-id="5e23a-138">ID de recurso de Cluster Gerenciado</span><span class="sxs-lookup"><span data-stu-id="5e23a-138">Managed Cluster resource id</span></span>

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

### <span data-ttu-id="5e23a-139">-ReverseProxyEndpointPort</span><span class="sxs-lookup"><span data-stu-id="5e23a-139">-ReverseProxyEndpointPort</span></span>
<span data-ttu-id="5e23a-140">Ponto de extremidade usado pelo proxy reverso.</span><span class="sxs-lookup"><span data-stu-id="5e23a-140">Endpoint used by reverse proxy.</span></span>

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

### <span data-ttu-id="5e23a-141">-UpgradeMode</span><span class="sxs-lookup"><span data-stu-id="5e23a-141">-UpgradeMode</span></span>
<span data-ttu-id="5e23a-142">Modo de atualização de versão de código de cluster.</span><span class="sxs-lookup"><span data-stu-id="5e23a-142">Cluster code version upgrade mode.</span></span> <span data-ttu-id="5e23a-143">Automático ou Manual.</span><span class="sxs-lookup"><span data-stu-id="5e23a-143">Automatic or Manual.</span></span>

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

### <span data-ttu-id="5e23a-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5e23a-144">-Confirm</span></span>
<span data-ttu-id="5e23a-145">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5e23a-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5e23a-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5e23a-146">-WhatIf</span></span>
<span data-ttu-id="5e23a-147">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="5e23a-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5e23a-148">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5e23a-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5e23a-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e23a-149">CommonParameters</span></span>
<span data-ttu-id="5e23a-150">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e23a-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e23a-151">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5e23a-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e23a-152">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5e23a-152">INPUTS</span></span>

### <span data-ttu-id="5e23a-153">System.String</span><span class="sxs-lookup"><span data-stu-id="5e23a-153">System.String</span></span>

## <span data-ttu-id="5e23a-154">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="5e23a-154">OUTPUTS</span></span>

### <span data-ttu-id="5e23a-155">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster</span><span class="sxs-lookup"><span data-stu-id="5e23a-155">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster</span></span>

## <span data-ttu-id="5e23a-156">NOTES</span><span class="sxs-lookup"><span data-stu-id="5e23a-156">NOTES</span></span>

## <span data-ttu-id="5e23a-157">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5e23a-157">RELATED LINKS</span></span>
