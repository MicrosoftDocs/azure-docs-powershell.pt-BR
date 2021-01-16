---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/update-aziothubdevicetwin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Update-AzIotHubDeviceTwin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Update-AzIotHubDeviceTwin.md
ms.openlocfilehash: 451f809687ea768800f0e9e33ef4c5af9c425150
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98257756"
---
# <span data-ttu-id="361cc-101">Update-AzIotHubDeviceTwin</span><span class="sxs-lookup"><span data-stu-id="361cc-101">Update-AzIotHubDeviceTwin</span></span>

## <span data-ttu-id="361cc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="361cc-102">SYNOPSIS</span></span>
<span data-ttu-id="361cc-103">Atualiza as marcas e as propriedades desejadas de um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="361cc-103">Updates tags and desired properties of a device twin.</span></span>

## <span data-ttu-id="361cc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="361cc-104">SYNTAX</span></span>

### <span data-ttu-id="361cc-105">ResourceSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="361cc-105">ResourceSet (Default)</span></span>
```
Update-AzIotHubDeviceTwin [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-Tag <Hashtable>] [-Desired <Hashtable>] [-Partial] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="361cc-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="361cc-106">InputObjectSet</span></span>
```
Update-AzIotHubDeviceTwin [-InputObject] <PSIotHub> [-DeviceId] <String> [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-Partial] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="361cc-107">ResourceSet</span><span class="sxs-lookup"><span data-stu-id="361cc-107">ResourceIdSet</span></span>
```
Update-AzIotHubDeviceTwin [-ResourceId] <String> [-DeviceId] <String> [-Tag <Hashtable>] [-Desired <Hashtable>]
 [-Partial] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="361cc-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="361cc-108">DESCRIPTION</span></span>
<span data-ttu-id="361cc-109">Atualiza ou substitui um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="361cc-109">Updates or replaces a device twin.</span></span> <span data-ttu-id="361cc-110">Consulte https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-device-twins para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="361cc-110">See https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-device-twins for more information.</span></span>

## <span data-ttu-id="361cc-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="361cc-111">EXAMPLES</span></span>

### <span data-ttu-id="361cc-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="361cc-112">Example 1</span></span>
```powershell
PS C:\> Update-AzIotHubDeviceTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Tag $updatedTag -Desired $updatedDesired -Partial
```

<span data-ttu-id="361cc-113">Retorna o objeto atualizado do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="361cc-113">Returns the updated device twin object.</span></span>

### <span data-ttu-id="361cc-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="361cc-114">Example 2</span></span>
```powershell
PS C:\> Update-AzIotHubDeviceTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Desired $updatedDesired -Partial
```

<span data-ttu-id="361cc-115">Retorna o objeto adddevice com as propriedades desejadas atualizadas.</span><span class="sxs-lookup"><span data-stu-id="361cc-115">Returns the device twin object with updated desired properties.</span></span>

### <span data-ttu-id="361cc-116">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="361cc-116">Example 3</span></span>
```powershell
PS C:\> Update-AzIotHubDeviceTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Tag $updatedTag -Partial
```

<span data-ttu-id="361cc-117">Retorna o objeto adddevice com a propriedade Tags atualizadas.</span><span class="sxs-lookup"><span data-stu-id="361cc-117">Returns the device twin object with updated tags property.</span></span>

### <span data-ttu-id="361cc-118">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="361cc-118">Example 4</span></span>
```powershell
PS C:\> $updatedTag = @{}
PS C:\> $updatedTag.add("key0","value0")
PS C:\> $updatedDesired =@{}
PS C:\> $updatedDesired.add("desiredkey","desiredvalue")
PS C:\> Update-AzIotHubDeviceTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Tag $updatedTag -Desired $updatedDesired
```

<span data-ttu-id="361cc-119">Retorna o objeto de dispositivo de substituição.</span><span class="sxs-lookup"><span data-stu-id="361cc-119">Returns the replaced device twin object.</span></span>

## <span data-ttu-id="361cc-120">OS</span><span class="sxs-lookup"><span data-stu-id="361cc-120">PARAMETERS</span></span>

### <span data-ttu-id="361cc-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="361cc-121">-DefaultProfile</span></span>
<span data-ttu-id="361cc-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="361cc-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="361cc-123">-Desejado</span><span class="sxs-lookup"><span data-stu-id="361cc-123">-Desired</span></span>
<span data-ttu-id="361cc-124">Adicione ou atualize a propriedade desejada em um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="361cc-124">Add or update the desired property in a device twin.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="361cc-125">-DeviceID</span><span class="sxs-lookup"><span data-stu-id="361cc-125">-DeviceId</span></span>
<span data-ttu-id="361cc-126">ID do dispositivo de destino.</span><span class="sxs-lookup"><span data-stu-id="361cc-126">Target Device Id.</span></span>

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

### <span data-ttu-id="361cc-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="361cc-127">-InputObject</span></span>
<span data-ttu-id="361cc-128">Objeto IotHub</span><span class="sxs-lookup"><span data-stu-id="361cc-128">IotHub object</span></span>

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

### <span data-ttu-id="361cc-129">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="361cc-129">-IotHubName</span></span>
<span data-ttu-id="361cc-130">Nome do Hub IOT</span><span class="sxs-lookup"><span data-stu-id="361cc-130">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="361cc-131">-Parcial</span><span class="sxs-lookup"><span data-stu-id="361cc-131">-Partial</span></span>
<span data-ttu-id="361cc-132">Permite apenas atualizar parcialmente as marcas e as propriedades desejadas de um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="361cc-132">Allows to only partially update the tags and desired properties of a device twin.</span></span>

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

### <span data-ttu-id="361cc-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="361cc-133">-ResourceGroupName</span></span>
<span data-ttu-id="361cc-134">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="361cc-134">Name of the Resource Group</span></span>

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

### <span data-ttu-id="361cc-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="361cc-135">-ResourceId</span></span>
<span data-ttu-id="361cc-136">ID do recurso IotHub</span><span class="sxs-lookup"><span data-stu-id="361cc-136">IotHub Resource Id</span></span>

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

### <span data-ttu-id="361cc-137">-Marca</span><span class="sxs-lookup"><span data-stu-id="361cc-137">-Tag</span></span>
<span data-ttu-id="361cc-138">Adicione ou atualize a propriedade Tags em um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="361cc-138">Add or update the tags property in a device twin.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="361cc-139">-Confirme</span><span class="sxs-lookup"><span data-stu-id="361cc-139">-Confirm</span></span>
<span data-ttu-id="361cc-140">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="361cc-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="361cc-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="361cc-141">-WhatIf</span></span>
<span data-ttu-id="361cc-142">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="361cc-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="361cc-143">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="361cc-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="361cc-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="361cc-144">CommonParameters</span></span>
<span data-ttu-id="361cc-145">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="361cc-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="361cc-146">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="361cc-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="361cc-147">SENSORES</span><span class="sxs-lookup"><span data-stu-id="361cc-147">INPUTS</span></span>

### <span data-ttu-id="361cc-148">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="361cc-148">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="361cc-149">System. String</span><span class="sxs-lookup"><span data-stu-id="361cc-149">System.String</span></span>

## <span data-ttu-id="361cc-150">EXIBE</span><span class="sxs-lookup"><span data-stu-id="361cc-150">OUTPUTS</span></span>

### <span data-ttu-id="361cc-151">System. String</span><span class="sxs-lookup"><span data-stu-id="361cc-151">System.String</span></span>

## <span data-ttu-id="361cc-152">INFORMA</span><span class="sxs-lookup"><span data-stu-id="361cc-152">NOTES</span></span>

## <span data-ttu-id="361cc-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="361cc-153">RELATED LINKS</span></span>
