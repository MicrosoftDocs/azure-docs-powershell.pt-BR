---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/invoke-aziothubquery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubQuery.md
ms.openlocfilehash: 6445e6281ff69f4eef54a5694f953beaa08ad098
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98258022"
---
# <span data-ttu-id="a8ccf-101">Invoke-AzIotHubQuery</span><span class="sxs-lookup"><span data-stu-id="a8ccf-101">Invoke-AzIotHubQuery</span></span>

## <span data-ttu-id="a8ccf-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a8ccf-102">SYNOPSIS</span></span>
<span data-ttu-id="a8ccf-103">Consulta um hub IoT usando uma linguagem poderosa semelhante ao SQL.</span><span class="sxs-lookup"><span data-stu-id="a8ccf-103">Query an IoT Hub using a powerful SQL-like language.</span></span>

## <span data-ttu-id="a8ccf-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a8ccf-104">SYNTAX</span></span>

### <span data-ttu-id="a8ccf-105">ResourceSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="a8ccf-105">ResourceSet (Default)</span></span>
```
Invoke-AzIotHubQuery [-ResourceGroupName] <String> [-IotHubName] <String> [-Query] <String> [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a8ccf-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="a8ccf-106">InputObjectSet</span></span>
```
Invoke-AzIotHubQuery [-InputObject] <PSIotHub> [-Query] <String> [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a8ccf-107">ResourceSet</span><span class="sxs-lookup"><span data-stu-id="a8ccf-107">ResourceIdSet</span></span>
```
Invoke-AzIotHubQuery [-ResourceId] <String> [-Query] <String> [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a8ccf-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a8ccf-108">DESCRIPTION</span></span>
<span data-ttu-id="a8ccf-109">Consulte um hub IoT usando uma poderosa linguagem SQL para recuperar informações sobre Twins de dispositivos e módulos, trabalhos e roteamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="a8ccf-109">Query an IoT Hub using a powerful SQL-like language to retrieve information regarding device and module twins, jobs and message routing.</span></span>
<span data-ttu-id="a8ccf-110">Consulte https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-query-language para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="a8ccf-110">See https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-query-language for more information.</span></span>

## <span data-ttu-id="a8ccf-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a8ccf-111">EXAMPLES</span></span>

### <span data-ttu-id="a8ccf-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a8ccf-112">Example 1</span></span>
```powershell
PS C:\> Invoke-AzIotHubQuery -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Query "select * from devices"
```

<span data-ttu-id="a8ccf-113">Consultar todos os dados do dispositivo de dados em um hub IoT do Azure.</span><span class="sxs-lookup"><span data-stu-id="a8ccf-113">Query all device twin data in an Azure IoT Hub.</span></span>

### <span data-ttu-id="a8ccf-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="a8ccf-114">Example 2</span></span>
```powershell
PS C:\> Invoke-AzIotHubQuery -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Query "select * from devices.modules where devices.deviceId = 'myDevice1'" -Top 2
```

<span data-ttu-id="a8ccf-115">Consultar os 2 dados do módulo top 10 em um dispositivo de destino.</span><span class="sxs-lookup"><span data-stu-id="a8ccf-115">Query top 2 module twin data on a target device.</span></span>

## <span data-ttu-id="a8ccf-116">OS</span><span class="sxs-lookup"><span data-stu-id="a8ccf-116">PARAMETERS</span></span>

### <span data-ttu-id="a8ccf-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8ccf-117">-DefaultProfile</span></span>
<span data-ttu-id="a8ccf-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a8ccf-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a8ccf-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a8ccf-119">-InputObject</span></span>
<span data-ttu-id="a8ccf-120">Objeto IotHub</span><span class="sxs-lookup"><span data-stu-id="a8ccf-120">IotHub object</span></span>

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

### <span data-ttu-id="a8ccf-121">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="a8ccf-121">-IotHubName</span></span>
<span data-ttu-id="a8ccf-122">Nome do Hub IOT</span><span class="sxs-lookup"><span data-stu-id="a8ccf-122">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="a8ccf-123">-Consulta</span><span class="sxs-lookup"><span data-stu-id="a8ccf-123">-Query</span></span>
<span data-ttu-id="a8ccf-124">Consulta de usuário a ser executada.</span><span class="sxs-lookup"><span data-stu-id="a8ccf-124">User query to be executed.</span></span>

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

### <span data-ttu-id="a8ccf-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a8ccf-125">-ResourceGroupName</span></span>
<span data-ttu-id="a8ccf-126">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="a8ccf-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="a8ccf-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a8ccf-127">-ResourceId</span></span>
<span data-ttu-id="a8ccf-128">ID do recurso IotHub</span><span class="sxs-lookup"><span data-stu-id="a8ccf-128">IotHub Resource Id</span></span>

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

### <span data-ttu-id="a8ccf-129">-Início</span><span class="sxs-lookup"><span data-stu-id="a8ccf-129">-Top</span></span>
<span data-ttu-id="a8ccf-130">Número máximo de elementos a serem retornados.</span><span class="sxs-lookup"><span data-stu-id="a8ccf-130">Maximum number of elements to return.</span></span>
<span data-ttu-id="a8ccf-131">Por padrão, a consulta não tem nenhum limite.</span><span class="sxs-lookup"><span data-stu-id="a8ccf-131">By default query has no cap.</span></span>

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

### <span data-ttu-id="a8ccf-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="a8ccf-132">-Confirm</span></span>
<span data-ttu-id="a8ccf-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a8ccf-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a8ccf-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a8ccf-134">-WhatIf</span></span>
<span data-ttu-id="a8ccf-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a8ccf-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a8ccf-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a8ccf-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a8ccf-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8ccf-137">CommonParameters</span></span>
<span data-ttu-id="a8ccf-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a8ccf-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8ccf-139">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a8ccf-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8ccf-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a8ccf-140">INPUTS</span></span>

### <span data-ttu-id="a8ccf-141">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="a8ccf-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="a8ccf-142">System. String</span><span class="sxs-lookup"><span data-stu-id="a8ccf-142">System.String</span></span>

## <span data-ttu-id="a8ccf-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a8ccf-143">OUTPUTS</span></span>

### <span data-ttu-id="a8ccf-144">System. String</span><span class="sxs-lookup"><span data-stu-id="a8ccf-144">System.String</span></span>

## <span data-ttu-id="a8ccf-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a8ccf-145">NOTES</span></span>

## <span data-ttu-id="a8ccf-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a8ccf-146">RELATED LINKS</span></span>
