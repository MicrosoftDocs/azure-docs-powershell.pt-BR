---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/set-azservicefabricupgradetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricUpgradeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricUpgradeType.md
ms.openlocfilehash: c117937d674c95f69eb967667c86c503ffbb62c1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888426"
---
# <span data-ttu-id="49a49-101">Set-AzServiceFabricUpgradeType</span><span class="sxs-lookup"><span data-stu-id="49a49-101">Set-AzServiceFabricUpgradeType</span></span>

## <span data-ttu-id="49a49-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="49a49-102">SYNOPSIS</span></span>
<span data-ttu-id="49a49-103">Altere o tipo de atualização do Service Fabric do cluster.</span><span class="sxs-lookup"><span data-stu-id="49a49-103">Change the Service Fabric upgrade type of the cluster.</span></span>

## <span data-ttu-id="49a49-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="49a49-104">SYNTAX</span></span>

### <span data-ttu-id="49a49-105">Automático</span><span class="sxs-lookup"><span data-stu-id="49a49-105">Automatic</span></span>
```
Set-AzServiceFabricUpgradeType [-ResourceGroupName] <String> [-Name] <String> -UpgradeMode <ClusterUpgradeMode>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="49a49-106">Manual</span><span class="sxs-lookup"><span data-stu-id="49a49-106">Manual</span></span>
```
Set-AzServiceFabricUpgradeType [-ResourceGroupName] <String> [-Name] <String> -UpgradeMode <ClusterUpgradeMode>
 -Version <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="49a49-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="49a49-107">DESCRIPTION</span></span>
<span data-ttu-id="49a49-108">Use **Set-AzServiceFabricUpgradeType** para definir o tipo de atualização como automático ou manual com a versão de código do Service Fabric específica.</span><span class="sxs-lookup"><span data-stu-id="49a49-108">Use **Set-AzServiceFabricUpgradeType** to set upgrade type to automatic or manual with specific Service Fabric code version.</span></span>

## <span data-ttu-id="49a49-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="49a49-109">EXAMPLES</span></span>

### <span data-ttu-id="49a49-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="49a49-110">Example 1</span></span>
```
PS c:> Set-AzServiceFabricUpgradeType -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster'  -UpgradeMode Automatic
```

<span data-ttu-id="49a49-111">Este comando definirá o modo de atualização de cluster como automático.</span><span class="sxs-lookup"><span data-stu-id="49a49-111">This command will set the cluster upgrade mode to automatic.</span></span>

## <span data-ttu-id="49a49-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="49a49-112">PARAMETERS</span></span>

### <span data-ttu-id="49a49-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49a49-113">-DefaultProfile</span></span>
<span data-ttu-id="49a49-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="49a49-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="49a49-115">-Name</span><span class="sxs-lookup"><span data-stu-id="49a49-115">-Name</span></span>
<span data-ttu-id="49a49-116">Especificar o nome do cluster</span><span class="sxs-lookup"><span data-stu-id="49a49-116">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="49a49-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49a49-117">-ResourceGroupName</span></span>
<span data-ttu-id="49a49-118">Especifique o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="49a49-118">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="49a49-119">-UpgradeMode</span><span class="sxs-lookup"><span data-stu-id="49a49-119">-UpgradeMode</span></span>
<span data-ttu-id="49a49-120">ClusterUpgradeMode</span><span class="sxs-lookup"><span data-stu-id="49a49-120">ClusterUpgradeMode</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.ClusterUpgradeMode
Parameter Sets: (All)
Aliases:
Accepted values: Automatic, Manual

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="49a49-121">-Version</span><span class="sxs-lookup"><span data-stu-id="49a49-121">-Version</span></span>
<span data-ttu-id="49a49-122">Versão de código de cluster</span><span class="sxs-lookup"><span data-stu-id="49a49-122">Cluster code version</span></span>

```yaml
Type: System.String
Parameter Sets: Manual
Aliases: ClusterCodeVersion

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="49a49-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="49a49-123">-Confirm</span></span>
<span data-ttu-id="49a49-124">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="49a49-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="49a49-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="49a49-125">-WhatIf</span></span>
<span data-ttu-id="49a49-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="49a49-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="49a49-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="49a49-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="49a49-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49a49-128">CommonParameters</span></span>
<span data-ttu-id="49a49-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49a49-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49a49-130">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="49a49-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49a49-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="49a49-131">INPUTS</span></span>

### <span data-ttu-id="49a49-132">System.String</span><span class="sxs-lookup"><span data-stu-id="49a49-132">System.String</span></span>

### <span data-ttu-id="49a49-133">Microsoft.Azure.Commands.ServiceFabric.Models.ClusterUpgradeMode</span><span class="sxs-lookup"><span data-stu-id="49a49-133">Microsoft.Azure.Commands.ServiceFabric.Models.ClusterUpgradeMode</span></span>

## <span data-ttu-id="49a49-134">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="49a49-134">OUTPUTS</span></span>

### <span data-ttu-id="49a49-135">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span><span class="sxs-lookup"><span data-stu-id="49a49-135">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="49a49-136">NOTES</span><span class="sxs-lookup"><span data-stu-id="49a49-136">NOTES</span></span>

## <span data-ttu-id="49a49-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="49a49-137">RELATED LINKS</span></span>
