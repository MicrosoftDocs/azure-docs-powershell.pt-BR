---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/new-azservicefabricapplicationtype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricApplicationType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricApplicationType.md
ms.openlocfilehash: 690b00c41aea571786916d2055eb4063c51c4370
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116381"
---
# <span data-ttu-id="11e38-101">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="11e38-101">New-AzServiceFabricApplicationType</span></span>

## <span data-ttu-id="11e38-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="11e38-102">SYNOPSIS</span></span>
<span data-ttu-id="11e38-103">Crie um novo tipo de aplicativo de malha de serviço sob o grupo e o cluster de recursos especificados.</span><span class="sxs-lookup"><span data-stu-id="11e38-103">Create new service fabric application type under the specified resource group and cluster.</span></span>

## <span data-ttu-id="11e38-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="11e38-104">SYNTAX</span></span>

```
New-AzServiceFabricApplicationType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="11e38-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="11e38-105">DESCRIPTION</span></span>
<span data-ttu-id="11e38-106">O cmdlet cria um novo tipo de aplicativo de malha de serviço sob o grupo de recursos e cluster especificados.</span><span class="sxs-lookup"><span data-stu-id="11e38-106">The cmdlet creates a new service fabric application type under the specified resource group and cluster.</span></span>

## <span data-ttu-id="11e38-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="11e38-107">EXAMPLES</span></span>

### <span data-ttu-id="11e38-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="11e38-108">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> $appType = New-AzServiceFabricApplicationType -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName -Verbose
```

<span data-ttu-id="11e38-109">Este exemplo criará um novo tipo de aplicativo "testAppType" no grupo de recursos e cluster especificados.</span><span class="sxs-lookup"><span data-stu-id="11e38-109">This example will create a new application type "testAppType" under the resource group and cluster specified.</span></span>

## <span data-ttu-id="11e38-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="11e38-110">PARAMETERS</span></span>

### <span data-ttu-id="11e38-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="11e38-111">-ClusterName</span></span>
<span data-ttu-id="11e38-112">Especifique o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="11e38-112">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="11e38-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11e38-113">-DefaultProfile</span></span>
<span data-ttu-id="11e38-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="11e38-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="11e38-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="11e38-115">-Name</span></span>
<span data-ttu-id="11e38-116">Especificar o nome do tipo de aplicativo</span><span class="sxs-lookup"><span data-stu-id="11e38-116">Specify the name of the application type</span></span>

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

### <span data-ttu-id="11e38-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11e38-117">-ResourceGroupName</span></span>
<span data-ttu-id="11e38-118">Especifique o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="11e38-118">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="11e38-119">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="11e38-119">-Confirm</span></span>
<span data-ttu-id="11e38-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="11e38-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="11e38-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11e38-121">-WhatIf</span></span>
<span data-ttu-id="11e38-122">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="11e38-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="11e38-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="11e38-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="11e38-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11e38-124">CommonParameters</span></span>
<span data-ttu-id="11e38-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11e38-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11e38-126">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="11e38-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11e38-127">Entradas</span><span class="sxs-lookup"><span data-stu-id="11e38-127">INPUTS</span></span>

### <span data-ttu-id="11e38-128">System.String</span><span class="sxs-lookup"><span data-stu-id="11e38-128">System.String</span></span>

## <span data-ttu-id="11e38-129">Saídas</span><span class="sxs-lookup"><span data-stu-id="11e38-129">OUTPUTS</span></span>

### <span data-ttu-id="11e38-130">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationType</span><span class="sxs-lookup"><span data-stu-id="11e38-130">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationType</span></span>

## <span data-ttu-id="11e38-131">Notas</span><span class="sxs-lookup"><span data-stu-id="11e38-131">NOTES</span></span>

## <span data-ttu-id="11e38-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="11e38-132">RELATED LINKS</span></span>
