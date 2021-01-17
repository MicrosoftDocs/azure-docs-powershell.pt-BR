---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubdeviceparent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeviceParent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeviceParent.md
ms.openlocfilehash: 14e5bbc222bf92f95d77277c6f8d82f578efd0b3
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98433729"
---
# <span data-ttu-id="ea570-101">Get-AzIotHubDeviceParent</span><span class="sxs-lookup"><span data-stu-id="ea570-101">Get-AzIotHubDeviceParent</span></span>

## <span data-ttu-id="ea570-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ea570-102">SYNOPSIS</span></span>
<span data-ttu-id="ea570-103">Obter o dispositivo pai do dispositivo especificado.</span><span class="sxs-lookup"><span data-stu-id="ea570-103">Get the parent device of the specified device.</span></span>

## <span data-ttu-id="ea570-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ea570-104">SYNTAX</span></span>

### <span data-ttu-id="ea570-105">ResourceSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="ea570-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubDeviceParent [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ea570-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="ea570-106">InputObjectSet</span></span>
```
Get-AzIotHubDeviceParent [-InputObject] <PSIotHub> [-DeviceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ea570-107">ResourceSet</span><span class="sxs-lookup"><span data-stu-id="ea570-107">ResourceIdSet</span></span>
```
Get-AzIotHubDeviceParent [-ResourceId] <String> [-DeviceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ea570-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ea570-108">DESCRIPTION</span></span>
<span data-ttu-id="ea570-109">Obter o dispositivo pai do dispositivo sem borda especificado.</span><span class="sxs-lookup"><span data-stu-id="ea570-109">Get the parent device of the specified non-edge device.</span></span>

## <span data-ttu-id="ea570-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ea570-110">EXAMPLES</span></span>

### <span data-ttu-id="ea570-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ea570-111">Example 1</span></span>
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

<span data-ttu-id="ea570-112">Obter o dispositivo pai do dispositivo sem borda especificado.</span><span class="sxs-lookup"><span data-stu-id="ea570-112">Get the parent device of the specified non-edge device.</span></span>

## <span data-ttu-id="ea570-113">OS</span><span class="sxs-lookup"><span data-stu-id="ea570-113">PARAMETERS</span></span>

### <span data-ttu-id="ea570-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea570-114">-DefaultProfile</span></span>
<span data-ttu-id="ea570-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ea570-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ea570-116">-DeviceID</span><span class="sxs-lookup"><span data-stu-id="ea570-116">-DeviceId</span></span>
<span data-ttu-id="ea570-117">ID do dispositivo não-Edge.</span><span class="sxs-lookup"><span data-stu-id="ea570-117">Id of non-edge device.</span></span>

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

### <span data-ttu-id="ea570-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ea570-118">-InputObject</span></span>
<span data-ttu-id="ea570-119">Objeto IotHub</span><span class="sxs-lookup"><span data-stu-id="ea570-119">IotHub object</span></span>

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

### <span data-ttu-id="ea570-120">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="ea570-120">-IotHubName</span></span>
<span data-ttu-id="ea570-121">Nome do Hub IOT</span><span class="sxs-lookup"><span data-stu-id="ea570-121">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="ea570-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea570-122">-ResourceGroupName</span></span>
<span data-ttu-id="ea570-123">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="ea570-123">Name of the Resource Group</span></span>

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

### <span data-ttu-id="ea570-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ea570-124">-ResourceId</span></span>
<span data-ttu-id="ea570-125">ID do recurso IotHub</span><span class="sxs-lookup"><span data-stu-id="ea570-125">IotHub Resource Id</span></span>

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

### <span data-ttu-id="ea570-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea570-126">CommonParameters</span></span>
<span data-ttu-id="ea570-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea570-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea570-128">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea570-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea570-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ea570-129">INPUTS</span></span>

### <span data-ttu-id="ea570-130">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="ea570-130">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="ea570-131">System. String</span><span class="sxs-lookup"><span data-stu-id="ea570-131">System.String</span></span>

## <span data-ttu-id="ea570-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ea570-132">OUTPUTS</span></span>

### <span data-ttu-id="ea570-133">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice</span><span class="sxs-lookup"><span data-stu-id="ea570-133">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice</span></span>

## <span data-ttu-id="ea570-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ea570-134">NOTES</span></span>

## <span data-ttu-id="ea570-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ea570-135">RELATED LINKS</span></span>
