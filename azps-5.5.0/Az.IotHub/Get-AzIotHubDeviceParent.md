---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubdeviceparent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeviceParent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeviceParent.md
ms.openlocfilehash: 14e5bbc222bf92f95d77277c6f8d82f578efd0b3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113153"
---
# <span data-ttu-id="fa5e4-101">Get-AzIotHubDeviceParent</span><span class="sxs-lookup"><span data-stu-id="fa5e4-101">Get-AzIotHubDeviceParent</span></span>

## <span data-ttu-id="fa5e4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fa5e4-102">SYNOPSIS</span></span>
<span data-ttu-id="fa5e4-103">Obter o dispositivo pai do dispositivo especificado.</span><span class="sxs-lookup"><span data-stu-id="fa5e4-103">Get the parent device of the specified device.</span></span>

## <span data-ttu-id="fa5e4-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fa5e4-104">SYNTAX</span></span>

### <span data-ttu-id="fa5e4-105">ResourceSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="fa5e4-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubDeviceParent [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fa5e4-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="fa5e4-106">InputObjectSet</span></span>
```
Get-AzIotHubDeviceParent [-InputObject] <PSIotHub> [-DeviceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fa5e4-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="fa5e4-107">ResourceIdSet</span></span>
```
Get-AzIotHubDeviceParent [-ResourceId] <String> [-DeviceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fa5e4-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="fa5e4-108">DESCRIPTION</span></span>
<span data-ttu-id="fa5e4-109">Obter o dispositivo pai do dispositivo especificado sem borda.</span><span class="sxs-lookup"><span data-stu-id="fa5e4-109">Get the parent device of the specified non-edge device.</span></span>

## <span data-ttu-id="fa5e4-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="fa5e4-110">EXAMPLES</span></span>

### <span data-ttu-id="fa5e4-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="fa5e4-111">Example 1</span></span>
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

<span data-ttu-id="fa5e4-112">Obter o dispositivo pai do dispositivo especificado sem borda.</span><span class="sxs-lookup"><span data-stu-id="fa5e4-112">Get the parent device of the specified non-edge device.</span></span>

## <span data-ttu-id="fa5e4-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fa5e4-113">PARAMETERS</span></span>

### <span data-ttu-id="fa5e4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa5e4-114">-DefaultProfile</span></span>
<span data-ttu-id="fa5e4-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fa5e4-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fa5e4-116">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="fa5e4-116">-DeviceId</span></span>
<span data-ttu-id="fa5e4-117">ID de dispositivo sem borda.</span><span class="sxs-lookup"><span data-stu-id="fa5e4-117">Id of non-edge device.</span></span>

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

### <span data-ttu-id="fa5e4-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fa5e4-118">-InputObject</span></span>
<span data-ttu-id="fa5e4-119">Objeto IotHub</span><span class="sxs-lookup"><span data-stu-id="fa5e4-119">IotHub object</span></span>

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

### <span data-ttu-id="fa5e4-120">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="fa5e4-120">-IotHubName</span></span>
<span data-ttu-id="fa5e4-121">Nome do Hub de Iot</span><span class="sxs-lookup"><span data-stu-id="fa5e4-121">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="fa5e4-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa5e4-122">-ResourceGroupName</span></span>
<span data-ttu-id="fa5e4-123">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="fa5e4-123">Name of the Resource Group</span></span>

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

### <span data-ttu-id="fa5e4-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fa5e4-124">-ResourceId</span></span>
<span data-ttu-id="fa5e4-125">ID de Recurso do IotHub</span><span class="sxs-lookup"><span data-stu-id="fa5e4-125">IotHub Resource Id</span></span>

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

### <span data-ttu-id="fa5e4-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa5e4-126">CommonParameters</span></span>
<span data-ttu-id="fa5e4-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fa5e4-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa5e4-128">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fa5e4-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa5e4-129">Entradas</span><span class="sxs-lookup"><span data-stu-id="fa5e4-129">INPUTS</span></span>

### <span data-ttu-id="fa5e4-130">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="fa5e4-130">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="fa5e4-131">System.String</span><span class="sxs-lookup"><span data-stu-id="fa5e4-131">System.String</span></span>

## <span data-ttu-id="fa5e4-132">Saídas</span><span class="sxs-lookup"><span data-stu-id="fa5e4-132">OUTPUTS</span></span>

### <span data-ttu-id="fa5e4-133">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice</span><span class="sxs-lookup"><span data-stu-id="fa5e4-133">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice</span></span>

## <span data-ttu-id="fa5e4-134">Notas</span><span class="sxs-lookup"><span data-stu-id="fa5e4-134">NOTES</span></span>

## <span data-ttu-id="fa5e4-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fa5e4-135">RELATED LINKS</span></span>
