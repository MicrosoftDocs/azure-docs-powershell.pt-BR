---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerInstance.dll-Help.xml
Module Name: Az.ContainerInstance
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerinstance/get-azcontainergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerInstance/ContainerInstance/help/Get-AzContainerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerInstance/ContainerInstance/help/Get-AzContainerGroup.md
ms.openlocfilehash: 2dadcac9f0b537a52a0a7270b7d20fc08e80461c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98430122"
---
# <span data-ttu-id="7cc1b-101">Get-AzContainerGroup</span><span class="sxs-lookup"><span data-stu-id="7cc1b-101">Get-AzContainerGroup</span></span>

## <span data-ttu-id="7cc1b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7cc1b-102">SYNOPSIS</span></span>
<span data-ttu-id="7cc1b-103">Obtém grupos de contêineres.</span><span class="sxs-lookup"><span data-stu-id="7cc1b-103">Gets container groups.</span></span>

## <span data-ttu-id="7cc1b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7cc1b-104">SYNTAX</span></span>

### <span data-ttu-id="7cc1b-105">ListContainerGroupParamSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="7cc1b-105">ListContainerGroupParamSet (Default)</span></span>
```
Get-AzContainerGroup [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7cc1b-106">GetContainerGroupInResourceGroupParamSet</span><span class="sxs-lookup"><span data-stu-id="7cc1b-106">GetContainerGroupInResourceGroupParamSet</span></span>
```
Get-AzContainerGroup [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7cc1b-107">GetContainerGroupByResourceIdParamSet</span><span class="sxs-lookup"><span data-stu-id="7cc1b-107">GetContainerGroupByResourceIdParamSet</span></span>
```
Get-AzContainerGroup -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7cc1b-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7cc1b-108">DESCRIPTION</span></span>
<span data-ttu-id="7cc1b-109">O cmdlet **Get-AzContainerGroup** Obtém um grupo de contêiner específico ou todos os grupos de contêineres em um grupo de recursos ou a assinatura.</span><span class="sxs-lookup"><span data-stu-id="7cc1b-109">The **Get-AzContainerGroup** cmdlet gets a specified container group or all the container groups in a resource group or the subscription.</span></span>

## <span data-ttu-id="7cc1b-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7cc1b-110">EXAMPLES</span></span>

### <span data-ttu-id="7cc1b-111">Exemplo 1: Obtém um grupo de contêineres especificado</span><span class="sxs-lookup"><span data-stu-id="7cc1b-111">Example 1: Gets a specified container group</span></span>
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

<span data-ttu-id="7cc1b-112">O comando obtém o grupo de contêineres especificado.</span><span class="sxs-lookup"><span data-stu-id="7cc1b-112">The command gets the specified container group.</span></span>

### <span data-ttu-id="7cc1b-113">Exemplo 2: Obtém grupos de contêineres em um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="7cc1b-113">Example 2: Gets container groups in a resource group</span></span>
```
PS C:\> Get-AzContainerGroup -ResourceGroupName demo

ResourceGroupName Name                     Location   OsType  Image                         IP                   Resources        ProvisioningState
----------------- ----                     --------   ------  -----                         --                   ---------        -----------------
demo              container1               west us    Linux   alpine:latest                 40.83.144.50:8002    1 cores/1 gb             Succeeded
demo              container2               west us    Linux   alpine:latest                 104.42.228.253:8001  1 cores/1 gb             Succeeded
```

<span data-ttu-id="7cc1b-114">O comando obtém os grupos de contêineres no grupo de recursos `demo` .</span><span class="sxs-lookup"><span data-stu-id="7cc1b-114">The command gets the container groups in the resource group `demo`.</span></span>

### <span data-ttu-id="7cc1b-115">Exemplo 3: Obtém grupos de contêineres na assinatura atual</span><span class="sxs-lookup"><span data-stu-id="7cc1b-115">Example 3: Gets container groups in the current subscription</span></span>
```
PS C:\> Get-AzContainerGroup

ResourceGroupName Name                     Location   OsType  Image                         IP                   Resources        ProvisioningState
----------------- ----                     --------   ------  -----                         --                   ---------        -----------------
demo1             container1               west us    Linux   alpine:latest                 40.83.144.50:8002    1 cores/1 gb             Succeeded
demo2             container2               west us    Linux   alpine:latest                 104.42.228.253:8001  1 cores/1 gb             Succeeded
```

<span data-ttu-id="7cc1b-116">O comando obtém os grupos de contêineres na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="7cc1b-116">The command gets the container groups in the current subscription.</span></span>

### <span data-ttu-id="7cc1b-117">Exemplo 4: Obtém grupos de contêineres usando a ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="7cc1b-117">Example 4: Gets container groups using resource Id.</span></span>
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

<span data-ttu-id="7cc1b-118">O comando obtém o grupo de contêineres com a ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="7cc1b-118">The command gets the container group with the resource Id.</span></span>

## <span data-ttu-id="7cc1b-119">OS</span><span class="sxs-lookup"><span data-stu-id="7cc1b-119">PARAMETERS</span></span>

### <span data-ttu-id="7cc1b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7cc1b-120">-DefaultProfile</span></span>
<span data-ttu-id="7cc1b-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7cc1b-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7cc1b-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="7cc1b-122">-Name</span></span>
<span data-ttu-id="7cc1b-123">O nome do grupo de contêineres.</span><span class="sxs-lookup"><span data-stu-id="7cc1b-123">The container group Name.</span></span>

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

### <span data-ttu-id="7cc1b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7cc1b-124">-ResourceGroupName</span></span>
<span data-ttu-id="7cc1b-125">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="7cc1b-125">The resource Group Name.</span></span>

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

### <span data-ttu-id="7cc1b-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7cc1b-126">-ResourceId</span></span>
<span data-ttu-id="7cc1b-127">A ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="7cc1b-127">The resource id.</span></span>

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

### <span data-ttu-id="7cc1b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7cc1b-128">CommonParameters</span></span>
<span data-ttu-id="7cc1b-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7cc1b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7cc1b-130">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7cc1b-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7cc1b-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7cc1b-131">INPUTS</span></span>

### <span data-ttu-id="7cc1b-132">System. String</span><span class="sxs-lookup"><span data-stu-id="7cc1b-132">System.String</span></span>

## <span data-ttu-id="7cc1b-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7cc1b-133">OUTPUTS</span></span>

### <span data-ttu-id="7cc1b-134">Microsoft. Azure. Commands. ContainerInstance. Models. PSContainerGroup</span><span class="sxs-lookup"><span data-stu-id="7cc1b-134">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span></span>

## <span data-ttu-id="7cc1b-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7cc1b-135">NOTES</span></span>

## <span data-ttu-id="7cc1b-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7cc1b-136">RELATED LINKS</span></span>
