---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/new-aziothubsastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHubSasToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHubSasToken.md
ms.openlocfilehash: 486ca6543bb32d096e454d16ff3640720f2f53fe
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116741"
---
# <span data-ttu-id="ebc9c-101">New-AzIotHubSasToken</span><span class="sxs-lookup"><span data-stu-id="ebc9c-101">New-AzIotHubSasToken</span></span>

## <span data-ttu-id="ebc9c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ebc9c-102">SYNOPSIS</span></span>
<span data-ttu-id="ebc9c-103">Gere um token SAS para um Hub de IoT de destino, dispositivo ou módulo.</span><span class="sxs-lookup"><span data-stu-id="ebc9c-103">Generate a SAS token for a target IoT Hub, device or module.</span></span>

## <span data-ttu-id="ebc9c-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ebc9c-104">SYNTAX</span></span>

### <span data-ttu-id="ebc9c-105">ResourceSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="ebc9c-105">ResourceSet (Default)</span></span>
```
New-AzIotHubSasToken [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId <String>]
 [-ModuleId <String>] [-KeyName <String>] [-KeyType <PSKeyType>] [-Duration <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ebc9c-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="ebc9c-106">InputObjectSet</span></span>
```
New-AzIotHubSasToken [-InputObject] <PSIotHub> [-DeviceId <String>] [-ModuleId <String>] [-KeyName <String>]
 [-KeyType <PSKeyType>] [-Duration <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ebc9c-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="ebc9c-107">ResourceIdSet</span></span>
```
New-AzIotHubSasToken [-ResourceId] <String> [-DeviceId <String>] [-ModuleId <String>] [-KeyName <String>]
 [-KeyType <PSKeyType>] [-Duration <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ebc9c-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="ebc9c-108">DESCRIPTION</span></span>
<span data-ttu-id="ebc9c-109">Para tokens SAS de dispositivo, o parâmetro de política é usado para acessar apenas o registro de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ebc9c-109">For device SAS tokens, the policy parameter is used to access the the device registry only.</span></span> <span data-ttu-id="ebc9c-110">Portanto, a política deve ter acesso de leitura ao registro.</span><span class="sxs-lookup"><span data-stu-id="ebc9c-110">Therefore the policy should have read access to the registry.</span></span>
<span data-ttu-id="ebc9c-111">Para tokens do Hub IoT, a política faz parte do SAS.</span><span class="sxs-lookup"><span data-stu-id="ebc9c-111">For IoT Hub tokens the policy is part of the SAS.</span></span>

## <span data-ttu-id="ebc9c-112">Exemplos</span><span class="sxs-lookup"><span data-stu-id="ebc9c-112">EXAMPLES</span></span>

### <span data-ttu-id="ebc9c-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ebc9c-113">Example 1</span></span>
```powershell
PS C:\> New-AzIotHubSasToken -ResourceGroupName "myresourcegroup" -IotHubName "myiothub"
```

<span data-ttu-id="ebc9c-114">Gere um token SAS do Hub IoT usando a política iothuvitner e a chave primária.</span><span class="sxs-lookup"><span data-stu-id="ebc9c-114">Generate an IoT Hub SAS token using the iothubowner policy and primary key.</span></span>

### <span data-ttu-id="ebc9c-115">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="ebc9c-115">Example 2</span></span>
```powershell
PS C:\> New-AzIotHubSasToken -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -KeyName "registryRead" -KeyType "secondary"
```

<span data-ttu-id="ebc9c-116">Gere um token SAS do Hub IoT usando a política registryRead e a chave secundária.</span><span class="sxs-lookup"><span data-stu-id="ebc9c-116">Generate an IoT Hub SAS token using the registryRead policy and secondary key.</span></span>

### <span data-ttu-id="ebc9c-117">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="ebc9c-117">Example 3</span></span>
```powershell
PS C:\> New-AzIotHubSasToken -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1"
```

<span data-ttu-id="ebc9c-118">Gere um token SAS de dispositivo usando a política iothu bowlner para acessar o registro de dispositivo {iothub_name}.</span><span class="sxs-lookup"><span data-stu-id="ebc9c-118">Generate a device SAS token using the iothubowner policy to access the {iothub_name} device registry.</span></span>

### <span data-ttu-id="ebc9c-119">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="ebc9c-119">Example 4</span></span>
```powershell
PS C:\> New-AzIotHubSasToken -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1"
```

<span data-ttu-id="ebc9c-120">Gere um token SAS de módulo usando a política iothu bowlner para acessar o registro de dispositivos {iothub_name}.</span><span class="sxs-lookup"><span data-stu-id="ebc9c-120">Generate a module SAS token using the iothubowner policy to access the {iothub_name} device registry.</span></span>

## <span data-ttu-id="ebc9c-121">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ebc9c-121">PARAMETERS</span></span>

### <span data-ttu-id="ebc9c-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ebc9c-122">-DefaultProfile</span></span>
<span data-ttu-id="ebc9c-123">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ebc9c-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ebc9c-124">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="ebc9c-124">-DeviceId</span></span>
<span data-ttu-id="ebc9c-125">ID do Dispositivo de Destino.</span><span class="sxs-lookup"><span data-stu-id="ebc9c-125">Target Device Id.</span></span>

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

### <span data-ttu-id="ebc9c-126">-Duração</span><span class="sxs-lookup"><span data-stu-id="ebc9c-126">-Duration</span></span>
<span data-ttu-id="ebc9c-127">Expiração futura (em segundos) do token a ser gerado.</span><span class="sxs-lookup"><span data-stu-id="ebc9c-127">Future expiry (in seconds) of the token to be generated.</span></span>
<span data-ttu-id="ebc9c-128">O padrão é 3600.</span><span class="sxs-lookup"><span data-stu-id="ebc9c-128">Default is 3600.</span></span>

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

### <span data-ttu-id="ebc9c-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ebc9c-129">-InputObject</span></span>
<span data-ttu-id="ebc9c-130">Objeto IotHub</span><span class="sxs-lookup"><span data-stu-id="ebc9c-130">IotHub object</span></span>

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

### <span data-ttu-id="ebc9c-131">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="ebc9c-131">-IotHubName</span></span>
<span data-ttu-id="ebc9c-132">Nome do Hub de Iot</span><span class="sxs-lookup"><span data-stu-id="ebc9c-132">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="ebc9c-133">-KeyName</span><span class="sxs-lookup"><span data-stu-id="ebc9c-133">-KeyName</span></span>
<span data-ttu-id="ebc9c-134">Nome da chave do Access.</span><span class="sxs-lookup"><span data-stu-id="ebc9c-134">Access key name.</span></span>

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

### <span data-ttu-id="ebc9c-135">-KeyType</span><span class="sxs-lookup"><span data-stu-id="ebc9c-135">-KeyType</span></span>
<span data-ttu-id="ebc9c-136">Tipo de tecla do Access.</span><span class="sxs-lookup"><span data-stu-id="ebc9c-136">Access key type.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSKeyType
Parameter Sets: (All)
Aliases:
Accepted values: primary, secondary

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebc9c-137">-ModuleId</span><span class="sxs-lookup"><span data-stu-id="ebc9c-137">-ModuleId</span></span>
<span data-ttu-id="ebc9c-138">ID do Módulo de Destino.</span><span class="sxs-lookup"><span data-stu-id="ebc9c-138">Target Module Id.</span></span>

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

### <span data-ttu-id="ebc9c-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ebc9c-139">-ResourceGroupName</span></span>
<span data-ttu-id="ebc9c-140">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="ebc9c-140">Name of the Resource Group</span></span>

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

### <span data-ttu-id="ebc9c-141">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ebc9c-141">-ResourceId</span></span>
<span data-ttu-id="ebc9c-142">ID de Recurso do IotHub</span><span class="sxs-lookup"><span data-stu-id="ebc9c-142">IotHub Resource Id</span></span>

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

### <span data-ttu-id="ebc9c-143">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="ebc9c-143">-Confirm</span></span>
<span data-ttu-id="ebc9c-144">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ebc9c-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ebc9c-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ebc9c-145">-WhatIf</span></span>
<span data-ttu-id="ebc9c-146">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="ebc9c-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ebc9c-147">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ebc9c-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ebc9c-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ebc9c-148">CommonParameters</span></span>
<span data-ttu-id="ebc9c-149">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ebc9c-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ebc9c-150">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ebc9c-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ebc9c-151">Entradas</span><span class="sxs-lookup"><span data-stu-id="ebc9c-151">INPUTS</span></span>

### <span data-ttu-id="ebc9c-152">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="ebc9c-152">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="ebc9c-153">System.String</span><span class="sxs-lookup"><span data-stu-id="ebc9c-153">System.String</span></span>

## <span data-ttu-id="ebc9c-154">Saídas</span><span class="sxs-lookup"><span data-stu-id="ebc9c-154">OUTPUTS</span></span>

### <span data-ttu-id="ebc9c-155">System.String</span><span class="sxs-lookup"><span data-stu-id="ebc9c-155">System.String</span></span>

## <span data-ttu-id="ebc9c-156">Notas</span><span class="sxs-lookup"><span data-stu-id="ebc9c-156">NOTES</span></span>

## <span data-ttu-id="ebc9c-157">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ebc9c-157">RELATED LINKS</span></span>
