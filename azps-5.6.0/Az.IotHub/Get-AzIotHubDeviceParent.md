---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/get-aziothubdeviceparent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeviceParent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeviceParent.md
ms.openlocfilehash: 06eb84ea854e9c0262f6f3e00e3e13e90f630baa
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889959"
---
# <span data-ttu-id="1d681-101">Get-AzIotHubDeviceParent</span><span class="sxs-lookup"><span data-stu-id="1d681-101">Get-AzIotHubDeviceParent</span></span>

## <span data-ttu-id="1d681-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1d681-102">SYNOPSIS</span></span>
<span data-ttu-id="1d681-103">Obter o dispositivo pai do dispositivo especificado.</span><span class="sxs-lookup"><span data-stu-id="1d681-103">Get the parent device of the specified device.</span></span>

## <span data-ttu-id="1d681-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="1d681-104">SYNTAX</span></span>

### <span data-ttu-id="1d681-105">ResourceSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="1d681-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubDeviceParent [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1d681-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="1d681-106">InputObjectSet</span></span>
```
Get-AzIotHubDeviceParent [-InputObject] <PSIotHub> [-DeviceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1d681-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="1d681-107">ResourceIdSet</span></span>
```
Get-AzIotHubDeviceParent [-ResourceId] <String> [-DeviceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1d681-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="1d681-108">DESCRIPTION</span></span>
<span data-ttu-id="1d681-109">Obter o dispositivo pai do dispositivo não-borda especificado.</span><span class="sxs-lookup"><span data-stu-id="1d681-109">Get the parent device of the specified non-edge device.</span></span>

## <span data-ttu-id="1d681-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1d681-110">EXAMPLES</span></span>

### <span data-ttu-id="1d681-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="1d681-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubDeviceParent -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1"

DeviceId                   : myParentDevice1
GenerationId               : 637148941292917073
ETag                       : "NzIyMDI4MTk3"
LastActivityTime           : 1/1/0001 12:00:00 AM
ConnectionState            : Disconnected
ConnectionStateUpdatedTime : 1/1/0001 12:00:00 AM
Status                     : Enabled
StatusReason               : 
StatusUpdatedTime          : 1/17/2020 10:15:04 PM
CloudToDeviceMessageCount  : 0
Authentication             : Sas
EdgeEnabled                : True
DeviceScope                : ms-azure-iot-edge://myParentDevice1-637176526047419634
```

<span data-ttu-id="1d681-112">Obter o dispositivo pai do dispositivo não-borda especificado.</span><span class="sxs-lookup"><span data-stu-id="1d681-112">Get the parent device of the specified non-edge device.</span></span>

## <span data-ttu-id="1d681-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="1d681-113">PARAMETERS</span></span>

### <span data-ttu-id="1d681-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d681-114">-DefaultProfile</span></span>
<span data-ttu-id="1d681-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1d681-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1d681-116">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="1d681-116">-DeviceId</span></span>
<span data-ttu-id="1d681-117">ID de dispositivo sem borda.</span><span class="sxs-lookup"><span data-stu-id="1d681-117">Id of non-edge device.</span></span>

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

### <span data-ttu-id="1d681-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1d681-118">-InputObject</span></span>
<span data-ttu-id="1d681-119">Objeto IotHub</span><span class="sxs-lookup"><span data-stu-id="1d681-119">IotHub object</span></span>

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

### <span data-ttu-id="1d681-120">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="1d681-120">-IotHubName</span></span>
<span data-ttu-id="1d681-121">Nome do Hub de Iot</span><span class="sxs-lookup"><span data-stu-id="1d681-121">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="1d681-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1d681-122">-ResourceGroupName</span></span>
<span data-ttu-id="1d681-123">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="1d681-123">Name of the Resource Group</span></span>

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

### <span data-ttu-id="1d681-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1d681-124">-ResourceId</span></span>
<span data-ttu-id="1d681-125">Id de Recurso IotHub</span><span class="sxs-lookup"><span data-stu-id="1d681-125">IotHub Resource Id</span></span>

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

### <span data-ttu-id="1d681-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d681-126">CommonParameters</span></span>
<span data-ttu-id="1d681-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1d681-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d681-128">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1d681-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d681-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1d681-129">INPUTS</span></span>

### <span data-ttu-id="1d681-130">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="1d681-130">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="1d681-131">System.String</span><span class="sxs-lookup"><span data-stu-id="1d681-131">System.String</span></span>

## <span data-ttu-id="1d681-132">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="1d681-132">OUTPUTS</span></span>

### <span data-ttu-id="1d681-133">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice</span><span class="sxs-lookup"><span data-stu-id="1d681-133">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice</span></span>

## <span data-ttu-id="1d681-134">NOTES</span><span class="sxs-lookup"><span data-stu-id="1d681-134">NOTES</span></span>

## <span data-ttu-id="1d681-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1d681-135">RELATED LINKS</span></span>
