---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothubdeviceparent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDeviceParent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDeviceParent.md
ms.openlocfilehash: 1ad24866b4e0403693ace7b53b17271786f218d1
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93941415"
---
# <span data-ttu-id="09129-101">Set-AzIotHubDeviceParent</span><span class="sxs-lookup"><span data-stu-id="09129-101">Set-AzIotHubDeviceParent</span></span>

## <span data-ttu-id="09129-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="09129-102">SYNOPSIS</span></span>
<span data-ttu-id="09129-103">Definir o dispositivo pai do dispositivo especificado.</span><span class="sxs-lookup"><span data-stu-id="09129-103">Set the parent device of the specified device.</span></span>

## <span data-ttu-id="09129-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="09129-104">SYNTAX</span></span>

### <span data-ttu-id="09129-105">ResourceSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="09129-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubDeviceParent [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-ParentDeviceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="09129-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="09129-106">InputObjectSet</span></span>
```
Set-AzIotHubDeviceParent [-InputObject] <PSIotHub> [-DeviceId] <String> [-ParentDeviceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="09129-107">ResourceSet</span><span class="sxs-lookup"><span data-stu-id="09129-107">ResourceIdSet</span></span>
```
Set-AzIotHubDeviceParent [-ResourceId] <String> [-DeviceId] <String> [-ParentDeviceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="09129-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="09129-108">DESCRIPTION</span></span>
<span data-ttu-id="09129-109">Definir o dispositivo pai do dispositivo sem borda especificado.</span><span class="sxs-lookup"><span data-stu-id="09129-109">Set the parent device of the specified non-edge device.</span></span>

## <span data-ttu-id="09129-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="09129-110">EXAMPLES</span></span>

### <span data-ttu-id="09129-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="09129-111">Example 1</span></span>
```powershell
PS C:\> Set-AzIotHubDeviceParent -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ParentDeviceId "myParentDevice1"

DeviceId                   : myDevice1
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
EdgeEnabled                : False
DeviceScope                : ms-azure-iot-edge://myParentDevice1-637176526047419634
```

## <span data-ttu-id="09129-112">OS</span><span class="sxs-lookup"><span data-stu-id="09129-112">PARAMETERS</span></span>

### <span data-ttu-id="09129-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09129-113">-DefaultProfile</span></span>
<span data-ttu-id="09129-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="09129-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="09129-115">-DeviceID</span><span class="sxs-lookup"><span data-stu-id="09129-115">-DeviceId</span></span>
<span data-ttu-id="09129-116">ID do dispositivo não-Edge.</span><span class="sxs-lookup"><span data-stu-id="09129-116">Id of non-edge device.</span></span>

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

### <span data-ttu-id="09129-117">-Force</span><span class="sxs-lookup"><span data-stu-id="09129-117">-Force</span></span>
<span data-ttu-id="09129-118">Substitui o dispositivo pai do dispositivo não-Edge.</span><span class="sxs-lookup"><span data-stu-id="09129-118">Overwrites the non-edge device's parent device.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09129-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="09129-119">-InputObject</span></span>
<span data-ttu-id="09129-120">Objeto IotHub</span><span class="sxs-lookup"><span data-stu-id="09129-120">IotHub object</span></span>

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

### <span data-ttu-id="09129-121">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="09129-121">-IotHubName</span></span>
<span data-ttu-id="09129-122">Nome do Hub IOT</span><span class="sxs-lookup"><span data-stu-id="09129-122">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="09129-123">-ParentDeviceId</span><span class="sxs-lookup"><span data-stu-id="09129-123">-ParentDeviceId</span></span>
<span data-ttu-id="09129-124">ID do dispositivo de borda.</span><span class="sxs-lookup"><span data-stu-id="09129-124">Id of edge device.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09129-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09129-125">-ResourceGroupName</span></span>
<span data-ttu-id="09129-126">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="09129-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="09129-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="09129-127">-ResourceId</span></span>
<span data-ttu-id="09129-128">ID do recurso IotHub</span><span class="sxs-lookup"><span data-stu-id="09129-128">IotHub Resource Id</span></span>

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

### <span data-ttu-id="09129-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="09129-129">-Confirm</span></span>
<span data-ttu-id="09129-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="09129-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="09129-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="09129-131">-WhatIf</span></span>
<span data-ttu-id="09129-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="09129-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="09129-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="09129-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="09129-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09129-134">CommonParameters</span></span>
<span data-ttu-id="09129-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09129-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09129-136">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="09129-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09129-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="09129-137">INPUTS</span></span>

### <span data-ttu-id="09129-138">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="09129-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="09129-139">System. String</span><span class="sxs-lookup"><span data-stu-id="09129-139">System.String</span></span>

## <span data-ttu-id="09129-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="09129-140">OUTPUTS</span></span>

### <span data-ttu-id="09129-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice</span><span class="sxs-lookup"><span data-stu-id="09129-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice</span></span>

## <span data-ttu-id="09129-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="09129-142">NOTES</span></span>

## <span data-ttu-id="09129-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="09129-143">RELATED LINKS</span></span>
