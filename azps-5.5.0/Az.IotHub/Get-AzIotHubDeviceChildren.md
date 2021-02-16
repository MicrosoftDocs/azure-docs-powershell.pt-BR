---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubdevicechildren
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeviceChildren.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeviceChildren.md
ms.openlocfilehash: 1bc45aa06db70aff6eaec8eb1ff20b12318bb7e2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113156"
---
# <span data-ttu-id="60adc-101">Get-AzIotHubDeviceChildren</span><span class="sxs-lookup"><span data-stu-id="60adc-101">Get-AzIotHubDeviceChildren</span></span>

## <span data-ttu-id="60adc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="60adc-102">SYNOPSIS</span></span>
<span data-ttu-id="60adc-103">Imprimir lista separada por vírgulas de dispositivos filho atribuídos.</span><span class="sxs-lookup"><span data-stu-id="60adc-103">Print comma-separated list of assigned child devices.</span></span>

## <span data-ttu-id="60adc-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="60adc-104">SYNTAX</span></span>

### <span data-ttu-id="60adc-105">ResourceSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="60adc-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubDeviceChildren [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="60adc-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="60adc-106">InputObjectSet</span></span>
```
Get-AzIotHubDeviceChildren [-InputObject] <PSIotHub> [-DeviceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="60adc-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="60adc-107">ResourceIdSet</span></span>
```
Get-AzIotHubDeviceChildren [-ResourceId] <String> [-DeviceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="60adc-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="60adc-108">DESCRIPTION</span></span>
<span data-ttu-id="60adc-109">Mostrar todos os dispositivos sem borda atribuídos como uma lista separada por vírgula de todos os dispositivos de borda ou dispositivo especificado.</span><span class="sxs-lookup"><span data-stu-id="60adc-109">Show all assigned non-edge devices as comma-separated list of all edge devices or specified device.</span></span>

## <span data-ttu-id="60adc-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="60adc-110">EXAMPLES</span></span>

### <span data-ttu-id="60adc-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="60adc-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubDeviceChildren -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1"

DeviceId  ChildrenDeviceId
--------  ----------------
myDevice1 {device1, device2}
```

<span data-ttu-id="60adc-112">Mostrar todos os dispositivos sem borda atribuídos como lista separada por vírgulas.</span><span class="sxs-lookup"><span data-stu-id="60adc-112">Show all assigned non-edge devices as comma-separated list.</span></span>

### <span data-ttu-id="60adc-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="60adc-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIotHubDeviceChildren -ResourceGroupName "myresourcegroup" -IotHubName "myiothub"

DeviceId  ChildrenDeviceId
--------  ----------------
myDevice1 {device1, device2}
myDevice2 {device3, device4, device5}
```

<span data-ttu-id="60adc-114">Mostrar todos os dispositivos sem borda atribuídos como uma lista separada por vírgula de todos os dispositivos de borda.</span><span class="sxs-lookup"><span data-stu-id="60adc-114">Show all assigned non-edge devices as comma-separated list of all edge devices.</span></span>

## <span data-ttu-id="60adc-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="60adc-115">PARAMETERS</span></span>

### <span data-ttu-id="60adc-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60adc-116">-DefaultProfile</span></span>
<span data-ttu-id="60adc-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="60adc-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="60adc-118">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="60adc-118">-DeviceId</span></span>
<span data-ttu-id="60adc-119">ID do dispositivo de borda.</span><span class="sxs-lookup"><span data-stu-id="60adc-119">Id of edge device.</span></span>

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

### <span data-ttu-id="60adc-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="60adc-120">-InputObject</span></span>
<span data-ttu-id="60adc-121">Objeto IotHub</span><span class="sxs-lookup"><span data-stu-id="60adc-121">IotHub object</span></span>

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

### <span data-ttu-id="60adc-122">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="60adc-122">-IotHubName</span></span>
<span data-ttu-id="60adc-123">Nome do Hub de Iot</span><span class="sxs-lookup"><span data-stu-id="60adc-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="60adc-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60adc-124">-ResourceGroupName</span></span>
<span data-ttu-id="60adc-125">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="60adc-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="60adc-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="60adc-126">-ResourceId</span></span>
<span data-ttu-id="60adc-127">ID de Recurso do IotHub</span><span class="sxs-lookup"><span data-stu-id="60adc-127">IotHub Resource Id</span></span>

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

### <span data-ttu-id="60adc-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60adc-128">CommonParameters</span></span>
<span data-ttu-id="60adc-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60adc-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60adc-130">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="60adc-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60adc-131">Entradas</span><span class="sxs-lookup"><span data-stu-id="60adc-131">INPUTS</span></span>

### <span data-ttu-id="60adc-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="60adc-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="60adc-133">System.String</span><span class="sxs-lookup"><span data-stu-id="60adc-133">System.String</span></span>

## <span data-ttu-id="60adc-134">Saídas</span><span class="sxs-lookup"><span data-stu-id="60adc-134">OUTPUTS</span></span>

### <span data-ttu-id="60adc-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceChildren</span><span class="sxs-lookup"><span data-stu-id="60adc-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceChildren</span></span>

### <span data-ttu-id="60adc-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevicesChildren[]</span><span class="sxs-lookup"><span data-stu-id="60adc-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevicesChildren[]</span></span>

## <span data-ttu-id="60adc-137">Notas</span><span class="sxs-lookup"><span data-stu-id="60adc-137">NOTES</span></span>

## <span data-ttu-id="60adc-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="60adc-138">RELATED LINKS</span></span>
