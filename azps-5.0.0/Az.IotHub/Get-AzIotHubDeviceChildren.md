---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubdevicechildren
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeviceChildren.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeviceChildren.md
ms.openlocfilehash: 1bc45aa06db70aff6eaec8eb1ff20b12318bb7e2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94117754"
---
# <span data-ttu-id="b8f1b-101">Get-AzIotHubDeviceChildren</span><span class="sxs-lookup"><span data-stu-id="b8f1b-101">Get-AzIotHubDeviceChildren</span></span>

## <span data-ttu-id="b8f1b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b8f1b-102">SYNOPSIS</span></span>
<span data-ttu-id="b8f1b-103">Imprimir uma lista separada por vírgulas de dispositivos filho atribuídos.</span><span class="sxs-lookup"><span data-stu-id="b8f1b-103">Print comma-separated list of assigned child devices.</span></span>

## <span data-ttu-id="b8f1b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b8f1b-104">SYNTAX</span></span>

### <span data-ttu-id="b8f1b-105">ResourceSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="b8f1b-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubDeviceChildren [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b8f1b-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="b8f1b-106">InputObjectSet</span></span>
```
Get-AzIotHubDeviceChildren [-InputObject] <PSIotHub> [-DeviceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b8f1b-107">ResourceSet</span><span class="sxs-lookup"><span data-stu-id="b8f1b-107">ResourceIdSet</span></span>
```
Get-AzIotHubDeviceChildren [-ResourceId] <String> [-DeviceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b8f1b-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b8f1b-108">DESCRIPTION</span></span>
<span data-ttu-id="b8f1b-109">Mostrar todos os dispositivos sem borda atribuídos como lista separada por vírgulas de todos os dispositivos de borda ou dispositivo especificado.</span><span class="sxs-lookup"><span data-stu-id="b8f1b-109">Show all assigned non-edge devices as comma-separated list of all edge devices or specified device.</span></span>

## <span data-ttu-id="b8f1b-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b8f1b-110">EXAMPLES</span></span>

### <span data-ttu-id="b8f1b-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b8f1b-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubDeviceChildren -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1"

DeviceId  ChildrenDeviceId
--------  ----------------
myDevice1 {device1, device2}
```

<span data-ttu-id="b8f1b-112">Mostrar todos os dispositivos sem borda atribuídos como lista separada por vírgulas.</span><span class="sxs-lookup"><span data-stu-id="b8f1b-112">Show all assigned non-edge devices as comma-separated list.</span></span>

### <span data-ttu-id="b8f1b-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="b8f1b-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIotHubDeviceChildren -ResourceGroupName "myresourcegroup" -IotHubName "myiothub"

DeviceId  ChildrenDeviceId
--------  ----------------
myDevice1 {device1, device2}
myDevice2 {device3, device4, device5}
```

<span data-ttu-id="b8f1b-114">Mostrar todos os dispositivos sem borda atribuídos como lista separada por vírgulas de todos os dispositivos de borda.</span><span class="sxs-lookup"><span data-stu-id="b8f1b-114">Show all assigned non-edge devices as comma-separated list of all edge devices.</span></span>

## <span data-ttu-id="b8f1b-115">OS</span><span class="sxs-lookup"><span data-stu-id="b8f1b-115">PARAMETERS</span></span>

### <span data-ttu-id="b8f1b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8f1b-116">-DefaultProfile</span></span>
<span data-ttu-id="b8f1b-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b8f1b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b8f1b-118">-DeviceID</span><span class="sxs-lookup"><span data-stu-id="b8f1b-118">-DeviceId</span></span>
<span data-ttu-id="b8f1b-119">ID do dispositivo de borda.</span><span class="sxs-lookup"><span data-stu-id="b8f1b-119">Id of edge device.</span></span>

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

### <span data-ttu-id="b8f1b-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b8f1b-120">-InputObject</span></span>
<span data-ttu-id="b8f1b-121">Objeto IotHub</span><span class="sxs-lookup"><span data-stu-id="b8f1b-121">IotHub object</span></span>

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

### <span data-ttu-id="b8f1b-122">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="b8f1b-122">-IotHubName</span></span>
<span data-ttu-id="b8f1b-123">Nome do Hub IOT</span><span class="sxs-lookup"><span data-stu-id="b8f1b-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="b8f1b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8f1b-124">-ResourceGroupName</span></span>
<span data-ttu-id="b8f1b-125">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="b8f1b-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="b8f1b-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b8f1b-126">-ResourceId</span></span>
<span data-ttu-id="b8f1b-127">ID do recurso IotHub</span><span class="sxs-lookup"><span data-stu-id="b8f1b-127">IotHub Resource Id</span></span>

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

### <span data-ttu-id="b8f1b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8f1b-128">CommonParameters</span></span>
<span data-ttu-id="b8f1b-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b8f1b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8f1b-130">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b8f1b-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8f1b-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b8f1b-131">INPUTS</span></span>

### <span data-ttu-id="b8f1b-132">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="b8f1b-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="b8f1b-133">System. String</span><span class="sxs-lookup"><span data-stu-id="b8f1b-133">System.String</span></span>

## <span data-ttu-id="b8f1b-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b8f1b-134">OUTPUTS</span></span>

### <span data-ttu-id="b8f1b-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceChildren</span><span class="sxs-lookup"><span data-stu-id="b8f1b-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceChildren</span></span>

### <span data-ttu-id="b8f1b-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevicesChildren []</span><span class="sxs-lookup"><span data-stu-id="b8f1b-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevicesChildren[]</span></span>

## <span data-ttu-id="b8f1b-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b8f1b-137">NOTES</span></span>

## <span data-ttu-id="b8f1b-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b8f1b-138">RELATED LINKS</span></span>
