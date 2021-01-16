---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubConfiguration.md
ms.openlocfilehash: 616fface9f20609c043884754e9b3904ffc83e67
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98257713"
---
# <span data-ttu-id="5a20d-101">Get-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="5a20d-101">Get-AzIotHubConfiguration</span></span>

## <span data-ttu-id="5a20d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5a20d-102">SYNOPSIS</span></span>
<span data-ttu-id="5a20d-103">Lista todas ou uma configuração específica de gerenciamento automático de dispositivos da IoT.</span><span class="sxs-lookup"><span data-stu-id="5a20d-103">Lists all or a particular IoT automatic device management configuration.</span></span>

## <span data-ttu-id="5a20d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5a20d-104">SYNTAX</span></span>

### <span data-ttu-id="5a20d-105">ResourceSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="5a20d-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubConfiguration [-ResourceGroupName] <String> [-IotHubName] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5a20d-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="5a20d-106">InputObjectSet</span></span>
```
Get-AzIotHubConfiguration [-InputObject] <PSIotHub> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5a20d-107">ResourceSet</span><span class="sxs-lookup"><span data-stu-id="5a20d-107">ResourceIdSet</span></span>
```
Get-AzIotHubConfiguration [-ResourceId] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5a20d-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5a20d-108">DESCRIPTION</span></span>
<span data-ttu-id="5a20d-109">Obtenha os detalhes de uma configuração de gerenciamento automático de dispositivos da IoT ou liste as configurações de gerenciamento automático de dispositivos do IoT em um hub IoT.</span><span class="sxs-lookup"><span data-stu-id="5a20d-109">Get the details of an IoT automatic device management configuration or list IoT automatic device management configurations in an IoT Hub.</span></span>
<span data-ttu-id="5a20d-110">Consulte https://docs.microsoft.com/azure/iot-hub/iot-hub-automatic-device-management para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="5a20d-110">See https://docs.microsoft.com/azure/iot-hub/iot-hub-automatic-device-management for more information.</span></span>

## <span data-ttu-id="5a20d-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5a20d-111">EXAMPLES</span></span>

### <span data-ttu-id="5a20d-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="5a20d-112">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "config1"
```

<span data-ttu-id="5a20d-113">Obtenha os detalhes de uma configuração de gerenciamento automático de dispositivos da IoT.</span><span class="sxs-lookup"><span data-stu-id="5a20d-113">Get the details of an IoT automatic device management configuration.</span></span>

### <span data-ttu-id="5a20d-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="5a20d-114">Example 2</span></span>
```powershell
PS C:\> Get-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub"
```

<span data-ttu-id="5a20d-115">Liste as configurações de gerenciamento automático de dispositivos da IoT em um hub IoT.</span><span class="sxs-lookup"><span data-stu-id="5a20d-115">List IoT automatic device management configurations in an IoT Hub.</span></span>

## <span data-ttu-id="5a20d-116">OS</span><span class="sxs-lookup"><span data-stu-id="5a20d-116">PARAMETERS</span></span>

### <span data-ttu-id="5a20d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a20d-117">-DefaultProfile</span></span>
<span data-ttu-id="5a20d-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5a20d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5a20d-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5a20d-119">-InputObject</span></span>
<span data-ttu-id="5a20d-120">Objeto IotHub</span><span class="sxs-lookup"><span data-stu-id="5a20d-120">IotHub object</span></span>

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

### <span data-ttu-id="5a20d-121">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="5a20d-121">-IotHubName</span></span>
<span data-ttu-id="5a20d-122">Nome do Hub IOT</span><span class="sxs-lookup"><span data-stu-id="5a20d-122">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="5a20d-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="5a20d-123">-Name</span></span>
<span data-ttu-id="5a20d-124">Identificador para a configuração.</span><span class="sxs-lookup"><span data-stu-id="5a20d-124">Identifier for the configuration.</span></span>

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

### <span data-ttu-id="5a20d-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a20d-125">-ResourceGroupName</span></span>
<span data-ttu-id="5a20d-126">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="5a20d-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="5a20d-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5a20d-127">-ResourceId</span></span>
<span data-ttu-id="5a20d-128">ID do recurso IotHub</span><span class="sxs-lookup"><span data-stu-id="5a20d-128">IotHub Resource Id</span></span>

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

### <span data-ttu-id="5a20d-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a20d-129">CommonParameters</span></span>
<span data-ttu-id="5a20d-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a20d-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a20d-131">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a20d-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a20d-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5a20d-132">INPUTS</span></span>

### <span data-ttu-id="5a20d-133">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="5a20d-133">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="5a20d-134">System. String</span><span class="sxs-lookup"><span data-stu-id="5a20d-134">System.String</span></span>

## <span data-ttu-id="5a20d-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5a20d-135">OUTPUTS</span></span>

### <span data-ttu-id="5a20d-136">Microsoft. Azure. Commands. Management. IotHub. Models. PSConfiguration</span><span class="sxs-lookup"><span data-stu-id="5a20d-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSConfiguration</span></span>

### <span data-ttu-id="5a20d-137">Microsoft. Azure. Commands. Management. IotHub. Models. PSConfigurations []</span><span class="sxs-lookup"><span data-stu-id="5a20d-137">Microsoft.Azure.Commands.Management.IotHub.Models.PSConfigurations[]</span></span>

## <span data-ttu-id="5a20d-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5a20d-138">NOTES</span></span>

## <span data-ttu-id="5a20d-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5a20d-139">RELATED LINKS</span></span>
