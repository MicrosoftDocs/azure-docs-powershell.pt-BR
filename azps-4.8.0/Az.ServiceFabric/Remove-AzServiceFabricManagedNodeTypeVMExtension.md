---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricmanagednodetypevmextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricManagedNodeTypeVMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricManagedNodeTypeVMExtension.md
ms.openlocfilehash: dfe88add0571fe460520e7af3b8dece4c4d0bc6f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94110851"
---
# <span data-ttu-id="ddcb5-101">Remove-AzServiceFabricManagedNodeTypeVMExtension</span><span class="sxs-lookup"><span data-stu-id="ddcb5-101">Remove-AzServiceFabricManagedNodeTypeVMExtension</span></span>

## <span data-ttu-id="ddcb5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ddcb5-102">SYNOPSIS</span></span>
<span data-ttu-id="ddcb5-103">Remova a extensão de VM do tipo de nó.</span><span class="sxs-lookup"><span data-stu-id="ddcb5-103">Remove vm extension from the node type.</span></span>

## <span data-ttu-id="ddcb5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ddcb5-104">SYNTAX</span></span>

### <span data-ttu-id="ddcb5-105">ByObj (padrão)</span><span class="sxs-lookup"><span data-stu-id="ddcb5-105">ByObj (Default)</span></span>
```
Remove-AzServiceFabricManagedNodeTypeVMExtension [-InputObject] <PSManagedNodeType> -Name <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ddcb5-106">ByName</span><span class="sxs-lookup"><span data-stu-id="ddcb5-106">ByName</span></span>
```
Remove-AzServiceFabricManagedNodeTypeVMExtension [-ResourceGroupName] <String> [-ClusterName] <String>
 [-NodeTypeName] <String> -Name <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ddcb5-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ddcb5-107">DESCRIPTION</span></span>
<span data-ttu-id="ddcb5-108">Remova a extensão de VM do tipo de nó por nome.</span><span class="sxs-lookup"><span data-stu-id="ddcb5-108">Remove vm extension from the node type by name.</span></span> <span data-ttu-id="ddcb5-109">Use [Get-AzServiceFabricManagedNodeType](./Get-AzServiceFabricManagedNodeType.md) e examine a propriedade VmExtensions para ver a extensão atual no tipo de nó.</span><span class="sxs-lookup"><span data-stu-id="ddcb5-109">Use [Get-AzServiceFabricManagedNodeType](./Get-AzServiceFabricManagedNodeType.md) and look at the VmExtensions property to see the current extension on the node type.</span></span>

## <span data-ttu-id="ddcb5-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ddcb5-110">EXAMPLES</span></span>

### <span data-ttu-id="ddcb5-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ddcb5-111">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
Remove-AzServiceFabricManagedNodeTypeVMExtension -ResourceGroupName $rgName -ClusterName $clusterName -NodeTypeName $NodeTypeName -Name MyExtensionName
```

<span data-ttu-id="ddcb5-112">Remova a extensão do tipo de nó por nome.</span><span class="sxs-lookup"><span data-stu-id="ddcb5-112">Remove extension from node type by name.</span></span>

### <span data-ttu-id="ddcb5-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="ddcb5-113">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
$nodeType = Get-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -Name $NodeTypeName

$nodeType | Remove-AzServiceFabricManagedNodeTypeVMExtension -Name MyExtensionName
```

<span data-ttu-id="ddcb5-114">Remova a extensão do tipo de nó por nome, com tubulação.</span><span class="sxs-lookup"><span data-stu-id="ddcb5-114">Remove extension from node type by name, with piping.</span></span>

## <span data-ttu-id="ddcb5-115">OS</span><span class="sxs-lookup"><span data-stu-id="ddcb5-115">PARAMETERS</span></span>

### <span data-ttu-id="ddcb5-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ddcb5-116">-AsJob</span></span>
<span data-ttu-id="ddcb5-117">Execute o cmdlet em segundo plano e retorne um trabalho para acompanhar o progresso.</span><span class="sxs-lookup"><span data-stu-id="ddcb5-117">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="ddcb5-118">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="ddcb5-118">-ClusterName</span></span>
<span data-ttu-id="ddcb5-119">Especifique o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="ddcb5-119">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="ddcb5-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ddcb5-120">-DefaultProfile</span></span>
<span data-ttu-id="ddcb5-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ddcb5-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ddcb5-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ddcb5-122">-InputObject</span></span>
<span data-ttu-id="ddcb5-123">Recurso de tipo de nó</span><span class="sxs-lookup"><span data-stu-id="ddcb5-123">Node type resource</span></span>

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

### <span data-ttu-id="ddcb5-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="ddcb5-124">-Name</span></span>
<span data-ttu-id="ddcb5-125">nome da extensão.</span><span class="sxs-lookup"><span data-stu-id="ddcb5-125">extension name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddcb5-126">-NodeTypename</span><span class="sxs-lookup"><span data-stu-id="ddcb5-126">-NodeTypeName</span></span>
<span data-ttu-id="ddcb5-127">Especifique o nome do tipo de nó.</span><span class="sxs-lookup"><span data-stu-id="ddcb5-127">Specify the name of the node type.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ddcb5-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ddcb5-128">-PassThru</span></span>
<span data-ttu-id="ddcb5-129">{{Descrição do PassThru de preenchimento}}</span><span class="sxs-lookup"><span data-stu-id="ddcb5-129">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="ddcb5-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ddcb5-130">-ResourceGroupName</span></span>
<span data-ttu-id="ddcb5-131">Especifique o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ddcb5-131">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="ddcb5-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="ddcb5-132">-Confirm</span></span>
<span data-ttu-id="ddcb5-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ddcb5-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ddcb5-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ddcb5-134">-WhatIf</span></span>
<span data-ttu-id="ddcb5-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ddcb5-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ddcb5-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ddcb5-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ddcb5-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ddcb5-137">CommonParameters</span></span>
<span data-ttu-id="ddcb5-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ddcb5-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ddcb5-139">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ddcb5-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ddcb5-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ddcb5-140">INPUTS</span></span>

### <span data-ttu-id="ddcb5-141">System. String</span><span class="sxs-lookup"><span data-stu-id="ddcb5-141">System.String</span></span>

## <span data-ttu-id="ddcb5-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ddcb5-142">OUTPUTS</span></span>

### <span data-ttu-id="ddcb5-143">Microsoft. Azure. Commands. imfabric. Models. PSManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="ddcb5-143">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType</span></span>

## <span data-ttu-id="ddcb5-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ddcb5-144">NOTES</span></span>

## <span data-ttu-id="ddcb5-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ddcb5-145">RELATED LINKS</span></span>
