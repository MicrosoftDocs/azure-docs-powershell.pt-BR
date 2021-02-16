---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/invoke-aziothubquery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubQuery.md
ms.openlocfilehash: 6445e6281ff69f4eef54a5694f953beaa08ad098
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113626"
---
# <span data-ttu-id="5b7d5-101">Invoke-AzIotHubQuery</span><span class="sxs-lookup"><span data-stu-id="5b7d5-101">Invoke-AzIotHubQuery</span></span>

## <span data-ttu-id="5b7d5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5b7d5-102">SYNOPSIS</span></span>
<span data-ttu-id="5b7d5-103">Consultar um Hub de IoT usando um idioma poderoso do tipo SQL.</span><span class="sxs-lookup"><span data-stu-id="5b7d5-103">Query an IoT Hub using a powerful SQL-like language.</span></span>

## <span data-ttu-id="5b7d5-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5b7d5-104">SYNTAX</span></span>

### <span data-ttu-id="5b7d5-105">ResourceSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="5b7d5-105">ResourceSet (Default)</span></span>
```
Invoke-AzIotHubQuery [-ResourceGroupName] <String> [-IotHubName] <String> [-Query] <String> [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5b7d5-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="5b7d5-106">InputObjectSet</span></span>
```
Invoke-AzIotHubQuery [-InputObject] <PSIotHub> [-Query] <String> [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5b7d5-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="5b7d5-107">ResourceIdSet</span></span>
```
Invoke-AzIotHubQuery [-ResourceId] <String> [-Query] <String> [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5b7d5-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="5b7d5-108">DESCRIPTION</span></span>
<span data-ttu-id="5b7d5-109">Consulte um Hub de IoT usando um idioma poderoso do tipo SQL para recuperar informações sobre o módulo e os módulos, trabalhos e roteamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="5b7d5-109">Query an IoT Hub using a powerful SQL-like language to retrieve information regarding device and module twins, jobs and message routing.</span></span>
<span data-ttu-id="5b7d5-110">Confira https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-query-language mais informações.</span><span class="sxs-lookup"><span data-stu-id="5b7d5-110">See https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-query-language for more information.</span></span>

## <span data-ttu-id="5b7d5-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="5b7d5-111">EXAMPLES</span></span>

### <span data-ttu-id="5b7d5-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="5b7d5-112">Example 1</span></span>
```powershell
PS C:\> Invoke-AzIotHubQuery -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Query "select * from devices"
```

<span data-ttu-id="5b7d5-113">Consultar todos os dados de dispositivo em um Hub IoT do Azure.</span><span class="sxs-lookup"><span data-stu-id="5b7d5-113">Query all device twin data in an Azure IoT Hub.</span></span>

### <span data-ttu-id="5b7d5-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="5b7d5-114">Example 2</span></span>
```powershell
PS C:\> Invoke-AzIotHubQuery -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Query "select * from devices.modules where devices.deviceId = 'myDevice1'" -Top 2
```

<span data-ttu-id="5b7d5-115">Consultar os dois principais dados do módulo em um dispositivo de destino.</span><span class="sxs-lookup"><span data-stu-id="5b7d5-115">Query top 2 module twin data on a target device.</span></span>

## <span data-ttu-id="5b7d5-116">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5b7d5-116">PARAMETERS</span></span>

### <span data-ttu-id="5b7d5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b7d5-117">-DefaultProfile</span></span>
<span data-ttu-id="5b7d5-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5b7d5-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5b7d5-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5b7d5-119">-InputObject</span></span>
<span data-ttu-id="5b7d5-120">Objeto IotHub</span><span class="sxs-lookup"><span data-stu-id="5b7d5-120">IotHub object</span></span>

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

### <span data-ttu-id="5b7d5-121">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="5b7d5-121">-IotHubName</span></span>
<span data-ttu-id="5b7d5-122">Nome do Hub de Iot</span><span class="sxs-lookup"><span data-stu-id="5b7d5-122">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="5b7d5-123">-Consulta</span><span class="sxs-lookup"><span data-stu-id="5b7d5-123">-Query</span></span>
<span data-ttu-id="5b7d5-124">Consulta de usuário a ser executada.</span><span class="sxs-lookup"><span data-stu-id="5b7d5-124">User query to be executed.</span></span>

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

### <span data-ttu-id="5b7d5-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b7d5-125">-ResourceGroupName</span></span>
<span data-ttu-id="5b7d5-126">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="5b7d5-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="5b7d5-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5b7d5-127">-ResourceId</span></span>
<span data-ttu-id="5b7d5-128">ID de Recurso do IotHub</span><span class="sxs-lookup"><span data-stu-id="5b7d5-128">IotHub Resource Id</span></span>

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

### <span data-ttu-id="5b7d5-129">-Superior</span><span class="sxs-lookup"><span data-stu-id="5b7d5-129">-Top</span></span>
<span data-ttu-id="5b7d5-130">Número máximo de elementos a retornar.</span><span class="sxs-lookup"><span data-stu-id="5b7d5-130">Maximum number of elements to return.</span></span>
<span data-ttu-id="5b7d5-131">Por padrão, a consulta não tem nenhum limite.</span><span class="sxs-lookup"><span data-stu-id="5b7d5-131">By default query has no cap.</span></span>

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

### <span data-ttu-id="5b7d5-132">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="5b7d5-132">-Confirm</span></span>
<span data-ttu-id="5b7d5-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5b7d5-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5b7d5-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5b7d5-134">-WhatIf</span></span>
<span data-ttu-id="5b7d5-135">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="5b7d5-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5b7d5-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5b7d5-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5b7d5-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b7d5-137">CommonParameters</span></span>
<span data-ttu-id="5b7d5-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5b7d5-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b7d5-139">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5b7d5-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b7d5-140">Entradas</span><span class="sxs-lookup"><span data-stu-id="5b7d5-140">INPUTS</span></span>

### <span data-ttu-id="5b7d5-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="5b7d5-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="5b7d5-142">System.String</span><span class="sxs-lookup"><span data-stu-id="5b7d5-142">System.String</span></span>

## <span data-ttu-id="5b7d5-143">Saídas</span><span class="sxs-lookup"><span data-stu-id="5b7d5-143">OUTPUTS</span></span>

### <span data-ttu-id="5b7d5-144">System.String</span><span class="sxs-lookup"><span data-stu-id="5b7d5-144">System.String</span></span>

## <span data-ttu-id="5b7d5-145">Notas</span><span class="sxs-lookup"><span data-stu-id="5b7d5-145">NOTES</span></span>

## <span data-ttu-id="5b7d5-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5b7d5-146">RELATED LINKS</span></span>
