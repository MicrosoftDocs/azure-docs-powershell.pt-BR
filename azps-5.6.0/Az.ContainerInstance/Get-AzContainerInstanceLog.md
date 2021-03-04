---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerInstance.dll-Help.xml
Module Name: Az.ContainerInstance
online version: https://docs.microsoft.com/powershell/module/az.containerinstance/get-azcontainerinstancelog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerInstance/ContainerInstance/help/Get-AzContainerInstanceLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerInstance/ContainerInstance/help/Get-AzContainerInstanceLog.md
ms.openlocfilehash: 2ab0102534a8773ca1ca206bde2075e2bd7930f4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101893184"
---
# <span data-ttu-id="e8444-101">Get-AzContainerInstanceLog</span><span class="sxs-lookup"><span data-stu-id="e8444-101">Get-AzContainerInstanceLog</span></span>

## <span data-ttu-id="e8444-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e8444-102">SYNOPSIS</span></span>
<span data-ttu-id="e8444-103">Obter os logs de uma instância de contêiner em um grupo de contêineres.</span><span class="sxs-lookup"><span data-stu-id="e8444-103">Get the logs of a container instance in a container group.</span></span>

## <span data-ttu-id="e8444-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="e8444-104">SYNTAX</span></span>

### <span data-ttu-id="e8444-105">GetContainerInstanceLogByNamesParamSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="e8444-105">GetContainerInstanceLogByNamesParamSet (Default)</span></span>
```
Get-AzContainerInstanceLog [-ResourceGroupName] <String> -ContainerGroupName <String> [-Name <String>]
 [-Tail <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e8444-106">GetContainerInstanceLogByPSContainerGroupParamSet</span><span class="sxs-lookup"><span data-stu-id="e8444-106">GetContainerInstanceLogByPSContainerGroupParamSet</span></span>
```
Get-AzContainerInstanceLog -InputContainerGroup <PSContainerGroup> [-Name <String>] [-Tail <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e8444-107">GetContainerInstanceLogByResourceIdParamSet</span><span class="sxs-lookup"><span data-stu-id="e8444-107">GetContainerInstanceLogByResourceIdParamSet</span></span>
```
Get-AzContainerInstanceLog -ResourceId <String> [-Name <String>] [-Tail <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e8444-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="e8444-108">DESCRIPTION</span></span>
<span data-ttu-id="e8444-109">O cmdlet **Get-AzContainerInstanceLog** obtém os logs de um contêiner em um grupo de contêineres.</span><span class="sxs-lookup"><span data-stu-id="e8444-109">The **Get-AzContainerInstanceLog** cmdlet gets the logs of a container in a container group.</span></span>

## <span data-ttu-id="e8444-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e8444-110">EXAMPLES</span></span>

### <span data-ttu-id="e8444-111">Exemplo 1: Obter o log de cauda de uma instância de contêiner</span><span class="sxs-lookup"><span data-stu-id="e8444-111">Example 1: Get the tail log of a container instance</span></span>
```
PS C:\> Get-AzContainerInstanceLog -ResourceGroupName demo -ContainerGroupName mycontainer -Name container1

Log line 1.
Log line 2.
Log line 3.
Log line 4.
```

<span data-ttu-id="e8444-112">Obter o log no `container1` grupo contêiner `mycontainer` .</span><span class="sxs-lookup"><span data-stu-id="e8444-112">Get the log from `container1` in container group `mycontainer`.</span></span> <span data-ttu-id="e8444-113">Por padrão, ele retornará até 4 MB de conteúdo de log.</span><span class="sxs-lookup"><span data-stu-id="e8444-113">By default, it will return up to 4MB log content.</span></span>

### <span data-ttu-id="e8444-114">Exemplo 2: Obter o log de cauda de uma instância de contêiner que tenha o mesmo nome do grupo de contêineres</span><span class="sxs-lookup"><span data-stu-id="e8444-114">Example 2: Get the tail log of a container instance that has the same name as the container group</span></span>
```
PS C:\> Get-AzContainerInstanceLog -ResourceGroupName demo -ContainerGroupName mycontainer

Log line 1.
Log line 2.
Log line 3.
Log line 4.
```

<span data-ttu-id="e8444-115">Obter o log no `mycontainer` grupo contêiner `mycontainer` .</span><span class="sxs-lookup"><span data-stu-id="e8444-115">Get the log from `mycontainer` in container group `mycontainer`.</span></span> <span data-ttu-id="e8444-116">Por padrão, ele retornará até 4 MB de conteúdo de log.</span><span class="sxs-lookup"><span data-stu-id="e8444-116">By default, it will return up to 4MB log content.</span></span>

### <span data-ttu-id="e8444-117">Exemplo 3: Obter a cauda 2 linhas de log de uma instância de contêiner</span><span class="sxs-lookup"><span data-stu-id="e8444-117">Example 3: Get the tail 2 lines of log of a container instance</span></span>
```
PS C:\> Get-AzContainerInstanceLog -ResourceGroupName demo -ContainerGroupName mycontainer -Name container1 -Tail 2

Log line 3.
Log line 4.
```

<span data-ttu-id="e8444-118">Obter a cauda 2 linhas de log no `container1` grupo de `mycontainer` contêineres .</span><span class="sxs-lookup"><span data-stu-id="e8444-118">Get the tail 2 lines of log from `container1` in container group `mycontainer`.</span></span>

### <span data-ttu-id="e8444-119">Exemplo 4: Obter o log de cauda de uma instância de contêiner em um grupo de contêineres canalado</span><span class="sxs-lookup"><span data-stu-id="e8444-119">Example 4: Get the tail log of a container instance in a piped in container group</span></span>
```
PS C:\> Get-AzContainerGroup -ResourceGroupName demo -Name mycontainer | Get-AzContainerInstanceLog

Log line 1.
Log line 2.
Log line 3.
Log line 4.
```

<span data-ttu-id="e8444-120">Obter o log `mycontainer` de dentro canalizou no grupo de `mycontainer` contêineres .</span><span class="sxs-lookup"><span data-stu-id="e8444-120">Get the log from `mycontainer` in piped in container group `mycontainer`.</span></span> <span data-ttu-id="e8444-121">Por padrão, ele retornará até 4 MB de conteúdo de log.</span><span class="sxs-lookup"><span data-stu-id="e8444-121">By default, it will return up to 4MB log content.</span></span>

## <span data-ttu-id="e8444-122">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="e8444-122">PARAMETERS</span></span>

### <span data-ttu-id="e8444-123">-ContainerGroupName</span><span class="sxs-lookup"><span data-stu-id="e8444-123">-ContainerGroupName</span></span>
<span data-ttu-id="e8444-124">O nome do grupo do contêiner.</span><span class="sxs-lookup"><span data-stu-id="e8444-124">The container group name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetContainerInstanceLogByNamesParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8444-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8444-125">-DefaultProfile</span></span>
<span data-ttu-id="e8444-126">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="e8444-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e8444-127">-InputContainerGroup</span><span class="sxs-lookup"><span data-stu-id="e8444-127">-InputContainerGroup</span></span>
<span data-ttu-id="e8444-128">O objeto de grupo do contêiner de entrada.</span><span class="sxs-lookup"><span data-stu-id="e8444-128">The input container group object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup
Parameter Sets: GetContainerInstanceLogByPSContainerGroupParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e8444-129">-Name</span><span class="sxs-lookup"><span data-stu-id="e8444-129">-Name</span></span>
<span data-ttu-id="e8444-130">O nome da instância do contêiner no grupo de contêineres.</span><span class="sxs-lookup"><span data-stu-id="e8444-130">The container instance name in the container group.</span></span>
<span data-ttu-id="e8444-131">Padrão: o mesmo que o nome do grupo de contêineres</span><span class="sxs-lookup"><span data-stu-id="e8444-131">Default: the same as the container group name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8444-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8444-132">-ResourceGroupName</span></span>
<span data-ttu-id="e8444-133">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e8444-133">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetContainerInstanceLogByNamesParamSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8444-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e8444-134">-ResourceId</span></span>
<span data-ttu-id="e8444-135">A ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="e8444-135">The resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: GetContainerInstanceLogByResourceIdParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8444-136">-Tail</span><span class="sxs-lookup"><span data-stu-id="e8444-136">-Tail</span></span>
<span data-ttu-id="e8444-137">O número de linhas para seguir o log.</span><span class="sxs-lookup"><span data-stu-id="e8444-137">The number of lines to tail the log.</span></span>
<span data-ttu-id="e8444-138">Se não for especificado, o cmdlet retornará até 4 MB de log com cauda</span><span class="sxs-lookup"><span data-stu-id="e8444-138">If not specify, the cmdlet will return up to 4MB tailed log</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8444-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8444-139">CommonParameters</span></span>
<span data-ttu-id="e8444-140">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e8444-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8444-141">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e8444-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8444-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e8444-142">INPUTS</span></span>

### <span data-ttu-id="e8444-143">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span><span class="sxs-lookup"><span data-stu-id="e8444-143">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span></span>

### <span data-ttu-id="e8444-144">System.String</span><span class="sxs-lookup"><span data-stu-id="e8444-144">System.String</span></span>

## <span data-ttu-id="e8444-145">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="e8444-145">OUTPUTS</span></span>

### <span data-ttu-id="e8444-146">System.String</span><span class="sxs-lookup"><span data-stu-id="e8444-146">System.String</span></span>

## <span data-ttu-id="e8444-147">NOTES</span><span class="sxs-lookup"><span data-stu-id="e8444-147">NOTES</span></span>

## <span data-ttu-id="e8444-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e8444-148">RELATED LINKS</span></span>
