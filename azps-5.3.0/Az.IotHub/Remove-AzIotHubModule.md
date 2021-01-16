---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubModule.md
ms.openlocfilehash: 3362fd6b1e60fa975277c97ea76a8e8c15ee29a4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98272815"
---
# <span data-ttu-id="44510-101">Remove-AzIotHubModule</span><span class="sxs-lookup"><span data-stu-id="44510-101">Remove-AzIotHubModule</span></span>

## <span data-ttu-id="44510-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="44510-102">SYNOPSIS</span></span>
<span data-ttu-id="44510-103">Excluir módulo (s) em um dispositivo IoT de destino em um hub IoT.</span><span class="sxs-lookup"><span data-stu-id="44510-103">Delete module(s) on a target IoT device in an IoT Hub.</span></span>

## <span data-ttu-id="44510-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="44510-104">SYNTAX</span></span>

### <span data-ttu-id="44510-105">ResourceSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="44510-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubModule [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-ModuleId <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="44510-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="44510-106">InputObjectSet</span></span>
```
Remove-AzIotHubModule [-InputObject] <PSIotHub> [-DeviceId] <String> [-ModuleId <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="44510-107">ResourceSet</span><span class="sxs-lookup"><span data-stu-id="44510-107">ResourceIdSet</span></span>
```
Remove-AzIotHubModule [-ResourceId] <String> [-DeviceId] <String> [-ModuleId <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="44510-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="44510-108">DESCRIPTION</span></span>
<span data-ttu-id="44510-109">Excluir módulo (s) em um dispositivo IoT de destino em um hub IoT.</span><span class="sxs-lookup"><span data-stu-id="44510-109">Delete module(s) on a target IoT device in an IoT Hub.</span></span>

## <span data-ttu-id="44510-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="44510-110">EXAMPLES</span></span>

### <span data-ttu-id="44510-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="44510-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzIotHubModule -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1" -PassThru

True
```

<span data-ttu-id="44510-112">Excluir um módulo de dispositivo IOT.</span><span class="sxs-lookup"><span data-stu-id="44510-112">Delete an Iot device module.</span></span>

### <span data-ttu-id="44510-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="44510-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzIotHubModule -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -PassThru

True
```

<span data-ttu-id="44510-114">Exclua todos os módulos de dispositivo IOT.</span><span class="sxs-lookup"><span data-stu-id="44510-114">Delete all Iot device modules.</span></span>

## <span data-ttu-id="44510-115">OS</span><span class="sxs-lookup"><span data-stu-id="44510-115">PARAMETERS</span></span>

### <span data-ttu-id="44510-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44510-116">-DefaultProfile</span></span>
<span data-ttu-id="44510-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="44510-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="44510-118">-DeviceID</span><span class="sxs-lookup"><span data-stu-id="44510-118">-DeviceId</span></span>
<span data-ttu-id="44510-119">ID do dispositivo de destino.</span><span class="sxs-lookup"><span data-stu-id="44510-119">Target Device Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44510-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="44510-120">-InputObject</span></span>
<span data-ttu-id="44510-121">Objeto IotHub</span><span class="sxs-lookup"><span data-stu-id="44510-121">IotHub object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="44510-122">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="44510-122">-IotHubName</span></span>
<span data-ttu-id="44510-123">Nome do Hub IOT</span><span class="sxs-lookup"><span data-stu-id="44510-123">Name of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44510-124">-ModuleID</span><span class="sxs-lookup"><span data-stu-id="44510-124">-ModuleId</span></span>
<span data-ttu-id="44510-125">ID do módulo de destino.</span><span class="sxs-lookup"><span data-stu-id="44510-125">Target Module Id.</span></span>

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

### <span data-ttu-id="44510-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="44510-126">-PassThru</span></span>
<span data-ttu-id="44510-127">Permite retornar o objeto booliano.</span><span class="sxs-lookup"><span data-stu-id="44510-127">Allows to return the boolean object.</span></span>
<span data-ttu-id="44510-128">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="44510-128">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44510-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44510-129">-ResourceGroupName</span></span>
<span data-ttu-id="44510-130">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="44510-130">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44510-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="44510-131">-ResourceId</span></span>
<span data-ttu-id="44510-132">ID do recurso IotHub</span><span class="sxs-lookup"><span data-stu-id="44510-132">IotHub Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44510-133">-Confirme</span><span class="sxs-lookup"><span data-stu-id="44510-133">-Confirm</span></span>
<span data-ttu-id="44510-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="44510-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="44510-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="44510-135">-WhatIf</span></span>
<span data-ttu-id="44510-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="44510-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="44510-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="44510-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="44510-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44510-138">CommonParameters</span></span>
<span data-ttu-id="44510-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="44510-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44510-140">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="44510-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44510-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="44510-141">INPUTS</span></span>

### <span data-ttu-id="44510-142">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="44510-142">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="44510-143">System. String</span><span class="sxs-lookup"><span data-stu-id="44510-143">System.String</span></span>

## <span data-ttu-id="44510-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="44510-144">OUTPUTS</span></span>

### <span data-ttu-id="44510-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="44510-145">System.Boolean</span></span>

## <span data-ttu-id="44510-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="44510-146">NOTES</span></span>

## <span data-ttu-id="44510-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="44510-147">RELATED LINKS</span></span>
