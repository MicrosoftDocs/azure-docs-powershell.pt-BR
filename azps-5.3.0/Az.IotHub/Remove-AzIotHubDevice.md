---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubdevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubDevice.md
ms.openlocfilehash: 3d137f93c32b77afd29a833086ff5c55823bc104
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98272822"
---
# <span data-ttu-id="019bf-101">Remove-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="019bf-101">Remove-AzIotHubDevice</span></span>

## <span data-ttu-id="019bf-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="019bf-102">SYNOPSIS</span></span>
<span data-ttu-id="019bf-103">Excluir um dispositivo Hub IoT.</span><span class="sxs-lookup"><span data-stu-id="019bf-103">Delete an IoT Hub device.</span></span>

## <span data-ttu-id="019bf-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="019bf-104">SYNTAX</span></span>

### <span data-ttu-id="019bf-105">ResourceSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="019bf-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubDevice [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="019bf-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="019bf-106">InputObjectSet</span></span>
```
Remove-AzIotHubDevice [-InputObject] <PSIotHub> [-DeviceId <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="019bf-107">ResourceSet</span><span class="sxs-lookup"><span data-stu-id="019bf-107">ResourceIdSet</span></span>
```
Remove-AzIotHubDevice [-ResourceId] <String> [-DeviceId <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="019bf-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="019bf-108">DESCRIPTION</span></span>
<span data-ttu-id="019bf-109">Exclua todos os dispositivos ou um dispositivo específico de um hub IOT.</span><span class="sxs-lookup"><span data-stu-id="019bf-109">Delete all devices or a specific device from an Iot Hub.</span></span>

## <span data-ttu-id="019bf-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="019bf-110">EXAMPLES</span></span>

### <span data-ttu-id="019bf-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="019bf-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub"
```

<span data-ttu-id="019bf-112">Exclua todos os dispositivos de Hub IOT.</span><span class="sxs-lookup"><span data-stu-id="019bf-112">Delete all Iot Hub devices.</span></span>

### <span data-ttu-id="019bf-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="019bf-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -PassThru

True
```

<span data-ttu-id="019bf-114">Excluir um dispositivo Hub IOT.</span><span class="sxs-lookup"><span data-stu-id="019bf-114">Delete an Iot Hub device.</span></span>

## <span data-ttu-id="019bf-115">OS</span><span class="sxs-lookup"><span data-stu-id="019bf-115">PARAMETERS</span></span>

### <span data-ttu-id="019bf-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="019bf-116">-DefaultProfile</span></span>
<span data-ttu-id="019bf-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="019bf-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="019bf-118">-DeviceID</span><span class="sxs-lookup"><span data-stu-id="019bf-118">-DeviceId</span></span>
<span data-ttu-id="019bf-119">ID do dispositivo de destino.</span><span class="sxs-lookup"><span data-stu-id="019bf-119">Target Device Id.</span></span>

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

### <span data-ttu-id="019bf-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="019bf-120">-InputObject</span></span>
<span data-ttu-id="019bf-121">Objeto IotHub</span><span class="sxs-lookup"><span data-stu-id="019bf-121">IotHub object</span></span>

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

### <span data-ttu-id="019bf-122">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="019bf-122">-IotHubName</span></span>
<span data-ttu-id="019bf-123">Nome do Hub IOT</span><span class="sxs-lookup"><span data-stu-id="019bf-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="019bf-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="019bf-124">-PassThru</span></span>
<span data-ttu-id="019bf-125">Permite retornar o objeto booliano.</span><span class="sxs-lookup"><span data-stu-id="019bf-125">Allows to return the boolean object.</span></span>
<span data-ttu-id="019bf-126">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="019bf-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="019bf-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="019bf-127">-ResourceGroupName</span></span>
<span data-ttu-id="019bf-128">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="019bf-128">Name of the Resource Group</span></span>

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

### <span data-ttu-id="019bf-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="019bf-129">-ResourceId</span></span>
<span data-ttu-id="019bf-130">ID do recurso IotHub</span><span class="sxs-lookup"><span data-stu-id="019bf-130">IotHub Resource Id</span></span>

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

### <span data-ttu-id="019bf-131">-Confirme</span><span class="sxs-lookup"><span data-stu-id="019bf-131">-Confirm</span></span>
<span data-ttu-id="019bf-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="019bf-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="019bf-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="019bf-133">-WhatIf</span></span>
<span data-ttu-id="019bf-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="019bf-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="019bf-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="019bf-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="019bf-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="019bf-136">CommonParameters</span></span>
<span data-ttu-id="019bf-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="019bf-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="019bf-138">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="019bf-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="019bf-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="019bf-139">INPUTS</span></span>

### <span data-ttu-id="019bf-140">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="019bf-140">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="019bf-141">System. String</span><span class="sxs-lookup"><span data-stu-id="019bf-141">System.String</span></span>

## <span data-ttu-id="019bf-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="019bf-142">OUTPUTS</span></span>

### <span data-ttu-id="019bf-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="019bf-143">System.Boolean</span></span>

## <span data-ttu-id="019bf-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="019bf-144">NOTES</span></span>

## <span data-ttu-id="019bf-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="019bf-145">RELATED LINKS</span></span>
