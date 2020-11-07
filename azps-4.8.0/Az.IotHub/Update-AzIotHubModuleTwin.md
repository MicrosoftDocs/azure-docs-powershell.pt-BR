---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/update-aziothubmoduletwin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Update-AzIotHubModuleTwin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Update-AzIotHubModuleTwin.md
ms.openlocfilehash: fb2b984453f87422d7a5b9ec5d5178ca6b6c55d5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93948233"
---
# <span data-ttu-id="58854-101">Update-AzIotHubModuleTwin</span><span class="sxs-lookup"><span data-stu-id="58854-101">Update-AzIotHubModuleTwin</span></span>

## <span data-ttu-id="58854-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="58854-102">SYNOPSIS</span></span>
<span data-ttu-id="58854-103">Atualiza as marcas e as propriedades desejadas de um módulo de dispositivo IoT.</span><span class="sxs-lookup"><span data-stu-id="58854-103">Updates tags and desired properties of an IoT device module twin.</span></span>

## <span data-ttu-id="58854-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="58854-104">SYNTAX</span></span>

### <span data-ttu-id="58854-105">ResourceSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="58854-105">ResourceSet (Default)</span></span>
```
Update-AzIotHubModuleTwin [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 -ModuleId <String> [-Tag <Hashtable>] [-Desired <Hashtable>] [-Partial]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="58854-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="58854-106">InputObjectSet</span></span>
```
Update-AzIotHubModuleTwin [-InputObject] <PSIotHub> [-DeviceId] <String> -ModuleId <String> [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-Partial] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="58854-107">ResourceSet</span><span class="sxs-lookup"><span data-stu-id="58854-107">ResourceIdSet</span></span>
```
Update-AzIotHubModuleTwin [-ResourceId] <String> [-DeviceId] <String> -ModuleId <String> [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-Partial] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="58854-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="58854-108">DESCRIPTION</span></span>
<span data-ttu-id="58854-109">Atualiza ou substitui um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="58854-109">Updates or replaces a device twin.</span></span> <span data-ttu-id="58854-110">Consulte https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-devguide-module-twins para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="58854-110">See https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-devguide-module-twins for more information.</span></span>

## <span data-ttu-id="58854-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="58854-111">EXAMPLES</span></span>

### <span data-ttu-id="58854-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="58854-112">Example 1</span></span>
```powershell
PS C:\> Update-AzIotHubModuleTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1" -Tag $updatedTag -Desired $updatedDesired -Partial
```

<span data-ttu-id="58854-113">Retorna o objeto atualizado do módulo de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="58854-113">Returns the updated device module twin object.</span></span>

### <span data-ttu-id="58854-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="58854-114">Example 2</span></span>
```powershell
PS C:\> Update-AzIotHubModuleTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1" -Desired $updatedDesired -Partial
```

<span data-ttu-id="58854-115">Retorna o objeto adddevice do módulo com as propriedades desejadas atualizadas.</span><span class="sxs-lookup"><span data-stu-id="58854-115">Returns the device module twin object with updated desired properties.</span></span>

### <span data-ttu-id="58854-116">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="58854-116">Example 3</span></span>
```powershell
PS C:\> Update-AzIotHubModuleTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1" -Tag $updatedTag -Partial
```

<span data-ttu-id="58854-117">Retorna o objeto adddevice do módulo com a propriedade Tags atualizadas.</span><span class="sxs-lookup"><span data-stu-id="58854-117">Returns the device module twin object with updated tags property.</span></span>

### <span data-ttu-id="58854-118">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="58854-118">Example 4</span></span>
```powershell
PS C:\> Update-AzIotHubModuleTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1" -Tag $updatedTag -Desired $updatedDesired
```

<span data-ttu-id="58854-119">Retorna o objeto de módulo de dispositivo de substituição.</span><span class="sxs-lookup"><span data-stu-id="58854-119">Returns the replaced device module twin object.</span></span>

## <span data-ttu-id="58854-120">OS</span><span class="sxs-lookup"><span data-stu-id="58854-120">PARAMETERS</span></span>

### <span data-ttu-id="58854-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58854-121">-DefaultProfile</span></span>
<span data-ttu-id="58854-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="58854-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="58854-123">-Desejado</span><span class="sxs-lookup"><span data-stu-id="58854-123">-Desired</span></span>
<span data-ttu-id="58854-124">Adicione ou atualize a propriedade desejada em um módulo.</span><span class="sxs-lookup"><span data-stu-id="58854-124">Add or update the desired property in a module twin.</span></span>

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

### <span data-ttu-id="58854-125">-DeviceID</span><span class="sxs-lookup"><span data-stu-id="58854-125">-DeviceId</span></span>
<span data-ttu-id="58854-126">ID do dispositivo de destino.</span><span class="sxs-lookup"><span data-stu-id="58854-126">Target Device Id.</span></span>

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

### <span data-ttu-id="58854-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="58854-127">-InputObject</span></span>
<span data-ttu-id="58854-128">Objeto IotHub</span><span class="sxs-lookup"><span data-stu-id="58854-128">IotHub object</span></span>

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

### <span data-ttu-id="58854-129">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="58854-129">-IotHubName</span></span>
<span data-ttu-id="58854-130">Nome do Hub IOT</span><span class="sxs-lookup"><span data-stu-id="58854-130">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="58854-131">-ModuleID</span><span class="sxs-lookup"><span data-stu-id="58854-131">-ModuleId</span></span>
<span data-ttu-id="58854-132">ID do módulo de destino.</span><span class="sxs-lookup"><span data-stu-id="58854-132">Target Module Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58854-133">-Parcial</span><span class="sxs-lookup"><span data-stu-id="58854-133">-Partial</span></span>
<span data-ttu-id="58854-134">Permite apenas atualizar parcialmente as marcas e as propriedades desejadas de um módulo.</span><span class="sxs-lookup"><span data-stu-id="58854-134">Allows to only partially update the tags and desired properties of a module twin.</span></span>

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

### <span data-ttu-id="58854-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58854-135">-ResourceGroupName</span></span>
<span data-ttu-id="58854-136">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="58854-136">Name of the Resource Group</span></span>

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

### <span data-ttu-id="58854-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="58854-137">-ResourceId</span></span>
<span data-ttu-id="58854-138">ID do recurso IotHub</span><span class="sxs-lookup"><span data-stu-id="58854-138">IotHub Resource Id</span></span>

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

### <span data-ttu-id="58854-139">-Marca</span><span class="sxs-lookup"><span data-stu-id="58854-139">-Tag</span></span>
<span data-ttu-id="58854-140">Adicione ou atualize a propriedade Tags em um módulo.</span><span class="sxs-lookup"><span data-stu-id="58854-140">Add or update the tags property in a module twin.</span></span>

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

### <span data-ttu-id="58854-141">-Confirme</span><span class="sxs-lookup"><span data-stu-id="58854-141">-Confirm</span></span>
<span data-ttu-id="58854-142">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="58854-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="58854-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="58854-143">-WhatIf</span></span>
<span data-ttu-id="58854-144">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="58854-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="58854-145">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="58854-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="58854-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58854-146">CommonParameters</span></span>
<span data-ttu-id="58854-147">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58854-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58854-148">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="58854-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58854-149">SENSORES</span><span class="sxs-lookup"><span data-stu-id="58854-149">INPUTS</span></span>

### <span data-ttu-id="58854-150">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="58854-150">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="58854-151">System. String</span><span class="sxs-lookup"><span data-stu-id="58854-151">System.String</span></span>

## <span data-ttu-id="58854-152">EXIBE</span><span class="sxs-lookup"><span data-stu-id="58854-152">OUTPUTS</span></span>

### <span data-ttu-id="58854-153">Microsoft. Azure. Commands. Management. IotHub. Models. PSModuleTwin</span><span class="sxs-lookup"><span data-stu-id="58854-153">Microsoft.Azure.Commands.Management.IotHub.Models.PSModuleTwin</span></span>

## <span data-ttu-id="58854-154">INFORMA</span><span class="sxs-lookup"><span data-stu-id="58854-154">NOTES</span></span>

## <span data-ttu-id="58854-155">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="58854-155">RELATED LINKS</span></span>
