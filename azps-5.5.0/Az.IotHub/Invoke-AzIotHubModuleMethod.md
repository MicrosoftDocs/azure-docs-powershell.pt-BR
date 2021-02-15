---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/invoke-aziothubmodulemethod
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubModuleMethod.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubModuleMethod.md
ms.openlocfilehash: e9faa07f4addabcb556819e1d45b63a0dec0f6b3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111860"
---
# <span data-ttu-id="d959b-101">Invoke-AzIotHubModuleMethod</span><span class="sxs-lookup"><span data-stu-id="d959b-101">Invoke-AzIotHubModuleMethod</span></span>

## <span data-ttu-id="d959b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d959b-102">SYNOPSIS</span></span>
<span data-ttu-id="d959b-103">Invocar um método de módulo do Edge.</span><span class="sxs-lookup"><span data-stu-id="d959b-103">Invoke an Edge module method.</span></span>

## <span data-ttu-id="d959b-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d959b-104">SYNTAX</span></span>

### <span data-ttu-id="d959b-105">ResourceSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="d959b-105">ResourceSet (Default)</span></span>
```
Invoke-AzIotHubModuleMethod [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-ModuleId] <String> -Name <String> [-Payload <String>] [-ResponseTimeOut <Int32>]
 [-ConnectionTimeOut <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d959b-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="d959b-106">InputObjectSet</span></span>
```
Invoke-AzIotHubModuleMethod [-InputObject] <PSIotHub> [-DeviceId] <String> [-ModuleId] <String> -Name <String>
 [-Payload <String>] [-ResponseTimeOut <Int32>] [-ConnectionTimeOut <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d959b-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="d959b-107">ResourceIdSet</span></span>
```
Invoke-AzIotHubModuleMethod [-ResourceId] <String> [-DeviceId] <String> [-ModuleId] <String> -Name <String>
 [-Payload <String>] [-ResponseTimeOut <Int32>] [-ConnectionTimeOut <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d959b-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="d959b-108">DESCRIPTION</span></span>
<span data-ttu-id="d959b-109">Invocar um método de módulo do Edge.</span><span class="sxs-lookup"><span data-stu-id="d959b-109">Invoke an Edge module method.</span></span> <span data-ttu-id="d959b-110">Confira https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-direct-methods mais informações.</span><span class="sxs-lookup"><span data-stu-id="d959b-110">See https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-direct-methods for more information.</span></span>

## <span data-ttu-id="d959b-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="d959b-111">EXAMPLES</span></span>

### <span data-ttu-id="d959b-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d959b-112">Example 1</span></span>
```powershell
PS C:\> Invoke-AzIotHubModuleMethod -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1" -Name "methodName" -Payload "method-input" -ResponseTimeOut 20 -ConnectionTimeOut 15
```

<span data-ttu-id="d959b-113">Invocar um método de módulo do Edge.</span><span class="sxs-lookup"><span data-stu-id="d959b-113">Invoke an Edge module method.</span></span>

## <span data-ttu-id="d959b-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d959b-114">PARAMETERS</span></span>

### <span data-ttu-id="d959b-115">-ConnectionTimeOut</span><span class="sxs-lookup"><span data-stu-id="d959b-115">-ConnectionTimeOut</span></span>
<span data-ttu-id="d959b-116">Número de segundos para aguardar até que uma conexão seja feita com êxito.</span><span class="sxs-lookup"><span data-stu-id="d959b-116">Number of seconds to wait until a connection is successfully made.</span></span>
<span data-ttu-id="d959b-117">O padrão é 10.</span><span class="sxs-lookup"><span data-stu-id="d959b-117">Default is 10.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d959b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d959b-118">-DefaultProfile</span></span>
<span data-ttu-id="d959b-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d959b-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d959b-120">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="d959b-120">-DeviceId</span></span>
<span data-ttu-id="d959b-121">ID do Dispositivo de Destino.</span><span class="sxs-lookup"><span data-stu-id="d959b-121">Target Device Id.</span></span>

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

### <span data-ttu-id="d959b-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d959b-122">-InputObject</span></span>
<span data-ttu-id="d959b-123">Objeto IotHub</span><span class="sxs-lookup"><span data-stu-id="d959b-123">IotHub object</span></span>

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

### <span data-ttu-id="d959b-124">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="d959b-124">-IotHubName</span></span>
<span data-ttu-id="d959b-125">Nome do Hub de Iot</span><span class="sxs-lookup"><span data-stu-id="d959b-125">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="d959b-126">-ModuleId</span><span class="sxs-lookup"><span data-stu-id="d959b-126">-ModuleId</span></span>
<span data-ttu-id="d959b-127">ID do módulo do dispositivo de destino.</span><span class="sxs-lookup"><span data-stu-id="d959b-127">Target device's module id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d959b-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="d959b-128">-Name</span></span>
<span data-ttu-id="d959b-129">O nome do método a ser invocado neste módulo de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d959b-129">The name of the method to invoke on this device module.</span></span>

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

### <span data-ttu-id="d959b-130">-Carga</span><span class="sxs-lookup"><span data-stu-id="d959b-130">-Payload</span></span>
<span data-ttu-id="d959b-131">A carga do método a ser invocado neste módulo de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d959b-131">The payload for the method to invoke on this device module.</span></span>

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

### <span data-ttu-id="d959b-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d959b-132">-ResourceGroupName</span></span>
<span data-ttu-id="d959b-133">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="d959b-133">Name of the Resource Group</span></span>

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

### <span data-ttu-id="d959b-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d959b-134">-ResourceId</span></span>
<span data-ttu-id="d959b-135">ID de Recurso do IotHub</span><span class="sxs-lookup"><span data-stu-id="d959b-135">IotHub Resource Id</span></span>

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

### <span data-ttu-id="d959b-136">-ResponseTimeOut</span><span class="sxs-lookup"><span data-stu-id="d959b-136">-ResponseTimeOut</span></span>
<span data-ttu-id="d959b-137">Número de segundos para aguardar até que um resultado seja recebido do método direto.</span><span class="sxs-lookup"><span data-stu-id="d959b-137">Number of seconds to wait until a result is received from the direct method.</span></span>
<span data-ttu-id="d959b-138">O padrão é 10.</span><span class="sxs-lookup"><span data-stu-id="d959b-138">Default is 10.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d959b-139">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="d959b-139">-Confirm</span></span>
<span data-ttu-id="d959b-140">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d959b-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d959b-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d959b-141">-WhatIf</span></span>
<span data-ttu-id="d959b-142">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="d959b-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d959b-143">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d959b-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d959b-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d959b-144">CommonParameters</span></span>
<span data-ttu-id="d959b-145">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d959b-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d959b-146">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d959b-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d959b-147">Entradas</span><span class="sxs-lookup"><span data-stu-id="d959b-147">INPUTS</span></span>

### <span data-ttu-id="d959b-148">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="d959b-148">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="d959b-149">System.String</span><span class="sxs-lookup"><span data-stu-id="d959b-149">System.String</span></span>

## <span data-ttu-id="d959b-150">Saídas</span><span class="sxs-lookup"><span data-stu-id="d959b-150">OUTPUTS</span></span>

### <span data-ttu-id="d959b-151">Microsoft.Azure.Commands.Management.IotHub.Models.PSCloudToDeviceMethodResult</span><span class="sxs-lookup"><span data-stu-id="d959b-151">Microsoft.Azure.Commands.Management.IotHub.Models.PSCloudToDeviceMethodResult</span></span>

## <span data-ttu-id="d959b-152">Notas</span><span class="sxs-lookup"><span data-stu-id="d959b-152">NOTES</span></span>

## <span data-ttu-id="d959b-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d959b-153">RELATED LINKS</span></span>
