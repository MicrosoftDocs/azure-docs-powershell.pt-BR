---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/update-aziothubdevicetwin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Update-AzIotHubDeviceTwin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Update-AzIotHubDeviceTwin.md
ms.openlocfilehash: 451f809687ea768800f0e9e33ef4c5af9c425150
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113114"
---
# <span data-ttu-id="99d51-101">Update-AzIotHubDeviceTwin</span><span class="sxs-lookup"><span data-stu-id="99d51-101">Update-AzIotHubDeviceTwin</span></span>

## <span data-ttu-id="99d51-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="99d51-102">SYNOPSIS</span></span>
<span data-ttu-id="99d51-103">Atualiza as marcas e as propriedades desejadas de um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="99d51-103">Updates tags and desired properties of a device twin.</span></span>

## <span data-ttu-id="99d51-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="99d51-104">SYNTAX</span></span>

### <span data-ttu-id="99d51-105">ResourceSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="99d51-105">ResourceSet (Default)</span></span>
```
Update-AzIotHubDeviceTwin [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-Tag <Hashtable>] [-Desired <Hashtable>] [-Partial] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="99d51-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="99d51-106">InputObjectSet</span></span>
```
Update-AzIotHubDeviceTwin [-InputObject] <PSIotHub> [-DeviceId] <String> [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-Partial] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="99d51-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="99d51-107">ResourceIdSet</span></span>
```
Update-AzIotHubDeviceTwin [-ResourceId] <String> [-DeviceId] <String> [-Tag <Hashtable>] [-Desired <Hashtable>]
 [-Partial] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="99d51-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="99d51-108">DESCRIPTION</span></span>
<span data-ttu-id="99d51-109">Atualiza ou substitui um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="99d51-109">Updates or replaces a device twin.</span></span> <span data-ttu-id="99d51-110">Confira https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-device-twins mais informações.</span><span class="sxs-lookup"><span data-stu-id="99d51-110">See https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-device-twins for more information.</span></span>

## <span data-ttu-id="99d51-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="99d51-111">EXAMPLES</span></span>

### <span data-ttu-id="99d51-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="99d51-112">Example 1</span></span>
```powershell
PS C:\> Update-AzIotHubDeviceTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Tag $updatedTag -Desired $updatedDesired -Partial
```

<span data-ttu-id="99d51-113">Retorna o objeto de brilho do dispositivo atualizado.</span><span class="sxs-lookup"><span data-stu-id="99d51-113">Returns the updated device twin object.</span></span>

### <span data-ttu-id="99d51-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="99d51-114">Example 2</span></span>
```powershell
PS C:\> Update-AzIotHubDeviceTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Desired $updatedDesired -Partial
```

<span data-ttu-id="99d51-115">Retorna o objeto de brilho do dispositivo com as propriedades desejadas atualizadas.</span><span class="sxs-lookup"><span data-stu-id="99d51-115">Returns the device twin object with updated desired properties.</span></span>

### <span data-ttu-id="99d51-116">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="99d51-116">Example 3</span></span>
```powershell
PS C:\> Update-AzIotHubDeviceTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Tag $updatedTag -Partial
```

<span data-ttu-id="99d51-117">Retorna o objeto de brilho do dispositivo com a propriedade de marcas atualizadas.</span><span class="sxs-lookup"><span data-stu-id="99d51-117">Returns the device twin object with updated tags property.</span></span>

### <span data-ttu-id="99d51-118">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="99d51-118">Example 4</span></span>
```powershell
PS C:\> $updatedTag = @{}
PS C:\> $updatedTag.add("key0","value0")
PS C:\> $updatedDesired =@{}
PS C:\> $updatedDesired.add("desiredkey","desiredvalue")
PS C:\> Update-AzIotHubDeviceTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Tag $updatedTag -Desired $updatedDesired
```

<span data-ttu-id="99d51-119">Retorna o objeto de brilho do dispositivo substituído.</span><span class="sxs-lookup"><span data-stu-id="99d51-119">Returns the replaced device twin object.</span></span>

## <span data-ttu-id="99d51-120">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="99d51-120">PARAMETERS</span></span>

### <span data-ttu-id="99d51-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99d51-121">-DefaultProfile</span></span>
<span data-ttu-id="99d51-122">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="99d51-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="99d51-123">-Desejado</span><span class="sxs-lookup"><span data-stu-id="99d51-123">-Desired</span></span>
<span data-ttu-id="99d51-124">Adicione ou atualize a propriedade desejada em um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="99d51-124">Add or update the desired property in a device twin.</span></span>

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

### <span data-ttu-id="99d51-125">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="99d51-125">-DeviceId</span></span>
<span data-ttu-id="99d51-126">ID do Dispositivo de Destino.</span><span class="sxs-lookup"><span data-stu-id="99d51-126">Target Device Id.</span></span>

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

### <span data-ttu-id="99d51-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="99d51-127">-InputObject</span></span>
<span data-ttu-id="99d51-128">Objeto IotHub</span><span class="sxs-lookup"><span data-stu-id="99d51-128">IotHub object</span></span>

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

### <span data-ttu-id="99d51-129">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="99d51-129">-IotHubName</span></span>
<span data-ttu-id="99d51-130">Nome do Hub de Iot</span><span class="sxs-lookup"><span data-stu-id="99d51-130">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="99d51-131">-Parcial</span><span class="sxs-lookup"><span data-stu-id="99d51-131">-Partial</span></span>
<span data-ttu-id="99d51-132">Permite atualizar parcialmente as marcas e as propriedades desejadas de um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="99d51-132">Allows to only partially update the tags and desired properties of a device twin.</span></span>

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

### <span data-ttu-id="99d51-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99d51-133">-ResourceGroupName</span></span>
<span data-ttu-id="99d51-134">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="99d51-134">Name of the Resource Group</span></span>

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

### <span data-ttu-id="99d51-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="99d51-135">-ResourceId</span></span>
<span data-ttu-id="99d51-136">ID de Recurso do IotHub</span><span class="sxs-lookup"><span data-stu-id="99d51-136">IotHub Resource Id</span></span>

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

### <span data-ttu-id="99d51-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="99d51-137">-Tag</span></span>
<span data-ttu-id="99d51-138">Adicione ou atualize a propriedade de marcas em um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="99d51-138">Add or update the tags property in a device twin.</span></span>

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

### <span data-ttu-id="99d51-139">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="99d51-139">-Confirm</span></span>
<span data-ttu-id="99d51-140">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="99d51-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="99d51-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="99d51-141">-WhatIf</span></span>
<span data-ttu-id="99d51-142">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="99d51-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="99d51-143">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="99d51-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="99d51-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99d51-144">CommonParameters</span></span>
<span data-ttu-id="99d51-145">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99d51-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99d51-146">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="99d51-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99d51-147">Entradas</span><span class="sxs-lookup"><span data-stu-id="99d51-147">INPUTS</span></span>

### <span data-ttu-id="99d51-148">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="99d51-148">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="99d51-149">System.String</span><span class="sxs-lookup"><span data-stu-id="99d51-149">System.String</span></span>

## <span data-ttu-id="99d51-150">Saídas</span><span class="sxs-lookup"><span data-stu-id="99d51-150">OUTPUTS</span></span>

### <span data-ttu-id="99d51-151">System.String</span><span class="sxs-lookup"><span data-stu-id="99d51-151">System.String</span></span>

## <span data-ttu-id="99d51-152">Notas</span><span class="sxs-lookup"><span data-stu-id="99d51-152">NOTES</span></span>

## <span data-ttu-id="99d51-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="99d51-153">RELATED LINKS</span></span>
