---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/update-aziothubmoduletwin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Update-AzIotHubModuleTwin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Update-AzIotHubModuleTwin.md
ms.openlocfilehash: 72e9b809ac2b2894b34aefeddd17473cc29d9f35
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889275"
---
# <span data-ttu-id="70e04-101">Update-AzIotHubModuleTwin</span><span class="sxs-lookup"><span data-stu-id="70e04-101">Update-AzIotHubModuleTwin</span></span>

## <span data-ttu-id="70e04-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="70e04-102">SYNOPSIS</span></span>
<span data-ttu-id="70e04-103">Atualiza marcas e propriedades desejadas de um módulo de dispositivo IoT duplo.</span><span class="sxs-lookup"><span data-stu-id="70e04-103">Updates tags and desired properties of an IoT device module twin.</span></span>

## <span data-ttu-id="70e04-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="70e04-104">SYNTAX</span></span>

### <span data-ttu-id="70e04-105">ResourceSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="70e04-105">ResourceSet (Default)</span></span>
```
Update-AzIotHubModuleTwin [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 -ModuleId <String> [-Tag <Hashtable>] [-Desired <Hashtable>] [-Partial]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="70e04-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="70e04-106">InputObjectSet</span></span>
```
Update-AzIotHubModuleTwin [-InputObject] <PSIotHub> [-DeviceId] <String> -ModuleId <String> [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-Partial] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="70e04-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="70e04-107">ResourceIdSet</span></span>
```
Update-AzIotHubModuleTwin [-ResourceId] <String> [-DeviceId] <String> -ModuleId <String> [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-Partial] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="70e04-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="70e04-108">DESCRIPTION</span></span>
<span data-ttu-id="70e04-109">Atualiza ou substitui um dispositivo duplo.</span><span class="sxs-lookup"><span data-stu-id="70e04-109">Updates or replaces a device twin.</span></span> <span data-ttu-id="70e04-110">Confira https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-module-twins mais informações.</span><span class="sxs-lookup"><span data-stu-id="70e04-110">See https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-module-twins for more information.</span></span>

## <span data-ttu-id="70e04-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="70e04-111">EXAMPLES</span></span>

### <span data-ttu-id="70e04-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="70e04-112">Example 1</span></span>
```powershell
PS C:\> Update-AzIotHubModuleTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1" -Tag $updatedTag -Desired $updatedDesired -Partial
```

<span data-ttu-id="70e04-113">Retorna o objeto duplo do módulo de dispositivo atualizado.</span><span class="sxs-lookup"><span data-stu-id="70e04-113">Returns the updated device module twin object.</span></span>

### <span data-ttu-id="70e04-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="70e04-114">Example 2</span></span>
```powershell
PS C:\> Update-AzIotHubModuleTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1" -Desired $updatedDesired -Partial
```

<span data-ttu-id="70e04-115">Retorna o objeto duplo do módulo de dispositivo com as propriedades desejadas atualizadas.</span><span class="sxs-lookup"><span data-stu-id="70e04-115">Returns the device module twin object with updated desired properties.</span></span>

### <span data-ttu-id="70e04-116">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="70e04-116">Example 3</span></span>
```powershell
PS C:\> Update-AzIotHubModuleTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1" -Tag $updatedTag -Partial
```

<span data-ttu-id="70e04-117">Retorna o objeto duplo do módulo de dispositivo com a propriedade de marcas atualizadas.</span><span class="sxs-lookup"><span data-stu-id="70e04-117">Returns the device module twin object with updated tags property.</span></span>

### <span data-ttu-id="70e04-118">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="70e04-118">Example 4</span></span>
```powershell
PS C:\> Update-AzIotHubModuleTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1" -Tag $updatedTag -Desired $updatedDesired
```

<span data-ttu-id="70e04-119">Retorna o objeto duplo do módulo de dispositivo substituído.</span><span class="sxs-lookup"><span data-stu-id="70e04-119">Returns the replaced device module twin object.</span></span>

## <span data-ttu-id="70e04-120">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="70e04-120">PARAMETERS</span></span>

### <span data-ttu-id="70e04-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70e04-121">-DefaultProfile</span></span>
<span data-ttu-id="70e04-122">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="70e04-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="70e04-123">-Desired</span><span class="sxs-lookup"><span data-stu-id="70e04-123">-Desired</span></span>
<span data-ttu-id="70e04-124">Adicione ou atualize a propriedade desejada em um módulo duplo.</span><span class="sxs-lookup"><span data-stu-id="70e04-124">Add or update the desired property in a module twin.</span></span>

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

### <span data-ttu-id="70e04-125">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="70e04-125">-DeviceId</span></span>
<span data-ttu-id="70e04-126">ID do dispositivo de destino.</span><span class="sxs-lookup"><span data-stu-id="70e04-126">Target Device Id.</span></span>

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

### <span data-ttu-id="70e04-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="70e04-127">-InputObject</span></span>
<span data-ttu-id="70e04-128">Objeto IotHub</span><span class="sxs-lookup"><span data-stu-id="70e04-128">IotHub object</span></span>

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

### <span data-ttu-id="70e04-129">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="70e04-129">-IotHubName</span></span>
<span data-ttu-id="70e04-130">Nome do Hub de Iot</span><span class="sxs-lookup"><span data-stu-id="70e04-130">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="70e04-131">-ModuleId</span><span class="sxs-lookup"><span data-stu-id="70e04-131">-ModuleId</span></span>
<span data-ttu-id="70e04-132">ID do Módulo de Destino.</span><span class="sxs-lookup"><span data-stu-id="70e04-132">Target Module Id.</span></span>

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

### <span data-ttu-id="70e04-133">-Partial</span><span class="sxs-lookup"><span data-stu-id="70e04-133">-Partial</span></span>
<span data-ttu-id="70e04-134">Permite apenas atualizar parcialmente as marcas e as propriedades desejadas de um módulo duplo.</span><span class="sxs-lookup"><span data-stu-id="70e04-134">Allows to only partially update the tags and desired properties of a module twin.</span></span>

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

### <span data-ttu-id="70e04-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70e04-135">-ResourceGroupName</span></span>
<span data-ttu-id="70e04-136">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="70e04-136">Name of the Resource Group</span></span>

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

### <span data-ttu-id="70e04-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="70e04-137">-ResourceId</span></span>
<span data-ttu-id="70e04-138">Id de Recurso IotHub</span><span class="sxs-lookup"><span data-stu-id="70e04-138">IotHub Resource Id</span></span>

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

### <span data-ttu-id="70e04-139">-Tag</span><span class="sxs-lookup"><span data-stu-id="70e04-139">-Tag</span></span>
<span data-ttu-id="70e04-140">Adicione ou atualize a propriedade tags em um módulo duplo.</span><span class="sxs-lookup"><span data-stu-id="70e04-140">Add or update the tags property in a module twin.</span></span>

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

### <span data-ttu-id="70e04-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="70e04-141">-Confirm</span></span>
<span data-ttu-id="70e04-142">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="70e04-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="70e04-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="70e04-143">-WhatIf</span></span>
<span data-ttu-id="70e04-144">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="70e04-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="70e04-145">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="70e04-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="70e04-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70e04-146">CommonParameters</span></span>
<span data-ttu-id="70e04-147">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="70e04-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70e04-148">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="70e04-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70e04-149">INPUTS</span><span class="sxs-lookup"><span data-stu-id="70e04-149">INPUTS</span></span>

### <span data-ttu-id="70e04-150">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="70e04-150">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="70e04-151">System.String</span><span class="sxs-lookup"><span data-stu-id="70e04-151">System.String</span></span>

## <span data-ttu-id="70e04-152">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="70e04-152">OUTPUTS</span></span>

### <span data-ttu-id="70e04-153">Microsoft.Azure.Commands.Management.IotHub.Models.PSModuleTwin</span><span class="sxs-lookup"><span data-stu-id="70e04-153">Microsoft.Azure.Commands.Management.IotHub.Models.PSModuleTwin</span></span>

## <span data-ttu-id="70e04-154">NOTES</span><span class="sxs-lookup"><span data-stu-id="70e04-154">NOTES</span></span>

## <span data-ttu-id="70e04-155">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="70e04-155">RELATED LINKS</span></span>
