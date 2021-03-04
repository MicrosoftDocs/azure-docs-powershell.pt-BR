---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/invoke-aziothubquery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubQuery.md
ms.openlocfilehash: 955e09ab17644009f281223581ae2f5f45adfb33
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885466"
---
# <span data-ttu-id="dbc59-101">Invoke-AzIotHubQuery</span><span class="sxs-lookup"><span data-stu-id="dbc59-101">Invoke-AzIotHubQuery</span></span>

## <span data-ttu-id="dbc59-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dbc59-102">SYNOPSIS</span></span>
<span data-ttu-id="dbc59-103">Consultar um Hub de IoT usando um idioma SQL de uso eficiente.</span><span class="sxs-lookup"><span data-stu-id="dbc59-103">Query an IoT Hub using a powerful SQL-like language.</span></span>

## <span data-ttu-id="dbc59-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="dbc59-104">SYNTAX</span></span>

### <span data-ttu-id="dbc59-105">ResourceSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="dbc59-105">ResourceSet (Default)</span></span>
```
Invoke-AzIotHubQuery [-ResourceGroupName] <String> [-IotHubName] <String> [-Query] <String> [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dbc59-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="dbc59-106">InputObjectSet</span></span>
```
Invoke-AzIotHubQuery [-InputObject] <PSIotHub> [-Query] <String> [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dbc59-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="dbc59-107">ResourceIdSet</span></span>
```
Invoke-AzIotHubQuery [-ResourceId] <String> [-Query] <String> [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dbc59-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="dbc59-108">DESCRIPTION</span></span>
<span data-ttu-id="dbc59-109">Consultar um Hub de IoT usando um idioma SQL de usuário poderoso para recuperar informações sobre os modelos de dispositivo e módulo, trabalhos e roteamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="dbc59-109">Query an IoT Hub using a powerful SQL-like language to retrieve information regarding device and module twins, jobs and message routing.</span></span>
<span data-ttu-id="dbc59-110">Confira https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-query-language mais informações.</span><span class="sxs-lookup"><span data-stu-id="dbc59-110">See https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-query-language for more information.</span></span>

## <span data-ttu-id="dbc59-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="dbc59-111">EXAMPLES</span></span>

### <span data-ttu-id="dbc59-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="dbc59-112">Example 1</span></span>
```powershell
PS C:\> Invoke-AzIotHubQuery -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Query "select * from devices"
```

<span data-ttu-id="dbc59-113">Consultar todos os dados duplos do dispositivo em um Hub do Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="dbc59-113">Query all device twin data in an Azure IoT Hub.</span></span>

### <span data-ttu-id="dbc59-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="dbc59-114">Example 2</span></span>
```powershell
PS C:\> Invoke-AzIotHubQuery -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Query "select * from devices.modules where devices.deviceId = 'myDevice1'" -Top 2
```

<span data-ttu-id="dbc59-115">Consultar dados duplos do módulo 2 principais em um dispositivo de destino.</span><span class="sxs-lookup"><span data-stu-id="dbc59-115">Query top 2 module twin data on a target device.</span></span>

## <span data-ttu-id="dbc59-116">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="dbc59-116">PARAMETERS</span></span>

### <span data-ttu-id="dbc59-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dbc59-117">-DefaultProfile</span></span>
<span data-ttu-id="dbc59-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="dbc59-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dbc59-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dbc59-119">-InputObject</span></span>
<span data-ttu-id="dbc59-120">Objeto IotHub</span><span class="sxs-lookup"><span data-stu-id="dbc59-120">IotHub object</span></span>

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

### <span data-ttu-id="dbc59-121">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="dbc59-121">-IotHubName</span></span>
<span data-ttu-id="dbc59-122">Nome do Hub de Iot</span><span class="sxs-lookup"><span data-stu-id="dbc59-122">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="dbc59-123">-Query</span><span class="sxs-lookup"><span data-stu-id="dbc59-123">-Query</span></span>
<span data-ttu-id="dbc59-124">Consulta do usuário a ser executada.</span><span class="sxs-lookup"><span data-stu-id="dbc59-124">User query to be executed.</span></span>

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

### <span data-ttu-id="dbc59-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dbc59-125">-ResourceGroupName</span></span>
<span data-ttu-id="dbc59-126">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="dbc59-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="dbc59-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dbc59-127">-ResourceId</span></span>
<span data-ttu-id="dbc59-128">Id de Recurso IotHub</span><span class="sxs-lookup"><span data-stu-id="dbc59-128">IotHub Resource Id</span></span>

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

### <span data-ttu-id="dbc59-129">-Top</span><span class="sxs-lookup"><span data-stu-id="dbc59-129">-Top</span></span>
<span data-ttu-id="dbc59-130">Número máximo de elementos a retornar.</span><span class="sxs-lookup"><span data-stu-id="dbc59-130">Maximum number of elements to return.</span></span>
<span data-ttu-id="dbc59-131">Por padrão, a consulta não tem nenhum limite.</span><span class="sxs-lookup"><span data-stu-id="dbc59-131">By default query has no cap.</span></span>

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

### <span data-ttu-id="dbc59-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dbc59-132">-Confirm</span></span>
<span data-ttu-id="dbc59-133">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dbc59-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dbc59-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dbc59-134">-WhatIf</span></span>
<span data-ttu-id="dbc59-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="dbc59-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="dbc59-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="dbc59-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dbc59-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbc59-137">CommonParameters</span></span>
<span data-ttu-id="dbc59-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dbc59-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dbc59-139">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dbc59-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbc59-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="dbc59-140">INPUTS</span></span>

### <span data-ttu-id="dbc59-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="dbc59-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="dbc59-142">System.String</span><span class="sxs-lookup"><span data-stu-id="dbc59-142">System.String</span></span>

## <span data-ttu-id="dbc59-143">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="dbc59-143">OUTPUTS</span></span>

### <span data-ttu-id="dbc59-144">System.String</span><span class="sxs-lookup"><span data-stu-id="dbc59-144">System.String</span></span>

## <span data-ttu-id="dbc59-145">NOTES</span><span class="sxs-lookup"><span data-stu-id="dbc59-145">NOTES</span></span>

## <span data-ttu-id="dbc59-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="dbc59-146">RELATED LINKS</span></span>
