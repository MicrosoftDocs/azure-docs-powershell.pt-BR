---
external help file: Microsoft.Azure.Commands.ContainerInstance.dll-Help.xml
Module Name: AzureRM.ContainerInstance
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerinstance/get-azurermcontainerinstancelog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerInstance/Commands.ContainerInstance/help/Get-AzureRmContainerInstanceLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerInstance/Commands.ContainerInstance/help/Get-AzureRmContainerInstanceLog.md
ms.openlocfilehash: 346973683ca7e360c4b4d63a4f2ed4f4856a0797
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426751"
---
# <span data-ttu-id="ded9a-101">Get-AzureRmContainerInstanceLog</span><span class="sxs-lookup"><span data-stu-id="ded9a-101">Get-AzureRmContainerInstanceLog</span></span>

## <span data-ttu-id="ded9a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ded9a-102">SYNOPSIS</span></span>
<span data-ttu-id="ded9a-103">Obter os logs de uma instância de contêiner em um grupo de contêineres.</span><span class="sxs-lookup"><span data-stu-id="ded9a-103">Get the logs of a container instance in a container group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ded9a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ded9a-104">SYNTAX</span></span>

### <span data-ttu-id="ded9a-105">GetContainerInstanceLogByNamesParamSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="ded9a-105">GetContainerInstanceLogByNamesParamSet (Default)</span></span>
```
Get-AzureRmContainerInstanceLog [-ResourceGroupName] <String> -ContainerGroupName <String> [-Name <String>]
 [-Tail <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ded9a-106">GetContainerInstanceLogByPSContainerGroupParamSet</span><span class="sxs-lookup"><span data-stu-id="ded9a-106">GetContainerInstanceLogByPSContainerGroupParamSet</span></span>
```
Get-AzureRmContainerInstanceLog -InputContainerGroup <PSContainerGroup> [-Name <String>] [-Tail <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ded9a-107">GetContainerInstanceLogByResourceIdParamSet</span><span class="sxs-lookup"><span data-stu-id="ded9a-107">GetContainerInstanceLogByResourceIdParamSet</span></span>
```
Get-AzureRmContainerInstanceLog -ResourceId <String> [-Name <String>] [-Tail <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ded9a-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ded9a-108">DESCRIPTION</span></span>
<span data-ttu-id="ded9a-109">O cmdlet **Get-AzureRmContainerInstanceLog** Obtém os logs de um contêiner em um grupo de contêineres.</span><span class="sxs-lookup"><span data-stu-id="ded9a-109">The **Get-AzureRmContainerInstanceLog** cmdlet gets the logs of a container in a container group.</span></span>

## <span data-ttu-id="ded9a-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ded9a-110">EXAMPLES</span></span>

### <span data-ttu-id="ded9a-111">Exemplo 1: obter o log final de uma instância de contêiner</span><span class="sxs-lookup"><span data-stu-id="ded9a-111">Example 1: Get the tail log of a container instance</span></span>
```
PS C:\> Get-AzureRmContainerInstanceLog -ResourceGroupName demo -ContainerGroupName mycontainer -Name container1

Log line 1.
Log line 2.
Log line 3.
Log line 4.
```

<span data-ttu-id="ded9a-112">Obter o log de `container1` no grupo de contêineres `mycontainer` .</span><span class="sxs-lookup"><span data-stu-id="ded9a-112">Get the log from `container1` in container group `mycontainer`.</span></span> <span data-ttu-id="ded9a-113">Por padrão, ele retornará até 4MB de conteúdo de log.</span><span class="sxs-lookup"><span data-stu-id="ded9a-113">By default, it will return up to 4MB log content.</span></span>

### <span data-ttu-id="ded9a-114">Exemplo 2: obter o log final de uma instância de contêiner que tem o mesmo nome que o grupo de contêineres</span><span class="sxs-lookup"><span data-stu-id="ded9a-114">Example 2: Get the tail log of a container instance that has the same name as the container group</span></span>
```
PS C:\> Get-AzureRmContainerInstanceLog -ResourceGroupName demo -ContainerGroupName mycontainer

Log line 1.
Log line 2.
Log line 3.
Log line 4.
```

<span data-ttu-id="ded9a-115">Obter o log de `mycontainer` no grupo de contêineres `mycontainer` .</span><span class="sxs-lookup"><span data-stu-id="ded9a-115">Get the log from `mycontainer` in container group `mycontainer`.</span></span> <span data-ttu-id="ded9a-116">Por padrão, ele retornará até 4MB de conteúdo de log.</span><span class="sxs-lookup"><span data-stu-id="ded9a-116">By default, it will return up to 4MB log content.</span></span>

### <span data-ttu-id="ded9a-117">Exemplo 3: obter a cauda 2 linhas de log de uma instância de contêiner</span><span class="sxs-lookup"><span data-stu-id="ded9a-117">Example 3: Get the tail 2 lines of log of a container instance</span></span>
```
PS C:\> Get-AzureRmContainerInstanceLog -ResourceGroupName demo -ContainerGroupName mycontainer -Name container1 -Tail 2

Log line 3.
Log line 4.
```

<span data-ttu-id="ded9a-118">Obter as linhas caudais 2 de log a partir do `container1` grupo de contêineres `mycontainer` .</span><span class="sxs-lookup"><span data-stu-id="ded9a-118">Get the tail 2 lines of log from `container1` in container group `mycontainer`.</span></span>

### <span data-ttu-id="ded9a-119">Exemplo 4: obter o log final de uma instância de contêiner em um grupo canalizado em um grupo de contêineres</span><span class="sxs-lookup"><span data-stu-id="ded9a-119">Example 4: Get the tail log of a container instance in a piped in container group</span></span>
```
PS C:\> Get-AzureRmContainerGroup -ResourceGroupName demo -Name mycontainer | Get-AzureRmContainerInstanceLog

Log line 1.
Log line 2.
Log line 3.
Log line 4.
```

<span data-ttu-id="ded9a-120">Obter o log de `mycontainer` em piped no grupo de contêineres `mycontainer` .</span><span class="sxs-lookup"><span data-stu-id="ded9a-120">Get the log from `mycontainer` in piped in container group `mycontainer`.</span></span> <span data-ttu-id="ded9a-121">Por padrão, ele retornará até 4MB de conteúdo de log.</span><span class="sxs-lookup"><span data-stu-id="ded9a-121">By default, it will return up to 4MB log content.</span></span>

## <span data-ttu-id="ded9a-122">OS</span><span class="sxs-lookup"><span data-stu-id="ded9a-122">PARAMETERS</span></span>

### <span data-ttu-id="ded9a-123">-ContainerGroupName</span><span class="sxs-lookup"><span data-stu-id="ded9a-123">-ContainerGroupName</span></span>
<span data-ttu-id="ded9a-124">O nome do grupo de contêineres.</span><span class="sxs-lookup"><span data-stu-id="ded9a-124">The container group name.</span></span>

```yaml
Type: String
Parameter Sets: GetContainerInstanceLogByNamesParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ded9a-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ded9a-125">-DefaultProfile</span></span>
<span data-ttu-id="ded9a-126">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ded9a-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ded9a-127">-InputContainerGroup</span><span class="sxs-lookup"><span data-stu-id="ded9a-127">-InputContainerGroup</span></span>
<span data-ttu-id="ded9a-128">Objeto do grupo de contêineres de entrada.</span><span class="sxs-lookup"><span data-stu-id="ded9a-128">The input container group object.</span></span>

```yaml
Type: PSContainerGroup
Parameter Sets: GetContainerInstanceLogByPSContainerGroupParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ded9a-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="ded9a-129">-Name</span></span>
<span data-ttu-id="ded9a-130">O nome da instância do contêiner no grupo contêiner.</span><span class="sxs-lookup"><span data-stu-id="ded9a-130">The container instance name in the container group.</span></span>
<span data-ttu-id="ded9a-131">Padrão: o mesmo que o nome do grupo de contêineres</span><span class="sxs-lookup"><span data-stu-id="ded9a-131">Default: the same as the container group name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ded9a-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ded9a-132">-ResourceGroupName</span></span>
<span data-ttu-id="ded9a-133">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ded9a-133">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: GetContainerInstanceLogByNamesParamSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ded9a-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ded9a-134">-ResourceId</span></span>
<span data-ttu-id="ded9a-135">A ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="ded9a-135">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: GetContainerInstanceLogByResourceIdParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ded9a-136">-Caudal</span><span class="sxs-lookup"><span data-stu-id="ded9a-136">-Tail</span></span>
<span data-ttu-id="ded9a-137">O número de linhas a serem caudadas no log.</span><span class="sxs-lookup"><span data-stu-id="ded9a-137">The number of lines to tail the log.</span></span>
<span data-ttu-id="ded9a-138">Se não for especificado, o cmdlet retornará até 4MB de log com cauda</span><span class="sxs-lookup"><span data-stu-id="ded9a-138">If not specify, the cmdlet will return up to 4MB tailed log</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ded9a-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ded9a-139">CommonParameters</span></span>
<span data-ttu-id="ded9a-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ded9a-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ded9a-141">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ded9a-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ded9a-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ded9a-142">INPUTS</span></span>

### <span data-ttu-id="ded9a-143">Microsoft. Azure. Commands. ContainerInstance. Models. PSContainerGroup</span><span class="sxs-lookup"><span data-stu-id="ded9a-143">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span></span>

## <span data-ttu-id="ded9a-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ded9a-144">OUTPUTS</span></span>

### <span data-ttu-id="ded9a-145">System. String</span><span class="sxs-lookup"><span data-stu-id="ded9a-145">System.String</span></span>

## <span data-ttu-id="ded9a-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ded9a-146">NOTES</span></span>

## <span data-ttu-id="ded9a-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ded9a-147">RELATED LINKS</span></span>
