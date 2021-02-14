---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerInstance.dll-Help.xml
Module Name: Az.ContainerInstance
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerinstance/get-azcontainerinstancelog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerInstance/ContainerInstance/help/Get-AzContainerInstanceLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerInstance/ContainerInstance/help/Get-AzContainerInstanceLog.md
ms.openlocfilehash: d279e5c08b43640d629e4146faf306d0e85482a8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111062"
---
# <span data-ttu-id="307f7-101">Get-AzContainerInstanceLog</span><span class="sxs-lookup"><span data-stu-id="307f7-101">Get-AzContainerInstanceLog</span></span>

## <span data-ttu-id="307f7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="307f7-102">SYNOPSIS</span></span>
<span data-ttu-id="307f7-103">Obter os logs de uma instância de contêiner em um grupo de contêineres.</span><span class="sxs-lookup"><span data-stu-id="307f7-103">Get the logs of a container instance in a container group.</span></span>

## <span data-ttu-id="307f7-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="307f7-104">SYNTAX</span></span>

### <span data-ttu-id="307f7-105">GetContainerInstanceLogByNamesParamSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="307f7-105">GetContainerInstanceLogByNamesParamSet (Default)</span></span>
```
Get-AzContainerInstanceLog [-ResourceGroupName] <String> -ContainerGroupName <String> [-Name <String>]
 [-Tail <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="307f7-106">GetContainerInstanceLogByPSContainerGroupParamSet</span><span class="sxs-lookup"><span data-stu-id="307f7-106">GetContainerInstanceLogByPSContainerGroupParamSet</span></span>
```
Get-AzContainerInstanceLog -InputContainerGroup <PSContainerGroup> [-Name <String>] [-Tail <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="307f7-107">GetContainerInstanceLogByResourceIdParamSet</span><span class="sxs-lookup"><span data-stu-id="307f7-107">GetContainerInstanceLogByResourceIdParamSet</span></span>
```
Get-AzContainerInstanceLog -ResourceId <String> [-Name <String>] [-Tail <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="307f7-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="307f7-108">DESCRIPTION</span></span>
<span data-ttu-id="307f7-109">O cmdlet **Get-AzContainerInstanceLog obtém** os logs de um contêiner em um grupo de contêineres.</span><span class="sxs-lookup"><span data-stu-id="307f7-109">The **Get-AzContainerInstanceLog** cmdlet gets the logs of a container in a container group.</span></span>

## <span data-ttu-id="307f7-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="307f7-110">EXAMPLES</span></span>

### <span data-ttu-id="307f7-111">Exemplo 1: Obter o log caudal de uma instância de contêiner</span><span class="sxs-lookup"><span data-stu-id="307f7-111">Example 1: Get the tail log of a container instance</span></span>
```
PS C:\> Get-AzContainerInstanceLog -ResourceGroupName demo -ContainerGroupName mycontainer -Name container1

Log line 1.
Log line 2.
Log line 3.
Log line 4.
```

<span data-ttu-id="307f7-112">Obter o log do `container1` grupo `mycontainer` contêiner.</span><span class="sxs-lookup"><span data-stu-id="307f7-112">Get the log from `container1` in container group `mycontainer`.</span></span> <span data-ttu-id="307f7-113">Por padrão, ele retornará até 4 MB de conteúdo de log.</span><span class="sxs-lookup"><span data-stu-id="307f7-113">By default, it will return up to 4MB log content.</span></span>

### <span data-ttu-id="307f7-114">Exemplo 2: Obter o log caudal de uma instância de contêiner que tenha o mesmo nome que o grupo contêiner</span><span class="sxs-lookup"><span data-stu-id="307f7-114">Example 2: Get the tail log of a container instance that has the same name as the container group</span></span>
```
PS C:\> Get-AzContainerInstanceLog -ResourceGroupName demo -ContainerGroupName mycontainer

Log line 1.
Log line 2.
Log line 3.
Log line 4.
```

<span data-ttu-id="307f7-115">Obter o log do `mycontainer` grupo `mycontainer` contêiner.</span><span class="sxs-lookup"><span data-stu-id="307f7-115">Get the log from `mycontainer` in container group `mycontainer`.</span></span> <span data-ttu-id="307f7-116">Por padrão, ele retornará até 4 MB de conteúdo de log.</span><span class="sxs-lookup"><span data-stu-id="307f7-116">By default, it will return up to 4MB log content.</span></span>

### <span data-ttu-id="307f7-117">Exemplo 3: Obter as 2 linhas caudais de log de uma instância de contêiner</span><span class="sxs-lookup"><span data-stu-id="307f7-117">Example 3: Get the tail 2 lines of log of a container instance</span></span>
```
PS C:\> Get-AzContainerInstanceLog -ResourceGroupName demo -ContainerGroupName mycontainer -Name container1 -Tail 2

Log line 3.
Log line 4.
```

<span data-ttu-id="307f7-118">Obter as 2 linhas de log caudais do `container1` grupo `mycontainer` contêiner.</span><span class="sxs-lookup"><span data-stu-id="307f7-118">Get the tail 2 lines of log from `container1` in container group `mycontainer`.</span></span>

### <span data-ttu-id="307f7-119">Exemplo 4: Obter o log caudal de uma instância de contêiner em um grupo de contêineres encadeado</span><span class="sxs-lookup"><span data-stu-id="307f7-119">Example 4: Get the tail log of a container instance in a piped in container group</span></span>
```
PS C:\> Get-AzContainerGroup -ResourceGroupName demo -Name mycontainer | Get-AzContainerInstanceLog

Log line 1.
Log line 2.
Log line 3.
Log line 4.
```

<span data-ttu-id="307f7-120">Obter o log `mycontainer` no grupo de `mycontainer` contêineres.</span><span class="sxs-lookup"><span data-stu-id="307f7-120">Get the log from `mycontainer` in piped in container group `mycontainer`.</span></span> <span data-ttu-id="307f7-121">Por padrão, ele retornará até 4 MB de conteúdo de log.</span><span class="sxs-lookup"><span data-stu-id="307f7-121">By default, it will return up to 4MB log content.</span></span>

## <span data-ttu-id="307f7-122">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="307f7-122">PARAMETERS</span></span>

### <span data-ttu-id="307f7-123">-ContainerGroupName</span><span class="sxs-lookup"><span data-stu-id="307f7-123">-ContainerGroupName</span></span>
<span data-ttu-id="307f7-124">O nome do grupo de contêineres.</span><span class="sxs-lookup"><span data-stu-id="307f7-124">The container group name.</span></span>

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

### <span data-ttu-id="307f7-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="307f7-125">-DefaultProfile</span></span>
<span data-ttu-id="307f7-126">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="307f7-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="307f7-127">-InputContainerGroup</span><span class="sxs-lookup"><span data-stu-id="307f7-127">-InputContainerGroup</span></span>
<span data-ttu-id="307f7-128">O objeto de grupo de contêiner de entrada.</span><span class="sxs-lookup"><span data-stu-id="307f7-128">The input container group object.</span></span>

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

### <span data-ttu-id="307f7-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="307f7-129">-Name</span></span>
<span data-ttu-id="307f7-130">O nome da instância do contêiner no grupo contêiner.</span><span class="sxs-lookup"><span data-stu-id="307f7-130">The container instance name in the container group.</span></span>
<span data-ttu-id="307f7-131">Padrão: o mesmo que o nome do grupo de contêineres</span><span class="sxs-lookup"><span data-stu-id="307f7-131">Default: the same as the container group name</span></span>

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

### <span data-ttu-id="307f7-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="307f7-132">-ResourceGroupName</span></span>
<span data-ttu-id="307f7-133">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="307f7-133">The resource group name.</span></span>

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

### <span data-ttu-id="307f7-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="307f7-134">-ResourceId</span></span>
<span data-ttu-id="307f7-135">A ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="307f7-135">The resource id.</span></span>

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

### <span data-ttu-id="307f7-136">-Tail</span><span class="sxs-lookup"><span data-stu-id="307f7-136">-Tail</span></span>
<span data-ttu-id="307f7-137">O número de linhas para seguir o log.</span><span class="sxs-lookup"><span data-stu-id="307f7-137">The number of lines to tail the log.</span></span>
<span data-ttu-id="307f7-138">Se não especificar, o cmdlet retornará até 4 MB de log caudal</span><span class="sxs-lookup"><span data-stu-id="307f7-138">If not specify, the cmdlet will return up to 4MB tailed log</span></span>

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

### <span data-ttu-id="307f7-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="307f7-139">CommonParameters</span></span>
<span data-ttu-id="307f7-140">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="307f7-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="307f7-141">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="307f7-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="307f7-142">Entradas</span><span class="sxs-lookup"><span data-stu-id="307f7-142">INPUTS</span></span>

### <span data-ttu-id="307f7-143">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span><span class="sxs-lookup"><span data-stu-id="307f7-143">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span></span>

### <span data-ttu-id="307f7-144">System.String</span><span class="sxs-lookup"><span data-stu-id="307f7-144">System.String</span></span>

## <span data-ttu-id="307f7-145">Saídas</span><span class="sxs-lookup"><span data-stu-id="307f7-145">OUTPUTS</span></span>

### <span data-ttu-id="307f7-146">System.String</span><span class="sxs-lookup"><span data-stu-id="307f7-146">System.String</span></span>

## <span data-ttu-id="307f7-147">Notas</span><span class="sxs-lookup"><span data-stu-id="307f7-147">NOTES</span></span>

## <span data-ttu-id="307f7-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="307f7-148">RELATED LINKS</span></span>
