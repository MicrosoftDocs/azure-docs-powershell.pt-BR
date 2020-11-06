---
external help file: Microsoft.Azure.Commands.ContainerInstance.dll-Help.xml
Module Name: AzureRM.ContainerInstance
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerinstance/get-azurermcontainergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerInstance/Commands.ContainerInstance/help/Get-AzureRmContainerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerInstance/Commands.ContainerInstance/help/Get-AzureRmContainerGroup.md
ms.openlocfilehash: 665fcc30b0b9c2769af66ae4a590f3526438cae6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426755"
---
# <span data-ttu-id="09163-101">Get-AzureRmContainerGroup</span><span class="sxs-lookup"><span data-stu-id="09163-101">Get-AzureRmContainerGroup</span></span>

## <span data-ttu-id="09163-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="09163-102">SYNOPSIS</span></span>
<span data-ttu-id="09163-103">Obtém grupos de contêineres.</span><span class="sxs-lookup"><span data-stu-id="09163-103">Gets container groups.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="09163-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="09163-104">SYNTAX</span></span>

### <span data-ttu-id="09163-105">ListContainerGroupParamSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="09163-105">ListContainerGroupParamSet (Default)</span></span>
```
Get-AzureRmContainerGroup [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="09163-106">GetContainerGroupInResourceGroupParamSet</span><span class="sxs-lookup"><span data-stu-id="09163-106">GetContainerGroupInResourceGroupParamSet</span></span>
```
Get-AzureRmContainerGroup [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="09163-107">GetContainerGroupByResourceIdParamSet</span><span class="sxs-lookup"><span data-stu-id="09163-107">GetContainerGroupByResourceIdParamSet</span></span>
```
Get-AzureRmContainerGroup -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="09163-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="09163-108">DESCRIPTION</span></span>
<span data-ttu-id="09163-109">O cmdlet **Get-AzureRmContainerGroup** Obtém um grupo de contêiner específico ou todos os grupos de contêineres em um grupo de recursos ou a assinatura.</span><span class="sxs-lookup"><span data-stu-id="09163-109">The **Get-AzureRmContainerGroup** cmdlet gets a specified container group or all the container groups in a resource group or the subscription.</span></span>

## <span data-ttu-id="09163-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="09163-110">EXAMPLES</span></span>

### <span data-ttu-id="09163-111">Exemplo 1: Obtém um grupo de contêineres especificado</span><span class="sxs-lookup"><span data-stu-id="09163-111">Example 1: Gets a specified container group</span></span>
```
PS C:\> Get-AzureRmContainerGroup -ResourceGroupName demo -Name mycontainer

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

<span data-ttu-id="09163-112">O comando obtém o grupo de contêineres especificado.</span><span class="sxs-lookup"><span data-stu-id="09163-112">The command gets the specified container group.</span></span>

### <span data-ttu-id="09163-113">Exemplo 2: Obtém grupos de contêineres em um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="09163-113">Example 2: Gets container groups in a resource group</span></span>
```
PS C:\> Get-AzureRmContainerGroup -ResourceGroupName demo

ResourceGroupName Name                     Location   OsType  Image                         IP                   Resources        ProvisioningState
----------------- ----                     --------   ------  -----                         --                   ---------        -----------------
demo              container1               west us    Linux   alpine:latest                 40.83.144.50:8002    1 cores/1 gb             Succeeded
demo              container2               west us    Linux   alpine:latest                 104.42.228.253:8001  1 cores/1 gb             Succeeded
```

<span data-ttu-id="09163-114">O comando obtém os grupos de contêineres no grupo de recursos `demo` .</span><span class="sxs-lookup"><span data-stu-id="09163-114">The command gets the container groups in the resource group `demo`.</span></span>

### <span data-ttu-id="09163-115">Exemplo 3: Obtém grupos de contêineres na assinatura atual</span><span class="sxs-lookup"><span data-stu-id="09163-115">Example 3: Gets container groups in the current subscription</span></span>
```
PS C:\> Get-AzureRmContainerGroup

ResourceGroupName Name                     Location   OsType  Image                         IP                   Resources        ProvisioningState
----------------- ----                     --------   ------  -----                         --                   ---------        -----------------
demo1             container1               west us    Linux   alpine:latest                 40.83.144.50:8002    1 cores/1 gb             Succeeded
demo2             container2               west us    Linux   alpine:latest                 104.42.228.253:8001  1 cores/1 gb             Succeeded
```

<span data-ttu-id="09163-116">O comando obtém os grupos de contêineres na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="09163-116">The command gets the container groups in the current subscription.</span></span>

### <span data-ttu-id="09163-117">Exemplo 4: Obtém grupos de contêineres usando a ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="09163-117">Example 4: Gets container groups using resource Id.</span></span>
```
PS C:\> Find-AzureRmResource -ResourceGroupEquals demo -ResourceNameEquals mycontainer | Get-AzureRmContainerGroup

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

<span data-ttu-id="09163-118">O comando obtém o grupo de contêineres com a ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="09163-118">The command gets the container group with the resource Id.</span></span>

## <span data-ttu-id="09163-119">OS</span><span class="sxs-lookup"><span data-stu-id="09163-119">PARAMETERS</span></span>

### <span data-ttu-id="09163-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09163-120">-DefaultProfile</span></span>
<span data-ttu-id="09163-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="09163-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09163-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="09163-122">-Name</span></span>
<span data-ttu-id="09163-123">O nome do grupo de contêineres.</span><span class="sxs-lookup"><span data-stu-id="09163-123">The container group Name.</span></span>

```yaml
Type: String
Parameter Sets: GetContainerGroupInResourceGroupParamSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09163-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09163-124">-ResourceGroupName</span></span>
<span data-ttu-id="09163-125">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="09163-125">The resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: ListContainerGroupParamSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: GetContainerGroupInResourceGroupParamSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09163-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="09163-126">-ResourceId</span></span>
<span data-ttu-id="09163-127">A ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="09163-127">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: GetContainerGroupByResourceIdParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09163-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09163-128">CommonParameters</span></span>
<span data-ttu-id="09163-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09163-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09163-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="09163-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09163-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="09163-131">INPUTS</span></span>

### <span data-ttu-id="09163-132">System. String</span><span class="sxs-lookup"><span data-stu-id="09163-132">System.String</span></span>

## <span data-ttu-id="09163-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="09163-133">OUTPUTS</span></span>

### <span data-ttu-id="09163-134">Microsoft. Azure. Commands. ContainerInstance. Models. PSContainerGroup</span><span class="sxs-lookup"><span data-stu-id="09163-134">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span></span>

## <span data-ttu-id="09163-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="09163-135">NOTES</span></span>

## <span data-ttu-id="09163-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="09163-136">RELATED LINKS</span></span>
