---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/restart-azservicefabricmanagednodetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Restart-AzServiceFabricManagedNodeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Restart-AzServiceFabricManagedNodeType.md
ms.openlocfilehash: 341684705b869c0a1b2b405b7f21f7fc84dcbf8d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94115853"
---
# <span data-ttu-id="439c2-101">Restart-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="439c2-101">Restart-AzServiceFabricManagedNodeType</span></span>

## <span data-ttu-id="439c2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="439c2-102">SYNOPSIS</span></span>
<span data-ttu-id="439c2-103">Reinicie os nós específicos do tipo de nó.</span><span class="sxs-lookup"><span data-stu-id="439c2-103">Restart specific nodes from the node type.</span></span>

## <span data-ttu-id="439c2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="439c2-104">SYNTAX</span></span>

```
Restart-AzServiceFabricManagedNodeType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 -NodeName <String[]> [-ForceRestart] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="439c2-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="439c2-105">DESCRIPTION</span></span>
<span data-ttu-id="439c2-106">Reinicie os nós específicos do tipo de nó.</span><span class="sxs-lookup"><span data-stu-id="439c2-106">Restart specific nodes from the node type.</span></span> <span data-ttu-id="439c2-107">Ele desativará os nós da malha de serviços antes de reiniciar as VMs e habilitá-las novamente depois que elas forem retomadas.</span><span class="sxs-lookup"><span data-stu-id="439c2-107">It will disabled the service fabric nodes before restarting the vms and enabled them back again once they come back.</span></span> <span data-ttu-id="439c2-108">Se isso for feito nos tipos de nó primário, pode demorar um pouco, pois ele pode não reiniciar todos os nós ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="439c2-108">If this is done on primary node types it might take a while as it might not restart all the nodes at the same time.</span></span> <span data-ttu-id="439c2-109">Use-ForceRestart force a operação mesmo que o Service Fabric não consiga desabilitar os nós, mas use com cuidado, pois isso pode causar perda de dados se cargas de trabalho com estado estiverem em execução no nó.</span><span class="sxs-lookup"><span data-stu-id="439c2-109">Use -ForceRestart force the operation even if service fabric is unable to disable the nodes but use with caution as this might cause data loss if stateful workloads are running on the node.</span></span>

## <span data-ttu-id="439c2-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="439c2-110">EXAMPLES</span></span>

### <span data-ttu-id="439c2-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="439c2-111">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
Restart-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName  -Name $NodeTypeName -NodeName nt1_0, nt1_3
```

<span data-ttu-id="439c2-112">Reinicie o nó 0 e 3 no tipo de nó.</span><span class="sxs-lookup"><span data-stu-id="439c2-112">Restart node 0 and 3 on the node type.</span></span>

## <span data-ttu-id="439c2-113">OS</span><span class="sxs-lookup"><span data-stu-id="439c2-113">PARAMETERS</span></span>

### <span data-ttu-id="439c2-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="439c2-114">-AsJob</span></span>
<span data-ttu-id="439c2-115">Execute o cmdlet em segundo plano e retorne um trabalho para acompanhar o progresso.</span><span class="sxs-lookup"><span data-stu-id="439c2-115">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="439c2-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="439c2-116">-ClusterName</span></span>
<span data-ttu-id="439c2-117">Especifique o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="439c2-117">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="439c2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="439c2-118">-DefaultProfile</span></span>
<span data-ttu-id="439c2-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="439c2-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="439c2-120">-ForceRestart</span><span class="sxs-lookup"><span data-stu-id="439c2-120">-ForceRestart</span></span>
<span data-ttu-id="439c2-121">Usar esse sinalizador forçará o nó a reiniciar mesmo se o Service Fabric não conseguir desabilitar os nós.</span><span class="sxs-lookup"><span data-stu-id="439c2-121">Using this flag will force the node to restart even if service fabric is unable to disable the nodes.</span></span>

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

### <span data-ttu-id="439c2-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="439c2-122">-Name</span></span>
<span data-ttu-id="439c2-123">Especifique o nome do tipo de nó.</span><span class="sxs-lookup"><span data-stu-id="439c2-123">Specify the name of the node type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NodeTypeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="439c2-124">-NodeName</span><span class="sxs-lookup"><span data-stu-id="439c2-124">-NodeName</span></span>
<span data-ttu-id="439c2-125">Lista de nomes de nó para a operação.</span><span class="sxs-lookup"><span data-stu-id="439c2-125">List of node names for the operation.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="439c2-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="439c2-126">-PassThru</span></span>
<span data-ttu-id="439c2-127">{{Descrição do PassThru de preenchimento}}</span><span class="sxs-lookup"><span data-stu-id="439c2-127">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="439c2-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="439c2-128">-ResourceGroupName</span></span>
<span data-ttu-id="439c2-129">Especifique o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="439c2-129">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="439c2-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="439c2-130">-Confirm</span></span>
<span data-ttu-id="439c2-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="439c2-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="439c2-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="439c2-132">-WhatIf</span></span>
<span data-ttu-id="439c2-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="439c2-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="439c2-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="439c2-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="439c2-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="439c2-135">CommonParameters</span></span>
<span data-ttu-id="439c2-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="439c2-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="439c2-137">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="439c2-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="439c2-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="439c2-138">INPUTS</span></span>

### <span data-ttu-id="439c2-139">System. String</span><span class="sxs-lookup"><span data-stu-id="439c2-139">System.String</span></span>

## <span data-ttu-id="439c2-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="439c2-140">OUTPUTS</span></span>

### <span data-ttu-id="439c2-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="439c2-141">System.Boolean</span></span>

## <span data-ttu-id="439c2-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="439c2-142">NOTES</span></span>

## <span data-ttu-id="439c2-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="439c2-143">RELATED LINKS</span></span>
