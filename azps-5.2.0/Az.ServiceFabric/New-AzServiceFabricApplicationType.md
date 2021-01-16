---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/new-azservicefabricapplicationtype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricApplicationType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricApplicationType.md
ms.openlocfilehash: 690b00c41aea571786916d2055eb4063c51c4370
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98260676"
---
# <span data-ttu-id="8331f-101">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="8331f-101">New-AzServiceFabricApplicationType</span></span>

## <span data-ttu-id="8331f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8331f-102">SYNOPSIS</span></span>
<span data-ttu-id="8331f-103">Criar novo tipo de aplicativo Service Fabric no grupo de recursos e no cluster especificado.</span><span class="sxs-lookup"><span data-stu-id="8331f-103">Create new service fabric application type under the specified resource group and cluster.</span></span>

## <span data-ttu-id="8331f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8331f-104">SYNTAX</span></span>

```
New-AzServiceFabricApplicationType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8331f-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8331f-105">DESCRIPTION</span></span>
<span data-ttu-id="8331f-106">O cmdlet cria um novo tipo de aplicativo Service Fabric no grupo de recursos e no cluster especificado.</span><span class="sxs-lookup"><span data-stu-id="8331f-106">The cmdlet creates a new service fabric application type under the specified resource group and cluster.</span></span>

## <span data-ttu-id="8331f-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8331f-107">EXAMPLES</span></span>

### <span data-ttu-id="8331f-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="8331f-108">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> $appType = New-AzServiceFabricApplicationType -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName -Verbose
```

<span data-ttu-id="8331f-109">Este exemplo criará um novo tipo de aplicativo "testAppType", no grupo de recursos e no cluster especificado.</span><span class="sxs-lookup"><span data-stu-id="8331f-109">This example will create a new application type "testAppType" under the resource group and cluster specified.</span></span>

## <span data-ttu-id="8331f-110">OS</span><span class="sxs-lookup"><span data-stu-id="8331f-110">PARAMETERS</span></span>

### <span data-ttu-id="8331f-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="8331f-111">-ClusterName</span></span>
<span data-ttu-id="8331f-112">Especifique o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="8331f-112">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="8331f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8331f-113">-DefaultProfile</span></span>
<span data-ttu-id="8331f-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8331f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8331f-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="8331f-115">-Name</span></span>
<span data-ttu-id="8331f-116">Especificar o nome do tipo de aplicativo</span><span class="sxs-lookup"><span data-stu-id="8331f-116">Specify the name of the application type</span></span>

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

### <span data-ttu-id="8331f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8331f-117">-ResourceGroupName</span></span>
<span data-ttu-id="8331f-118">Especifique o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="8331f-118">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="8331f-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="8331f-119">-Confirm</span></span>
<span data-ttu-id="8331f-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8331f-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8331f-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8331f-121">-WhatIf</span></span>
<span data-ttu-id="8331f-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="8331f-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8331f-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8331f-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8331f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8331f-124">CommonParameters</span></span>
<span data-ttu-id="8331f-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8331f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8331f-126">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8331f-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8331f-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8331f-127">INPUTS</span></span>

### <span data-ttu-id="8331f-128">System. String</span><span class="sxs-lookup"><span data-stu-id="8331f-128">System.String</span></span>

## <span data-ttu-id="8331f-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8331f-129">OUTPUTS</span></span>

### <span data-ttu-id="8331f-130">Microsoft. Azure. Commands. imfabric. Models. PSApplicationType</span><span class="sxs-lookup"><span data-stu-id="8331f-130">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationType</span></span>

## <span data-ttu-id="8331f-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8331f-131">NOTES</span></span>

## <span data-ttu-id="8331f-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8331f-132">RELATED LINKS</span></span>
