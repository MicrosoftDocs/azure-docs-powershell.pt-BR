---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubdevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubDevice.md
ms.openlocfilehash: 3d137f93c32b77afd29a833086ff5c55823bc104
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98258653"
---
# <span data-ttu-id="e9c15-101">Remove-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="e9c15-101">Remove-AzIotHubDevice</span></span>

## <span data-ttu-id="e9c15-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e9c15-102">SYNOPSIS</span></span>
<span data-ttu-id="e9c15-103">Excluir um dispositivo Hub IoT.</span><span class="sxs-lookup"><span data-stu-id="e9c15-103">Delete an IoT Hub device.</span></span>

## <span data-ttu-id="e9c15-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e9c15-104">SYNTAX</span></span>

### <span data-ttu-id="e9c15-105">ResourceSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="e9c15-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubDevice [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e9c15-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="e9c15-106">InputObjectSet</span></span>
```
Remove-AzIotHubDevice [-InputObject] <PSIotHub> [-DeviceId <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e9c15-107">ResourceSet</span><span class="sxs-lookup"><span data-stu-id="e9c15-107">ResourceIdSet</span></span>
```
Remove-AzIotHubDevice [-ResourceId] <String> [-DeviceId <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e9c15-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e9c15-108">DESCRIPTION</span></span>
<span data-ttu-id="e9c15-109">Exclua todos os dispositivos ou um dispositivo específico de um hub IOT.</span><span class="sxs-lookup"><span data-stu-id="e9c15-109">Delete all devices or a specific device from an Iot Hub.</span></span>

## <span data-ttu-id="e9c15-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e9c15-110">EXAMPLES</span></span>

### <span data-ttu-id="e9c15-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e9c15-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub"
```

<span data-ttu-id="e9c15-112">Exclua todos os dispositivos de Hub IOT.</span><span class="sxs-lookup"><span data-stu-id="e9c15-112">Delete all Iot Hub devices.</span></span>

### <span data-ttu-id="e9c15-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="e9c15-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -PassThru

True
```

<span data-ttu-id="e9c15-114">Excluir um dispositivo Hub IOT.</span><span class="sxs-lookup"><span data-stu-id="e9c15-114">Delete an Iot Hub device.</span></span>

## <span data-ttu-id="e9c15-115">OS</span><span class="sxs-lookup"><span data-stu-id="e9c15-115">PARAMETERS</span></span>

### <span data-ttu-id="e9c15-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9c15-116">-DefaultProfile</span></span>
<span data-ttu-id="e9c15-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e9c15-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e9c15-118">-DeviceID</span><span class="sxs-lookup"><span data-stu-id="e9c15-118">-DeviceId</span></span>
<span data-ttu-id="e9c15-119">ID do dispositivo de destino.</span><span class="sxs-lookup"><span data-stu-id="e9c15-119">Target Device Id.</span></span>

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

### <span data-ttu-id="e9c15-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e9c15-120">-InputObject</span></span>
<span data-ttu-id="e9c15-121">Objeto IotHub</span><span class="sxs-lookup"><span data-stu-id="e9c15-121">IotHub object</span></span>

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

### <span data-ttu-id="e9c15-122">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="e9c15-122">-IotHubName</span></span>
<span data-ttu-id="e9c15-123">Nome do Hub IOT</span><span class="sxs-lookup"><span data-stu-id="e9c15-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="e9c15-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e9c15-124">-PassThru</span></span>
<span data-ttu-id="e9c15-125">Permite retornar o objeto booliano.</span><span class="sxs-lookup"><span data-stu-id="e9c15-125">Allows to return the boolean object.</span></span>
<span data-ttu-id="e9c15-126">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="e9c15-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e9c15-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e9c15-127">-ResourceGroupName</span></span>
<span data-ttu-id="e9c15-128">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="e9c15-128">Name of the Resource Group</span></span>

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

### <span data-ttu-id="e9c15-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e9c15-129">-ResourceId</span></span>
<span data-ttu-id="e9c15-130">ID do recurso IotHub</span><span class="sxs-lookup"><span data-stu-id="e9c15-130">IotHub Resource Id</span></span>

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

### <span data-ttu-id="e9c15-131">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e9c15-131">-Confirm</span></span>
<span data-ttu-id="e9c15-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e9c15-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e9c15-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e9c15-133">-WhatIf</span></span>
<span data-ttu-id="e9c15-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e9c15-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e9c15-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e9c15-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e9c15-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9c15-136">CommonParameters</span></span>
<span data-ttu-id="e9c15-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e9c15-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9c15-138">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e9c15-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9c15-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e9c15-139">INPUTS</span></span>

### <span data-ttu-id="e9c15-140">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="e9c15-140">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="e9c15-141">System. String</span><span class="sxs-lookup"><span data-stu-id="e9c15-141">System.String</span></span>

## <span data-ttu-id="e9c15-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e9c15-142">OUTPUTS</span></span>

### <span data-ttu-id="e9c15-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e9c15-143">System.Boolean</span></span>

## <span data-ttu-id="e9c15-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e9c15-144">NOTES</span></span>

## <span data-ttu-id="e9c15-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e9c15-145">RELATED LINKS</span></span>
