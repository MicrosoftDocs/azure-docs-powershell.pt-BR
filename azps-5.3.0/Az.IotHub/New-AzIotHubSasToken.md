---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/new-aziothubsastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHubSasToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHubSasToken.md
ms.openlocfilehash: 486ca6543bb32d096e454d16ff3640720f2f53fe
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98272833"
---
# <span data-ttu-id="27792-101">New-AzIotHubSasToken</span><span class="sxs-lookup"><span data-stu-id="27792-101">New-AzIotHubSasToken</span></span>

## <span data-ttu-id="27792-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="27792-102">SYNOPSIS</span></span>
<span data-ttu-id="27792-103">Gerar um token SAS para um hub IoT, dispositivo ou módulo de destino.</span><span class="sxs-lookup"><span data-stu-id="27792-103">Generate a SAS token for a target IoT Hub, device or module.</span></span>

## <span data-ttu-id="27792-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="27792-104">SYNTAX</span></span>

### <span data-ttu-id="27792-105">ResourceSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="27792-105">ResourceSet (Default)</span></span>
```
New-AzIotHubSasToken [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId <String>]
 [-ModuleId <String>] [-KeyName <String>] [-KeyType <PSKeyType>] [-Duration <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="27792-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="27792-106">InputObjectSet</span></span>
```
New-AzIotHubSasToken [-InputObject] <PSIotHub> [-DeviceId <String>] [-ModuleId <String>] [-KeyName <String>]
 [-KeyType <PSKeyType>] [-Duration <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="27792-107">ResourceSet</span><span class="sxs-lookup"><span data-stu-id="27792-107">ResourceIdSet</span></span>
```
New-AzIotHubSasToken [-ResourceId] <String> [-DeviceId <String>] [-ModuleId <String>] [-KeyName <String>]
 [-KeyType <PSKeyType>] [-Duration <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="27792-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="27792-108">DESCRIPTION</span></span>
<span data-ttu-id="27792-109">Para tokens SAS de dispositivo, o parâmetro política é usado para acessar somente o registro do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="27792-109">For device SAS tokens, the policy parameter is used to access the the device registry only.</span></span> <span data-ttu-id="27792-110">Portanto, a política deve ter acesso de leitura ao registro.</span><span class="sxs-lookup"><span data-stu-id="27792-110">Therefore the policy should have read access to the registry.</span></span>
<span data-ttu-id="27792-111">Para tokens de Hub IoT, a política faz parte da SAS.</span><span class="sxs-lookup"><span data-stu-id="27792-111">For IoT Hub tokens the policy is part of the SAS.</span></span>

## <span data-ttu-id="27792-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="27792-112">EXAMPLES</span></span>

### <span data-ttu-id="27792-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="27792-113">Example 1</span></span>
```powershell
PS C:\> New-AzIotHubSasToken -ResourceGroupName "myresourcegroup" -IotHubName "myiothub"
```

<span data-ttu-id="27792-114">Gere um token SAS de Hub IoT usando a política iothubowner e a chave primária.</span><span class="sxs-lookup"><span data-stu-id="27792-114">Generate an IoT Hub SAS token using the iothubowner policy and primary key.</span></span>

### <span data-ttu-id="27792-115">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="27792-115">Example 2</span></span>
```powershell
PS C:\> New-AzIotHubSasToken -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -KeyName "registryRead" -KeyType "secondary"
```

<span data-ttu-id="27792-116">Gere um token SAS de Hub IoT usando a política registryRead e a chave secundária.</span><span class="sxs-lookup"><span data-stu-id="27792-116">Generate an IoT Hub SAS token using the registryRead policy and secondary key.</span></span>

### <span data-ttu-id="27792-117">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="27792-117">Example 3</span></span>
```powershell
PS C:\> New-AzIotHubSasToken -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1"
```

<span data-ttu-id="27792-118">Gere um token de dispositivo SAS usando a política iothubowner para acessar o registro de dispositivo {iothub_name}.</span><span class="sxs-lookup"><span data-stu-id="27792-118">Generate a device SAS token using the iothubowner policy to access the {iothub_name} device registry.</span></span>

### <span data-ttu-id="27792-119">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="27792-119">Example 4</span></span>
```powershell
PS C:\> New-AzIotHubSasToken -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1"
```

<span data-ttu-id="27792-120">Gere um token de módulo SAS usando a política iothubowner para acessar o registro de dispositivo {iothub_name}.</span><span class="sxs-lookup"><span data-stu-id="27792-120">Generate a module SAS token using the iothubowner policy to access the {iothub_name} device registry.</span></span>

## <span data-ttu-id="27792-121">OS</span><span class="sxs-lookup"><span data-stu-id="27792-121">PARAMETERS</span></span>

### <span data-ttu-id="27792-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27792-122">-DefaultProfile</span></span>
<span data-ttu-id="27792-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="27792-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="27792-124">-DeviceID</span><span class="sxs-lookup"><span data-stu-id="27792-124">-DeviceId</span></span>
<span data-ttu-id="27792-125">ID do dispositivo de destino.</span><span class="sxs-lookup"><span data-stu-id="27792-125">Target Device Id.</span></span>

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

### <span data-ttu-id="27792-126">-Duração</span><span class="sxs-lookup"><span data-stu-id="27792-126">-Duration</span></span>
<span data-ttu-id="27792-127">Vencimento futuro (em segundos) do token a ser gerado.</span><span class="sxs-lookup"><span data-stu-id="27792-127">Future expiry (in seconds) of the token to be generated.</span></span>
<span data-ttu-id="27792-128">O padrão é 3600.</span><span class="sxs-lookup"><span data-stu-id="27792-128">Default is 3600.</span></span>

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

### <span data-ttu-id="27792-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="27792-129">-InputObject</span></span>
<span data-ttu-id="27792-130">Objeto IotHub</span><span class="sxs-lookup"><span data-stu-id="27792-130">IotHub object</span></span>

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

### <span data-ttu-id="27792-131">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="27792-131">-IotHubName</span></span>
<span data-ttu-id="27792-132">Nome do Hub IOT</span><span class="sxs-lookup"><span data-stu-id="27792-132">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="27792-133">-KeyName</span><span class="sxs-lookup"><span data-stu-id="27792-133">-KeyName</span></span>
<span data-ttu-id="27792-134">Nome da tecla de acesso.</span><span class="sxs-lookup"><span data-stu-id="27792-134">Access key name.</span></span>

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

### <span data-ttu-id="27792-135">-KeyType</span><span class="sxs-lookup"><span data-stu-id="27792-135">-KeyType</span></span>
<span data-ttu-id="27792-136">Tipo de tecla de acesso.</span><span class="sxs-lookup"><span data-stu-id="27792-136">Access key type.</span></span>

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

### <span data-ttu-id="27792-137">-ModuleID</span><span class="sxs-lookup"><span data-stu-id="27792-137">-ModuleId</span></span>
<span data-ttu-id="27792-138">ID do módulo de destino.</span><span class="sxs-lookup"><span data-stu-id="27792-138">Target Module Id.</span></span>

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

### <span data-ttu-id="27792-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27792-139">-ResourceGroupName</span></span>
<span data-ttu-id="27792-140">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="27792-140">Name of the Resource Group</span></span>

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

### <span data-ttu-id="27792-141">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="27792-141">-ResourceId</span></span>
<span data-ttu-id="27792-142">ID do recurso IotHub</span><span class="sxs-lookup"><span data-stu-id="27792-142">IotHub Resource Id</span></span>

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

### <span data-ttu-id="27792-143">-Confirme</span><span class="sxs-lookup"><span data-stu-id="27792-143">-Confirm</span></span>
<span data-ttu-id="27792-144">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="27792-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="27792-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="27792-145">-WhatIf</span></span>
<span data-ttu-id="27792-146">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="27792-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="27792-147">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="27792-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="27792-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27792-148">CommonParameters</span></span>
<span data-ttu-id="27792-149">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="27792-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27792-150">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="27792-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27792-151">SENSORES</span><span class="sxs-lookup"><span data-stu-id="27792-151">INPUTS</span></span>

### <span data-ttu-id="27792-152">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="27792-152">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="27792-153">System. String</span><span class="sxs-lookup"><span data-stu-id="27792-153">System.String</span></span>

## <span data-ttu-id="27792-154">EXIBE</span><span class="sxs-lookup"><span data-stu-id="27792-154">OUTPUTS</span></span>

### <span data-ttu-id="27792-155">System. String</span><span class="sxs-lookup"><span data-stu-id="27792-155">System.String</span></span>

## <span data-ttu-id="27792-156">INFORMA</span><span class="sxs-lookup"><span data-stu-id="27792-156">NOTES</span></span>

## <span data-ttu-id="27792-157">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="27792-157">RELATED LINKS</span></span>
