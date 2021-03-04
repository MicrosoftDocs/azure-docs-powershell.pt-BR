---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/new-azservicefabricapplicationtype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricApplicationType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricApplicationType.md
ms.openlocfilehash: f8724fe13cb44ac3e2640f747026c121303be252
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888790"
---
# <span data-ttu-id="c376a-101">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="c376a-101">New-AzServiceFabricApplicationType</span></span>

## <span data-ttu-id="c376a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c376a-102">SYNOPSIS</span></span>
<span data-ttu-id="c376a-103">Crie um novo tipo de aplicativo de malha de serviço no grupo de recursos especificado e cluster.</span><span class="sxs-lookup"><span data-stu-id="c376a-103">Create new service fabric application type under the specified resource group and cluster.</span></span>

## <span data-ttu-id="c376a-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="c376a-104">SYNTAX</span></span>

```
New-AzServiceFabricApplicationType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c376a-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="c376a-105">DESCRIPTION</span></span>
<span data-ttu-id="c376a-106">O cmdlet cria um novo tipo de aplicativo de malha de serviço sob o grupo de recursos especificado e o cluster.</span><span class="sxs-lookup"><span data-stu-id="c376a-106">The cmdlet creates a new service fabric application type under the specified resource group and cluster.</span></span>

## <span data-ttu-id="c376a-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c376a-107">EXAMPLES</span></span>

### <span data-ttu-id="c376a-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c376a-108">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> $appType = New-AzServiceFabricApplicationType -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName -Verbose
```

<span data-ttu-id="c376a-109">Este exemplo criará um novo tipo de aplicativo "testAppType" no grupo de recursos e cluster especificados.</span><span class="sxs-lookup"><span data-stu-id="c376a-109">This example will create a new application type "testAppType" under the resource group and cluster specified.</span></span>

## <span data-ttu-id="c376a-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="c376a-110">PARAMETERS</span></span>

### <span data-ttu-id="c376a-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="c376a-111">-ClusterName</span></span>
<span data-ttu-id="c376a-112">Especifique o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="c376a-112">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="c376a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c376a-113">-DefaultProfile</span></span>
<span data-ttu-id="c376a-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c376a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c376a-115">-Name</span><span class="sxs-lookup"><span data-stu-id="c376a-115">-Name</span></span>
<span data-ttu-id="c376a-116">Especificar o nome do tipo de aplicativo</span><span class="sxs-lookup"><span data-stu-id="c376a-116">Specify the name of the application type</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ApplicationTypeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c376a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c376a-117">-ResourceGroupName</span></span>
<span data-ttu-id="c376a-118">Especifique o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c376a-118">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="c376a-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c376a-119">-Confirm</span></span>
<span data-ttu-id="c376a-120">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c376a-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c376a-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c376a-121">-WhatIf</span></span>
<span data-ttu-id="c376a-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c376a-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c376a-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c376a-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c376a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c376a-124">CommonParameters</span></span>
<span data-ttu-id="c376a-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c376a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c376a-126">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c376a-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c376a-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c376a-127">INPUTS</span></span>

### <span data-ttu-id="c376a-128">System.String</span><span class="sxs-lookup"><span data-stu-id="c376a-128">System.String</span></span>

## <span data-ttu-id="c376a-129">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="c376a-129">OUTPUTS</span></span>

### <span data-ttu-id="c376a-130">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationType</span><span class="sxs-lookup"><span data-stu-id="c376a-130">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationType</span></span>

## <span data-ttu-id="c376a-131">NOTES</span><span class="sxs-lookup"><span data-stu-id="c376a-131">NOTES</span></span>

## <span data-ttu-id="c376a-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c376a-132">RELATED LINKS</span></span>
