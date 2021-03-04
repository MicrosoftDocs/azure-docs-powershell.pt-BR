---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerInstance.dll-Help.xml
Module Name: Az.ContainerInstance
online version: https://docs.microsoft.com/powershell/module/az.containerinstance/get-azcontainergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerInstance/ContainerInstance/help/Get-AzContainerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerInstance/ContainerInstance/help/Get-AzContainerGroup.md
ms.openlocfilehash: 65e6fbaa61285f946726fee9dce2261c998931cd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101893186"
---
# <span data-ttu-id="f69db-101">Get-AzContainerGroup</span><span class="sxs-lookup"><span data-stu-id="f69db-101">Get-AzContainerGroup</span></span>

## <span data-ttu-id="f69db-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f69db-102">SYNOPSIS</span></span>
<span data-ttu-id="f69db-103">Obtém grupos de contêineres.</span><span class="sxs-lookup"><span data-stu-id="f69db-103">Gets container groups.</span></span>

## <span data-ttu-id="f69db-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="f69db-104">SYNTAX</span></span>

### <span data-ttu-id="f69db-105">ListContainerGroupParamSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="f69db-105">ListContainerGroupParamSet (Default)</span></span>
```
Get-AzContainerGroup [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f69db-106">GetContainerGroupInResourceGroupParamSet</span><span class="sxs-lookup"><span data-stu-id="f69db-106">GetContainerGroupInResourceGroupParamSet</span></span>
```
Get-AzContainerGroup [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f69db-107">GetContainerGroupByResourceIdParamSet</span><span class="sxs-lookup"><span data-stu-id="f69db-107">GetContainerGroupByResourceIdParamSet</span></span>
```
Get-AzContainerGroup -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f69db-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="f69db-108">DESCRIPTION</span></span>
<span data-ttu-id="f69db-109">O cmdlet **Get-AzContainerGroup** obtém um grupo de contêineres especificado ou todos os grupos de contêineres em um grupo de recursos ou na assinatura.</span><span class="sxs-lookup"><span data-stu-id="f69db-109">The **Get-AzContainerGroup** cmdlet gets a specified container group or all the container groups in a resource group or the subscription.</span></span>

## <span data-ttu-id="f69db-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f69db-110">EXAMPLES</span></span>

### <span data-ttu-id="f69db-111">Exemplo 1: Obtém um grupo de contêineres especificado</span><span class="sxs-lookup"><span data-stu-id="f69db-111">Example 1: Gets a specified container group</span></span>
```
PS C:\> Get-AzContainerGroup -ResourceGroupName demo -Name mycontainer

ResourceGroupName        : demo
Id                       : /subscriptions/ae43b1e3-c35d-4c8c-bc0d-f148b4c52b78/resourceGroups/demo/providers/Microsoft.ContainerInstance/containerGroups/mycontainer
Name                     : mycontainer
Type                     : Microsoft.ContainerInstance/containerGroups
Location                 : westus
Tags                     :
ProvisioningState        : Succeeded
Containers               : {mycontainer}
ImageRegistryCredentials :
RestartPolicy            :
IpAddress                : 13.88.10.240
Ports                    : {8000}
OsType                   : Linux
Volumes                  :
State                    : Running
Events                   : {}
```

<span data-ttu-id="f69db-112">O comando obtém o grupo de contêineres especificado.</span><span class="sxs-lookup"><span data-stu-id="f69db-112">The command gets the specified container group.</span></span>

### <span data-ttu-id="f69db-113">Exemplo 2: Obtém grupos de contêineres em um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="f69db-113">Example 2: Gets container groups in a resource group</span></span>
```
PS C:\> Get-AzContainerGroup -ResourceGroupName demo

ResourceGroupName Name                     Location   OsType  Image                         IP                   Resources        ProvisioningState
----------------- ----                     --------   ------  -----                         --                   ---------        -----------------
demo              container1               west us    Linux   alpine:latest                 40.83.144.50:8002    1 cores/1 gb             Succeeded
demo              container2               west us    Linux   alpine:latest                 104.42.228.253:8001  1 cores/1 gb             Succeeded
```

<span data-ttu-id="f69db-114">O comando obtém os grupos de contêineres no grupo de recursos `demo` .</span><span class="sxs-lookup"><span data-stu-id="f69db-114">The command gets the container groups in the resource group `demo`.</span></span>

### <span data-ttu-id="f69db-115">Exemplo 3: Obtém grupos de contêineres na assinatura atual</span><span class="sxs-lookup"><span data-stu-id="f69db-115">Example 3: Gets container groups in the current subscription</span></span>
```
PS C:\> Get-AzContainerGroup

ResourceGroupName Name                     Location   OsType  Image                         IP                   Resources        ProvisioningState
----------------- ----                     --------   ------  -----                         --                   ---------        -----------------
demo1             container1               west us    Linux   alpine:latest                 40.83.144.50:8002    1 cores/1 gb             Succeeded
demo2             container2               west us    Linux   alpine:latest                 104.42.228.253:8001  1 cores/1 gb             Succeeded
```

<span data-ttu-id="f69db-116">O comando obtém os grupos de contêineres na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="f69db-116">The command gets the container groups in the current subscription.</span></span>

### <span data-ttu-id="f69db-117">Exemplo 4: Obtém grupos de contêineres usando a ID de recurso.</span><span class="sxs-lookup"><span data-stu-id="f69db-117">Example 4: Gets container groups using resource Id.</span></span>
```
PS C:\> Find-AzResource -ResourceGroupEquals demo -ResourceNameEquals mycontainer | Get-AzContainerGroup

ResourceGroupName        : demo
Id                       : /subscriptions/ae43b1e3-c35d-4c8c-bc0d-f148b4c52b78/resourceGroups/demo/providers/Microsoft.ContainerInstance/containerGroups/mycontainer
Name                     : mycontainer
Type                     : Microsoft.ContainerInstance/containerGroups
Location                 : westus
Tags                     :
ProvisioningState        : Succeeded
Containers               : {mycontainer}
ImageRegistryCredentials :
RestartPolicy            :
IpAddress                : 13.88.10.240
Ports                    : {8000}
OsType                   : Linux
Volumes                  :
State                    : Running
Events                   : {}
```

<span data-ttu-id="f69db-118">O comando obtém o grupo de contêineres com a ID de recurso.</span><span class="sxs-lookup"><span data-stu-id="f69db-118">The command gets the container group with the resource Id.</span></span>

## <span data-ttu-id="f69db-119">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="f69db-119">PARAMETERS</span></span>

### <span data-ttu-id="f69db-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f69db-120">-DefaultProfile</span></span>
<span data-ttu-id="f69db-121">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="f69db-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f69db-122">-Name</span><span class="sxs-lookup"><span data-stu-id="f69db-122">-Name</span></span>
<span data-ttu-id="f69db-123">O nome do grupo de contêineres.</span><span class="sxs-lookup"><span data-stu-id="f69db-123">The container group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetContainerGroupInResourceGroupParamSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f69db-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f69db-124">-ResourceGroupName</span></span>
<span data-ttu-id="f69db-125">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f69db-125">The resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListContainerGroupParamSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetContainerGroupInResourceGroupParamSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f69db-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f69db-126">-ResourceId</span></span>
<span data-ttu-id="f69db-127">A ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="f69db-127">The resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: GetContainerGroupByResourceIdParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f69db-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f69db-128">CommonParameters</span></span>
<span data-ttu-id="f69db-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f69db-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f69db-130">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f69db-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f69db-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f69db-131">INPUTS</span></span>

### <span data-ttu-id="f69db-132">System.String</span><span class="sxs-lookup"><span data-stu-id="f69db-132">System.String</span></span>

## <span data-ttu-id="f69db-133">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="f69db-133">OUTPUTS</span></span>

### <span data-ttu-id="f69db-134">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span><span class="sxs-lookup"><span data-stu-id="f69db-134">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span></span>

## <span data-ttu-id="f69db-135">NOTES</span><span class="sxs-lookup"><span data-stu-id="f69db-135">NOTES</span></span>

## <span data-ttu-id="f69db-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f69db-136">RELATED LINKS</span></span>
