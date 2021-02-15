---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothubdeviceparent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDeviceParent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDeviceParent.md
ms.openlocfilehash: 1ad24866b4e0403693ace7b53b17271786f218d1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111846"
---
# <span data-ttu-id="3498f-101">Set-AzIotHubDeviceParent</span><span class="sxs-lookup"><span data-stu-id="3498f-101">Set-AzIotHubDeviceParent</span></span>

## <span data-ttu-id="3498f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3498f-102">SYNOPSIS</span></span>
<span data-ttu-id="3498f-103">Definir o dispositivo pai do dispositivo especificado.</span><span class="sxs-lookup"><span data-stu-id="3498f-103">Set the parent device of the specified device.</span></span>

## <span data-ttu-id="3498f-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3498f-104">SYNTAX</span></span>

### <span data-ttu-id="3498f-105">ResourceSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="3498f-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubDeviceParent [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-ParentDeviceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3498f-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="3498f-106">InputObjectSet</span></span>
```
Set-AzIotHubDeviceParent [-InputObject] <PSIotHub> [-DeviceId] <String> [-ParentDeviceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3498f-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="3498f-107">ResourceIdSet</span></span>
```
Set-AzIotHubDeviceParent [-ResourceId] <String> [-DeviceId] <String> [-ParentDeviceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3498f-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="3498f-108">DESCRIPTION</span></span>
<span data-ttu-id="3498f-109">De definir o dispositivo pai do dispositivo não edge especificado.</span><span class="sxs-lookup"><span data-stu-id="3498f-109">Set the parent device of the specified non-edge device.</span></span>

## <span data-ttu-id="3498f-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="3498f-110">EXAMPLES</span></span>

### <span data-ttu-id="3498f-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="3498f-111">Example 1</span></span>
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

## <span data-ttu-id="3498f-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3498f-112">PARAMETERS</span></span>

### <span data-ttu-id="3498f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3498f-113">-DefaultProfile</span></span>
<span data-ttu-id="3498f-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3498f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3498f-115">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="3498f-115">-DeviceId</span></span>
<span data-ttu-id="3498f-116">ID de dispositivo sem borda.</span><span class="sxs-lookup"><span data-stu-id="3498f-116">Id of non-edge device.</span></span>

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

### <span data-ttu-id="3498f-117">-Forçar</span><span class="sxs-lookup"><span data-stu-id="3498f-117">-Force</span></span>
<span data-ttu-id="3498f-118">Substitui o dispositivo pai do dispositivo sem borda.</span><span class="sxs-lookup"><span data-stu-id="3498f-118">Overwrites the non-edge device's parent device.</span></span>

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

### <span data-ttu-id="3498f-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3498f-119">-InputObject</span></span>
<span data-ttu-id="3498f-120">Objeto IotHub</span><span class="sxs-lookup"><span data-stu-id="3498f-120">IotHub object</span></span>

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

### <span data-ttu-id="3498f-121">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="3498f-121">-IotHubName</span></span>
<span data-ttu-id="3498f-122">Nome do Hub de Iot</span><span class="sxs-lookup"><span data-stu-id="3498f-122">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="3498f-123">-ParentDeviceId</span><span class="sxs-lookup"><span data-stu-id="3498f-123">-ParentDeviceId</span></span>
<span data-ttu-id="3498f-124">ID do dispositivo de borda.</span><span class="sxs-lookup"><span data-stu-id="3498f-124">Id of edge device.</span></span>

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

### <span data-ttu-id="3498f-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3498f-125">-ResourceGroupName</span></span>
<span data-ttu-id="3498f-126">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="3498f-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="3498f-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3498f-127">-ResourceId</span></span>
<span data-ttu-id="3498f-128">ID de Recurso do IotHub</span><span class="sxs-lookup"><span data-stu-id="3498f-128">IotHub Resource Id</span></span>

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

### <span data-ttu-id="3498f-129">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="3498f-129">-Confirm</span></span>
<span data-ttu-id="3498f-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3498f-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3498f-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3498f-131">-WhatIf</span></span>
<span data-ttu-id="3498f-132">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="3498f-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3498f-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3498f-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3498f-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3498f-134">CommonParameters</span></span>
<span data-ttu-id="3498f-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3498f-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3498f-136">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3498f-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3498f-137">Entradas</span><span class="sxs-lookup"><span data-stu-id="3498f-137">INPUTS</span></span>

### <span data-ttu-id="3498f-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="3498f-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="3498f-139">System.String</span><span class="sxs-lookup"><span data-stu-id="3498f-139">System.String</span></span>

## <span data-ttu-id="3498f-140">Saídas</span><span class="sxs-lookup"><span data-stu-id="3498f-140">OUTPUTS</span></span>

### <span data-ttu-id="3498f-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice</span><span class="sxs-lookup"><span data-stu-id="3498f-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice</span></span>

## <span data-ttu-id="3498f-142">Notas</span><span class="sxs-lookup"><span data-stu-id="3498f-142">NOTES</span></span>

## <span data-ttu-id="3498f-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3498f-143">RELATED LINKS</span></span>
