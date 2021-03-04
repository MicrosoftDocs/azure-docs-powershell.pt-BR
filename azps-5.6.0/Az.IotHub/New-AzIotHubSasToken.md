---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/new-aziothubsastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHubSasToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHubSasToken.md
ms.openlocfilehash: 39b936f6b9ec4bb133ecc6510963207c5e7d96a8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888516"
---
# <span data-ttu-id="62907-101">New-AzIotHubSasToken</span><span class="sxs-lookup"><span data-stu-id="62907-101">New-AzIotHubSasToken</span></span>

## <span data-ttu-id="62907-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="62907-102">SYNOPSIS</span></span>
<span data-ttu-id="62907-103">Gere um token SAS para um Hub de IoT de destino, dispositivo ou módulo.</span><span class="sxs-lookup"><span data-stu-id="62907-103">Generate a SAS token for a target IoT Hub, device or module.</span></span>

## <span data-ttu-id="62907-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="62907-104">SYNTAX</span></span>

### <span data-ttu-id="62907-105">ResourceSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="62907-105">ResourceSet (Default)</span></span>
```
New-AzIotHubSasToken [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId <String>]
 [-ModuleId <String>] [-KeyName <String>] [-KeyType <PSKeyType>] [-Duration <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="62907-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="62907-106">InputObjectSet</span></span>
```
New-AzIotHubSasToken [-InputObject] <PSIotHub> [-DeviceId <String>] [-ModuleId <String>] [-KeyName <String>]
 [-KeyType <PSKeyType>] [-Duration <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="62907-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="62907-107">ResourceIdSet</span></span>
```
New-AzIotHubSasToken [-ResourceId] <String> [-DeviceId <String>] [-ModuleId <String>] [-KeyName <String>]
 [-KeyType <PSKeyType>] [-Duration <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="62907-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="62907-108">DESCRIPTION</span></span>
<span data-ttu-id="62907-109">Para tokens SAS de dispositivo, o parâmetro de política é usado apenas para acessar o registro do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="62907-109">For device SAS tokens, the policy parameter is used to access the the device registry only.</span></span> <span data-ttu-id="62907-110">Portanto, a política deve ter acesso de leitura ao Registro.</span><span class="sxs-lookup"><span data-stu-id="62907-110">Therefore the policy should have read access to the registry.</span></span>
<span data-ttu-id="62907-111">Para tokens de Hub de IoT, a política faz parte do SAS.</span><span class="sxs-lookup"><span data-stu-id="62907-111">For IoT Hub tokens the policy is part of the SAS.</span></span>

## <span data-ttu-id="62907-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="62907-112">EXAMPLES</span></span>

### <span data-ttu-id="62907-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="62907-113">Example 1</span></span>
```powershell
PS C:\> New-AzIotHubSasToken -ResourceGroupName "myresourcegroup" -IotHubName "myiothub"
```

<span data-ttu-id="62907-114">Gere um token SAS do Hub IoT usando a política iothubowner e a chave primária.</span><span class="sxs-lookup"><span data-stu-id="62907-114">Generate an IoT Hub SAS token using the iothubowner policy and primary key.</span></span>

### <span data-ttu-id="62907-115">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="62907-115">Example 2</span></span>
```powershell
PS C:\> New-AzIotHubSasToken -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -KeyName "registryRead" -KeyType "secondary"
```

<span data-ttu-id="62907-116">Gere um token SAS do Hub IoT usando a política registryRead e a chave secundária.</span><span class="sxs-lookup"><span data-stu-id="62907-116">Generate an IoT Hub SAS token using the registryRead policy and secondary key.</span></span>

### <span data-ttu-id="62907-117">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="62907-117">Example 3</span></span>
```powershell
PS C:\> New-AzIotHubSasToken -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1"
```

<span data-ttu-id="62907-118">Gere um token SAS de dispositivo usando a política iothubowner para acessar o registro de dispositivo {iothub_name} .</span><span class="sxs-lookup"><span data-stu-id="62907-118">Generate a device SAS token using the iothubowner policy to access the {iothub_name} device registry.</span></span>

### <span data-ttu-id="62907-119">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="62907-119">Example 4</span></span>
```powershell
PS C:\> New-AzIotHubSasToken -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1"
```

<span data-ttu-id="62907-120">Gere um token SAS de módulo usando a política iothubowner para acessar o Registro de dispositivo {iothub_name}.</span><span class="sxs-lookup"><span data-stu-id="62907-120">Generate a module SAS token using the iothubowner policy to access the {iothub_name} device registry.</span></span>

## <span data-ttu-id="62907-121">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="62907-121">PARAMETERS</span></span>

### <span data-ttu-id="62907-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62907-122">-DefaultProfile</span></span>
<span data-ttu-id="62907-123">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="62907-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="62907-124">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="62907-124">-DeviceId</span></span>
<span data-ttu-id="62907-125">ID do dispositivo de destino.</span><span class="sxs-lookup"><span data-stu-id="62907-125">Target Device Id.</span></span>

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

### <span data-ttu-id="62907-126">-Duration</span><span class="sxs-lookup"><span data-stu-id="62907-126">-Duration</span></span>
<span data-ttu-id="62907-127">Expiração futura (em segundos) do token a ser gerado.</span><span class="sxs-lookup"><span data-stu-id="62907-127">Future expiry (in seconds) of the token to be generated.</span></span>
<span data-ttu-id="62907-128">O padrão é 3600.</span><span class="sxs-lookup"><span data-stu-id="62907-128">Default is 3600.</span></span>

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

### <span data-ttu-id="62907-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="62907-129">-InputObject</span></span>
<span data-ttu-id="62907-130">Objeto IotHub</span><span class="sxs-lookup"><span data-stu-id="62907-130">IotHub object</span></span>

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

### <span data-ttu-id="62907-131">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="62907-131">-IotHubName</span></span>
<span data-ttu-id="62907-132">Nome do Hub de Iot</span><span class="sxs-lookup"><span data-stu-id="62907-132">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="62907-133">-KeyName</span><span class="sxs-lookup"><span data-stu-id="62907-133">-KeyName</span></span>
<span data-ttu-id="62907-134">Nome da chave de acesso.</span><span class="sxs-lookup"><span data-stu-id="62907-134">Access key name.</span></span>

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

### <span data-ttu-id="62907-135">-KeyType</span><span class="sxs-lookup"><span data-stu-id="62907-135">-KeyType</span></span>
<span data-ttu-id="62907-136">Tipo de chave de acesso.</span><span class="sxs-lookup"><span data-stu-id="62907-136">Access key type.</span></span>

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

### <span data-ttu-id="62907-137">-ModuleId</span><span class="sxs-lookup"><span data-stu-id="62907-137">-ModuleId</span></span>
<span data-ttu-id="62907-138">ID do Módulo de Destino.</span><span class="sxs-lookup"><span data-stu-id="62907-138">Target Module Id.</span></span>

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

### <span data-ttu-id="62907-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62907-139">-ResourceGroupName</span></span>
<span data-ttu-id="62907-140">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="62907-140">Name of the Resource Group</span></span>

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

### <span data-ttu-id="62907-141">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="62907-141">-ResourceId</span></span>
<span data-ttu-id="62907-142">Id de Recurso IotHub</span><span class="sxs-lookup"><span data-stu-id="62907-142">IotHub Resource Id</span></span>

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

### <span data-ttu-id="62907-143">-Confirm</span><span class="sxs-lookup"><span data-stu-id="62907-143">-Confirm</span></span>
<span data-ttu-id="62907-144">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="62907-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="62907-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="62907-145">-WhatIf</span></span>
<span data-ttu-id="62907-146">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="62907-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="62907-147">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="62907-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="62907-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62907-148">CommonParameters</span></span>
<span data-ttu-id="62907-149">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62907-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62907-150">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="62907-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62907-151">INPUTS</span><span class="sxs-lookup"><span data-stu-id="62907-151">INPUTS</span></span>

### <span data-ttu-id="62907-152">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="62907-152">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="62907-153">System.String</span><span class="sxs-lookup"><span data-stu-id="62907-153">System.String</span></span>

## <span data-ttu-id="62907-154">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="62907-154">OUTPUTS</span></span>

### <span data-ttu-id="62907-155">System.String</span><span class="sxs-lookup"><span data-stu-id="62907-155">System.String</span></span>

## <span data-ttu-id="62907-156">NOTES</span><span class="sxs-lookup"><span data-stu-id="62907-156">NOTES</span></span>

## <span data-ttu-id="62907-157">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="62907-157">RELATED LINKS</span></span>
