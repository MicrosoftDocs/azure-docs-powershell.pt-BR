---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/update-aziothubmoduletwin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Update-AzIotHubModuleTwin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Update-AzIotHubModuleTwin.md
ms.openlocfilehash: fb2b984453f87422d7a5b9ec5d5178ca6b6c55d5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116729"
---
# <span data-ttu-id="7a6ad-101">Update-AzIotHubModuleTwin</span><span class="sxs-lookup"><span data-stu-id="7a6ad-101">Update-AzIotHubModuleTwin</span></span>

## <span data-ttu-id="7a6ad-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7a6ad-102">SYNOPSIS</span></span>
<span data-ttu-id="7a6ad-103">Atualiza as marcas e as propriedades desejadas de um módulo de dispositivo IoT.</span><span class="sxs-lookup"><span data-stu-id="7a6ad-103">Updates tags and desired properties of an IoT device module twin.</span></span>

## <span data-ttu-id="7a6ad-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7a6ad-104">SYNTAX</span></span>

### <span data-ttu-id="7a6ad-105">ResourceSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="7a6ad-105">ResourceSet (Default)</span></span>
```
Update-AzIotHubModuleTwin [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 -ModuleId <String> [-Tag <Hashtable>] [-Desired <Hashtable>] [-Partial]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7a6ad-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="7a6ad-106">InputObjectSet</span></span>
```
Update-AzIotHubModuleTwin [-InputObject] <PSIotHub> [-DeviceId] <String> -ModuleId <String> [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-Partial] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7a6ad-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="7a6ad-107">ResourceIdSet</span></span>
```
Update-AzIotHubModuleTwin [-ResourceId] <String> [-DeviceId] <String> -ModuleId <String> [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-Partial] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7a6ad-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="7a6ad-108">DESCRIPTION</span></span>
<span data-ttu-id="7a6ad-109">Atualiza ou substitui um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7a6ad-109">Updates or replaces a device twin.</span></span> <span data-ttu-id="7a6ad-110">Confira https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-devguide-module-twins mais informações.</span><span class="sxs-lookup"><span data-stu-id="7a6ad-110">See https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-devguide-module-twins for more information.</span></span>

## <span data-ttu-id="7a6ad-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="7a6ad-111">EXAMPLES</span></span>

### <span data-ttu-id="7a6ad-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="7a6ad-112">Example 1</span></span>
```powershell
PS C:\> Update-AzIotHubModuleTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1" -Tag $updatedTag -Desired $updatedDesired -Partial
```

<span data-ttu-id="7a6ad-113">Retorna o módulo de dispositivo atualizado com o objeto duplo.</span><span class="sxs-lookup"><span data-stu-id="7a6ad-113">Returns the updated device module twin object.</span></span>

### <span data-ttu-id="7a6ad-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="7a6ad-114">Example 2</span></span>
```powershell
PS C:\> Update-AzIotHubModuleTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1" -Desired $updatedDesired -Partial
```

<span data-ttu-id="7a6ad-115">Retorna o módulo do dispositivo com as propriedades desejadas atualizadas.</span><span class="sxs-lookup"><span data-stu-id="7a6ad-115">Returns the device module twin object with updated desired properties.</span></span>

### <span data-ttu-id="7a6ad-116">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="7a6ad-116">Example 3</span></span>
```powershell
PS C:\> Update-AzIotHubModuleTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1" -Tag $updatedTag -Partial
```

<span data-ttu-id="7a6ad-117">Retorna o objeto de módulo de dispositivo com a propriedade de marcas atualizadas.</span><span class="sxs-lookup"><span data-stu-id="7a6ad-117">Returns the device module twin object with updated tags property.</span></span>

### <span data-ttu-id="7a6ad-118">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="7a6ad-118">Example 4</span></span>
```powershell
PS C:\> Update-AzIotHubModuleTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1" -Tag $updatedTag -Desired $updatedDesired
```

<span data-ttu-id="7a6ad-119">Retorna o módulo de dispositivo substituído.</span><span class="sxs-lookup"><span data-stu-id="7a6ad-119">Returns the replaced device module twin object.</span></span>

## <span data-ttu-id="7a6ad-120">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7a6ad-120">PARAMETERS</span></span>

### <span data-ttu-id="7a6ad-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a6ad-121">-DefaultProfile</span></span>
<span data-ttu-id="7a6ad-122">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7a6ad-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7a6ad-123">-Desejado</span><span class="sxs-lookup"><span data-stu-id="7a6ad-123">-Desired</span></span>
<span data-ttu-id="7a6ad-124">Adicione ou atualize a propriedade desejada em um módulo.</span><span class="sxs-lookup"><span data-stu-id="7a6ad-124">Add or update the desired property in a module twin.</span></span>

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

### <span data-ttu-id="7a6ad-125">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="7a6ad-125">-DeviceId</span></span>
<span data-ttu-id="7a6ad-126">ID do Dispositivo de Destino.</span><span class="sxs-lookup"><span data-stu-id="7a6ad-126">Target Device Id.</span></span>

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

### <span data-ttu-id="7a6ad-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7a6ad-127">-InputObject</span></span>
<span data-ttu-id="7a6ad-128">Objeto IotHub</span><span class="sxs-lookup"><span data-stu-id="7a6ad-128">IotHub object</span></span>

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

### <span data-ttu-id="7a6ad-129">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="7a6ad-129">-IotHubName</span></span>
<span data-ttu-id="7a6ad-130">Nome do Hub de Iot</span><span class="sxs-lookup"><span data-stu-id="7a6ad-130">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="7a6ad-131">-ModuleId</span><span class="sxs-lookup"><span data-stu-id="7a6ad-131">-ModuleId</span></span>
<span data-ttu-id="7a6ad-132">ID do Módulo de Destino.</span><span class="sxs-lookup"><span data-stu-id="7a6ad-132">Target Module Id.</span></span>

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

### <span data-ttu-id="7a6ad-133">-Parcial</span><span class="sxs-lookup"><span data-stu-id="7a6ad-133">-Partial</span></span>
<span data-ttu-id="7a6ad-134">Permite atualizar parcialmente as marcas e as propriedades desejadas de um módulo.</span><span class="sxs-lookup"><span data-stu-id="7a6ad-134">Allows to only partially update the tags and desired properties of a module twin.</span></span>

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

### <span data-ttu-id="7a6ad-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a6ad-135">-ResourceGroupName</span></span>
<span data-ttu-id="7a6ad-136">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="7a6ad-136">Name of the Resource Group</span></span>

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

### <span data-ttu-id="7a6ad-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7a6ad-137">-ResourceId</span></span>
<span data-ttu-id="7a6ad-138">ID de Recurso do IotHub</span><span class="sxs-lookup"><span data-stu-id="7a6ad-138">IotHub Resource Id</span></span>

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

### <span data-ttu-id="7a6ad-139">-Tag</span><span class="sxs-lookup"><span data-stu-id="7a6ad-139">-Tag</span></span>
<span data-ttu-id="7a6ad-140">Adicione ou atualize a propriedade de marcas em um módulo.</span><span class="sxs-lookup"><span data-stu-id="7a6ad-140">Add or update the tags property in a module twin.</span></span>

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

### <span data-ttu-id="7a6ad-141">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="7a6ad-141">-Confirm</span></span>
<span data-ttu-id="7a6ad-142">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7a6ad-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7a6ad-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7a6ad-143">-WhatIf</span></span>
<span data-ttu-id="7a6ad-144">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="7a6ad-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7a6ad-145">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7a6ad-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7a6ad-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a6ad-146">CommonParameters</span></span>
<span data-ttu-id="7a6ad-147">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a6ad-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a6ad-148">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7a6ad-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a6ad-149">Entradas</span><span class="sxs-lookup"><span data-stu-id="7a6ad-149">INPUTS</span></span>

### <span data-ttu-id="7a6ad-150">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="7a6ad-150">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="7a6ad-151">System.String</span><span class="sxs-lookup"><span data-stu-id="7a6ad-151">System.String</span></span>

## <span data-ttu-id="7a6ad-152">Saídas</span><span class="sxs-lookup"><span data-stu-id="7a6ad-152">OUTPUTS</span></span>

### <span data-ttu-id="7a6ad-153">Microsoft.Azure.Commands.Management.IotHub.Models.PSModuleTwin</span><span class="sxs-lookup"><span data-stu-id="7a6ad-153">Microsoft.Azure.Commands.Management.IotHub.Models.PSModuleTwin</span></span>

## <span data-ttu-id="7a6ad-154">Notas</span><span class="sxs-lookup"><span data-stu-id="7a6ad-154">NOTES</span></span>

## <span data-ttu-id="7a6ad-155">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7a6ad-155">RELATED LINKS</span></span>
