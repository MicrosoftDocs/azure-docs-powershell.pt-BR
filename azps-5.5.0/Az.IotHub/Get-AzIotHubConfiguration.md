---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubConfiguration.md
ms.openlocfilehash: 616fface9f20609c043884754e9b3904ffc83e67
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113774"
---
# <span data-ttu-id="84f4e-101">Get-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="84f4e-101">Get-AzIotHubConfiguration</span></span>

## <span data-ttu-id="84f4e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="84f4e-102">SYNOPSIS</span></span>
<span data-ttu-id="84f4e-103">Lista toda ou uma configuração de gerenciamento de dispositivo automática de IoT específica.</span><span class="sxs-lookup"><span data-stu-id="84f4e-103">Lists all or a particular IoT automatic device management configuration.</span></span>

## <span data-ttu-id="84f4e-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="84f4e-104">SYNTAX</span></span>

### <span data-ttu-id="84f4e-105">ResourceSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="84f4e-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubConfiguration [-ResourceGroupName] <String> [-IotHubName] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="84f4e-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="84f4e-106">InputObjectSet</span></span>
```
Get-AzIotHubConfiguration [-InputObject] <PSIotHub> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="84f4e-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="84f4e-107">ResourceIdSet</span></span>
```
Get-AzIotHubConfiguration [-ResourceId] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="84f4e-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="84f4e-108">DESCRIPTION</span></span>
<span data-ttu-id="84f4e-109">Obter os detalhes de uma configuração automática de gerenciamento de dispositivo de IoT ou de configurações de gerenciamento automático de dispositivo IoT em um Hub de IoT.</span><span class="sxs-lookup"><span data-stu-id="84f4e-109">Get the details of an IoT automatic device management configuration or list IoT automatic device management configurations in an IoT Hub.</span></span>
<span data-ttu-id="84f4e-110">Confira https://docs.microsoft.com/azure/iot-hub/iot-hub-automatic-device-management mais informações.</span><span class="sxs-lookup"><span data-stu-id="84f4e-110">See https://docs.microsoft.com/azure/iot-hub/iot-hub-automatic-device-management for more information.</span></span>

## <span data-ttu-id="84f4e-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="84f4e-111">EXAMPLES</span></span>

### <span data-ttu-id="84f4e-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="84f4e-112">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "config1"
```

<span data-ttu-id="84f4e-113">Obter os detalhes de uma configuração automática de gerenciamento de dispositivo de IoT.</span><span class="sxs-lookup"><span data-stu-id="84f4e-113">Get the details of an IoT automatic device management configuration.</span></span>

### <span data-ttu-id="84f4e-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="84f4e-114">Example 2</span></span>
```powershell
PS C:\> Get-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub"
```

<span data-ttu-id="84f4e-115">List IoT automatic device management configurations in a IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="84f4e-115">List IoT automatic device management configurations in an IoT Hub.</span></span>

## <span data-ttu-id="84f4e-116">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="84f4e-116">PARAMETERS</span></span>

### <span data-ttu-id="84f4e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84f4e-117">-DefaultProfile</span></span>
<span data-ttu-id="84f4e-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="84f4e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="84f4e-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="84f4e-119">-InputObject</span></span>
<span data-ttu-id="84f4e-120">Objeto IotHub</span><span class="sxs-lookup"><span data-stu-id="84f4e-120">IotHub object</span></span>

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

### <span data-ttu-id="84f4e-121">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="84f4e-121">-IotHubName</span></span>
<span data-ttu-id="84f4e-122">Nome do Hub de Iot</span><span class="sxs-lookup"><span data-stu-id="84f4e-122">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="84f4e-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="84f4e-123">-Name</span></span>
<span data-ttu-id="84f4e-124">Identificador da configuração.</span><span class="sxs-lookup"><span data-stu-id="84f4e-124">Identifier for the configuration.</span></span>

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

### <span data-ttu-id="84f4e-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84f4e-125">-ResourceGroupName</span></span>
<span data-ttu-id="84f4e-126">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="84f4e-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="84f4e-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="84f4e-127">-ResourceId</span></span>
<span data-ttu-id="84f4e-128">ID de Recurso do IotHub</span><span class="sxs-lookup"><span data-stu-id="84f4e-128">IotHub Resource Id</span></span>

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

### <span data-ttu-id="84f4e-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84f4e-129">CommonParameters</span></span>
<span data-ttu-id="84f4e-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="84f4e-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84f4e-131">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="84f4e-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84f4e-132">Entradas</span><span class="sxs-lookup"><span data-stu-id="84f4e-132">INPUTS</span></span>

### <span data-ttu-id="84f4e-133">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="84f4e-133">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="84f4e-134">System.String</span><span class="sxs-lookup"><span data-stu-id="84f4e-134">System.String</span></span>

## <span data-ttu-id="84f4e-135">Saídas</span><span class="sxs-lookup"><span data-stu-id="84f4e-135">OUTPUTS</span></span>

### <span data-ttu-id="84f4e-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSConfiguration</span><span class="sxs-lookup"><span data-stu-id="84f4e-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSConfiguration</span></span>

### <span data-ttu-id="84f4e-137">Microsoft.Azure.Commands.Management.IotHub.Models.PSConfigurations[]</span><span class="sxs-lookup"><span data-stu-id="84f4e-137">Microsoft.Azure.Commands.Management.IotHub.Models.PSConfigurations[]</span></span>

## <span data-ttu-id="84f4e-138">Notas</span><span class="sxs-lookup"><span data-stu-id="84f4e-138">NOTES</span></span>

## <span data-ttu-id="84f4e-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="84f4e-139">RELATED LINKS</span></span>
