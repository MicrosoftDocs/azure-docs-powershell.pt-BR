---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/add-aziothubdevicechildren
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubDeviceChildren.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubDeviceChildren.md
ms.openlocfilehash: e41030f30e3c5651aca3ddf716af99c919e6e6f2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891365"
---
# <span data-ttu-id="16794-101">Add-AzIotHubDeviceChildren</span><span class="sxs-lookup"><span data-stu-id="16794-101">Add-AzIotHubDeviceChildren</span></span>

## <span data-ttu-id="16794-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="16794-102">SYNOPSIS</span></span>
<span data-ttu-id="16794-103">Adicione dispositivos que não são de borda como filhos ao dispositivo de borda.</span><span class="sxs-lookup"><span data-stu-id="16794-103">Add non-edge devices as a children to the edge device.</span></span>

## <span data-ttu-id="16794-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="16794-104">SYNTAX</span></span>

### <span data-ttu-id="16794-105">ResourceSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="16794-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubDeviceChildren [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-Children] <String[]> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="16794-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="16794-106">InputObjectSet</span></span>
```
Add-AzIotHubDeviceChildren [-InputObject] <PSIotHub> [-DeviceId] <String> [-Children] <String[]> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="16794-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="16794-107">ResourceIdSet</span></span>
```
Add-AzIotHubDeviceChildren [-ResourceId] <String> [-DeviceId] <String> [-Children] <String[]> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="16794-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="16794-108">DESCRIPTION</span></span>
<span data-ttu-id="16794-109">Adicione uma lista separada por vírgulas especificadas de IDs de dispositivo não de borda como filhos do dispositivo de borda especificado.</span><span class="sxs-lookup"><span data-stu-id="16794-109">Add specified comma-separated list of non edge device ids as children of specified edge device.</span></span>

## <span data-ttu-id="16794-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="16794-110">EXAMPLES</span></span>

### <span data-ttu-id="16794-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="16794-111">Example 1</span></span>
```powershell
PS C:\> Add-AzIotHubDeviceChildren -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Children device1,device2

DeviceId  ChildrenDeviceId
--------  ----------------
myDevice1 {device1, device2}
```

<span data-ttu-id="16794-112">Adicione dispositivos que não são de borda como filhos ao dispositivo de borda.</span><span class="sxs-lookup"><span data-stu-id="16794-112">Add non-edge devices as a children to the edge device.</span></span>

### <span data-ttu-id="16794-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="16794-113">Example 2</span></span>
```powershell
PS C:\> Add-AzIotHubDeviceChildren -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice2" -Children "device1,device2" -Force

DeviceId  ChildrenDeviceId
--------  ----------------
myDevice2 {device1, device2}
```

<span data-ttu-id="16794-114">Adicione dispositivos que não são de borda como filhos ao dispositivo de borda independentemente de o dispositivo não-borda já ser filho de outro dispositivo de borda.</span><span class="sxs-lookup"><span data-stu-id="16794-114">Add non-edge devices as a children to the edge device irrespectively the non-edge device is already a child of other edge device.</span></span>

## <span data-ttu-id="16794-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="16794-115">PARAMETERS</span></span>

### <span data-ttu-id="16794-116">-Children</span><span class="sxs-lookup"><span data-stu-id="16794-116">-Children</span></span>
<span data-ttu-id="16794-117">A lista de dispositivos filho (vírgula separada) inclui apenas dispositivos que não são de borda.</span><span class="sxs-lookup"><span data-stu-id="16794-117">Child device list (comma separated) includes only non-edge devices.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16794-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16794-118">-DefaultProfile</span></span>
<span data-ttu-id="16794-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="16794-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="16794-120">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="16794-120">-DeviceId</span></span>
<span data-ttu-id="16794-121">ID do dispositivo de borda.</span><span class="sxs-lookup"><span data-stu-id="16794-121">Id of edge device.</span></span>

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

### <span data-ttu-id="16794-122">-Force</span><span class="sxs-lookup"><span data-stu-id="16794-122">-Force</span></span>
<span data-ttu-id="16794-123">Substitui o dispositivo pai do dispositivo sem borda.</span><span class="sxs-lookup"><span data-stu-id="16794-123">Overwrites the non-edge device's parent device.</span></span>

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

### <span data-ttu-id="16794-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="16794-124">-InputObject</span></span>
<span data-ttu-id="16794-125">Objeto IotHub</span><span class="sxs-lookup"><span data-stu-id="16794-125">IotHub object</span></span>

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

### <span data-ttu-id="16794-126">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="16794-126">-IotHubName</span></span>
<span data-ttu-id="16794-127">Nome do Hub de Iot</span><span class="sxs-lookup"><span data-stu-id="16794-127">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="16794-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16794-128">-ResourceGroupName</span></span>
<span data-ttu-id="16794-129">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="16794-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="16794-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="16794-130">-ResourceId</span></span>
<span data-ttu-id="16794-131">Id de Recurso IotHub</span><span class="sxs-lookup"><span data-stu-id="16794-131">IotHub Resource Id</span></span>

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

### <span data-ttu-id="16794-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="16794-132">-Confirm</span></span>
<span data-ttu-id="16794-133">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="16794-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="16794-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="16794-134">-WhatIf</span></span>
<span data-ttu-id="16794-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="16794-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="16794-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="16794-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="16794-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16794-137">CommonParameters</span></span>
<span data-ttu-id="16794-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="16794-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16794-139">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="16794-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16794-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="16794-140">INPUTS</span></span>

### <span data-ttu-id="16794-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="16794-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="16794-142">System.String</span><span class="sxs-lookup"><span data-stu-id="16794-142">System.String</span></span>

## <span data-ttu-id="16794-143">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="16794-143">OUTPUTS</span></span>

### <span data-ttu-id="16794-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceChildren</span><span class="sxs-lookup"><span data-stu-id="16794-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceChildren</span></span>

## <span data-ttu-id="16794-145">NOTES</span><span class="sxs-lookup"><span data-stu-id="16794-145">NOTES</span></span>

## <span data-ttu-id="16794-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="16794-146">RELATED LINKS</span></span>
